---
title: Sintassi delle annotazioni (Direct3D 11)
description: Un'annotazione è una parte di informazioni definita dall'utente, dichiarata con la sintassi descritta in questa sezione.
ms.assetid: a81198d2-c4d7-47b5-b3b8-2de11a9ee9a3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9583dafd3e1fb314ae6ac9e53d609bebc74a030
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963111"
---
# <a name="annotation-syntax-direct3d-11"></a><span data-ttu-id="6c8a6-103">Sintassi delle annotazioni (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="6c8a6-103">Annotation Syntax (Direct3D 11)</span></span>

<span data-ttu-id="6c8a6-104">Un'annotazione è una parte di informazioni definita dall'utente, dichiarata con la sintassi descritta in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-104">An annotation is a user-defined piece of information, declared with the syntax described in this section.</span></span>



| <span data-ttu-id="6c8a6-105"><   =  *Valore* nome DataType; *...* ; ></span><span class="sxs-lookup"><span data-stu-id="6c8a6-105"><*DataType* *Name* = *Value*; *...* ;></span></span> |
|----------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="6c8a6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c8a6-106">Parameters</span></span>



| <span data-ttu-id="6c8a6-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="6c8a6-107">Item</span></span>                                                                                                   | <span data-ttu-id="6c8a6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c8a6-108">Description</span></span>                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c8a6-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Tipo*</span><span class="sxs-lookup"><span data-stu-id="6c8a6-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*DataType*</span></span><br/> | <span data-ttu-id="6c8a6-110">\[nel \] tipo di dati, che include qualsiasi tipo di [HLSL scalare](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) , nonché il [tipo di stringa](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar).</span><span class="sxs-lookup"><span data-stu-id="6c8a6-110">\[in\] The data type, which includes any [scalar HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) type as well as the [string type](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar).</span></span><br/> |
| <span data-ttu-id="6c8a6-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nome*</span><span class="sxs-lookup"><span data-stu-id="6c8a6-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span><br/>                 | <span data-ttu-id="6c8a6-112">\[in \] una stringa ASCII che rappresenta il nome dell'annotazione.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-112">\[in\] An ASCII string, that represents the annotation name.</span></span><br/>                                                                                                          |
| <span data-ttu-id="6c8a6-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Valore*</span><span class="sxs-lookup"><span data-stu-id="6c8a6-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Value*</span></span><br/>             | <span data-ttu-id="6c8a6-114">\[\]valore iniziale dell'annotazione.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-114">\[in\] The initial value of the annotation.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="6c8a6-115"><span id="..."></span>*...*</span><span class="sxs-lookup"><span data-stu-id="6c8a6-115"><span id="..."></span>*...*</span></span><br/>                                                                 | <span data-ttu-id="6c8a6-116">\[in \] altre annotazioni (coppie nome-valore).</span><span class="sxs-lookup"><span data-stu-id="6c8a6-116">\[in\] Additional annotations (name-value pairs).</span></span><br/>                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="6c8a6-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c8a6-117">Remarks</span></span>

<span data-ttu-id="6c8a6-118">È possibile aggiungere più di un'annotazione tra parentesi acute, ognuna delle quali è separata da un punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-118">You may add more than one annotation within the angle brackets, each one separated by a semicolon.</span></span> <span data-ttu-id="6c8a6-119">Le API del Framework degli effetti riconoscono le annotazioni sulle variabili globali. tutte le altre annotazioni vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-119">The effect framework APIs recognize annotations on global variables; all other annotations are ignored.</span></span>

## <a name="example"></a><span data-ttu-id="6c8a6-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="6c8a6-120">Example</span></span>

<span data-ttu-id="6c8a6-121">Di seguito sono riportati alcuni esempi.</span><span class="sxs-lookup"><span data-stu-id="6c8a6-121">Here are some examples.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6c8a6-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6c8a6-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c8a6-123">Formato effetto</span><span class="sxs-lookup"><span data-stu-id="6c8a6-123">Effect Format</span></span>](d3d11-effect-format.md)
</dt> <dt>

[<span data-ttu-id="6c8a6-124">Sintassi della variabile Effect</span><span class="sxs-lookup"><span data-stu-id="6c8a6-124">Effect Variable Syntax</span></span>](d3d11-effect-variable-syntax.md)
</dt> </dl>

 

