---
title: packoffset
description: Parola chiave facoltativa di compressione costante dello shader, che usa la sintassi seguente
ms.assetid: f0a3031b-d385-430d-83ee-7a8142334ad7
keywords:
- HLSL packoffset
topic_type:
- apiref
api_name:
- packoffset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6feeaa586abe30fa8a36c28d0298dc408cdfb099
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333908"
---
# <a name="packoffset"></a><span data-ttu-id="1cce4-104">packoffset</span><span class="sxs-lookup"><span data-stu-id="1cce4-104">packoffset</span></span>

<span data-ttu-id="1cce4-105">Parola chiave facoltativa di compressione costante dello shader, che usa la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="1cce4-105">Optional shader constant packing keyword, which uses the following syntax:</span></span>



|                                                 |
|-------------------------------------------------|
| <span data-ttu-id="1cce4-106">: packoffset (c \[ SubComponent \] \[ . Component \] )</span><span class="sxs-lookup"><span data-stu-id="1cce4-106">: packoffset( c\[Subcomponent\]\[.component\] )</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="1cce4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1cce4-107">Parameters</span></span>



| <span data-ttu-id="1cce4-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="1cce4-108">Item</span></span>                                                                                                                                                                                 | <span data-ttu-id="1cce4-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1cce4-109">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cce4-110"><span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**</span><span class="sxs-lookup"><span data-stu-id="1cce4-110"><span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**</span></span><br/>                                                                                                  | <span data-ttu-id="1cce4-111">Parola chiave required.</span><span class="sxs-lookup"><span data-stu-id="1cce4-111">Required keyword.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="1cce4-112"><span id="c"></span><span id="C"></span>**c**</span><span class="sxs-lookup"><span data-stu-id="1cce4-112"><span id="c"></span><span id="C"></span>**c**</span></span><br/>                                                                                                                             | <span data-ttu-id="1cce4-113">La compressione si applica solo ai registri costanti (c).</span><span class="sxs-lookup"><span data-stu-id="1cce4-113">Packing applies to constant registers (c) only.</span></span> <br/>                                                                                          |
| <span data-ttu-id="1cce4-114"><span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Sottocomponente \] \[ . componente\]**</span><span class="sxs-lookup"><span data-stu-id="1cce4-114"><span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Subcomponent\]\[.component\]**</span></span><br/> | <span data-ttu-id="1cce4-115">Componenti e sottocomponenti facoltativi.</span><span class="sxs-lookup"><span data-stu-id="1cce4-115">Optional subcomponents and components.</span></span> <span data-ttu-id="1cce4-116">Un sottocomponente è un numero di registro, ovvero un numero intero.</span><span class="sxs-lookup"><span data-stu-id="1cce4-116">A subcomponent is a register number, which is an integer.</span></span> <span data-ttu-id="1cce4-117">Il formato di un componente è \[ . xyzw \] .</span><span class="sxs-lookup"><span data-stu-id="1cce4-117">A component is in the form of \[.xyzw\].</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1cce4-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="1cce4-118">Remarks</span></span>

