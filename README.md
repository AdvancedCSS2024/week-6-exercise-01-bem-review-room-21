[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/P3kz0bBR)
# BEM in practice

## Part 1 - BEM
Below you can see examples of code and style from class exercises: 
- *Week 4 - Exercise 01 - Applying BEM and styling*
- *Week 5 - Exercise 01 - Inheritance and BEM* 

**Discuss** in groups of two below examples and **propose better solution** according to BEM principles if needed. 

If you need help feel free to use [BEM Naming Cheat Sheet](https://bem-cheat-sheet.9elements.com/) or discuss it on MS Teams -> Team: AdvancedCSS 2024 -> Channel: [General](https://teams.microsoft.com/l/channel/19%3AGcJsLef6WAE6qb-9gr01mLK-AJ8W7tCQaUsF15g5AJs1%40thread.tacv2/General?groupId=05ca134d-fae1-48db-b017-a4769681310d&tenantId=09a10672-822f-4467-a5ba-5bb375967c05)

## Part 2 - GitHub Collaboration
In addition to the above BEM exercise, in your group, practice Git collaboration:

1. Clone this repository to your machine.
2. One student takes exercises with even numbers, and the other student takes exercises with odd numbers.
3. Practice creating branches, pull requests, and merging.
4. Create a branch for each example.
5. Add your solution.
6. Create a Pull Request for that change.
7. Your colleague needs to approve your Pull Request.
8. Merge your changes into the "main" branch.
9. Repeat steps 4-8.
10. **Do not delete the Feedback branch.**

## Example 1
    <header class="card card__header">
        <h2 class="card card__h2">Cars</h2>
        <h3 class="card card__h3">Fiat</h3>
        <h3 class="card card__h3">Opel</h3>
        <h3 class="card card__h3">Volvo</h3>
    </header>

#### Solution 1:
    <header class="card__header">
        <h2 class="card__header--title">Cars</h2>
        <h3 class="card__header--subtitle">Fiat</h3>
        <h3 class="card__header--subtitle">Opel</h3>
        <h3 class="card__header--subtitle">Volvo</h3>
    </header>
> [!NOTE]
> block: card, element: header, modifier: title/subtitle

#### Solution 2:
    <header class="card__header">
        <h2 class="card__header card__header--title">Cars</h2>
        <h3 class="card__header card__header--subtitle">Fiat</h3>
        <h3 class="card__header card__header--subtitle">Opel</h3>
        <h3 class="card__header card__header--subtitle">Volvo</h3>
    </header>
> [!NOTE]
> this solution can be correct in case class `card_header` consist of some styles that cannot be inherit and needed to be specified and are shared between all headers

## Example 2
    .card__dog--color {
        background-color: pink;
    }
    
    .card__cat--color {
        background-color: yellow;
    }

## Example 3
    .Newcard {
      border: solid 1px rgb(255, 242, 0);
      border-width: 2rem;
      max-width: 260px;
      padding: 10px;
      }

### Solution 3
.card{
      border: solid 1px rgb(255, 242, 0);
      border-width: 2rem;
      max-width: 260px;
      padding: 10px;
      }

## Example 4
    <p class="card__description--text">
        Lorem ipsum dolor...
    </p>

## Example 5
> [!TIP]
> What is a purpose of section? does it make sense to call it "card"?

> [!TIP]
> There are more mistakes to fix here :)

    <section class="card">
        <article class="card article__dog">
            <aside class="article__dog aside">
                <figure class="article__dog figure">
                    <img src="..." alt="Dummy Image" class="" />
                </figure>
             </aside>
         </article>
    </section>

## Example 6
    .button__styled--disabled{
        background-color: orange;
    }

## Example 7
    <article class="card cat--card">
      ...
    </article>

### solution 7 
<article class="article__card--cat">
      ...
    </article>

## Example 8
    <article class="card card__dog card__dog--type1">
      ...
    </article>

## Example 9
    .card {
        border: solid 1px #000;
        max-width: 360px;
        padding: 20px;
    }
  
    .card {
        background-color: white;
        margin-bottom: 20px;
        padding: 15px;
        display: block;
        align-items: center;
        justify-content: center;
    }

## Solution 9
    .card {
        border: solid 1px #000;
        max-width: 360px;
        padding: 20px;
    }
  
    .card__content {
        background-color: white;
        margin-bottom: 20px;
        padding: 15px;
        display: block;
        align-items: center;
        justify-content: center;
    }

## Example 10
    .card--dog--type1 header{ 
        background-color: green;
    }

    .header__dog--type2{
        background-color: purple;
    }

    .header__dog--type3{
        background-color: orange;
    }

## Example 11
    <main class="main__flex-wrap">
        ...
    </main>
