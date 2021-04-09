---
description: Un'annotazione è una parte di informazioni definita dall'utente, dichiarata con la sintassi seguente.
ms.assetid: 9178e61e-05a4-441c-a9f1-e05e23ab48a5
title: Sintassi delle annotazioni (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303065e9c49c380a5accba6faadbc641ec0f528a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878410"
---
# <a name="annotation-syntax-direct3d-10"></a><span data-ttu-id="c9cb5-103">Sintassi delle annotazioni (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="c9cb5-103">Annotation Syntax (Direct3D 10)</span></span>

<span data-ttu-id="c9cb5-104">Un'annotazione è una parte di informazioni definita dall'utente, dichiarata con la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="c9cb5-104">An annotation is a user-defined piece of information, declared with the following syntax.</span></span>



| <span data-ttu-id="c9cb5-105"><   =  *Valore* nome DataType;...; ></span><span class="sxs-lookup"><span data-stu-id="c9cb5-105"><*DataType* *Name* = *Value*; ... ;></span></span> |
|--------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="c9cb5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9cb5-106">Parameters</span></span>



| <span data-ttu-id="c9cb5-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="c9cb5-107">Item</span></span>                                                                                                   | <span data-ttu-id="c9cb5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9cb5-108">Description</span></span>                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9cb5-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Tipo*</span><span class="sxs-lookup"><span data-stu-id="c9cb5-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*DataType*</span></span><br/> | <span data-ttu-id="c9cb5-110">\[nel \] tipo di dati, che include qualsiasi tipo di [HLSL scalare](../direct3dhlsl/dx-graphics-hlsl-scalar.md) , nonché il [tipo di stringa](../direct3dhlsl/dx-graphics-hlsl-scalar.md).</span><span class="sxs-lookup"><span data-stu-id="c9cb5-110">\[in\] The data type, which includes any [scalar HLSL](../direct3dhlsl/dx-graphics-hlsl-scalar.md) type as well as the [string type](../direct3dhlsl/dx-graphics-hlsl-scalar.md).</span></span><br/> |
| <span data-ttu-id="c9cb5-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nome*</span><span class="sxs-lookup"><span data-stu-id="c9cb5-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span><br/>                 | <span data-ttu-id="c9cb5-112">\[in \] una stringa ASCII che rappresenta il nome dell'annotazione.</span><span class="sxs-lookup"><span data-stu-id="c9cb5-112">\[in\] An ASCII string, that represents the annotation name.</span></span><br/>                                                                                                          |
| <span data-ttu-id="c9cb5-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Valore*</span><span class="sxs-lookup"><span data-stu-id="c9cb5-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Value*</span></span><br/>             | <span data-ttu-id="c9cb5-114">\[\]valore iniziale dell'annotazione.</span><span class="sxs-lookup"><span data-stu-id="c9cb5-114">\[in\] The initial value of the annotation.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="c9cb5-115"><span id="..."></span>*...*</span><span class="sxs-lookup"><span data-stu-id="c9cb5-115"><span id="..."></span>*...*</span></span><br/>                                                                 | <span data-ttu-id="c9cb5-116">\[in \] altre annotazioni (coppie nome-valore).</span><span class="sxs-lookup"><span data-stu-id="c9cb5-116">\[in\] Additional annotations (name-value pairs).</span></span><br/>                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="c9cb5-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="c9cb5-117">Remarks</span></span>

<span data-ttu-id="c9cb5-118">È possibile aggiungere più di un'annotazione tra parentesi acute, ognuna delle quali è separata da un punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="c9cb5-118">You may add more than one annotation within the angle brackets, each one separated by a semicolon.</span></span> <span data-ttu-id="c9cb5-119">Le API del Framework degli effetti riconoscono le annotazioni sulle variabili globali. tutte le altre annotazioni vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="c9cb5-119">The effect framework APIs recognize annotations on global variables; all other annotations are ignored.</span></span>

## <a name="example"></a><span data-ttu-id="c9cb5-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="c9cb5-120">Example</span></span>

<span data-ttu-id="c9cb5-121">Di seguito sono riportati alcuni esempi.</span><span class="sxs-lookup"><span data-stu-id="c9cb5-121">Here are some examples.</span></span>


```
       
int i <int blabla=27; string blacksheep="Hello There";>;

int j <int bambam=30; string blacksheep="Goodbye There";> = 5 ;

float y <float y=2.3;> = 2.3, z <float y=1.3;> = 1.3 ;

half w <half GlobalW = 3.62;>;

float4 main(float4 pos : SV_POSITION ) : SV_POSITION
{
    pos.y = pos.x > 0 ? pos.w * 1.3 : pos.z * .032;
    for (int x = i; x < j ; x++) 
    {
        pos.w = pos.w * pos.y + x + j - y * w;
    } 

return pos;
}
```



## <a name="related-topics"></a><span data-ttu-id="c9cb5-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c9cb5-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9cb5-123">Sintassi della variabile Effect</span><span class="sxs-lookup"><span data-stu-id="c9cb5-123">Effect Variable Syntax</span></span>](d3d10-effect-variable-syntax.md)
</dt> </dl>

 

 
