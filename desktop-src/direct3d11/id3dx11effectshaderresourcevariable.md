---
title: Interfaccia ID3DX11EffectShaderResourceVariable (D3dx11effect. h)
description: Un'interfaccia shader-Resource accede a una risorsa shader.
ms.assetid: 936a3439-1f7d-4fea-b124-1d6ead528250
keywords:
- Interfaccia ID3DX11EffectShaderResourceVariable Direct3D 11
- Interfaccia ID3DX11EffectShaderResourceVariable Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7abfc2bf29bf3ea5333bf9e7da6630a62c5747aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996297"
---
# <a name="id3dx11effectshaderresourcevariable-interface"></a><span data-ttu-id="6a1e0-105">Interfaccia ID3DX11EffectShaderResourceVariable</span><span class="sxs-lookup"><span data-stu-id="6a1e0-105">ID3DX11EffectShaderResourceVariable interface</span></span>

<span data-ttu-id="6a1e0-106">Un'interfaccia shader-Resource accede a una risorsa shader.</span><span class="sxs-lookup"><span data-stu-id="6a1e0-106">A shader-resource interface accesses a shader resource.</span></span>

## <a name="members"></a><span data-ttu-id="6a1e0-107">Membri</span><span class="sxs-lookup"><span data-stu-id="6a1e0-107">Members</span></span>

<span data-ttu-id="6a1e0-108">L'interfaccia **ID3DX11EffectShaderResourceVariable** eredita da [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="6a1e0-108">The **ID3DX11EffectShaderResourceVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="6a1e0-109">**ID3DX11EffectShaderResourceVariable** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6a1e0-109">**ID3DX11EffectShaderResourceVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="6a1e0-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="6a1e0-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6a1e0-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="6a1e0-111">Methods</span></span>

<span data-ttu-id="6a1e0-112">L'interfaccia **ID3DX11EffectShaderResourceVariable** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6a1e0-112">The **ID3DX11EffectShaderResourceVariable** interface has these methods.</span></span>



| <span data-ttu-id="6a1e0-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="6a1e0-113">Method</span></span>                                                                           | <span data-ttu-id="6a1e0-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a1e0-114">Description</span></span>                                  |
|:---------------------------------------------------------------------------------|:---------------------------------------------|
| [<span data-ttu-id="6a1e0-115">**GetResource**</span><span class="sxs-lookup"><span data-stu-id="6a1e0-115">**GetResource**</span></span>](id3dx11effectshaderresourcevariable-getresource.md)           | <span data-ttu-id="6a1e0-116">Ottenere una risorsa shader.</span><span class="sxs-lookup"><span data-stu-id="6a1e0-116">Get a shader resource.</span></span><br/>            |
| [<span data-ttu-id="6a1e0-117">**GetResourceArray**</span><span class="sxs-lookup"><span data-stu-id="6a1e0-117">**GetResourceArray**</span></span>](id3dx11effectshaderresourcevariable-getresourcearray.md) | <span data-ttu-id="6a1e0-118">Ottenere una matrice di risorse dello shader.</span><span class="sxs-lookup"><span data-stu-id="6a1e0-118">Get an array of shader resources.</span></span><br/> |
| [<span data-ttu-id="6a1e0-119">**SetResource**</span><span class="sxs-lookup"><span data-stu-id="6a1e0-119">**SetResource**</span></span>](id3dx11effectshaderresourcevariable-setresource.md)           | <span data-ttu-id="6a1e0-120">Impostare una risorsa shader.</span><span class="sxs-lookup"><span data-stu-id="6a1e0-120">Set a shader resource.</span></span><br/>            |
| [<span data-ttu-id="6a1e0-121">**SetResourceArray**</span><span class="sxs-lookup"><span data-stu-id="6a1e0-121">**SetResourceArray**</span></span>](id3dx11effectshaderresourcevariable-setresourcearray.md) | <span data-ttu-id="6a1e0-122">Impostare una matrice di risorse dello shader.</span><span class="sxs-lookup"><span data-stu-id="6a1e0-122">Set an array of shader resources.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6a1e0-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a1e0-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6a1e0-124">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="6a1e0-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6a1e0-125">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="6a1e0-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6a1e0-126">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="6a1e0-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6a1e0-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a1e0-127">Requirements</span></span>



| <span data-ttu-id="6a1e0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a1e0-128">Requirement</span></span> | <span data-ttu-id="6a1e0-129">Valore</span><span class="sxs-lookup"><span data-stu-id="6a1e0-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a1e0-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a1e0-130">Header</span></span><br/>  | <dl> <span data-ttu-id="6a1e0-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a1e0-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6a1e0-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="6a1e0-132">Library</span></span><br/> | <dl> <span data-ttu-id="6a1e0-133"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="6a1e0-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a1e0-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a1e0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a1e0-135">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="6a1e0-135">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="6a1e0-136">Interfacce Effects 11</span><span class="sxs-lookup"><span data-stu-id="6a1e0-136">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="6a1e0-137">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="6a1e0-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





