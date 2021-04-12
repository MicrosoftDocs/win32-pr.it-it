---
description: È possibile definire e assegnare ambiti di input personalizzati utilizzando la sintassi delle espressioni regolari della grafia riconosciuta da alcuni riconoscitori della grafia Microsoft.
ms.assetid: e3afe735-eca8-4fda-bd5b-cc0ab0b6a872
title: Riferimento alla sintassi delle espressioni regolari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c0de50ff37795032719d9bc90ee81891324ba9
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104234437"
---
# <a name="regular-expression-syntax-reference"></a><span data-ttu-id="4e895-103">Riferimento alla sintassi delle espressioni regolari</span><span class="sxs-lookup"><span data-stu-id="4e895-103">Regular Expression Syntax Reference</span></span>

<span data-ttu-id="4e895-104">È possibile definire e assegnare ambiti di input personalizzati utilizzando la sintassi delle espressioni regolari della grafia riconosciuta da alcuni riconoscitori della grafia Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4e895-104">You can define and assign custom input scopes using the handwriting regular expression syntax that is understood by some of the Microsoft handwriting recognizers.</span></span> <span data-ttu-id="4e895-105">La sintassi è un subset dell' [implementazione del linguaggio delle espressioni regolari](/documentation/?url=%2flibrary%2fcpgenref%2fhtml%2fcpconRegularExpressionsLanguageElements.asp%3fframe%3dtrue) nel .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="4e895-105">The syntax is a subset of the [Regular Expression Language Implementation](/documentation/?url=%2flibrary%2fcpgenref%2fhtml%2fcpconRegularExpressionsLanguageElements.asp%3fframe%3dtrue) in the .NET Framework.</span></span>

<span data-ttu-id="4e895-106">Esistono alcune differenze nel modo in cui vengono utilizzate le espressioni regolari della grafia e il modo in cui vengono utilizzati gli altri tipi di espressioni regolari.</span><span class="sxs-lookup"><span data-stu-id="4e895-106">There are some differences in the way that handwriting regular expressions are used and the way the other types of regular expressions are used.</span></span> <span data-ttu-id="4e895-107">La sintassi della grafia viene utilizzata per specificare una stringa esatta che verrà confrontata con il motore di riconoscimento e non con una sottostringa.</span><span class="sxs-lookup"><span data-stu-id="4e895-107">The handwriting syntax is used to specify an exact string that will be matched by the recognition engine and not a sub-string.</span></span> <span data-ttu-id="4e895-108">Ad esempio, l'espressione regolare s ( \[ a-z \] +) p restituirà corrispondenze per "soup", "Stop", "Instep" e "esofago".</span><span class="sxs-lookup"><span data-stu-id="4e895-108">For example, the regular expression s(\[a-z\]+)p would return matches for "soup", "stop", "instep", and "esophagus".</span></span> <span data-ttu-id="4e895-109">Invece, un'espressione regolare di grafia equivalente, ad esempio s (! IS \_ ONechar) + p, corrisponderebbe a "soup" e "Stop", ma non a "Instep" e "esofago".</span><span class="sxs-lookup"><span data-stu-id="4e895-109">Whereas, an equivalent handwriting regular expression such as s(!IS\_ONECHAR)+p would match "soup" and "stop", but not "instep" and "esophagus".</span></span>

<span data-ttu-id="4e895-110">Le espressioni regolari di grafia non supportano gli spazi non di suddivisione nelle espressioni regolari.</span><span class="sxs-lookup"><span data-stu-id="4e895-110">Handwriting regular expressions do not support non-breaking spaces within regular expressions.</span></span> <span data-ttu-id="4e895-111">Ovvero non è possibile utilizzare l'entità "nbsp" all'interno di un'espressione regolare di grafia.</span><span class="sxs-lookup"><span data-stu-id="4e895-111">That is, you cannot use the "nbsp" entity within a handwriting regular expression.</span></span>

<span data-ttu-id="4e895-112">Le sezioni seguenti descrivono la sintassi in modo più dettagliato.</span><span class="sxs-lookup"><span data-stu-id="4e895-112">The following sections describe the syntax in more detail.</span></span>

## <a name="valid-operators"></a><span data-ttu-id="4e895-113">Operatori validi</span><span class="sxs-lookup"><span data-stu-id="4e895-113">Valid Operators</span></span>

