---
title: Interfaccia ID3DX11EffectTechnique (D3dx11effect. h)
description: Un'interfaccia ID3DX11EffectTechnique è una raccolta di passaggi. La durata di un oggetto ID3DX11EffectTechnique è uguale alla durata del relativo oggetto ID3DX11Effect padre.
ms.assetid: 63d52cac-287d-4432-bf2b-7b4e67e525e6
keywords:
- Interfaccia ID3DX11EffectTechnique Direct3D 11
- Interfaccia ID3DX11EffectTechnique Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e582d8f94b2dbcbb2052a8cf3a59d8ba514367cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982539"
---
# <a name="id3dx11effecttechnique-interface"></a><span data-ttu-id="ba234-105">Interfaccia ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="ba234-105">ID3DX11EffectTechnique interface</span></span>

<span data-ttu-id="ba234-106">Un'interfaccia **ID3DX11EffectTechnique** è una raccolta di passaggi.</span><span class="sxs-lookup"><span data-stu-id="ba234-106">An **ID3DX11EffectTechnique** interface is a collection of passes.</span></span>

<span data-ttu-id="ba234-107">La durata di un oggetto **ID3DX11EffectTechnique** è uguale alla durata del relativo oggetto [**ID3DX11Effect**](id3dx11effect.md) padre.</span><span class="sxs-lookup"><span data-stu-id="ba234-107">The lifetime of an **ID3DX11EffectTechnique** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="ba234-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="ba234-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ba234-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="ba234-109">Methods</span></span>

<span data-ttu-id="ba234-110">L'interfaccia **ID3DX11EffectTechnique** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ba234-110">The **ID3DX11EffectTechnique** interface has these methods.</span></span>



| <span data-ttu-id="ba234-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="ba234-111">Method</span></span>                                                                        | <span data-ttu-id="ba234-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba234-112">Description</span></span>                                                           |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="ba234-113">**ComputeStateBlockMask**</span><span class="sxs-lookup"><span data-stu-id="ba234-113">**ComputeStateBlockMask**</span></span>](id3dx11effecttechnique-computestateblockmask.md) | <span data-ttu-id="ba234-114">Consente di calcolare una maschera a blocchi di stato per consentire o impedire modifiche di stato.</span><span class="sxs-lookup"><span data-stu-id="ba234-114">Compute a state-block mask to allow/prevent state changes.</span></span><br/> |
| [<span data-ttu-id="ba234-115">**GetAnnotationByIndex**</span><span class="sxs-lookup"><span data-stu-id="ba234-115">**GetAnnotationByIndex**</span></span>](id3dx11effecttechnique-getannotationbyindex.md)   | <span data-ttu-id="ba234-116">Ottenere un'annotazione in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="ba234-116">Get an annotation by index.</span></span><br/>                                |
| [<span data-ttu-id="ba234-117">**GetAnnotationByName**</span><span class="sxs-lookup"><span data-stu-id="ba234-117">**GetAnnotationByName**</span></span>](id3dx11effecttechnique-getannotationbyname.md)     | <span data-ttu-id="ba234-118">Ottenere un'annotazione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="ba234-118">Get an annotation by name.</span></span><br/>                                 |
| [<span data-ttu-id="ba234-119">**Getdesc**</span><span class="sxs-lookup"><span data-stu-id="ba234-119">**GetDesc**</span></span>](id3dx11effecttechnique-getdesc.md)                             | <span data-ttu-id="ba234-120">Ottenere una descrizione tecnica.</span><span class="sxs-lookup"><span data-stu-id="ba234-120">Get a technique description.</span></span><br/>                               |
| [<span data-ttu-id="ba234-121">**GetPassByIndex**</span><span class="sxs-lookup"><span data-stu-id="ba234-121">**GetPassByIndex**</span></span>](id3dx11effecttechnique-getpassbyindex.md)               | <span data-ttu-id="ba234-122">Ottenere un indice pass-by.</span><span class="sxs-lookup"><span data-stu-id="ba234-122">Get a pass by index.</span></span><br/>                                       |
| [<span data-ttu-id="ba234-123">**GetPassByName**</span><span class="sxs-lookup"><span data-stu-id="ba234-123">**GetPassByName**</span></span>](id3dx11effecttechnique-getpassbyname.md)                 | <span data-ttu-id="ba234-124">Ottenere un passaggio per nome.</span><span class="sxs-lookup"><span data-stu-id="ba234-124">Get a pass by name.</span></span><br/>                                        |
| [<span data-ttu-id="ba234-125">**isValid**</span><span class="sxs-lookup"><span data-stu-id="ba234-125">**IsValid**</span></span>](id3dx11effecttechnique-isvalid.md)                             | <span data-ttu-id="ba234-126">Testare una tecnica per verificare se contiene una sintassi valida.</span><span class="sxs-lookup"><span data-stu-id="ba234-126">Test a technique to see if it contains valid syntax.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="ba234-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba234-127">Remarks</span></span>

<span data-ttu-id="ba234-128">Un effetto contiene una o più tecniche. ogni tecnica contiene uno o più passaggi. ogni sessione contiene le assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="ba234-128">An effect contains one or more techniques; each technique contains one or more passes; each pass contains state assignments.</span></span>

<span data-ttu-id="ba234-129">Per ottenere un'interfaccia effetto-tecnica, chiamare un metodo come [**ID3DX11Effect:: GetTechniqueByName**](id3dx11effect-gettechniquebyname.md).</span><span class="sxs-lookup"><span data-stu-id="ba234-129">To get an effect-technique interface, call a method such as [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md).</span></span>

> [!Note]  
> <span data-ttu-id="ba234-130">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="ba234-130">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ba234-131">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="ba234-131">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ba234-132">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ba234-132">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ba234-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba234-133">Requirements</span></span>



| <span data-ttu-id="ba234-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba234-134">Requirement</span></span> | <span data-ttu-id="ba234-135">Valore</span><span class="sxs-lookup"><span data-stu-id="ba234-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba234-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ba234-136">Header</span></span><br/>  | <dl> <span data-ttu-id="ba234-137"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba234-137"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ba234-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="ba234-138">Library</span></span><br/> | <dl> <span data-ttu-id="ba234-139"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="ba234-139"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba234-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba234-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba234-141">Interfacce Effects 11</span><span class="sxs-lookup"><span data-stu-id="ba234-141">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="ba234-142">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="ba234-142">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





