<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive D&D 5e Player Cheat Sheet</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700&display=swap" rel="stylesheet">
    <!-- Chosen Palette: Warm Neutrals -->
    <!-- Application Structure Plan: A tabbed, single-page application with a fixed top navigation. This structure was chosen to allow new players to quickly find specific rules during a game without scrolling through a long document. It breaks down complex information into manageable, task-oriented sections (Your Turn, Rolls, Rules, Spells), reducing cognitive load and improving usability in a time-sensitive situation. -->
    <!-- Visualization & Content Choices: The source material is purely textual. Goal: Inform/Organize. Method: Interactive text blocks organized into tabs. Interaction: Users click navigation buttons to show/hide relevant content sections. Justification: This is the most direct and effective way to present a cheat sheet. It prioritizes speed and clarity over complex visualizations, which are not needed for this content. Method: Vanilla JS for tab switching. -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        .nav-button {
            transition: all 0.2s ease-in-out;
        }
        .nav-button.active {
            background-color: #ca8a04; /* amber-600 */
            color: #ffffff;
            box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);
        }
        .content-section {
            display: none;
        }
        .content-section.active {
            display: block;
        }
    </style>
</head>
<body class="bg-stone-100 text-stone-800">

    <div class="container mx-auto p-4 sm:p-6 md:p-8 max-w-4xl">
        <header class="text-center mb-6">
            <h1 class="text-3xl sm:text-4xl font-bold text-stone-900">D&D 5e Quick Reference</h1>
            <p class="text-stone-600 mt-2">Your interactive guide for adventure. Click a category below to get started.</p>
        </header>

        <nav class="flex flex-wrap justify-center gap-2 sm:gap-4 mb-8">
            <button data-target="turn" class="nav-button active text-sm sm:text-base font-medium py-2 px-4 rounded-full bg-white shadow-sm hover:bg-stone-200">
                <span class="hidden sm:inline">⚔️</span> Your Turn
            </button>
            <button data-target="rolls" class="nav-button text-sm sm:text-base font-medium py-2 px-4 rounded-full bg-white shadow-sm hover:bg-stone-200">
                <span class="hidden sm:inline">🎲</span> Making a Roll
            </button>
            <button data-target="rules" class="nav-button text-sm sm:text-base font-medium py-2 px-4 rounded-full bg-white shadow-sm hover:bg-stone-200">
                <span class="hidden sm:inline">📜</span> Key Rules
            </button>
            <button data-target="spellcasting" class="nav-button text-sm sm:text-base font-medium py-2 px-4 rounded-full bg-white shadow-sm hover:bg-stone-200">
                <span class="hidden sm:inline">✨</span> Spellcasting
            </button>
        </nav>

        <main id="content-container" class="bg-white p-6 sm:p-8 rounded-2xl shadow-lg">
            
            <section id="turn" class="content-section active">
                <h2 class="text-2xl font-bold mb-4 text-amber-700">Your Turn in Combat</h2>
                <p class="mb-6 text-stone-600">When it's your turn, you have a pool of options. You can use them in almost any order, but you typically only get one of each per turn.</p>
                <div class="space-y-4">
                    <div>
                        <h3 class="font-bold text-lg">Movement</h3>
                        <p>You can move up to your character's speed. You can also split your movement, for example: move, take an action, and then move again.</p>
                    </div>
                    <div>
                        <h3 class="font-bold text-lg">Action</h3>
                        <p>The main thing you do. You get **one** Action. Common choices include:</p>
                        <ul class="list-disc list-inside mt-2 space-y-1 pl-2 text-stone-700">
                            <li><strong class="font-semibold">Attack:</strong> Swing your sword or fire your bow.</li>
                            <li><strong class="font-semibold">Cast a Spell:</strong> Use a spell that has a casting time of 1 Action.</li>
                            <li><strong class="font-semibold">Dash:</strong> Double your movement speed for the turn.</li>
                            <li><strong class="font-semibold">Disengage:</strong> Move away from an enemy without provoking an attack.</li>
                            <li><strong class="font-semibold">Dodge:</strong> Focus on avoiding attacks. Attackers have disadvantage.</li>
                            <li><strong class="font-semibold">Help:</strong> Give an ally advantage on their next ability check or attack.</li>
                        </ul>
                    </div>
                    <div>
                        <h3 class="font-bold text-lg">Bonus Action</h3>
                        <p>A quick, extra thing you can do, but only if a spell or class feature specifically says you can. You get **one** Bonus Action.</p>
                    </div>
                    <div>
                        <h3 class="font-bold text-lg">Reaction</h3>
                        <p>A special action taken in response to a trigger, even when it's not your turn. You get **one** Reaction per round. The most common is an "Opportunity Attack."</p>
                    </div>
                </div>
            </section>

            <section id="rolls" class="content-section">
                <h2 class="text-2xl font-bold mb-4 text-amber-700">Making a Roll</h2>
                <p class="mb-6 text-stone-600">Most of the game is resolved by rolling a 20-sided die (d20). The goal is to meet or beat a target number.</p>
                <div class="space-y-4">
                    <div>
                        <h3 class="font-bold text-lg">Attack Rolls</h3>
                        <p>Roll a **d20** + your attack bonus. If the total equals or exceeds the enemy's Armor Class (AC), your attack hits!</p>
                    </div>
                    <div>
                        <h3 class="font-bold text-lg">Ability Checks</h3>
                        <p>Used for tasks like climbing, sneaking, or persuading. Roll a **d20** + your relevant ability modifier (e.g., Strength for climbing).</p>
                    </div>
                    <div>
                        <h3 class="font-bold text-lg">Saving Throws</h3>
                        <p>Used to resist spells or harmful effects. Roll a **d20** + your saving throw bonus. You are usually trying to avoid a negative effect.</p>
                    </div>
                    <div>
                        <h3 class="font-bold text-lg">Damage Rolls</h3>
                        <p>After a successful attack, roll the damage die for your weapon or spell (e.g., a d8 for a longsword) and add the relevant modifier.</p>
                    </div>
                </div>
            </section>

            <section id="rules" class="content-section">
                <h2 class="text-2xl font-bold mb-4 text-amber-700">Key Rules</h2>
                <p class="mb-6 text-stone-600">These are some fundamental rules that will come up often during your adventure.</p>
                <div class="space-y-4">
                    <div>
                        <h3 class="font-bold text-lg">Advantage & Disadvantage</h3>
                        <p>If you have **Advantage**, roll two d20s and take the **higher** result. If you have **Disadvantage**, roll two d20s and take the **lower** result. They cancel each other out.</p>
                    </div>
                    <div>
                        <h3 class="font-bold text-lg">Inspiration</h3>
                        <p>The DM can reward you with Inspiration for great roleplaying. You can spend it to give yourself Advantage on one roll.</p>
                    </div>
                    <div>
                        <h3 class="font-bold text-lg">Resting</h3>
                        <p>Characters need to rest to recover. There are two types:</p>
                        <ul class="list-disc list-inside mt-2 space-y-1 pl-2 text-stone-700">
                            <li><strong class="font-semibold">Short Rest:</strong> An hour of downtime. You can spend Hit Dice to heal.</li>
                            <li><strong class="font-semibold">Long Rest:</strong> Eight hours of sleep. Fully restores HP and most abilities.</li>
                        </ul>
                    </div>
                     <div>
                        <h3 class="font-bold text-lg">The Golden Rule</h3>
                        <p>The most important rule is to have fun! This is a collaborative story. If you have a cool idea, just ask the DM if you can try it!</p>
                    </div>
                </div>
            </section>

            <section id="spellcasting" class="content-section">
                <h2 class="text-2xl font-bold mb-4 text-amber-700">Spellcasting Basics</h2>
                <p class="mb-6 text-stone-600">For characters who wield magic, here are the core concepts to remember.</p>
                <div class="space-y-4">
                    <div>
                        <h3 class="font-bold text-lg">Cantrips</h3>
                        <p>These are simple spells you have mastered. You can cast them as often as you like without using any resources.</p>
                    </div>
                    <div>
                        <h3 class="font-bold text-lg">Spell Slots</h3>
                        <p>These are your magical fuel for casting more powerful spells. Casting a spell of a certain level consumes a spell slot of that level or higher. You regain spent spell slots after a Long Rest.</p>
                    </div>
                </div>
            </section>

        </main>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const navButtons = document.querySelectorAll('.nav-button');
            const contentSections = document.querySelectorAll('.content-section');

            navButtons.forEach(button => {
                button.addEventListener('click', () => {
                    const targetId = button.dataset.target;

                    navButtons.forEach(btn => {
                        btn.classList.remove('active');
                    });
                    button.classList.add('active');

                    contentSections.forEach(section => {
                        if (section.id === targetId) {
                            section.classList.add('active');
                        } else {
                            section.classList.remove('active');
                        }
                    });
                });
            });
        });
    </script>

</body>
</html>
