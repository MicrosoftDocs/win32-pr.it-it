---
description: In questa sezione viene descritta la sintassi delle istruzioni condizionali utilizzate dalla funzione MsiEvaluateCondition e dalle tabelle di sequenza delle azioni. Per ulteriori informazioni, vedere, esempi di sintassi delle istruzioni condizionali.
ms.assetid: 6f1657f9-063b-4d57-ad76-95e3dbe25786
title: Sintassi dell'istruzione condizionale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0548a71756faff654bfe2b49e14c0581a6248a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881053"
---
# <a name="conditional-statement-syntax"></a><span data-ttu-id="a3cff-104">Sintassi dell'istruzione condizionale</span><span class="sxs-lookup"><span data-stu-id="a3cff-104">Conditional Statement Syntax</span></span>

<span data-ttu-id="a3cff-105">In questa sezione viene descritta la sintassi delle istruzioni condizionali utilizzate dalla funzione [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) e dalle [tabelle di sequenza](using-a-sequence-table.md)delle azioni.</span><span class="sxs-lookup"><span data-stu-id="a3cff-105">This section describes the syntax of conditional statements used by the [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) function and the action [sequence tables](using-a-sequence-table.md).</span></span> <span data-ttu-id="a3cff-106">Per ulteriori informazioni, vedere, [esempi di sintassi delle istruzioni condizionali](examples-of-conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="a3cff-106">For more information, see, [Examples of Conditional Statement Syntax](examples-of-conditional-statement-syntax.md).</span></span>

## <a name="summary-of-conditional-statement-syntax"></a><span data-ttu-id="a3cff-107">Riepilogo della sintassi delle istruzioni condizionali</span><span class="sxs-lookup"><span data-stu-id="a3cff-107">Summary of Conditional Statement Syntax</span></span>

<span data-ttu-id="a3cff-108">Questa tabella e l'elenco seguente riepilogano la sintassi da usare nelle espressioni condizionali.</span><span class="sxs-lookup"><span data-stu-id="a3cff-108">This table and the following list summarize the syntax to use in conditional expressions.</span></span>



| <span data-ttu-id="a3cff-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="a3cff-109">Item</span></span>                | <span data-ttu-id="a3cff-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3cff-110">Syntax</span></span>                                                                                                          |
|---------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3cff-111">Valore</span><span class="sxs-lookup"><span data-stu-id="a3cff-111">value</span></span>               | <span data-ttu-id="a3cff-112">valore \| letterale \| Integer simbolo</span><span class="sxs-lookup"><span data-stu-id="a3cff-112">symbol \| literal \| integer</span></span>                                                                                    |
| <span data-ttu-id="a3cff-113">operatore di confronto</span><span class="sxs-lookup"><span data-stu-id="a3cff-113">comparison-operator</span></span> | < \| > \| <= \| >= \| = \| <>                                                                 |
| <span data-ttu-id="a3cff-114">Termine</span><span class="sxs-lookup"><span data-stu-id="a3cff-114">term</span></span>                | <span data-ttu-id="a3cff-115">valore valore \| confronto-valore operatore \| (espressione)\|</span><span class="sxs-lookup"><span data-stu-id="a3cff-115">value \| value comparison-operator value \| ( expression )\|</span></span>                                                    |
| <span data-ttu-id="a3cff-116">Fattore booleano</span><span class="sxs-lookup"><span data-stu-id="a3cff-116">Boolean-factor</span></span>      | <span data-ttu-id="a3cff-117">termine \| **non** termine</span><span class="sxs-lookup"><span data-stu-id="a3cff-117">term \| **NOT** term</span></span>                                                                                            |
| <span data-ttu-id="a3cff-118">Termine booleano</span><span class="sxs-lookup"><span data-stu-id="a3cff-118">Boolean-term</span></span>        | <span data-ttu-id="a3cff-119">Booleano-Factor \| -fattore **e** termine</span><span class="sxs-lookup"><span data-stu-id="a3cff-119">Boolean-factor \| Boolean-factor **AND** term</span></span>                                                                   |
| <span data-ttu-id="a3cff-120">expression</span><span class="sxs-lookup"><span data-stu-id="a3cff-120">expression</span></span>          | <span data-ttu-id="a3cff-121">Espressione booleana a termine booleano \| **o** espressione</span><span class="sxs-lookup"><span data-stu-id="a3cff-121">Boolean-term \| Boolean-term **OR** expression</span></span>                                                                  |
| <span data-ttu-id="a3cff-122">simbolo</span><span class="sxs-lookup"><span data-stu-id="a3cff-122">symbol</span></span>              | <span data-ttu-id="a3cff-123">proprietà \| % Environment-variable \| $Component-Action \| ? stato componente \| &funzionalità-azione \| ! funzionalità-stato</span><span class="sxs-lookup"><span data-stu-id="a3cff-123">property \| %environment-variable \| $component-action \| ?component-state \| &feature-action \| !feature-state</span></span> |



 

-   <span data-ttu-id="a3cff-124">Per i nomi dei simboli e i valori viene fatta distinzione tra maiuscole</span><span class="sxs-lookup"><span data-stu-id="a3cff-124">Symbol names and values are case sensitive.</span></span>
-   <span data-ttu-id="a3cff-125">Per i nomi delle variabili di ambiente non viene fatta distinzione tra maiuscole</span><span class="sxs-lookup"><span data-stu-id="a3cff-125">Environment variable names are not case sensitive.</span></span>
-   <span data-ttu-id="a3cff-126">Il testo letterale deve essere racchiuso tra virgolette ("testo").</span><span class="sxs-lookup"><span data-stu-id="a3cff-126">Literal text must be enclosed between quotation marks ("text").</span></span>
    > [!Note]  
    > <span data-ttu-id="a3cff-127">Impossibile utilizzare il testo letterale contenente virgolette nelle istruzioni condizionali perché non esiste alcun carattere di escape per le virgolette all'interno del testo letterale.</span><span class="sxs-lookup"><span data-stu-id="a3cff-127">Literal text containing quotation marks cannot be used in conditional statements because there is no escape character for quotation marks inside literal text.</span></span> <span data-ttu-id="a3cff-128">Per eseguire un confronto con il testo letterale contenente virgolette, il testo letterale deve essere inserito in una proprietà.</span><span class="sxs-lookup"><span data-stu-id="a3cff-128">To do a comparison against literal text containing quotation marks, the literal text should be put in a property.</span></span> <span data-ttu-id="a3cff-129">Per verificare, ad esempio, che la proprietà SERVERNAME non contenga virgolette, definire una proprietà denominata VIRGOLETte nella [tabella delle proprietà](property-table.md) con il valore "e modificare la condizione in not ServerName><virgolette.</span><span class="sxs-lookup"><span data-stu-id="a3cff-129">For example, to verify that the SERVERNAME property does not contain any quotation marks, define a property called QUOTES in the [Property table](property-table.md) with a value of " and change the condition to NOT SERVERNAME><QUOTES.</span></span>

     

-   <span data-ttu-id="a3cff-130">I valori di proprietà inesistenti vengono considerati come stringhe vuote.</span><span class="sxs-lookup"><span data-stu-id="a3cff-130">Nonexistent property values are treated as empty strings.</span></span>
-   <span data-ttu-id="a3cff-131">I valori numerici a virgola mobile non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="a3cff-131">Floating point numeric values are not supported.</span></span>
-   <span data-ttu-id="a3cff-132">Gli operatori e la precedenza sono identici a quelli dei linguaggi BASIC e SQL.</span><span class="sxs-lookup"><span data-stu-id="a3cff-132">Operators and precedence are the same as in the BASIC and SQL languages.</span></span>
-   <span data-ttu-id="a3cff-133">Gli operatori aritmetici non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="a3cff-133">Arithmetic operators are not supported.</span></span>
-   <span data-ttu-id="a3cff-134">Le parentesi possono essere utilizzate per eseguire l'override della precedenza degli operatori.</span><span class="sxs-lookup"><span data-stu-id="a3cff-134">Parentheses can be used to override operator precedence.</span></span>
-   <span data-ttu-id="a3cff-135">Gli operatori non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a3cff-135">Operators are not case sensitive.</span></span>
-   <span data-ttu-id="a3cff-136">Per i confronti di stringhe, un valore tilde "~" con prefisso per l'operatore esegue un confronto senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a3cff-136">For string comparisons, a tilde "~" prefixed to the operator performs a comparison that is not case sensitive.</span></span>
-   <span data-ttu-id="a3cff-137">Il confronto di un numero intero con un valore di stringa o di proprietà che non può essere convertito in un Integer è sempre **msiEvaluateConditionFalse**, ad eccezione dell'operatore di confronto "<>", che restituisce **msiEvaluateConditionTrue**.</span><span class="sxs-lookup"><span data-stu-id="a3cff-137">Comparison of an integer with a string or property value that cannot be converted to an integer is always **msiEvaluateConditionFalse**, except for the comparison operator "<>", which returns **msiEvaluateConditionTrue**.</span></span>

## <a name="access-prefixes"></a><span data-ttu-id="a3cff-138">Prefissi di accesso</span><span class="sxs-lookup"><span data-stu-id="a3cff-138">Access Prefixes</span></span>

<span data-ttu-id="a3cff-139">La tabella seguente illustra i prefissi da usare per accedere a diverse informazioni di sistema e di installazione da usare nelle espressioni condizionali.</span><span class="sxs-lookup"><span data-stu-id="a3cff-139">The following table shows the prefixes to use to access various system and installer information for use in conditional expressions.</span></span>



| <span data-ttu-id="a3cff-140">Tipo di simbolo</span><span class="sxs-lookup"><span data-stu-id="a3cff-140">Symbol type</span></span>          | <span data-ttu-id="a3cff-141">Prefisso</span><span class="sxs-lookup"><span data-stu-id="a3cff-141">Prefix</span></span> | <span data-ttu-id="a3cff-142">Valore</span><span class="sxs-lookup"><span data-stu-id="a3cff-142">Value</span></span>                                                     |
|----------------------|--------|-----------------------------------------------------------|
| <span data-ttu-id="a3cff-143">Proprietà Installer</span><span class="sxs-lookup"><span data-stu-id="a3cff-143">Installer property</span></span>   | <span data-ttu-id="a3cff-144">(nessuna)</span><span class="sxs-lookup"><span data-stu-id="a3cff-144">(none)</span></span> | <span data-ttu-id="a3cff-145">Valore della tabella Property ([Property](property-table.md)).</span><span class="sxs-lookup"><span data-stu-id="a3cff-145">Value of property ([Property](property-table.md)) table.</span></span> |
| <span data-ttu-id="a3cff-146">Variabile di ambiente</span><span class="sxs-lookup"><span data-stu-id="a3cff-146">Environment variable</span></span> | %      | <span data-ttu-id="a3cff-147">Valore della variabile di ambiente.</span><span class="sxs-lookup"><span data-stu-id="a3cff-147">Value of environment variable.</span></span>                            |
| <span data-ttu-id="a3cff-148">Chiave tabella componenti</span><span class="sxs-lookup"><span data-stu-id="a3cff-148">Component table key</span></span>  | $      | <span data-ttu-id="a3cff-149">Stato dell'azione del componente.</span><span class="sxs-lookup"><span data-stu-id="a3cff-149">Action state of the component.</span></span>                            |
| <span data-ttu-id="a3cff-150">Chiave tabella componenti</span><span class="sxs-lookup"><span data-stu-id="a3cff-150">Component table key</span></span>  | <span data-ttu-id="a3cff-151">?</span><span class="sxs-lookup"><span data-stu-id="a3cff-151">?</span></span>      | <span data-ttu-id="a3cff-152">Stato di installazione del componente.</span><span class="sxs-lookup"><span data-stu-id="a3cff-152">Installed state of the component.</span></span>                         |
| <span data-ttu-id="a3cff-153">Chiave della tabella delle funzionalità</span><span class="sxs-lookup"><span data-stu-id="a3cff-153">Feature table key</span></span>    | &      | <span data-ttu-id="a3cff-154">Stato dell'azione della funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a3cff-154">Action state of the feature.</span></span>                              |
| <span data-ttu-id="a3cff-155">Chiave della tabella delle funzionalità</span><span class="sxs-lookup"><span data-stu-id="a3cff-155">Feature table key</span></span>    | <span data-ttu-id="a3cff-156">!</span><span class="sxs-lookup"><span data-stu-id="a3cff-156">!</span></span>      | <span data-ttu-id="a3cff-157">Stato di installazione della funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a3cff-157">Installed state of the feature.</span></span>                           |



 

## <a name="logical-operators"></a><span data-ttu-id="a3cff-158">Operatori logici</span><span class="sxs-lookup"><span data-stu-id="a3cff-158">Logical Operators</span></span>

<span data-ttu-id="a3cff-159">Nella tabella seguente vengono illustrati gli operatori logici nelle espressioni condizionali, in ordine di precedenza alto-a-basso.</span><span class="sxs-lookup"><span data-stu-id="a3cff-159">The following table shows the logical operators in conditional expressions, in order of high-to-low precedence.</span></span>



| <span data-ttu-id="a3cff-160">Operatore</span><span class="sxs-lookup"><span data-stu-id="a3cff-160">Operator</span></span> | <span data-ttu-id="a3cff-161">Significato</span><span class="sxs-lookup"><span data-stu-id="a3cff-161">Meaning</span></span>                                                 |
|----------|---------------------------------------------------------|
| <span data-ttu-id="a3cff-162">Not</span><span class="sxs-lookup"><span data-stu-id="a3cff-162">Not</span></span>      | <span data-ttu-id="a3cff-163">Operatore unario prefix; inverte lo stato del termine seguente.</span><span class="sxs-lookup"><span data-stu-id="a3cff-163">Prefix unary operator; inverts state of following term.</span></span> |
| <span data-ttu-id="a3cff-164">e</span><span class="sxs-lookup"><span data-stu-id="a3cff-164">And</span></span>      | <span data-ttu-id="a3cff-165">TRUE se entrambi i termini sono TRUE.</span><span class="sxs-lookup"><span data-stu-id="a3cff-165">TRUE if both terms are TRUE.</span></span>                            |
| <span data-ttu-id="a3cff-166">Oppure</span><span class="sxs-lookup"><span data-stu-id="a3cff-166">Or</span></span>       | <span data-ttu-id="a3cff-167">TRUE se uno o entrambi i termini sono TRUE.</span><span class="sxs-lookup"><span data-stu-id="a3cff-167">TRUE if either or both terms are TRUE.</span></span>                  |
| <span data-ttu-id="a3cff-168">Xor</span><span class="sxs-lookup"><span data-stu-id="a3cff-168">Xor</span></span>      | <span data-ttu-id="a3cff-169">TRUE se uno o entrambi i termini sono TRUE.</span><span class="sxs-lookup"><span data-stu-id="a3cff-169">TRUE if either but not both terms are TRUE.</span></span>             |
| <span data-ttu-id="a3cff-170">Eqv</span><span class="sxs-lookup"><span data-stu-id="a3cff-170">Eqv</span></span>      | <span data-ttu-id="a3cff-171">TRUE se entrambi i termini sono TRUE o se entrambi i termini sono FALSE.</span><span class="sxs-lookup"><span data-stu-id="a3cff-171">TRUE if both terms are TRUE or both terms are FALSE.</span></span>    |
| <span data-ttu-id="a3cff-172">IMP</span><span class="sxs-lookup"><span data-stu-id="a3cff-172">Imp</span></span>      | <span data-ttu-id="a3cff-173">TRUE se il termine sinistro è FALSE o il termine corretto è TRUE.</span><span class="sxs-lookup"><span data-stu-id="a3cff-173">TRUE if left term is FALSE or right term is TRUE.</span></span>       |



 

## <a name="comparative-operators"></a><span data-ttu-id="a3cff-174">Operatori comparati</span><span class="sxs-lookup"><span data-stu-id="a3cff-174">Comparative Operators</span></span>

<span data-ttu-id="a3cff-175">Nella tabella seguente vengono illustrati gli operatori di confronto utilizzati nelle espressioni condizionali.</span><span class="sxs-lookup"><span data-stu-id="a3cff-175">The following table shows the comparison operators used in conditional expressions.</span></span> <span data-ttu-id="a3cff-176">Questi operatori di confronto possono essere presenti solo tra due valori.</span><span class="sxs-lookup"><span data-stu-id="a3cff-176">These comparison operators can only occur between two values.</span></span>



| <span data-ttu-id="a3cff-177">Operatore</span><span class="sxs-lookup"><span data-stu-id="a3cff-177">Operator</span></span> | <span data-ttu-id="a3cff-178">Significato</span><span class="sxs-lookup"><span data-stu-id="a3cff-178">Meaning</span></span>                                                     |
|----------|-------------------------------------------------------------|
| =        | <span data-ttu-id="a3cff-179">TRUE se il valore di sinistra è uguale a quello a destra.</span><span class="sxs-lookup"><span data-stu-id="a3cff-179">TRUE if left value is equal to right value.</span></span>                 |
| <> | <span data-ttu-id="a3cff-180">TRUE se il valore di sinistra non è uguale al valore di destra.</span><span class="sxs-lookup"><span data-stu-id="a3cff-180">TRUE if left value is not equal to right value.</span></span>             |
| >     | <span data-ttu-id="a3cff-181">TRUE se il valore a sinistra è maggiore del valore a destra.</span><span class="sxs-lookup"><span data-stu-id="a3cff-181">TRUE if left value is greater than right value.</span></span>             |
| >=    | <span data-ttu-id="a3cff-182">TRUE se il valore a sinistra è maggiore o uguale al valore a destra.</span><span class="sxs-lookup"><span data-stu-id="a3cff-182">TRUE if left value is greater than or equal to right value.</span></span> |
| <     | <span data-ttu-id="a3cff-183">TRUE se il valore a sinistra è minore del valore a destra.</span><span class="sxs-lookup"><span data-stu-id="a3cff-183">TRUE if left value is less than right value.</span></span>                |
| <=    | <span data-ttu-id="a3cff-184">TRUE se il valore di sinistra è minore o uguale al valore a destra.</span><span class="sxs-lookup"><span data-stu-id="a3cff-184">TRUE if left value is less than or equal to right value.</span></span>    |



 

## <a name="substring-operators"></a><span data-ttu-id="a3cff-185">Operatori di sottostringhe</span><span class="sxs-lookup"><span data-stu-id="a3cff-185">Substring Operators</span></span>

<span data-ttu-id="a3cff-186">Nella tabella seguente vengono illustrati gli operatori di sottostringa utilizzati nelle espressioni condizionali.</span><span class="sxs-lookup"><span data-stu-id="a3cff-186">The following table shows the substring operators used in conditional expressions.</span></span> <span data-ttu-id="a3cff-187">Gli operatori di sottostringhe possono essere presenti tra due valori di stringa.</span><span class="sxs-lookup"><span data-stu-id="a3cff-187">Substring operators can occur between two string values.</span></span>



| <span data-ttu-id="a3cff-188">Operatore</span><span class="sxs-lookup"><span data-stu-id="a3cff-188">Operator</span></span> | <span data-ttu-id="a3cff-189">Significato</span><span class="sxs-lookup"><span data-stu-id="a3cff-189">Meaning</span></span>                                           |
|----------|---------------------------------------------------|
| >< | <span data-ttu-id="a3cff-190">TRUE se la stringa a sinistra contiene la stringa a destra.</span><span class="sxs-lookup"><span data-stu-id="a3cff-190">TRUE if left string contains the right string.</span></span>    |
| << | <span data-ttu-id="a3cff-191">TRUE se la stringa a sinistra inizia con la stringa a destra.</span><span class="sxs-lookup"><span data-stu-id="a3cff-191">TRUE if left string starts with the right string.</span></span> |
| >> | <span data-ttu-id="a3cff-192">TRUE se la stringa a sinistra termina con la stringa a destra.</span><span class="sxs-lookup"><span data-stu-id="a3cff-192">TRUE if left string ends with the right string.</span></span>   |



 

## <a name="bitwise-numeric-operators"></a><span data-ttu-id="a3cff-193">Operatori numerici bit per bit</span><span class="sxs-lookup"><span data-stu-id="a3cff-193">Bitwise Numeric Operators</span></span>

<span data-ttu-id="a3cff-194">Nella tabella seguente vengono illustrati gli operatori numerici bit per bit nelle espressioni condizionali.</span><span class="sxs-lookup"><span data-stu-id="a3cff-194">The following table shows the bitwise numeric operators in conditional expressions.</span></span> <span data-ttu-id="a3cff-195">Questi operatori possono verificarsi tra due valori integer.</span><span class="sxs-lookup"><span data-stu-id="a3cff-195">These operators can occur between two integer values.</span></span>



| <span data-ttu-id="a3cff-196">Operatore</span><span class="sxs-lookup"><span data-stu-id="a3cff-196">Operator</span></span> | <span data-ttu-id="a3cff-197">Significato</span><span class="sxs-lookup"><span data-stu-id="a3cff-197">Meaning</span></span>                                                                      |
|----------|------------------------------------------------------------------------------|
| >< | <span data-ttu-id="a3cff-198">AND bit per bit, TRUE se gli Integer a sinistra e a destra hanno bit in comune.</span><span class="sxs-lookup"><span data-stu-id="a3cff-198">Bitwise AND, TRUE if the left and right integers have any bits in common.</span></span>    |
| << | <span data-ttu-id="a3cff-199">True se i 16 bit alti dell'intero a sinistra sono uguali all'intero a destra.</span><span class="sxs-lookup"><span data-stu-id="a3cff-199">True if the high 16-bits of the left integer are equal to the right integer.</span></span> |
| >> | <span data-ttu-id="a3cff-200">True se i 16 bit bassi dell'intero a sinistra sono uguali all'intero a destra.</span><span class="sxs-lookup"><span data-stu-id="a3cff-200">True if the low 16-bits of the left integer are equal to the right integer.</span></span>  |



 

## <a name="feature-and-component-state-values"></a><span data-ttu-id="a3cff-201">Valori dello stato delle funzionalità e dei componenti</span><span class="sxs-lookup"><span data-stu-id="a3cff-201">Feature and Component State Values</span></span>

<span data-ttu-id="a3cff-202">Nella tabella seguente viene indicato dove è possibile utilizzare i simboli di operatore feature e Component.</span><span class="sxs-lookup"><span data-stu-id="a3cff-202">The following table shows where it is valid to use the feature and component operator symbols.</span></span>



| <span data-ttu-id="a3cff-203">Operatore <state></span><span class="sxs-lookup"><span data-stu-id="a3cff-203">Operator <state></span></span> | <span data-ttu-id="a3cff-204">Dove questa sintassi è valida</span><span class="sxs-lookup"><span data-stu-id="a3cff-204">Where this syntax is valid</span></span>                                                                                                                                         |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3cff-205">$component-azione</span><span class="sxs-lookup"><span data-stu-id="a3cff-205">$component-action</span></span>      | <span data-ttu-id="a3cff-206">Nella tabella [Condition](condition-table.md) e nelle tabelle [Sequence](using-a-sequence-table.md) , dopo l'azione [CostFinalize secondo](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="a3cff-206">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |
| <span data-ttu-id="a3cff-207">Funzionalità &-azione</span><span class="sxs-lookup"><span data-stu-id="a3cff-207">&feature-action</span></span>        | <span data-ttu-id="a3cff-208">Nella tabella [Condition](condition-table.md) e nelle tabelle [Sequence](using-a-sequence-table.md) , dopo l'azione [CostFinalize secondo](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="a3cff-208">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |
| <span data-ttu-id="a3cff-209">! stato della funzionalità</span><span class="sxs-lookup"><span data-stu-id="a3cff-209">!feature-state</span></span>         | <span data-ttu-id="a3cff-210">Nella tabella [Condition](condition-table.md) e nelle tabelle [Sequence](using-a-sequence-table.md) , dopo l'azione [CostFinalize secondo](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="a3cff-210">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |
| <span data-ttu-id="a3cff-211">? componente-stato</span><span class="sxs-lookup"><span data-stu-id="a3cff-211">?component-state</span></span>       | <span data-ttu-id="a3cff-212">Nella tabella [Condition](condition-table.md) e nelle tabelle [Sequence](using-a-sequence-table.md) , dopo l'azione [CostFinalize secondo](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="a3cff-212">In the [Condition](condition-table.md) table, and in the [sequence](using-a-sequence-table.md) tables, after the [CostFinalize](costfinalize-action.md) action.</span></span> |



 

<span data-ttu-id="a3cff-213">Nella tabella seguente vengono illustrati i valori relativi allo stato delle funzionalità e dei componenti utilizzati nelle espressioni condizionali.</span><span class="sxs-lookup"><span data-stu-id="a3cff-213">The following table shows the feature and component state values used in conditional expressions.</span></span> <span data-ttu-id="a3cff-214">Questi Stati non vengono impostati fino a quando non viene chiamato [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) , direttamente o dall'azione [CostFinalize secondo](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="a3cff-214">These states are not set until [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) is called, either directly or by the [CostFinalize](costfinalize-action.md) action.</span></span>



| <span data-ttu-id="a3cff-215">State</span><span class="sxs-lookup"><span data-stu-id="a3cff-215">State</span></span>                    | <span data-ttu-id="a3cff-216">Valore</span><span class="sxs-lookup"><span data-stu-id="a3cff-216">Value</span></span> | <span data-ttu-id="a3cff-217">Significato</span><span class="sxs-lookup"><span data-stu-id="a3cff-217">Meaning</span></span>                                                         |
|--------------------------|-------|-----------------------------------------------------------------|
| <span data-ttu-id="a3cff-218">INSTALLSTATE \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="a3cff-218">INSTALLSTATE\_UNKNOWN</span></span>    | <span data-ttu-id="a3cff-219">-1</span><span class="sxs-lookup"><span data-stu-id="a3cff-219">-1</span></span>    | <span data-ttu-id="a3cff-220">Nessuna azione da intraprendere per la funzionalità o il componente.</span><span class="sxs-lookup"><span data-stu-id="a3cff-220">No action to be taken on the feature or component.</span></span>              |
| <span data-ttu-id="a3cff-221">INSTALLSTATE \_ annunciata</span><span class="sxs-lookup"><span data-stu-id="a3cff-221">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="a3cff-222">1</span><span class="sxs-lookup"><span data-stu-id="a3cff-222">1</span></span>     | <span data-ttu-id="a3cff-223">Funzionalità annunciata.</span><span class="sxs-lookup"><span data-stu-id="a3cff-223">Advertised feature.</span></span> <span data-ttu-id="a3cff-224">Questo stato non è disponibile per i componenti di.</span><span class="sxs-lookup"><span data-stu-id="a3cff-224">This state is not available for components.</span></span> |
| <span data-ttu-id="a3cff-225">INSTALLSTATE \_ assente</span><span class="sxs-lookup"><span data-stu-id="a3cff-225">INSTALLSTATE\_ABSENT</span></span>     | <span data-ttu-id="a3cff-226">2</span><span class="sxs-lookup"><span data-stu-id="a3cff-226">2</span></span>     | <span data-ttu-id="a3cff-227">La funzionalità o il componente non è presente.</span><span class="sxs-lookup"><span data-stu-id="a3cff-227">Feature or component is not present.</span></span>                            |
| <span data-ttu-id="a3cff-228">INSTALLSTATE \_ locale</span><span class="sxs-lookup"><span data-stu-id="a3cff-228">INSTALLSTATE\_LOCAL</span></span>      | <span data-ttu-id="a3cff-229">3</span><span class="sxs-lookup"><span data-stu-id="a3cff-229">3</span></span>     | <span data-ttu-id="a3cff-230">Funzionalità o componente nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="a3cff-230">Feature or component on the local computer.</span></span>                     |
| <span data-ttu-id="a3cff-231">\_origine InstallState</span><span class="sxs-lookup"><span data-stu-id="a3cff-231">INSTALLSTATE\_SOURCE</span></span>     | <span data-ttu-id="a3cff-232">4</span><span class="sxs-lookup"><span data-stu-id="a3cff-232">4</span></span>     | <span data-ttu-id="a3cff-233">Funzionalità o componente eseguiti dall'origine.</span><span class="sxs-lookup"><span data-stu-id="a3cff-233">Feature or component run from the source.</span></span>                       |



 

<span data-ttu-id="a3cff-234">Ad esempio, l'espressione condizionale "&la funzionalità = 3" restituisce true solo se la funzionalità è cambiata dallo stato corrente allo stato di installazione nel computer locale, INSTALLSTATE \_ locale.</span><span class="sxs-lookup"><span data-stu-id="a3cff-234">For example, the conditional expression "&MyFeature=3" evaluates to True only if MyFeature is changing from its current state to the state of being installed on the local computer, INSTALLSTATE\_LOCAL.</span></span>

<span data-ttu-id="a3cff-235">Si noti che non è necessario basarsi sulla condizione $Component 1 = 3 per verificare se Component1 è installato localmente nel computer.</span><span class="sxs-lookup"><span data-stu-id="a3cff-235">Note that you should not depend upon the condition $Component1=3 to check whether Component1 is locally installed on the computer.</span></span> <span data-ttu-id="a3cff-236">Questa operazione può avere esito negativo se Component1 è installato da più di un prodotto.</span><span class="sxs-lookup"><span data-stu-id="a3cff-236">This can fail if Component1 is installed by more than one product.</span></span> <span data-ttu-id="a3cff-237">Dopo che Component1 è stato installato localmente da product1, il programma di installazione valuta la condizione $Component 1 = 3 come false durante l'installazione di Product2.</span><span class="sxs-lookup"><span data-stu-id="a3cff-237">After Component1 has been installed locally by Product1, the installer evaluates the condition $Component1=3 as False during the installation of Product2.</span></span> <span data-ttu-id="a3cff-238">Questo perché il programma di installazione determina la versione del componente usando il percorso della chiave del componente e contrassegna il componente per l'installazione se la relativa versione è maggiore o uguale al componente installato.</span><span class="sxs-lookup"><span data-stu-id="a3cff-238">This is because the installer determines the version of the component using the component's key path and marks the component for installation if its version is greater than or equal to the installed component.</span></span>

<span data-ttu-id="a3cff-239">Si noti che il programma di installazione non esegue confronti diretti del tipo di dati [Version](version.md) nelle istruzioni condizionali.</span><span class="sxs-lookup"><span data-stu-id="a3cff-239">Note that the installer will not do direct comparisons of the [Version](version.md) data type in conditional statements.</span></span> <span data-ttu-id="a3cff-240">Ad esempio, non è possibile utilizzare operatori comparative per confrontare versioni quali "01,10" e "1,010" in un'istruzione condizionale.</span><span class="sxs-lookup"><span data-stu-id="a3cff-240">For example, you cannot use comparative operators to compare versions such as "01.10" and "1.010" in a conditional statement.</span></span> <span data-ttu-id="a3cff-241">Usare invece un metodo valido per cercare una versione, come descritto in [ricerca di applicazioni esistenti, file, voci del registro di sistema o voci di file ini](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md), quindi impostare una proprietà.</span><span class="sxs-lookup"><span data-stu-id="a3cff-241">Instead use a valid method to search for a version, such as described in [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md), and then set a property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3cff-242">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a3cff-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3cff-243">Uso delle proprietà nelle istruzioni condizionali</span><span class="sxs-lookup"><span data-stu-id="a3cff-243">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)
</dt> </dl>

 

 



