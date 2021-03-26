---
title: '\#define (direttiva) (costante)'
description: Direttiva per il preprocessore che assegna un nome significativo a una costante nell'applicazione.
ms.assetid: cc9b34a3-4c83-4999-99ec-e6261ecb2785
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: deae1ca92c2280cd31cbec2bf3482c61fcf2b88a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104046132"
---
# <a name="define-directive-constant"></a><span data-ttu-id="febd4-103">\#define (direttiva) (costante)</span><span class="sxs-lookup"><span data-stu-id="febd4-103">\#define directive (constant)</span></span>

<span data-ttu-id="febd4-104">Direttiva per il preprocessore che assegna un nome significativo a una costante nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="febd4-104">Preprocessor directive that assigns a meaningful name to a constant in your application.</span></span>



| <span data-ttu-id="febd4-105">\#definire *identifiertoken-String*</span><span class="sxs-lookup"><span data-stu-id="febd4-105">\#define *identifiertoken-string*</span></span> |
|-----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="febd4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="febd4-106">Parameters</span></span>



| <span data-ttu-id="febd4-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="febd4-107">Item</span></span>                                                                                                                       | <span data-ttu-id="febd4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="febd4-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="febd4-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*identificatore*</span><span class="sxs-lookup"><span data-stu-id="febd4-109"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/>                                          | <span data-ttu-id="febd4-110">Identificatore della costante.</span><span class="sxs-lookup"><span data-stu-id="febd4-110">Identifier of the constant.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="febd4-111"><span id="token-string__optional_"></span><span id="TOKEN-STRING__OPTIONAL_"></span>*stringa* \[ di token opzionale\]</span><span class="sxs-lookup"><span data-stu-id="febd4-111"><span id="token-string__optional_"></span><span id="TOKEN-STRING__OPTIONAL_"></span>*token-string* \[optional\]</span></span><br/> | <span data-ttu-id="febd4-112">Valore della costante.</span><span class="sxs-lookup"><span data-stu-id="febd4-112">Value of the constant.</span></span> <span data-ttu-id="febd4-113">Questo parametro è costituito da una serie di token, ad esempio parole chiave, costanti o istruzioni complete.</span><span class="sxs-lookup"><span data-stu-id="febd4-113">This parameter consists of a series of tokens, such as keywords, constants, or complete statements.</span></span> <span data-ttu-id="febd4-114">Uno o più caratteri di spazio vuoto devono separare questo parametro dal parametro *Identifier* . Questo spazio vuoto non è considerato parte del testo sostituito, né lo spazio vuoto dopo l'ultimo token del testo.</span><span class="sxs-lookup"><span data-stu-id="febd4-114">One or more white-space characters must separate this parameter from the *identifier* parameter; this white space is not considered part of the substituted text, nor is any white space following the last token of the text.</span></span> <br/> <span data-ttu-id="febd4-115">Se si esclude questo parametro, tutte le istanze del parametro *Identifier* verranno rimosse dal file di origine.</span><span class="sxs-lookup"><span data-stu-id="febd4-115">If you exclude this parameter, all instances of the *identifier* parameter are removed from the source file.</span></span> <span data-ttu-id="febd4-116">L'identificatore rimane definito e può essere testato utilizzando le direttive [ \# if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \# ifdef e \# ifndef.</span><span class="sxs-lookup"><span data-stu-id="febd4-116">The identifier remains defined, and can be tested using the [\#if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \#ifdef, and \#ifndef directives.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="febd4-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="febd4-117">Remarks</span></span>

<span data-ttu-id="febd4-118">Tutte le istanze del parametro *Identifier* che si verificano dopo la direttiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) nel file di origine verranno sostituite dal valore del parametro della *stringa di token* .</span><span class="sxs-lookup"><span data-stu-id="febd4-118">All instances of the *identifier* parameter that occur after the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive in the source file will be replaced by the value of the *token-string* parameter.</span></span> <span data-ttu-id="febd4-119">L'identificatore viene sostituito solo quando costituisce un token. l'identificatore, ad esempio, non viene sostituito se viene visualizzato in un commento, all'interno di una stringa o come parte di un identificatore più lungo.</span><span class="sxs-lookup"><span data-stu-id="febd4-119">The identifier is replaced only when it forms a token; for example, the identifier is not replaced if it appears in a comment, within a string, or as part of a longer identifier.</span></span>

