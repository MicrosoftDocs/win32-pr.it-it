---
title: " undef (direttiva)"
description: Direttiva per il preprocessore che rimuove la definizione corrente di una costante o di una macro definita in precedenza mediante la direttiva \ define.
ms.assetid: ba6bbe6b-ecfa-40cb-887f-e42b6e22c7bd
keywords:
- Direttiva undef HLSL
topic_type:
- apiref
api_name:
- undef Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7358dc60d002e784394f64773934a18f7413e493
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334031"
---
# <a name="undef-directive"></a><span data-ttu-id="15b9e-104">\#undef (direttiva)</span><span class="sxs-lookup"><span data-stu-id="15b9e-104">\#undef Directive</span></span>

<span data-ttu-id="15b9e-105">Direttiva per il preprocessore che rimuove la definizione corrente di una costante o di una macro definita in precedenza mediante la direttiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) .</span><span class="sxs-lookup"><span data-stu-id="15b9e-105">Preprocessor directive that removes the current definition of a constant or macro that was previously defined using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive.</span></span>



| <span data-ttu-id="15b9e-106">\#*identificatore* undef</span><span class="sxs-lookup"><span data-stu-id="15b9e-106">\#undef *identifier*</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="15b9e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="15b9e-107">Parameters</span></span>



| <span data-ttu-id="15b9e-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="15b9e-108">Item</span></span>                                                                              | <span data-ttu-id="15b9e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15b9e-109">Description</span></span>                                                                                                                                                      |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15b9e-110"><span id="identifier"></span><span id="IDENTIFIER"></span>*identificatore*</span><span class="sxs-lookup"><span data-stu-id="15b9e-110"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/> | <span data-ttu-id="15b9e-111">Identificatore della costante o della macro per cui rimuovere la definizione.</span><span class="sxs-lookup"><span data-stu-id="15b9e-111">Identifier of the constant or macro to remove the definition of.</span></span> <span data-ttu-id="15b9e-112">Se si sta annientendo la definizione di una macro, fornire solo l'identificatore, non l'elenco di parametri.</span><span class="sxs-lookup"><span data-stu-id="15b9e-112">If you are undefining a macro, provide only the identifier, not the parameter list.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="15b9e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="15b9e-113">Remarks</span></span>

<span data-ttu-id="15b9e-114">È possibile applicare la \# direttiva undef a un identificatore privo di definizione precedente, in modo da garantire che l'identificatore non sia definito.</span><span class="sxs-lookup"><span data-stu-id="15b9e-114">You can apply the \#undef directive to an identifier that has no previous definition; this ensures that the identifier is undefined.</span></span> <span data-ttu-id="15b9e-115">La sostituzione della macro non viene eseguita nelle \# istruzioni undef.</span><span class="sxs-lookup"><span data-stu-id="15b9e-115">Macro replacement is not performed within \#undef statements.</span></span>

<span data-ttu-id="15b9e-116">La \# direttiva undef viene in genere abbinata a una direttiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) per creare un'area in un programma di origine in cui un identificatore ha un significato speciale.</span><span class="sxs-lookup"><span data-stu-id="15b9e-116">The \#undef directive is typically paired with a [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive to create a region in a source program in which an identifier has a special meaning.</span></span> <span data-ttu-id="15b9e-117">Ad esempio, una funzione specifica del programma di origine può utilizzare le costanti manifesto per definire valori specifici dell'ambiente che non influiscono sul resto del programma.</span><span class="sxs-lookup"><span data-stu-id="15b9e-117">For example, a specific function of the source program can use manifest constants to define environment-specific values that do not affect the rest of the program.</span></span> <span data-ttu-id="15b9e-118">La \# direttiva undef funziona anche con la direttiva [) per controllare la compilazione condizionale del programma di origine.</span><span class="sxs-lookup"><span data-stu-id="15b9e-118">The \#undef directive also works with the [) directive to control conditional compilation of the source program.</span></span>

<span data-ttu-id="15b9e-119">Le costanti e le macro possono essere indefinite dalla riga di comando usando l'opzione/U, seguite dagli identificatori come indefiniti.</span><span class="sxs-lookup"><span data-stu-id="15b9e-119">Constants and macros can be undefined from the command line using the /U option, followed by the identifiers to be undefined.</span></span> <span data-ttu-id="15b9e-120">Questa operazione equivale all'aggiunta di una sequenza di \# direttive undef all'inizio del file di origine.</span><span class="sxs-lookup"><span data-stu-id="15b9e-120">This is equivalent to adding a sequence of \#undef directives at the beginning of the source file.</span></span>

## <a name="examples"></a><span data-ttu-id="15b9e-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="15b9e-121">Examples</span></span>

<span data-ttu-id="15b9e-122">Nell'esempio seguente viene illustrato come utilizzare la \# direttiva undef per rimuovere le definizioni di una costante simbolica e di una macro.</span><span class="sxs-lookup"><span data-stu-id="15b9e-122">The following example shows how to use the \#undef directive to remove definitions of a symbolic constant and a macro.</span></span>


```
#define WIDTH           80
#define ADD( X, Y )     (X) + (Y)

#undef WIDTH
#undef ADD
```



## <a name="see-also"></a><span data-ttu-id="15b9e-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15b9e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15b9e-124">Direttive per il preprocessore (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="15b9e-124">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="15b9e-125">\#define (direttiva) (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="15b9e-125">\#define Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[<span data-ttu-id="15b9e-126">\#Se,)</span><span class="sxs-lookup"><span data-stu-id="15b9e-126">\#if, )</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





