<script>
  let name = "Moka Pot by James Hoffman";

  import { mokaPot } from "../../components/store.js";

  let {
    waterAsMultipleOfCoffee,
    waterAmount,
    coffeeAmount,
    cupsAmount,
    grindSize,
    currentCalculator,
  } = mokaPot;

  import Recipe from "../../components/Recipe.svelte";
</script>

<Recipe {name} {...mokaPot}>
  <div slot="steps">
    <li>Add {$waterAmount}g of boiling water until it reaches below the valve</li>
    <li>Pour {$coffeeAmount}g of coffee into the basket</li>
    <li>Screw both parts together and bring it to the burner in medium heat</li>
    <li>Keep the lid open as the moka fills and watch for uncontrolled splatters</li>
    <li>If necessary, lower the stove heat or let cool water cool the bottom cup </li>
    <li>Turn off the stove when the splatters get more spaced out</li>
  </div>
  <div slot="notes">
    <p>
      This is a recipe simplified from
      <a href="https://www.youtube.com/watch?v=BfDLoIvb0w4">James Hoffman's
        video '<i>The Ultimate Moka Pot Technique</i></a>.'
    </p>

    <p>It uses a ratio of 30g coffee to 300g water (1 to 10).</p>
  </div>
</Recipe>
