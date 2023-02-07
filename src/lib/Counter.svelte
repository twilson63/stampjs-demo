<script>
  import Stamps from "@permaweb/stampjs";
  import { WarpFactory } from "https://unpkg.com/warp-contracts/bundles/web.bundle.min.js";

  let count = 0;
  const stamps = Stamps.init({ warp: WarpFactory.forMainnet() });
  const asset = "mKxjgkhXjqbK_kPWuUdJrkgus57qjEM63rp3_-8LE_E";
  stamps.count(asset).then((result) => (count = result.total));

  const increment = async () => {
    const result = await stamps.stamp(asset);
    console.log(result);
    count = await stamps.count(asset).then((result) => result.total);
  };
</script>

<button on:click={increment}>
  count is {count}
</button>
