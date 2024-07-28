<script setup>

</script>

<template>
  <div class="recipe-card">
    <img src="@/assets/images/omelette.jpeg" alt="Recipe preview of an omelette" class="top-image">
    
    <div class="text-content">
      <section class="title-section recipe-section">
        <h1 class="heading">Simple Omelette Recipe</h1>
        <p class="description">
          An easy and quick dish, perfect for any meal. This classic omelette combines beaten eggs cooked
          to perfection, optionally filled with your choice of cheese, vegetables, or meats.
        </p>
      </section>
      
      <section class="preparation-section recipe-section">
        <h3 class="preparation-heading">Preparation time</h3>
        <ul class="preparation-list base-list">
          <li><strong>Total:</strong> Approximately 10 minutes</li>
          <li><strong>Preparation:</strong> 5 minutes</li>
          <li><strong>Cooking:</strong> 5 minutes</li>
        </ul>
      </section>
      
      <section class="recipe-section">
        <h2 class="section-heading">Ingredients</h2>
        <ul class="base-list">
          <li>2-3 large eggs</li>
          <li>Salt, to taste</li>
          <li>Pepper, to taste</li>
          <li>1 tablespoon of butter or oil</li>
          <li>Optional fillings: cheese, diced vegetables, cooked meats, herbs</li>
        </ul>
      </section>
      
      <hr class="spacer">
      
      <section class="recipe-section">
        <h2 class="section-heading">Instructions</h2>
        <ol class="instructions-list base-list">
          <li>
            <strong>Beat the eggs:</strong> In a bowl,
            beat the eggs with a pinch of salt and pepper until they are well mixed.
            You can add a tablespoon of water or milk for a fluffier texture.
          </li>
          <li>
            <strong>Heat the pan:</strong> Place a non-stick frying pan over medium heat and add butter or oil.
          </li>
          <li>
            <strong>Cook the omelette:</strong> Once the butter is melted and bubbling, pour in the eggs.
            Tilt the pan to ensure the eggs evenly coat the surface.
          </li>
          <li>
            <strong>Add fillings (optional):</strong> When the eggs begin to set at the edges but are still
            slightly runny in the middle, sprinkle your chosen fillings over one half of the omelette.
          </li>
          <li>
            <strong>Fold and serve:</strong> As the omelette continues to cook,
            carefully lift one edge and fold it over the fillings.
            Let it cook for another minute, then slide it onto a plate.
          </li>
          <li>
            <strong>Enjoy:</strong> Serve hot, with additional salt and pepper if needed.
          </li>
        </ol>
      </section>
      
      <hr class="spacer">
      
      <section class="recipe-section">
        <h2 class="section-heading">Nutrition</h2>
        <p>The table below shows nutritional values per serving without the additional fillings.</p>
        <div class="nutrition-table">
          <div class="table-row">
            <span>Calories</span>
            <span class="highlight">277kcal</span>
          </div>
          <div class="spacer"></div>
          <div class="table-row">
            <span>Carbs</span>
            <span class="highlight">0g</span>
          </div>
          <div class="spacer"></div>
          <div class="table-row">
            <span>Protein</span>
            <span class="highlight">20g</span>
          </div>
          <div class="spacer"></div>
          <div class="table-row">
            <span>Fat</span>
            <span class="highlight">22g</span>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<style scoped lang="scss">
@import '@/styles/base/typography';
@import '@/styles/base/media-queries';

.recipe-card {
  background-color: var(--color-white);
  
  @media #{$tablet-and-up} {
    --inner-spacing: var(--spacing-500);
    
    max-width: 46rem;
    margin-inline: auto;
    padding: var(--inner-spacing);
    border-radius: 24px;
    display: grid;
    gap: var(--inner-spacing);
  }
  
  .top-image {
    object-fit: cover;
    
    @media #{$tablet-and-up} {
      height: 18.75rem;
      border-radius: 12px;
    }
  }
  
  .text-content {
    padding: var(--spacing-500) var(--spacing-400);
    display: grid;
    gap: var(--spacing-400);
    
    @media #{$tablet-and-up} {
      padding: 0;
    }
    
    .recipe-section {
      display: grid;
      gap: var(--spacing-300);
      
      .section-heading {
        color: var(--color-brown-800);
        @extend %typography-text-preset-2;
      }
    }
    
    .title-section {
      .heading {
        color: var(--color-stone-900);
        @extend %typography-text-preset-1;
      }
      
      .description {
        color: var(--color-stone-600);
      }
    }
    
    .preparation-section {
      padding: var(--spacing-300);
      background-color: var(--color-rose-50);
      border-radius: 12px;
      display: grid;
      gap: var(--spacing-200);
      
      .preparation-heading {
        color: var(--color-rose-800);
        @extend %typography-text-preset-3;
      }
      
      .preparation-list li::marker {
        color: var(--color-rose-800);
      }
    }
    
    .instructions-list li::marker {
      @extend %typography-text-preset-4-bold;
    }
    
    .nutrition-table {
      display: grid;
      gap: var(--spacing-150);
      
      .table-row {
        padding-inline: var(--spacing-400);
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: var(--spacing-200);
        
        .highlight {
          color: var(--color-brown-800);
          @extend %typography-text-preset-4-bold;
        }
      }
    }
  }
}
</style>