<span data-ttu-id="1cce4-119">Usare questa parola chiave per comprimere manualmente una costante dello shader quando si [dichiara un tipo di variabile](dx-graphics-hlsl-variable-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="1cce4-119">Use this keyword to manually pack a shader constant when [declaring a variable type](dx-graphics-hlsl-variable-syntax.md).</span></span>

<span data-ttu-id="1cce4-120">Quando si imballa una costante, non è possibile combinare tipi costanti.</span><span class="sxs-lookup"><span data-stu-id="1cce4-120">When packing a constant, you cannot mix constant types.</span></span>

<span data-ttu-id="1cce4-121">Il compilatore si comporta in modo leggermente diverso per le costanti globali e le costanti uniformi:</span><span class="sxs-lookup"><span data-stu-id="1cce4-121">The compiler behaves slightly differently for global constants and uniform constants:</span></span>

-   <span data-ttu-id="1cce4-122">Costante globale.</span><span class="sxs-lookup"><span data-stu-id="1cce4-122">A global constant.</span></span> <span data-ttu-id="1cce4-123">Una variabile globale viene aggiunta come costante globale a un *$Global* cbuffer dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="1cce4-123">A global variable is added as a global constant to a *$Global* cbuffer by the compiler.</span></span> <span data-ttu-id="1cce4-124">Gli elementi compressi automaticamente (quelli dichiarati senza packoffset) verranno visualizzati dopo l'ultima variabile compressa manualmente.</span><span class="sxs-lookup"><span data-stu-id="1cce4-124">Automatically packed elements (those declared without packoffset) will appear after the last manually packed variable.</span></span> <span data-ttu-id="1cce4-125">È possibile combinare i tipi durante la compressione delle costanti globali.</span><span class="sxs-lookup"><span data-stu-id="1cce4-125">You may mix types when packing global constants.</span></span>
-   <span data-ttu-id="1cce4-126">Costante uniforme.</span><span class="sxs-lookup"><span data-stu-id="1cce4-126">A uniform constant.</span></span> <span data-ttu-id="1cce4-127">Un parametro uniforme nell'elenco di parametri di una funzione verrà aggiunto a un buffer costante *$param* dal compilatore quando lo shader viene compilato all'esterno del Framework degli effetti.</span><span class="sxs-lookup"><span data-stu-id="1cce4-127">A uniform parameter in the parameter list of a function will be added to a *$Param* constant buffer by the compiler when the shader is compiled outside of the effects framework.</span></span> <span data-ttu-id="1cce4-128">Quando viene compilato all'interno del Framework degli effetti, una costante uniforme deve essere risolta in una variabile uniforme definita nell'ambito globale.</span><span class="sxs-lookup"><span data-stu-id="1cce4-128">When compiled inside the effect framework, a uniform constant must resolve to a uniform variable defined in global scope.</span></span> <span data-ttu-id="1cce4-129">Una costante uniforme non può essere offset manualmente; l'utilizzo consigliato è solo per la specializzazione di shader in cui viene eseguito l'aliasing a Globals, non come mezzo per passare i dati dell'applicazione allo shader.</span><span class="sxs-lookup"><span data-stu-id="1cce4-129">A uniform constant cannot be manually offset; their recommend use is only for specialization of shaders where they alias back to globals, not as a means of passing application data into the shader.</span></span>

<span data-ttu-id="1cce4-130">Di seguito sono riportati alcuni esempi aggiuntivi: le [costanti di compressione con il modello di Shader 4](dx-graphics-hlsl-packing-rules.md).</span><span class="sxs-lookup"><span data-stu-id="1cce4-130">Here are some additional examples: [packing constants using shader model 4](dx-graphics-hlsl-packing-rules.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1cce4-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="1cce4-131">Examples</span></span>

<span data-ttu-id="1cce4-132">Di seguito sono riportati alcuni esempi di compressione manuale delle costanti shader.</span><span class="sxs-lookup"><span data-stu-id="1cce4-132">Here are several examples of manually packing shader constants.</span></span>

<span data-ttu-id="1cce4-133">Comprimere i sottocomponenti di vettori e scalari le cui dimensioni sono sufficientemente grandi da impedire l'attraversamento dei limiti del registro.</span><span class="sxs-lookup"><span data-stu-id="1cce4-133">Pack subcomponents of vectors and scalars whose size is large enough to prevent crossing register boundaries.</span></span> <span data-ttu-id="1cce4-134">Ad esempio, sono tutti validi:</span><span class="sxs-lookup"><span data-stu-id="1cce4-134">For example, these are all valid:</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
```



## <a name="see-also"></a><span data-ttu-id="1cce4-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1cce4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cce4-136">Sintassi delle variabili</span><span class="sxs-lookup"><span data-stu-id="1cce4-136">Variable Syntax</span></span>](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[<span data-ttu-id="1cce4-137">Variabili (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1cce4-137">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 





