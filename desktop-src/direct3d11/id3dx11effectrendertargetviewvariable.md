---
title: Interfaccia ID3DX11EffectRenderTargetViewVariable (D3dx11effect. h)
description: Un'interfaccia di visualizzazione della destinazione di rendering accede a una destinazione di rendering.
ms.assetid: 35c4e1da-05a8-4f1c-8730-58e3c90ad213
keywords:
- Interfaccia ID3DX11EffectRenderTargetViewVariable Direct3D 11
- Interfaccia ID3DX11EffectRenderTargetViewVariable Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5b20f83639fd973016bbe263d9d21dae7b295c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982202"
---
# <a name="id3dx11effectrendertargetviewvariable-interface"></a><span data-ttu-id="e2f1f-105">Interfaccia ID3DX11EffectRenderTargetViewVariable</span><span class="sxs-lookup"><span data-stu-id="e2f1f-105">ID3DX11EffectRenderTargetViewVariable interface</span></span>

<span data-ttu-id="e2f1f-106">Un'interfaccia di visualizzazione della destinazione di rendering accede a una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="e2f1f-106">A render-target-view interface accesses a render target.</span></span>

## <a name="members"></a><span data-ttu-id="e2f1f-107">Membri</span><span class="sxs-lookup"><span data-stu-id="e2f1f-107">Members</span></span>

<span data-ttu-id="e2f1f-108">L'interfaccia **ID3DX11EffectRenderTargetViewVariable** eredita da [**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="e2f1f-108">The **ID3DX11EffectRenderTargetViewVariable** interface inherits from [**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="e2f1f-109">**ID3DX11EffectRenderTargetViewVariable** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e2f1f-109">**ID3DX11EffectRenderTargetViewVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="e2f1f-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="e2f1f-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e2f1f-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="e2f1f-111">Methods</span></span>

<span data-ttu-id="e2f1f-112">L'interfaccia **ID3DX11EffectRenderTargetViewVariable** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e2f1f-112">The **ID3DX11EffectRenderTargetViewVariable** interface has these methods.</span></span>



| <span data-ttu-id="e2f1f-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="e2f1f-113">Method</span></span>                                                                                     | <span data-ttu-id="e2f1f-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2f1f-114">Description</span></span>                                |
|:-------------------------------------------------------------------------------------------|:-------------------------------------------|
| [<span data-ttu-id="e2f1f-115">**GetRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="e2f1f-115">**GetRenderTarget**</span></span>](id3dx11effectrendertargetviewvariable-getrendertarget.md)           | <span data-ttu-id="e2f1f-116">Ottenere una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="e2f1f-116">Get a render-target.</span></span><br/>            |
| [<span data-ttu-id="e2f1f-117">**GetRenderTargetArray**</span><span class="sxs-lookup"><span data-stu-id="e2f1f-117">**GetRenderTargetArray**</span></span>](id3dx11effectrendertargetviewvariable-getrendertargetarray.md) | <span data-ttu-id="e2f1f-118">Ottenere una matrice di destinazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="e2f1f-118">Get an array of render-targets.</span></span><br/> |
| [<span data-ttu-id="e2f1f-119">**SetRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="e2f1f-119">**SetRenderTarget**</span></span>](id3dx11effectrendertargetviewvariable-setrendertarget.md)           | <span data-ttu-id="e2f1f-120">Impostare una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="e2f1f-120">Set a render-target.</span></span><br/>            |
| [<span data-ttu-id="e2f1f-121">**SetRenderTargetArray**</span><span class="sxs-lookup"><span data-stu-id="e2f1f-121">**SetRenderTargetArray**</span></span>](id3dx11effectrendertargetviewvariable-setrendertargetarray.md) | <span data-ttu-id="e2f1f-122">Impostare una matrice di destinazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="e2f1f-122">Set an array of render-targets.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e2f1f-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2f1f-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e2f1f-124">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="e2f1f-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e2f1f-125">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="e2f1f-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e2f1f-126">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e2f1f-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e2f1f-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2f1f-127">Requirements</span></span>



| <span data-ttu-id="e2f1f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2f1f-128">Requirement</span></span> | <span data-ttu-id="e2f1f-129">Valore</span><span class="sxs-lookup"><span data-stu-id="e2f1f-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2f1f-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e2f1f-130">Header</span></span><br/>  | <dl> <span data-ttu-id="e2f1f-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2f1f-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e2f1f-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="e2f1f-132">Library</span></span><br/> | <dl> <span data-ttu-id="e2f1f-133"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="e2f1f-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2f1f-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2f1f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2f1f-135">**ID3DX11EffectRasterizerVariable**</span><span class="sxs-lookup"><span data-stu-id="e2f1f-135">**ID3DX11EffectRasterizerVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="e2f1f-136">Interfacce Effects 11</span><span class="sxs-lookup"><span data-stu-id="e2f1f-136">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="e2f1f-137">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="e2f1f-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





