---
title: '\#Direttiva define (macro)'
description: Direttiva del preprocessore che crea una macro simile a una funzione.
ms.assetid: 73c19cf8-fbc5-444b-a51f-dc9f881f397b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d0c54c0c433c91522c8a72c5955a419eb72f9eee
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387517"
---
# <a name="define-directive-macro"></a><span data-ttu-id="72dc5-103">\#Direttiva define (macro)</span><span class="sxs-lookup"><span data-stu-id="72dc5-103">\#define directive (macro)</span></span>

<span data-ttu-id="72dc5-104">Direttiva del preprocessore che crea una macro simile a una funzione.</span><span class="sxs-lookup"><span data-stu-id="72dc5-104">Preprocessor directive that creates a function-like macro.</span></span>



| <span data-ttu-id="72dc5-105">\#identificatore *define*( *argument0*, ... , *argumentN-1* ) *token-string*</span><span class="sxs-lookup"><span data-stu-id="72dc5-105">\#define *identifier*( *argument0*, ... , *argumentN-1* ) *token-string*</span></span> |
|--------------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="72dc5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="72dc5-106">Parameters</span></span>



| <span data-ttu-id="72dc5-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="72dc5-107">Item</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="72dc5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72dc5-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72dc5-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*Identificatore*</span><span class="sxs-lookup"><span data-stu-id="72dc5-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/>                                                                                                                                                                             | <span data-ttu-id="72dc5-110">Identificatore della macro.</span><span class="sxs-lookup"><span data-stu-id="72dc5-110">Identifier of the macro.</span></span> <br/> <span data-ttu-id="72dc5-111">Una seconda [ \# definizione](dx-graphics-hlsl-appendix-pre-define.md) per una macro con un identificatore già esistente nel contesto corrente genera un errore a meno che la seconda sequenza di token non sia identica alla prima.</span><span class="sxs-lookup"><span data-stu-id="72dc5-111">A second [\#define](dx-graphics-hlsl-appendix-pre-define.md) for a macro with an identifier that already exists in the current context generates an error unless the second token sequence is identical to the first.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="72dc5-112"><span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*, ... , *argumentN-1* )</span><span class="sxs-lookup"><span data-stu-id="72dc5-112"><span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*, ... , *argumentN-1* )</span></span> <br/> | <span data-ttu-id="72dc5-113">Elenco di argomenti per la macro.</span><span class="sxs-lookup"><span data-stu-id="72dc5-113">List of arguments to the macro.</span></span> <span data-ttu-id="72dc5-114">L'elenco di argomenti è delimitato da virgole, può essere di qualsiasi lunghezza e deve essere racchiuso tra parentesi.</span><span class="sxs-lookup"><span data-stu-id="72dc5-114">The argument list is comma-delimited, can be of any length, and must be enclosed in parentheses.</span></span> <span data-ttu-id="72dc5-115">Ogni nome di argomento nell'elenco deve essere univoco.</span><span class="sxs-lookup"><span data-stu-id="72dc5-115">Each argument name in the list must be unique.</span></span> <span data-ttu-id="72dc5-116">Nessuno spazio vuoto può separare il *parametro identifier* e la parentesi di apertura.</span><span class="sxs-lookup"><span data-stu-id="72dc5-116">No white space can separate the *identifier* parameter and the opening parenthesis.</span></span> <br/> <span data-ttu-id="72dc5-117">Usare la concatenazione di righe posizionare una barra rovesciata ( ) immediatamente prima del carattere di nuova riga per dividere le direttive lunghe \\ in più righe di origine.</span><span class="sxs-lookup"><span data-stu-id="72dc5-117">Use line concatenation place a backslash (\\) immediately before the newline character to split long directives onto multiple source lines.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="72dc5-118"><span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*token-string* \[ Opzionale\]</span><span class="sxs-lookup"><span data-stu-id="72dc5-118"><span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*token-string* \[optional\]</span></span> <br/>                                                                                                                     | <span data-ttu-id="72dc5-119">Valore della macro.</span><span class="sxs-lookup"><span data-stu-id="72dc5-119">Value of the macro.</span></span> <span data-ttu-id="72dc5-120">Questo parametro è costituito da una serie di token, ad esempio parole chiave, costanti o istruzioni complete.</span><span class="sxs-lookup"><span data-stu-id="72dc5-120">This parameter consists of a series of tokens, such as keywords, constants, or complete statements.</span></span> <span data-ttu-id="72dc5-121">Uno o più spazi vuoti devono separare questo parametro dal parametro *identifier.* questo spazio vuoto non viene considerato parte del testo sostituito, né lo spazio vuoto dopo l'ultimo token del testo.</span><span class="sxs-lookup"><span data-stu-id="72dc5-121">One or more white-space characters must separate this parameter from the *identifier* parameter; this white space is not considered part of the substituted text, nor is any white space following the last token of the text.</span></span> <span data-ttu-id="72dc5-122">Usare liberamente le parentesi per garantire che gli argomenti complessi vengano interpretati correttamente.</span><span class="sxs-lookup"><span data-stu-id="72dc5-122">Make liberal use of parentheses to ensure that complicated arguments are interpreted correctly.</span></span> <br/> <span data-ttu-id="72dc5-123">Se il valore del parametro *identifier* si trova all'interno del *parametro token-string* (anche in seguito a un'altra espansione della macro), non viene espanso.</span><span class="sxs-lookup"><span data-stu-id="72dc5-123">If the value of the *identifier* parameter occurs within the *token-string* parameter (even as a result of another macro expansion), it is not expanded.</span></span> <br/> <span data-ttu-id="72dc5-124">Se si esclude questo parametro, tutte le istanze del parametro *identifier* vengono rimosse dal file di origine.</span><span class="sxs-lookup"><span data-stu-id="72dc5-124">If you exclude this parameter, all instances of the *identifier* parameter are removed from the source file.</span></span> <span data-ttu-id="72dc5-125">L'identificatore rimane definito e può essere testato usando le direttive [ \# ifdefined](dx-graphics-hlsl-appendix-pre-ifdef.md), \# ifdef e \# ifndef.</span><span class="sxs-lookup"><span data-stu-id="72dc5-125">The identifier remains defined, and can be tested using the [\#if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \#ifdef, and \#ifndef directives.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="72dc5-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="72dc5-126">Remarks</span></span>

