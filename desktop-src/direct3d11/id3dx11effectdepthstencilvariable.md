---
title: Interfaccia ID3DX11EffectDepthStencilVariable (D3dx11effect. h)
description: Un'interfaccia della variabile di stencil Depth accede allo stato di stencil Depth.
ms.assetid: 8fb1be19-eed4-4d69-bbbe-94484531eba2
keywords:
- Interfaccia ID3DX11EffectDepthStencilVariable Direct3D 11
- Interfaccia ID3DX11EffectDepthStencilVariable Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d7aa520df0c13c81435421d5f605f901a61da6e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969469"
---
# <a name="id3dx11effectdepthstencilvariable-interface"></a><span data-ttu-id="e9828-105">Interfaccia ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="e9828-105">ID3DX11EffectDepthStencilVariable interface</span></span>

<span data-ttu-id="e9828-106">Un'interfaccia della variabile di stencil Depth accede allo stato di stencil Depth.</span><span class="sxs-lookup"><span data-stu-id="e9828-106">A depth-stencil-variable interface accesses depth-stencil state.</span></span>

## <a name="members"></a><span data-ttu-id="e9828-107">Membri</span><span class="sxs-lookup"><span data-stu-id="e9828-107">Members</span></span>

<span data-ttu-id="e9828-108">L'interfaccia **ID3DX11EffectDepthStencilVariable** eredita da [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="e9828-108">The **ID3DX11EffectDepthStencilVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="e9828-109">**ID3DX11EffectDepthStencilVariable** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e9828-109">**ID3DX11EffectDepthStencilVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="e9828-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="e9828-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e9828-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="e9828-111">Methods</span></span>

<span data-ttu-id="e9828-112">L'interfaccia **ID3DX11EffectDepthStencilVariable** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e9828-112">The **ID3DX11EffectDepthStencilVariable** interface has these methods.</span></span>



| <span data-ttu-id="e9828-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="e9828-113">Method</span></span>                                                                                         | <span data-ttu-id="e9828-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9828-114">Description</span></span>                                                               |
|:-----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="e9828-115">**GetBackingStore**</span><span class="sxs-lookup"><span data-stu-id="e9828-115">**GetBackingStore**</span></span>](id3dx11effectdepthstencilvariable-getbackingstore.md)                   | <span data-ttu-id="e9828-116">Ottenere un puntatore a una variabile che contiene lo stato di stencil Depth.</span><span class="sxs-lookup"><span data-stu-id="e9828-116">Get a pointer to a variable that contains depth-stencil state.</span></span><br/> |
| [<span data-ttu-id="e9828-117">**GetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="e9828-117">**GetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-getdepthstencilstate.md)         | <span data-ttu-id="e9828-118">Ottenere un puntatore a un'interfaccia di stencil profondità.</span><span class="sxs-lookup"><span data-stu-id="e9828-118">Get a pointer to a depth-stencil interface.</span></span><br/>                    |
| [<span data-ttu-id="e9828-119">**SetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="e9828-119">**SetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)         | <span data-ttu-id="e9828-120">Imposta lo stato del depth stencil.</span><span class="sxs-lookup"><span data-stu-id="e9828-120">Sets the depth stencil state.</span></span><br/>                                  |
| [<span data-ttu-id="e9828-121">**UndoSetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="e9828-121">**UndoSetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md) | <span data-ttu-id="e9828-122">Ripristina uno stato di depth stencil impostato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="e9828-122">Reverts a previously set depth stencil state.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="e9828-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9828-123">Remarks</span></span>

<span data-ttu-id="e9828-124">Un'interfaccia [**ID3DX11EffectVariable**](id3dx11effectvariable.md) viene creata quando un effetto viene letto in memoria.</span><span class="sxs-lookup"><span data-stu-id="e9828-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="e9828-125">Le variabili di effetto vengono salvate in memoria nell'archivio di backup; Quando viene applicata una tecnica, i valori nell'archivio di backup vengono copiati nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9828-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="e9828-126">È possibile usare uno di questi metodi per restituire lo stato.</span><span class="sxs-lookup"><span data-stu-id="e9828-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="e9828-127">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="e9828-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e9828-128">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="e9828-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e9828-129">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e9828-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e9828-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9828-130">Requirements</span></span>



| <span data-ttu-id="e9828-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9828-131">Requirement</span></span> | <span data-ttu-id="e9828-132">Valore</span><span class="sxs-lookup"><span data-stu-id="e9828-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9828-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9828-133">Header</span></span><br/>  | <dl> <span data-ttu-id="e9828-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9828-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e9828-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="e9828-135">Library</span></span><br/> | <dl> <span data-ttu-id="e9828-136"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="e9828-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9828-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9828-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9828-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="e9828-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="e9828-139">Interfacce Effects 11</span><span class="sxs-lookup"><span data-stu-id="e9828-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="e9828-140">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="e9828-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





