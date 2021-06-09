---
title: packoffset
description: Parola chiave facoltativa per la creazione di un pacchetto di costanti shader, che usa la sintassi seguente
ms.assetid: f0a3031b-d385-430d-83ee-7a8142334ad7
keywords:
- packoffset HLSL
topic_type:
- apiref
api_name:
- packoffset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5c92a6375f0724a1910fc0f09b47e1593614f9f1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826080"
---
# <a name="packoffset"></a><span data-ttu-id="eecaa-104">packoffset</span><span class="sxs-lookup"><span data-stu-id="eecaa-104">packoffset</span></span>

<span data-ttu-id="eecaa-105">Parola chiave facoltativa per la creazione di un pacchetto di costanti shader, che usa la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="eecaa-105">Optional shader constant packing keyword, which uses the following syntax:</span></span>

<span data-ttu-id="eecaa-106">: packoffset( c \[ Subcomponent \] \[ .component \] )</span><span class="sxs-lookup"><span data-stu-id="eecaa-106">: packoffset( c\[Subcomponent\]\[.component\] )</span></span>



 

## <a name="parameters"></a><span data-ttu-id="eecaa-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="eecaa-107">Parameters</span></span>



| <span data-ttu-id="eecaa-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="eecaa-108">Item</span></span>                                                                                                                                                                                 | <span data-ttu-id="eecaa-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eecaa-109">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eecaa-110"><span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**</span><span class="sxs-lookup"><span data-stu-id="eecaa-110"><span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**</span></span><br/>                                                                                                  | <span data-ttu-id="eecaa-111">Parola chiave obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="eecaa-111">Required keyword.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="eecaa-112"><span id="c"></span><span id="C"></span>**C**</span><span class="sxs-lookup"><span data-stu-id="eecaa-112"><span id="c"></span><span id="C"></span>**c**</span></span><br/>                                                                                                                             | <span data-ttu-id="eecaa-113">La creazione di un pacchetto si applica solo ai registri costanti (c).</span><span class="sxs-lookup"><span data-stu-id="eecaa-113">Packing applies to constant registers (c) only.</span></span> <br/>                                                                                          |
| <span data-ttu-id="eecaa-114"><span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Componente \] \[ secondario .component\]**</span><span class="sxs-lookup"><span data-stu-id="eecaa-114"><span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Subcomponent\]\[.component\]**</span></span><br/> | <span data-ttu-id="eecaa-115">Sottocomponenti e componenti facoltativi.</span><span class="sxs-lookup"><span data-stu-id="eecaa-115">Optional subcomponents and components.</span></span> <span data-ttu-id="eecaa-116">Un sottocomponente è un numero di registro, ovvero un numero intero.</span><span class="sxs-lookup"><span data-stu-id="eecaa-116">A subcomponent is a register number, which is an integer.</span></span> <span data-ttu-id="eecaa-117">Un componente è nel formato \[ .xyzw \] .</span><span class="sxs-lookup"><span data-stu-id="eecaa-117">A component is in the form of \[.xyzw\].</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eecaa-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="eecaa-118">Remarks</span></span>