<span data-ttu-id="72dc5-127">Tutte le istanze del parametro *identifier* che si verificano dopo la direttiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) nel file di origine costituiscono una chiamata macro e l'identificatore verrà sostituito da una versione del parametro *token-string* con argomenti effettivi sostituiti da parametri formali.</span><span class="sxs-lookup"><span data-stu-id="72dc5-127">All instances of the *identifier* parameter that occur after the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive in the source file constitute a macro call, and the identifier will be replaced by a version of the *token-string* parameter that has actual arguments substituted for formal parameters.</span></span> <span data-ttu-id="72dc5-128">Il numero di parametri nella chiamata deve corrispondere al numero di parametri nella definizione della macro.</span><span class="sxs-lookup"><span data-stu-id="72dc5-128">The number of parameters in the call must match the number of parameters in the macro definition.</span></span> <span data-ttu-id="72dc5-129">L'identificatore viene sostituito solo quando forma un token. Ad esempio, l'identificatore non viene sostituito se viene visualizzato in un commento, all'interno di una stringa o come parte di un identificatore più lungo.</span><span class="sxs-lookup"><span data-stu-id="72dc5-129">The identifier is replaced only when it forms a token; for example, the identifier is not replaced if it appears in a comment, within a string, or as part of a longer identifier.</span></span>

<span data-ttu-id="72dc5-130">La [ \# direttiva undef](dx-graphics-hlsl-appendix-pre-undef.md) indica al preprocessore di dimenticare la definizione di un identificatore. Per altre informazioni, vedere Direttiva \# undef (DirectX HLSL).</span><span class="sxs-lookup"><span data-stu-id="72dc5-130">The [\#undef](dx-graphics-hlsl-appendix-pre-undef.md) directive instructs the preprocessor to forget the definition of an identifier; for more information, see \#undef Directive (DirectX HLSL).</span></span>

<span data-ttu-id="72dc5-131">La definizione di costanti con l'opzione del compilatore /D ha lo stesso effetto dell'uso della direttiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) all'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="72dc5-131">Defining constants with the /D compiler option has the same effect as using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive at the beginning of your file.</span></span> <span data-ttu-id="72dc5-132">È possibile definire fino a 30 macro con l'opzione /D.</span><span class="sxs-lookup"><span data-stu-id="72dc5-132">Up to 30 macros can be defined with the /D option.</span></span>