<span data-ttu-id="4e895-114">Gli operatori seguenti sono validi per la creazione di espressioni regolari per la definizione degli ambiti di input per i riconoscitori della grafia.</span><span class="sxs-lookup"><span data-stu-id="4e895-114">The following operators are valid for creating regular expressions to define input scopes for handwriting recognizers.</span></span>



| <span data-ttu-id="4e895-115">Operatore</span><span class="sxs-lookup"><span data-stu-id="4e895-115">Operator</span></span>      | <span data-ttu-id="4e895-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e895-116">Description</span></span>                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| \*<br/> | <span data-ttu-id="4e895-117">Operatore unario suffisso che significa zero o più occorrenze dell'operando.</span><span class="sxs-lookup"><span data-stu-id="4e895-117">Postfix unary operator signifying zero or more occurrences of the operand.</span></span><br/> |
| +<br/>  | <span data-ttu-id="4e895-118">Operatore unario suffisso che indica una o più occorrenze dell'operando.</span><span class="sxs-lookup"><span data-stu-id="4e895-118">Postfix unary operator signifying one or more occurrences of the operand.</span></span><br/>  |
| <span data-ttu-id="4e895-119">?</span><span class="sxs-lookup"><span data-stu-id="4e895-119">?</span></span><br/>  | <span data-ttu-id="4e895-120">Operatore unario suffisso che significa zero o una occorrenza dell'operando.</span><span class="sxs-lookup"><span data-stu-id="4e895-120">Postfix unary operator signifying zero or one occurrence of the operand.</span></span><br/>   |
| \|<br/> | <span data-ttu-id="4e895-121">Operatore infisso binario che significa "or".</span><span class="sxs-lookup"><span data-stu-id="4e895-121">Binary infix operator meaning "or".</span></span><br/>                                        |
| <span data-ttu-id="4e895-122">()</span><span class="sxs-lookup"><span data-stu-id="4e895-122">()</span></span><br/> | <span data-ttu-id="4e895-123">Utilizzato per raggruppare gli elementi.</span><span class="sxs-lookup"><span data-stu-id="4e895-123">Used to group items.</span></span><br/>                                                       |



 

<span data-ttu-id="4e895-124">L'implementazione Microsoft di espressioni regolari per i riconoscitori della grafia consente le applicazioni ripetute di operatori unari di suffisso.</span><span class="sxs-lookup"><span data-stu-id="4e895-124">The Microsoft implementation of regular expressions for handwriting recognizers allows repeated applications of postfix unary operators.</span></span> <span data-ttu-id="4e895-125">Ad esempio, a \* \* = (a \* ) \* = a \* , b??</span><span class="sxs-lookup"><span data-stu-id="4e895-125">For example, a\*\* = (a\*)\* = a\*, b??</span></span> <span data-ttu-id="4e895-126">= (b?)?</span><span class="sxs-lookup"><span data-stu-id="4e895-126">= (b?)?</span></span> <span data-ttu-id="4e895-127">= b?.</span><span class="sxs-lookup"><span data-stu-id="4e895-127">= b?.</span></span> <span data-ttu-id="4e895-128">Consentono inoltre ripetizioni non consecutive, ad esempio: a \* ? \* = ((a \* )?) \* = (a \* ) \* = a \* .</span><span class="sxs-lookup"><span data-stu-id="4e895-128">They also allow non-consecutive repetitions, for example: a\*?\* = ((a\*)?)\* = (a\*)\* = a\*.</span></span> <span data-ttu-id="4e895-129">Si tratta di una differenza rispetto a .NET Framework espressioni regolari, che consentono solo?</span><span class="sxs-lookup"><span data-stu-id="4e895-129">This is different from .NET Framework regular expressions, which only allow the ?</span></span> <span data-ttu-id="4e895-130">operatore da ripetere.</span><span class="sxs-lookup"><span data-stu-id="4e895-130">operator to be repeated.</span></span>

<span data-ttu-id="4e895-131">Un'altra differenza rispetto a .NET Framework espressioni regolari è che le espressioni regolari della grafia non supportano un'espressione vuota designata con una coppia di parentesi vuota, ().</span><span class="sxs-lookup"><span data-stu-id="4e895-131">Another difference from .NET Framework regular expressions is that handwriting regular expressions do not support an empty expression designated with an empty pair of parentheses, ().</span></span>

> [!Note]  
> <span data-ttu-id="4e895-132">Solo i caratteri della tabella codici 1252 sono supportati per le espressioni regolari di grafia.</span><span class="sxs-lookup"><span data-stu-id="4e895-132">Only characters in the 1252 codepage are supported for handwriting regular expressions.</span></span>

 

