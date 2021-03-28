---
title: '\#define (direttiva) (macro)'
description: Direttiva per il preprocessore che crea una macro simile a una funzione.
ms.assetid: 73c19cf8-fbc5-444b-a51f-dc9f881f397b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8de5a47fc92c02e9f565c80f600359e8e5b32f9
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104993277"
---
# <a name="define-directive-macro"></a><span data-ttu-id="3d07b-103">\#define (direttiva) (macro)</span><span class="sxs-lookup"><span data-stu-id="3d07b-103">\#define directive (macro)</span></span>

<span data-ttu-id="3d07b-104">Direttiva per il preprocessore che crea una macro simile a una funzione.</span><span class="sxs-lookup"><span data-stu-id="3d07b-104">Preprocessor directive that creates a function-like macro.</span></span>



| <span data-ttu-id="3d07b-105">\#define *Identifier*( *argument0*,..., *argumentn-1* ) *token-String*</span><span class="sxs-lookup"><span data-stu-id="3d07b-105">\#define *identifier*( *argument0*, ... , *argumentN-1* ) *token-string*</span></span> |
|--------------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="3d07b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d07b-106">Parameters</span></span>



| <span data-ttu-id="3d07b-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="3d07b-107">Item</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="3d07b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d07b-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d07b-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*identificatore*</span><span class="sxs-lookup"><span data-stu-id="3d07b-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/>                                                                                                                                                                             | <span data-ttu-id="3d07b-110">Identificatore della macro.</span><span class="sxs-lookup"><span data-stu-id="3d07b-110">Identifier of the macro.</span></span> <br/> <span data-ttu-id="3d07b-111">Una seconda [ \# definizione](dx-graphics-hlsl-appendix-pre-define.md) per una macro con un identificatore già esistente nel contesto corrente genera un errore a meno che la seconda sequenza di token non sia identica alla prima.</span><span class="sxs-lookup"><span data-stu-id="3d07b-111">A second [\#define](dx-graphics-hlsl-appendix-pre-define.md) for a macro with an identifier that already exists in the current context generates an error unless the second token sequence is identical to the first.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="3d07b-112"><span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*,..., *argomento-1* )</span><span class="sxs-lookup"><span data-stu-id="3d07b-112"><span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*, ... , *argumentN-1* )</span></span> <br/> | <span data-ttu-id="3d07b-113">Elenco di argomenti per la macro.</span><span class="sxs-lookup"><span data-stu-id="3d07b-113">List of arguments to the macro.</span></span> <span data-ttu-id="3d07b-114">L'elenco di argomenti è delimitato da virgole, può essere di qualsiasi lunghezza e deve essere racchiuso tra parentesi.</span><span class="sxs-lookup"><span data-stu-id="3d07b-114">The argument list is comma-delimited, can be of any length, and must be enclosed in parentheses.</span></span> <span data-ttu-id="3d07b-115">Ogni nome di argomento nell'elenco deve essere univoco.</span><span class="sxs-lookup"><span data-stu-id="3d07b-115">Each argument name in the list must be unique.</span></span> <span data-ttu-id="3d07b-116">Nessuno spazio vuoto può separare il parametro *Identifier* e la parentesi di apertura.</span><span class="sxs-lookup"><span data-stu-id="3d07b-116">No white space can separate the *identifier* parameter and the opening parenthesis.</span></span> <br/> <span data-ttu-id="3d07b-117">Utilizzare la concatenazione di righe per inserire una barra rovesciata ( \) immediatamente prima del carattere di nuova riga per suddividere le direttive Long su più righe di origine</span><span class="sxs-lookup"><span data-stu-id="3d07b-117">Use line concatenation place a backslash (\) immediately before the newline character to split long directives onto multiple source lines.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="3d07b-118"><span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*stringa* \[ di token opzionale\]</span><span class="sxs-lookup"><span data-stu-id="3d07b-118"><span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*token-string* \[optional\]</span></span> <br/>                                                                                                                     | <span data-ttu-id="3d07b-119">Valore della macro.</span><span class="sxs-lookup"><span data-stu-id="3d07b-119">Value of the macro.</span></span> <span data-ttu-id="3d07b-120">Questo parametro è costituito da una serie di token, ad esempio parole chiave, costanti o istruzioni complete.</span><span class="sxs-lookup"><span data-stu-id="3d07b-120">This parameter consists of a series of tokens, such as keywords, constants, or complete statements.</span></span> <span data-ttu-id="3d07b-121">Uno o più caratteri di spazio vuoto devono separare questo parametro dal parametro *Identifier* . Questo spazio vuoto non è considerato parte del testo sostituito, né lo spazio vuoto dopo l'ultimo token del testo.</span><span class="sxs-lookup"><span data-stu-id="3d07b-121">One or more white-space characters must separate this parameter from the *identifier* parameter; this white space is not considered part of the substituted text, nor is any white space following the last token of the text.</span></span> <span data-ttu-id="3d07b-122">Usare le parentesi per assicurarsi che gli argomenti complessi vengano interpretati correttamente.</span><span class="sxs-lookup"><span data-stu-id="3d07b-122">Make liberal use of parentheses to ensure that complicated arguments are interpreted correctly.</span></span> <br/> <span data-ttu-id="3d07b-123">Se il valore del parametro *Identifier* si verifica all'interno del parametro della *stringa del token* (anche come risultato di un'altra espansione di una macro), non viene espanso.</span><span class="sxs-lookup"><span data-stu-id="3d07b-123">If the value of the *identifier* parameter occurs within the *token-string* parameter (even as a result of another macro expansion), it is not expanded.</span></span> <br/> <span data-ttu-id="3d07b-124">Se si esclude questo parametro, tutte le istanze del parametro *Identifier* verranno rimosse dal file di origine.</span><span class="sxs-lookup"><span data-stu-id="3d07b-124">If you exclude this parameter, all instances of the *identifier* parameter are removed from the source file.</span></span> <span data-ttu-id="3d07b-125">L'identificatore rimane definito e può essere testato utilizzando le direttive [ \# if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \# ifdef e \# ifndef.</span><span class="sxs-lookup"><span data-stu-id="3d07b-125">The identifier remains defined, and can be tested using the [\#if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \#ifdef, and \#ifndef directives.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="3d07b-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d07b-126">Remarks</span></span>