<span data-ttu-id="72dc5-133">Gli argomenti effettivi nella chiamata di macro corrispondono agli argomenti formali corrispondenti nella definizione della macro.</span><span class="sxs-lookup"><span data-stu-id="72dc5-133">The actual arguments in the macro call are matched to the corresponding formal arguments in the macro definition.</span></span> <span data-ttu-id="72dc5-134">Ogni argomento formale nella stringa del token viene sostituito dall'argomento effettivo corrispondente, a meno che l'argomento non sia preceduto da un \# operatore stringizing ( ), charizing ( @) o token-pasting ( ) o seguito da \# \# \# un \# \# operatore .</span><span class="sxs-lookup"><span data-stu-id="72dc5-134">Each formal argument in the token string is replaced by the corresponding actual argument, unless the argument is preceded by a stringizing (\#), charizing (\#@), or token-pasting (\#\#) operator, or is followed by a \#\# operator.</span></span> <span data-ttu-id="72dc5-135">Eventuali macro presenti nell'argomento effettivo vengono espanse prima che la direttiva sostituisca il parametro formale.</span><span class="sxs-lookup"><span data-stu-id="72dc5-135">Any macros in the actual argument are expanded before the directive replaces the formal parameter.</span></span>

<span data-ttu-id="72dc5-136">L'incollamento di token nel compilatore HLSL è leggermente diverso dall'incollamento di token nel compilatore C, in cui i token incollati devono essere token validi per conto proprio.</span><span class="sxs-lookup"><span data-stu-id="72dc5-136">Token pasting in the HLSL compiler is slightly different from token pasting in the C compiler, in that the pasted tokens must be valid tokens on their own.</span></span> <span data-ttu-id="72dc5-137">Si consideri ad esempio la definizione di macro seguente:</span><span class="sxs-lookup"><span data-stu-id="72dc5-137">For example, consider the following macro definition:</span></span>


```
#define MERGE(a, b) a##b
MERGE(float, 4x4) test;
```



<span data-ttu-id="72dc5-138">Nel compilatore C il risultato è il seguente:</span><span class="sxs-lookup"><span data-stu-id="72dc5-138">In the C compiler, this results in the following:</span></span>


```
float4x4 test
```



<span data-ttu-id="72dc5-139">Nel compilatore HLSL, tuttavia, il risultato è il seguente:</span><span class="sxs-lookup"><span data-stu-id="72dc5-139">In the HLSL compiler however, this results in the following:</span></span>


```
float4 x4 test
```



<span data-ttu-id="72dc5-140">È possibile aggirare questo comportamento usando invece la definizione della macro seguente.</span><span class="sxs-lookup"><span data-stu-id="72dc5-140">You can work around this behavior by using the following macro definition instead.</span></span>


```
MERGE(MERGE(float, 4), x4) test;
```



## <a name="examples"></a><span data-ttu-id="72dc5-141">Esempio</span><span class="sxs-lookup"><span data-stu-id="72dc5-141">Examples</span></span>

<span data-ttu-id="72dc5-142">Nell'esempio seguente viene utilizzata una macro per definire le righe del cursore.</span><span class="sxs-lookup"><span data-stu-id="72dc5-142">The following example uses a macro to define cursor lines.</span></span>


```
#define CURSOR(top, bottom) (((top) << 8) | (bottom))
```



<span data-ttu-id="72dc5-143">Nell'esempio seguente viene definita una macro che recupera un intero pseudocasuale nell'intervallo specificato.</span><span class="sxs-lookup"><span data-stu-id="72dc5-143">The following example defines a macro that retrieves a pseudorandom integer in the specified range.</span></span>


```
#define getrandom(min, max) \
((rand()%(int)(((max) + 1)-(min)))+ (min))
```



## <a name="related-topics"></a><span data-ttu-id="72dc5-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="72dc5-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72dc5-145">Direttive per il preprocessore (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="72dc5-145">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="72dc5-146">\#definire gli overload</span><span class="sxs-lookup"><span data-stu-id="72dc5-146">\#define Overloads</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[<span data-ttu-id="72dc5-147">\#Direttiva undef (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="72dc5-147">\#undef Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