## <a name="using-input-scopes"></a><span data-ttu-id="4e895-133">Uso degli ambiti di input</span><span class="sxs-lookup"><span data-stu-id="4e895-133">Using Input Scopes</span></span>

<span data-ttu-id="4e895-134">È anche possibile usare il set di ambiti di input normali definiti come parte della funzione [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) nelle espressioni regolari.</span><span class="sxs-lookup"><span data-stu-id="4e895-134">You can also use the set of regular input scopes that are defined as part of the [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) function in your regular expressions.</span></span> <span data-ttu-id="4e895-135">Il valore per month (Numerical), ad esempio, è \_ date \_ Month.</span><span class="sxs-lookup"><span data-stu-id="4e895-135">For example, the value for Month (numerical) is IS\_DATE\_MONTH.</span></span> <span data-ttu-id="4e895-136">La sintassi per specificare un ambito di input come parte di un'espressione regolare è anteporre il valore enumerato dell'ambito di input con una parentesi aperta e un punto esclamativo, (!, e inserire una parentesi di chiusura,) alla fine.</span><span class="sxs-lookup"><span data-stu-id="4e895-136">The syntax for specifying an input scope as part of a regular expression is to prepend the input scope enumerated value with an open parenthesis and an exclamation point, (!, and place a closing parenthesis, ), on the end.</span></span> <span data-ttu-id="4e895-137">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="4e895-137">For example:</span></span>

<span data-ttu-id="4e895-138">(! È \_ \_mese data)</span><span class="sxs-lookup"><span data-stu-id="4e895-138">(!IS\_DATE\_MONTH)</span></span>

<span data-ttu-id="4e895-139">Se si combina l' \_ ambito di input predefinito Oring con qualsiasi altro ambito di input, l'effetto è che il riconoscimento può restituire qualsiasi espressione singola supportata dal modello di lingua predefinito (ad esempio, una parola dal dizionario di sistema o una data) con o senza punteggiatura oppure qualsiasi valore che soddisfi il resto dell'espressione regolare passata al riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="4e895-139">If you combine the IS\_DEFAULT input scope by ORing it with any other input scope, the effect is that the recognizer can return either any single expression that the default language model supports (for example, one word from the system dictionary or a date) with or without punctuation, or any value that meets the rest of the regular expression passed in to the recognizer.</span></span>

> [!Note]  
> <span data-ttu-id="4e895-140">I membri seguenti di [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) non sono supportati nelle espressioni regolari: è l'oggetto \_ Phrase, è \_ REGULAREXPRESSION, è \_ SRGS, è \_ XML.</span><span class="sxs-lookup"><span data-stu-id="4e895-140">The following members of [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) are not supported in regular expressions: IS\_PHRASELIST, IS\_REGULAREXPRESSION, IS\_SRGS, IS\_XML.</span></span>

 

## <a name="unsupported-operators"></a><span data-ttu-id="4e895-141">Operatori non supportati</span><span class="sxs-lookup"><span data-stu-id="4e895-141">Unsupported Operators</span></span>

<span data-ttu-id="4e895-142">Gli operatori di espressioni regolari seguenti non sono supportati quando si creano espressioni regolari della grafia.</span><span class="sxs-lookup"><span data-stu-id="4e895-142">The following regular expression operators are not supported when creating handwriting regular expressions.</span></span>