<span data-ttu-id="eecaa-119">Usare questa parola chiave per creare manualmente un pacchetto di una costante shader [quando si dichiara un tipo di variabile](dx-graphics-hlsl-variable-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="eecaa-119">Use this keyword to manually pack a shader constant when [declaring a variable type](dx-graphics-hlsl-variable-syntax.md).</span></span>

<span data-ttu-id="eecaa-120">Quando si esegue il pacchetto di una costante, non è possibile combinare tipi costanti.</span><span class="sxs-lookup"><span data-stu-id="eecaa-120">When packing a constant, you cannot mix constant types.</span></span>

<span data-ttu-id="eecaa-121">Il compilatore si comporta in modo leggermente diverso per le costanti globali e le costanti uniformi:</span><span class="sxs-lookup"><span data-stu-id="eecaa-121">The compiler behaves slightly differently for global constants and uniform constants:</span></span>

-   <span data-ttu-id="eecaa-122">Costante globale.</span><span class="sxs-lookup"><span data-stu-id="eecaa-122">A global constant.</span></span> <span data-ttu-id="eecaa-123">Una variabile globale viene aggiunta come costante globale *a* un $Global cbuffer dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="eecaa-123">A global variable is added as a global constant to a *$Global* cbuffer by the compiler.</span></span> <span data-ttu-id="eecaa-124">Gli elementi di tipo packed automaticamente (quelli dichiarati senza packoffset) verranno visualizzati dopo l'ultima variabile di tipo packed manualmente.</span><span class="sxs-lookup"><span data-stu-id="eecaa-124">Automatically packed elements (those declared without packoffset) will appear after the last manually packed variable.</span></span> <span data-ttu-id="eecaa-125">È possibile combinare tipi durante la creazione di un pacchetto di costanti globali.</span><span class="sxs-lookup"><span data-stu-id="eecaa-125">You may mix types when packing global constants.</span></span>
-   <span data-ttu-id="eecaa-126">Costante uniforme.</span><span class="sxs-lookup"><span data-stu-id="eecaa-126">A uniform constant.</span></span> <span data-ttu-id="eecaa-127">Un parametro uniforme nell'elenco di parametri di una funzione verrà aggiunto $Param un buffer costante di *$Param* dal compilatore quando lo shader viene compilato all'esterno del framework degli effetti.</span><span class="sxs-lookup"><span data-stu-id="eecaa-127">A uniform parameter in the parameter list of a function will be added to a *$Param* constant buffer by the compiler when the shader is compiled outside of the effects framework.</span></span> <span data-ttu-id="eecaa-128">Quando viene compilata all'interno del framework degli effetti, una costante uniforme deve risolversi in una variabile uniforme definita nell'ambito globale.</span><span class="sxs-lookup"><span data-stu-id="eecaa-128">When compiled inside the effect framework, a uniform constant must resolve to a uniform variable defined in global scope.</span></span> <span data-ttu-id="eecaa-129">Non è possibile eseguire manualmente l'offset di una costante uniforme. L'uso consigliato è solo per la specializzazione degli shader in cui vengono di nuovo alias alle variabili globali, non come mezzo per passare i dati dell'applicazione nello shader.</span><span class="sxs-lookup"><span data-stu-id="eecaa-129">A uniform constant cannot be manually offset; their recommend use is only for specialization of shaders where they alias back to globals, not as a means of passing application data into the shader.</span></span>

<span data-ttu-id="eecaa-130">Ecco alcuni esempi aggiuntivi: [creazione di un pacchetto di costanti usando il modello shader 4.](dx-graphics-hlsl-packing-rules.md)</span><span class="sxs-lookup"><span data-stu-id="eecaa-130">Here are some additional examples: [packing constants using shader model 4](dx-graphics-hlsl-packing-rules.md).</span></span>

## <a name="examples"></a><span data-ttu-id="eecaa-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="eecaa-131">Examples</span></span>

<span data-ttu-id="eecaa-132">Di seguito sono riportati alcuni esempi di creazione manuale di un pacchetto di costanti shader.</span><span class="sxs-lookup"><span data-stu-id="eecaa-132">Here are several examples of manually packing shader constants.</span></span>

<span data-ttu-id="eecaa-133">Creare un pacchetto di sottocomponenti di vettori e scalari la cui dimensione è sufficientemente grande da impedire l'attraversamento dei limiti del registro.</span><span class="sxs-lookup"><span data-stu-id="eecaa-133">Pack subcomponents of vectors and scalars whose size is large enough to prevent crossing register boundaries.</span></span> <span data-ttu-id="eecaa-134">Ad esempio, sono tutti validi:</span><span class="sxs-lookup"><span data-stu-id="eecaa-134">For example, these are all valid:</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
```



## <a name="see-also"></a><span data-ttu-id="eecaa-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eecaa-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eecaa-136">Sintassi delle variabili</span><span class="sxs-lookup"><span data-stu-id="eecaa-136">Variable Syntax</span></span>](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[<span data-ttu-id="eecaa-137">Variabili (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eecaa-137">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 