<span data-ttu-id="febd4-120">La direttiva [ \# undef](dx-graphics-hlsl-appendix-pre-undef.md) indica al preprocessore di dimenticare la definizione di un identificatore. per ulteriori informazioni, vedere la \# direttiva undef (DirectX HLSL).</span><span class="sxs-lookup"><span data-stu-id="febd4-120">The [\#undef](dx-graphics-hlsl-appendix-pre-undef.md) directive instructs the preprocessor to forget the definition of an identifier; for more information, see \#undef Directive (DirectX HLSL).</span></span>

<span data-ttu-id="febd4-121">La definizione di costanti con l'opzione del compilatore/D ha lo stesso effetto dell'uso della direttiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) all'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="febd4-121">Defining constants with the /D compiler option has the same effect as using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive at the beginning of your file.</span></span> <span data-ttu-id="febd4-122">Con l'opzione/D è possibile definire fino a 30 costanti.</span><span class="sxs-lookup"><span data-stu-id="febd4-122">Up to 30 constants can be defined with the /D option.</span></span> <span data-ttu-id="febd4-123">Per un esempio di come è possibile usarlo, vedere la sezione Esempi di [ \# ifdef e](dx-graphics-hlsl-appendix-pre-ifdef.md).</span><span class="sxs-lookup"><span data-stu-id="febd4-123">For an example of how this can be used, see the Examples section of [\#ifdef and )](dx-graphics-hlsl-appendix-pre-ifdef.md).</span></span>

## <a name="examples"></a><span data-ttu-id="febd4-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="febd4-124">Examples</span></span>

<span data-ttu-id="febd4-125">Nell'esempio seguente viene definita la larghezza dell'identificatore come costante Integer 80, quindi viene definita la lunghezza in termini di larghezza e la costante Integer 10.</span><span class="sxs-lookup"><span data-stu-id="febd4-125">The following example defines the identifier WIDTH as the integer constant 80 and then defines LENGTH in terms of WIDTH and the integer constant 10.</span></span>


```
#define WIDTH       80
#define LENGTH      ( WIDTH + 10 )
```



<span data-ttu-id="febd4-126">Ogni istanza successiva di LENGTH viene sostituita da (WIDTH + 10) e ogni istanza successiva di WIDTH + 10 viene sostituita dall'espressione (80 + 10).</span><span class="sxs-lookup"><span data-stu-id="febd4-126">Every subsequent instance of LENGTH is replaced by (WIDTH + 10), and every subsequent instance of WIDTH + 10 is replaced by the expression (80 + 10).</span></span> <span data-ttu-id="febd4-127">Le parentesi attorno alla larghezza + 10 sono importanti perché controllano l'interpretazione nelle istruzioni come le seguenti.</span><span class="sxs-lookup"><span data-stu-id="febd4-127">The parentheses around WIDTH + 10 are important because they control the interpretation in statements such as the following.</span></span>


```
var = LENGTH * 20;
```



<span data-ttu-id="febd4-128">Dopo la fase di pre-elaborazione l'istruzione diventa la seguente, che restituisce 1.800.</span><span class="sxs-lookup"><span data-stu-id="febd4-128">After the preprocessing stage the statement becomes the following, which evaluates to 1,800.</span></span>


```
var = ( 80 + 10 ) * 20;
```



<span data-ttu-id="febd4-129">Senza parentesi, il risultato sarà il seguente, che restituisce 280.</span><span class="sxs-lookup"><span data-stu-id="febd4-129">Without parentheses, the result would be the following, which evaluates to 280.</span></span>


```
var = 80 + 10 * 20;
```



## <a name="related-topics"></a><span data-ttu-id="febd4-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="febd4-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="febd4-131">Direttive per il preprocessore (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="febd4-131">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="febd4-132">\#definire gli overload</span><span class="sxs-lookup"><span data-stu-id="febd4-132">\#define Overloads</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[<span data-ttu-id="febd4-133">\#Direttiva undef (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="febd4-133">\#undef Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