> [!TIP]
> Why is it not a good idea to specify type of flex applied to element in the name of class?

## solution 11 
the description in exmpale 11 is related specific to a particular styling (flex-wrap) that is applied to the element. for best practice according to BEM class names should describe the purpose or role of the element and not the styling its self. that why keeping it like: 
 <main class="main">
        ...
    </main>
would be better
    
## Example 12
    <section class="dog__flex">
        ...
    </section>

## Example 13
    <footer class="card__options">
      <div class="card__options-buttons">
       ...
      </div>
    </footer>

## solution 13
    <footer class="card__options">
      <div class="card__options--buttons">
       ...
      </div>
    </footer>

## Example 14
    <header class="card__dog">
        <h2 class="card__dog--poster">Dog Poster</h2>
        <h3 class="card_dog--price">Dog poster - 50nok</h3>
    </header>

## Example 15
    <header class="card__header">
        <h2 class="card__title--cat">NEW! Cat Poster</h2>
        <h3 class="card__subtitle">Cat poster - 50nok</h3>
    </header>

## Solution 15 - in my opinion the name descriptions given here are alright
    <header class="card__header">
        <h2 class="card__title--cat">NEW! Cat Poster</h2>
        <h3 class="card__subtitle">Cat poster - 50nok</h3>
    </header>

## Example 16
    <section class="cat__box">
        ...
    </section>

## Example 17
    <button class="card_basked_button styled disabled">
        <span class="card_basket_button_icon">&#128722;</span>
        <span class="card_basket_button_text">Basket</span>
    </button>

## Example 18
    <header class="main_header">
        <h1>BEM</h1>
        <button class="styled disabled wishlist">
            <span>🚀</span>
            <span>Wish list</span>
        </button>
    </header>
    </header>

    <main class="main">
        <section>
        <section>
    </main>

## Example 19
> [!TIP]
> Why it is not a good idea to style cards based on `nth-of-type(even)` in context of shopping cards?
> In which context it will be a good idea?

    .card:nth-of-type(even) .card_basked_button {
        ...
    }
## solution 19
Styling cards based on nth-of-type(even) in shopping cards can cause problems because:

Dynamic Changes: The order of cards may change based on user actions, making the styling unreliable.
Semantic Meaning: The order of cards may not have any specific meaning, so styling based on odd/even doesn't make sense. 
However, using nth-of-type(even) can work well for creating visual effects in grid-based designs.



## Example 20
> [!TIP]
> Why it is not a good idea to create repetitive styles based on id?
> In which context we should use ids?
> IDs should only be used for unique elements, and are not to be repeated. 
    #wishlist {
        ...
    }

## Example 21
    <main class="main_flex-container">
        ...
    </main>

## solution 21 
<main class="main main--flex-container">
    ...
</main>

## Example 22
> [!TIP]
> BEM stands for block__element--modifier, is "cat" and "dog" an element? 

    <section class="card__section--cats">
        ...
    </section>

## Example 23
> [!TIP]
> Let's assume that in some case it make sense to call a section "cat" or "dog", the section "cat" will consist of multiple cards of cats, and the section "dog" will consist of multiple cards of dogs. Let's not focuse here on BEM. Nevertheless, how could you improve on class naming?
> 

    <section class="cat">
        ...
    </section>

## solution 23
<section class="cat-section">
    <!-- Cat Cards -->
</section>

<section class="dog-section">
    <!-- Dog Cards -->
</section>
to use descrptive class names like "cat-section" and "dog-section" for each section makes it clearer which section contains cats and which contains dogs. 

## Example 24
    .button__div--flex {
        display: flex;
        flex-direction: row-reverse;
    }

## Example 25
![image](https://github.com/aniWeyn/advancedcss-bemmistakes/assets/23743322/57049158-a239-4853-aa76-c2cf63e443fe)

## Example 26
    header {
      background-color: hsl(180, 31%, 95%);
      ...
    }

    header>button {
      border: none;
      ...
    }

    header>button:hover {
       background-color: hsl(180, 25%, 73%);
    }

    header>button:active {
      background-color: hsl(180, 29%, 50%);
    }

## Example 27
In what scenarios is it advantageous to use a class name that represents the animal, and in what scenarios would it be preferable to use a generic name like 'product_01' or 'product_02'?

## solution 27
using class names that represent animlas is helpful when: 
1. Clear Content: It's obvious what the content represents, making it easier to understand.
2.Easy Updates: Maintenance is simpler since the purpose of each element is clear.
3.Consistency: Following a consistent naming convention makes the code more organized.

however generic names are beter to use when contetn is varied, or there are frequently changes on the websites whcih allows more flexibility when using generic names. 