<span data-ttu-id="3d07b-127">Tutte le istanze del parametro *Identifier* che si verificano dopo la direttiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) nel file di origine costituiscono una chiamata di macro e l'identificatore verrà sostituito da una versione del parametro della *stringa di token* con argomenti effettivi sostituiti per i parametri formali.</span><span class="sxs-lookup"><span data-stu-id="3d07b-127">All instances of the *identifier* parameter that occur after the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive in the source file constitute a macro call, and the identifier will be replaced by a version of the *token-string* parameter that has actual arguments substituted for formal parameters.</span></span> <span data-ttu-id="3d07b-128">Il numero di parametri nella chiamata deve corrispondere al numero di parametri nella definizione della macro.</span><span class="sxs-lookup"><span data-stu-id="3d07b-128">The number of parameters in the call must match the number of parameters in the macro definition.</span></span> <span data-ttu-id="3d07b-129">L'identificatore viene sostituito solo quando costituisce un token. l'identificatore, ad esempio, non viene sostituito se viene visualizzato in un commento, all'interno di una stringa o come parte di un identificatore più lungo.</span><span class="sxs-lookup"><span data-stu-id="3d07b-129">The identifier is replaced only when it forms a token; for example, the identifier is not replaced if it appears in a comment, within a string, or as part of a longer identifier.</span></span>

<span data-ttu-id="3d07b-130">La direttiva [ \# undef](dx-graphics-hlsl-appendix-pre-undef.md) indica al preprocessore di dimenticare la definizione di un identificatore. per ulteriori informazioni, vedere la \# direttiva undef (DirectX HLSL).</span><span class="sxs-lookup"><span data-stu-id="3d07b-130">The [\#undef](dx-graphics-hlsl-appendix-pre-undef.md) directive instructs the preprocessor to forget the definition of an identifier; for more information, see \#undef Directive (DirectX HLSL).</span></span>

<span data-ttu-id="3d07b-131">La definizione di costanti con l'opzione del compilatore/D ha lo stesso effetto dell'uso della direttiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) all'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="3d07b-131">Defining constants with the /D compiler option has the same effect as using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive at the beginning of your file.</span></span> <span data-ttu-id="3d07b-132">Con l'opzione/D è possibile definire fino a 30 macro.</span><span class="sxs-lookup"><span data-stu-id="3d07b-132">Up to 30 macros can be defined with the /D option.</span></span>

