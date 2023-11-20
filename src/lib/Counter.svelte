<script>
  import Stamps from "@permaweb/stampjs";
  import { WarpFactory } from "https://unpkg.com/warp-contracts/bundles/web.bundle.min.js";
  import Arweave from "arweave";

  const arweave = Arweave.init({
    host: "arweave.net",
    port: 443,
    protocol: "https",
  });
  let count = 0;
  const stamps = Stamps.init({ warp: WarpFactory.forMainnet(), arweave });
  const asset = "fsxlnMB_OHQJJwnd-2uuGNOr9JrLRhyEnBPnIxHgzII";
  //stamps.count(asset).then((result) => (count = result.total));
  stamps.counts([asset]).then((results) => {
    console.log(results);
  });
  const increment = async () => {
    const result = await stamps.stamp(asset);
    console.log(result);
    count = await stamps.count(asset).then((result) => result.total);
  };
</script>

<button on:click={increment}>
  count is {count}
</button>