| <span data-ttu-id="4e895-143">Operatore</span><span class="sxs-lookup"><span data-stu-id="4e895-143">Operator</span></span>                                     | <span data-ttu-id="4e895-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e895-144">Description</span></span>                                                         |
|----------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="4e895-145">.</span><span class="sxs-lookup"><span data-stu-id="4e895-145">.</span></span><br/>                                 | <span data-ttu-id="4e895-146">Carattere punto.</span><span class="sxs-lookup"><span data-stu-id="4e895-146">Period character.</span></span><br/>                                        |
| \[\]<br/>                              | <span data-ttu-id="4e895-147">Parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="4e895-147">Square brackets.</span></span> <span data-ttu-id="4e895-148">Usare le parentesi per raggruppare gli elementi.</span><span class="sxs-lookup"><span data-stu-id="4e895-148">Use parenthesis for grouping items.</span></span><br/>     |
| {}<br/>                                | <span data-ttu-id="4e895-149">Parentesi graffe.</span><span class="sxs-lookup"><span data-stu-id="4e895-149">Curly brackets.</span></span><br/>                                          |
| <span data-ttu-id="4e895-150">(?\# commento) e \# \[ Commento\]</span><span class="sxs-lookup"><span data-stu-id="4e895-150">(?\# comment) and \#\[ comment \]</span></span><br/> | <span data-ttu-id="4e895-151">Commenti.</span><span class="sxs-lookup"><span data-stu-id="4e895-151">Comments.</span></span><br/>                                                |
| $<br/>                                 | <span data-ttu-id="4e895-152">Segno di dollaro.</span><span class="sxs-lookup"><span data-stu-id="4e895-152">Dollar sign character.</span></span><br/>                                   |
| ^<br/>                                 | <span data-ttu-id="4e895-153">Carattere del punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="4e895-153">Caret character.</span></span><br/>                                         |
| -<br/>                                 | <span data-ttu-id="4e895-154">Carattere tratteggiato.</span><span class="sxs-lookup"><span data-stu-id="4e895-154">Dash character.</span></span> <span data-ttu-id="4e895-155">Deve o ( \| ) insieme tutti i set di elementi.</span><span class="sxs-lookup"><span data-stu-id="4e895-155">Must OR (\|) together all sets of items.</span></span><br/> |



 

## <a name="escaping-characters"></a><span data-ttu-id="4e895-156">Utilizzo di caratteri di escape</span><span class="sxs-lookup"><span data-stu-id="4e895-156">Escaping Characters</span></span>

<span data-ttu-id="4e895-157">I caratteri ordinari, diversi da quelli nella tabella seguente, corrispondono a se stessi.</span><span class="sxs-lookup"><span data-stu-id="4e895-157">Ordinary characters, other than the ones in the following table, match themselves.</span></span> <span data-ttu-id="4e895-158">Ovvero un "a" in un'espressione regolare specifica che l'input deve corrispondere a "a".</span><span class="sxs-lookup"><span data-stu-id="4e895-158">That is, an "a" in a regular expression specifies that input should match an "a".</span></span>

<span data-ttu-id="4e895-159">Un'altra differenza significativa nella scrittura di espressioni regolari di grafia è che è possibile escludere solo un set limitato di caratteri all'interno di un'espressione regolare.</span><span class="sxs-lookup"><span data-stu-id="4e895-159">Another significant difference in writing handwriting regular expressions is that you can only escape a limited set of characters within a regular expression.</span></span> <span data-ttu-id="4e895-160">Nella tabella seguente viene descritto il set di caratteri consentito di cui è possibile utilizzare il carattere di escape.</span><span class="sxs-lookup"><span data-stu-id="4e895-160">The following table outlines the allowed set of characters that can be escaped.</span></span> <span data-ttu-id="4e895-161">Qualsiasi altro tentativo di eseguire l'escape di un carattere provocherà un errore generato dal riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="4e895-161">Any other attempt to escape a character will result in an error being thrown by the recognizer.</span></span>



| <span data-ttu-id="4e895-162">Carattere</span><span class="sxs-lookup"><span data-stu-id="4e895-162">Character</span></span>       |
|-----------------|
| \\\*<br/> |
| \\+<br/>  |
| <span data-ttu-id="4e895-163">\\?</span><span class="sxs-lookup"><span data-stu-id="4e895-163">\\?</span></span><br/>  |
| <span data-ttu-id="4e895-164">\\(</span><span class="sxs-lookup"><span data-stu-id="4e895-164">\\(</span></span><br/>  |
| <span data-ttu-id="4e895-165">\\)</span><span class="sxs-lookup"><span data-stu-id="4e895-165">\\)</span></span><br/>  |
| \\\|<br/> |
| \\\\<br/> |
| <span data-ttu-id="4e895-166">\\!</span><span class="sxs-lookup"><span data-stu-id="4e895-166">\\!</span></span><br/>  |
| <span data-ttu-id="4e895-167">\\.</span><span class="sxs-lookup"><span data-stu-id="4e895-167">\\.</span></span><br/>  |
| \\\[<br/> |
| \\\]<br/> |
| \\^<br/>  |
| <span data-ttu-id="4e895-168">\\{</span><span class="sxs-lookup"><span data-stu-id="4e895-168">\\{</span></span><br/>  |
| <span data-ttu-id="4e895-169">\\}</span><span class="sxs-lookup"><span data-stu-id="4e895-169">\\}</span></span><br/>  |
| \\$<br/>  |
| \\\#<br/> |



 

 

 