<span data-ttu-id="3d07b-133">Gli argomenti effettivi nella chiamata della macro vengono associati agli argomenti formali corrispondenti nella definizione della macro.</span><span class="sxs-lookup"><span data-stu-id="3d07b-133">The actual arguments in the macro call are matched to the corresponding formal arguments in the macro definition.</span></span> <span data-ttu-id="3d07b-134">Ogni argomento formale nella stringa del token viene sostituito dall'argomento effettivo corrispondente, a meno che l'argomento non sia preceduto da un operatore per ( \# ), charizing ( \# @) o da un token-Pasting ( \# \# ) o sia seguito da un \# \# operatore.</span><span class="sxs-lookup"><span data-stu-id="3d07b-134">Each formal argument in the token string is replaced by the corresponding actual argument, unless the argument is preceded by a stringizing (\#), charizing (\#@), or token-pasting (\#\#) operator, or is followed by a \#\# operator.</span></span> <span data-ttu-id="3d07b-135">Eventuali macro presenti nell'argomento effettivo vengono espanse prima che la direttiva sostituisca il parametro formale.</span><span class="sxs-lookup"><span data-stu-id="3d07b-135">Any macros in the actual argument are expanded before the directive replaces the formal parameter.</span></span>

<span data-ttu-id="3d07b-136">Il token incollato nel compilatore HLSL è leggermente diverso da quello del token incollato nel compilatore C, in quanto i token incollati devono essere token validi.</span><span class="sxs-lookup"><span data-stu-id="3d07b-136">Token pasting in the HLSL compiler is slightly different from token pasting in the C compiler, in that the pasted tokens must be valid tokens on their own.</span></span> <span data-ttu-id="3d07b-137">Si consideri, ad esempio, la seguente definizione di macro:</span><span class="sxs-lookup"><span data-stu-id="3d07b-137">For example, consider the following macro definition:</span></span>


```
#define MERGE(a, b) a##b
MERGE(float, 4x4) test;
```



<span data-ttu-id="3d07b-138">Nel compilatore C, il risultato è il seguente:</span><span class="sxs-lookup"><span data-stu-id="3d07b-138">In the C compiler, this results in the following:</span></span>


```
float4x4 test
```



<span data-ttu-id="3d07b-139">Nel compilatore HLSL, tuttavia, si ottiene quanto segue:</span><span class="sxs-lookup"><span data-stu-id="3d07b-139">In the HLSL compiler however, this results in the following:</span></span>


```
float4 x4 test
```



<span data-ttu-id="3d07b-140">È possibile ovviare a questo comportamento usando invece la definizione di macro seguente.</span><span class="sxs-lookup"><span data-stu-id="3d07b-140">You can work around this behavior by using the following macro definition instead.</span></span>


```
MERGE(MERGE(float, 4), x4) test;
```



## <a name="examples"></a><span data-ttu-id="3d07b-141">Esempio</span><span class="sxs-lookup"><span data-stu-id="3d07b-141">Examples</span></span>

<span data-ttu-id="3d07b-142">Nell'esempio seguente viene utilizzata una macro per definire le linee del cursore.</span><span class="sxs-lookup"><span data-stu-id="3d07b-142">The following example uses a macro to define cursor lines.</span></span>


```
#define CURSOR(top, bottom) (((top) << 8) | (bottom))
```



<span data-ttu-id="3d07b-143">Nell'esempio seguente viene definita una macro che recupera un Integer pseudocasuale nell'intervallo specificato.</span><span class="sxs-lookup"><span data-stu-id="3d07b-143">The following example defines a macro that retrieves a pseudorandom integer in the specified range.</span></span>


```
#define getrandom(min, max) \
((rand()%(int)(((max) + 1)-(min)))+ (min))
```



## <a name="related-topics"></a><span data-ttu-id="3d07b-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3d07b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d07b-145">Direttive per il preprocessore (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3d07b-145">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="3d07b-146">\#definire gli overload</span><span class="sxs-lookup"><span data-stu-id="3d07b-146">\#define Overloads</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[<span data-ttu-id="3d07b-147">\#Direttiva undef (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3d07b-147">\#undef Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





