---
title: Interfaccia ID3DX11EffectGroup (D3dx11effect. h)
description: L'interfaccia ID3DX11EffectGroup accede a un gruppo di effetti. La durata di un oggetto ID3DX11EffectGroup è uguale alla durata del relativo oggetto ID3DX11Effect padre.
ms.assetid: f5a35c47-0bac-4559-bd6c-5e8bc7699e10
keywords:
- Interfaccia ID3DX11EffectGroup Direct3D 11
- Interfaccia ID3DX11EffectGroup Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5970506b850d164a4018cd371e19bfab6cd3624
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982280"
---
# <a name="id3dx11effectgroup-interface"></a><span data-ttu-id="364a3-105">Interfaccia ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="364a3-105">ID3DX11EffectGroup interface</span></span>

<span data-ttu-id="364a3-106">L'interfaccia **ID3DX11EffectGroup** accede a un gruppo di effetti.</span><span class="sxs-lookup"><span data-stu-id="364a3-106">The **ID3DX11EffectGroup** interface accesses an Effect group.</span></span>

<span data-ttu-id="364a3-107">La durata di un oggetto **ID3DX11EffectGroup** è uguale alla durata del relativo oggetto [**ID3DX11Effect**](id3dx11effect.md) padre.</span><span class="sxs-lookup"><span data-stu-id="364a3-107">The lifetime of an **ID3DX11EffectGroup** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="364a3-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="364a3-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="364a3-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="364a3-109">Methods</span></span>

<span data-ttu-id="364a3-110">L'interfaccia **ID3DX11EffectGroup** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="364a3-110">The **ID3DX11EffectGroup** interface has these methods.</span></span>



| <span data-ttu-id="364a3-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="364a3-111">Method</span></span>                                                                  | <span data-ttu-id="364a3-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="364a3-112">Description</span></span>                                                   |
|:------------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="364a3-113">**GetAnnotationByIndex**</span><span class="sxs-lookup"><span data-stu-id="364a3-113">**GetAnnotationByIndex**</span></span>](id3dx11effectgroup-getannotationbyindex.md) | <span data-ttu-id="364a3-114">Ottenere un'annotazione in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="364a3-114">Get an annotation by index.</span></span><br/>                        |
| [<span data-ttu-id="364a3-115">**GetAnnotationByName**</span><span class="sxs-lookup"><span data-stu-id="364a3-115">**GetAnnotationByName**</span></span>](id3dx11effectgroup-getannotationbyname.md)   | <span data-ttu-id="364a3-116">Ottenere un'annotazione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="364a3-116">Get an annotation by name.</span></span><br/>                         |
| [<span data-ttu-id="364a3-117">**Getdesc**</span><span class="sxs-lookup"><span data-stu-id="364a3-117">**GetDesc**</span></span>](id3dx11effectgroup-getdesc.md)                           | <span data-ttu-id="364a3-118">Ottiene una descrizione del gruppo.</span><span class="sxs-lookup"><span data-stu-id="364a3-118">Gets a group description.</span></span><br/>                          |
| [<span data-ttu-id="364a3-119">**GetTechniqueByIndex**</span><span class="sxs-lookup"><span data-stu-id="364a3-119">**GetTechniqueByIndex**</span></span>](id3dx11effectgroup-gettechniquebyindex.md)   | <span data-ttu-id="364a3-120">Ottenere una tecnica in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="364a3-120">Get a technique by index.</span></span><br/>                          |
| [<span data-ttu-id="364a3-121">**GetTechniqueByName**</span><span class="sxs-lookup"><span data-stu-id="364a3-121">**GetTechniqueByName**</span></span>](id3dx11effectgroup-gettechniquebyname.md)     | <span data-ttu-id="364a3-122">Ottenere una tecnica in base al nome.</span><span class="sxs-lookup"><span data-stu-id="364a3-122">Get a technique by name.</span></span><br/>                           |
| [<span data-ttu-id="364a3-123">**isValid**</span><span class="sxs-lookup"><span data-stu-id="364a3-123">**IsValid**</span></span>](id3dx11effectgroup-isvalid.md)                           | <span data-ttu-id="364a3-124">Testare un effetto per verificare se contiene una sintassi valida.</span><span class="sxs-lookup"><span data-stu-id="364a3-124">Test an effect to see if it contains valid syntax.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="364a3-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="364a3-125">Remarks</span></span>

<span data-ttu-id="364a3-126">Per ottenere un'interfaccia **ID3DX11EffectGroup** , chiamare un metodo come [**ID3DX11Effect:: GetGroupByName**](id3dx11effect-getgroupbyname.md).</span><span class="sxs-lookup"><span data-stu-id="364a3-126">To get an **ID3DX11EffectGroup** interface, call a method like [**ID3DX11Effect::GetGroupByName**](id3dx11effect-getgroupbyname.md).</span></span>

> [!Note]  
> <span data-ttu-id="364a3-127">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="364a3-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="364a3-128">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="364a3-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="364a3-129">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="364a3-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="364a3-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="364a3-130">Requirements</span></span>



| <span data-ttu-id="364a3-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="364a3-131">Requirement</span></span> | <span data-ttu-id="364a3-132">Valore</span><span class="sxs-lookup"><span data-stu-id="364a3-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="364a3-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="364a3-133">Header</span></span><br/>  | <dl> <span data-ttu-id="364a3-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="364a3-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="364a3-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="364a3-135">Library</span></span><br/> | <dl> <span data-ttu-id="364a3-136"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="364a3-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="364a3-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="364a3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="364a3-138">Interfacce Effects 11</span><span class="sxs-lookup"><span data-stu-id="364a3-138">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="364a3-139">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="364a3-139">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





