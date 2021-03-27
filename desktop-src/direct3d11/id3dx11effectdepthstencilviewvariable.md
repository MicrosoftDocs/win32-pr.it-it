---
title: Interfaccia ID3DX11EffectDepthStencilViewVariable (D3dx11effect. h)
description: Un'interfaccia di profondità-stencil-visualizzazione-variabile accede a una visualizzazione stencil profondità.
ms.assetid: 316bf0cc-a7cd-4a40-932a-d566e3c2001e
keywords:
- Interfaccia ID3DX11EffectDepthStencilViewVariable Direct3D 11
- Interfaccia ID3DX11EffectDepthStencilViewVariable Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51961bd1300157eef4acb4dd15484d5146a166f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235107"
---
# <a name="id3dx11effectdepthstencilviewvariable-interface"></a><span data-ttu-id="0056a-105">Interfaccia ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="0056a-105">ID3DX11EffectDepthStencilViewVariable interface</span></span>

<span data-ttu-id="0056a-106">Un'interfaccia di profondità-stencil-visualizzazione-variabile accede a una visualizzazione stencil profondità.</span><span class="sxs-lookup"><span data-stu-id="0056a-106">A depth-stencil-view-variable interface accesses a depth-stencil view.</span></span>

## <a name="members"></a><span data-ttu-id="0056a-107">Membri</span><span class="sxs-lookup"><span data-stu-id="0056a-107">Members</span></span>

<span data-ttu-id="0056a-108">L'interfaccia **ID3DX11EffectDepthStencilViewVariable** eredita da [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="0056a-108">The **ID3DX11EffectDepthStencilViewVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="0056a-109">**ID3DX11EffectDepthStencilViewVariable** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0056a-109">**ID3DX11EffectDepthStencilViewVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="0056a-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="0056a-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0056a-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="0056a-111">Methods</span></span>

<span data-ttu-id="0056a-112">L'interfaccia **ID3DX11EffectDepthStencilViewVariable** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="0056a-112">The **ID3DX11EffectDepthStencilViewVariable** interface has these methods.</span></span>



| <span data-ttu-id="0056a-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="0056a-113">Method</span></span>                                                                                     | <span data-ttu-id="0056a-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0056a-114">Description</span></span>                                              |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="0056a-115">**GetDepthStencil**</span><span class="sxs-lookup"><span data-stu-id="0056a-115">**GetDepthStencil**</span></span>](id3dx11effectdepthstencilviewvariable-getdepthstencil.md)           | <span data-ttu-id="0056a-116">Ottenere una risorsa di visualizzazione stencil profondità.</span><span class="sxs-lookup"><span data-stu-id="0056a-116">Get a depth-stencil-view resource.</span></span><br/>            |
| [<span data-ttu-id="0056a-117">**GetDepthStencilArray**</span><span class="sxs-lookup"><span data-stu-id="0056a-117">**GetDepthStencilArray**</span></span>](id3dx11effectdepthstencilviewvariable-getdepthstencilarray.md) | <span data-ttu-id="0056a-118">Ottenere una matrice di risorse di visualizzazione degli stencil di profondità.</span><span class="sxs-lookup"><span data-stu-id="0056a-118">Get an array of depth-stencil-view resources.</span></span><br/> |
| [<span data-ttu-id="0056a-119">**SetDepthStencil**</span><span class="sxs-lookup"><span data-stu-id="0056a-119">**SetDepthStencil**</span></span>](id3dx11effectdepthstencilviewvariable-setdepthstencil.md)           | <span data-ttu-id="0056a-120">Impostare una risorsa di visualizzazione stencil profondità.</span><span class="sxs-lookup"><span data-stu-id="0056a-120">Set a depth-stencil-view resource.</span></span><br/>            |
| [<span data-ttu-id="0056a-121">**SetDepthStencilArray**</span><span class="sxs-lookup"><span data-stu-id="0056a-121">**SetDepthStencilArray**</span></span>](id3dx11effectdepthstencilviewvariable-setdepthstencilarray.md) | <span data-ttu-id="0056a-122">Impostare una matrice di risorse di visualizzazione degli stencil di profondità.</span><span class="sxs-lookup"><span data-stu-id="0056a-122">Set an array of depth-stencil-view resources.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0056a-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="0056a-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0056a-124">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="0056a-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0056a-125">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="0056a-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0056a-126">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0056a-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0056a-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0056a-127">Requirements</span></span>



| <span data-ttu-id="0056a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0056a-128">Requirement</span></span> | <span data-ttu-id="0056a-129">Valore</span><span class="sxs-lookup"><span data-stu-id="0056a-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0056a-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0056a-130">Header</span></span><br/>  | <dl> <span data-ttu-id="0056a-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0056a-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0056a-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="0056a-132">Library</span></span><br/> | <dl> <span data-ttu-id="0056a-133"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="0056a-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0056a-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0056a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0056a-135">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="0056a-135">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="0056a-136">Interfacce Effects 11</span><span class="sxs-lookup"><span data-stu-id="0056a-136">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="0056a-137">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="0056a-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





