---
title: Interfaccia ID3DX11EffectBlendVariable (D3dx11effect. h)
description: L'interfaccia della variabile Blend accede allo stato di Blend.
ms.assetid: 8a6e6e7e-2f1e-4e16-8d28-ffc7f3f018d6
keywords:
- Interfaccia ID3DX11EffectBlendVariable Direct3D 11
- Interfaccia ID3DX11EffectBlendVariable Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57a0a8a3ec0c2a3d92dfc9579fff8b3769dcfc5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969513"
---
# <a name="id3dx11effectblendvariable-interface"></a><span data-ttu-id="e5c9b-105">Interfaccia ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="e5c9b-105">ID3DX11EffectBlendVariable interface</span></span>

<span data-ttu-id="e5c9b-106">L'interfaccia della variabile Blend accede allo stato di Blend.</span><span class="sxs-lookup"><span data-stu-id="e5c9b-106">The blend-variable interface accesses blend state.</span></span>

## <a name="members"></a><span data-ttu-id="e5c9b-107">Membri</span><span class="sxs-lookup"><span data-stu-id="e5c9b-107">Members</span></span>

<span data-ttu-id="e5c9b-108">L'interfaccia **ID3DX11EffectBlendVariable** eredita da [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="e5c9b-108">The **ID3DX11EffectBlendVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="e5c9b-109">**ID3DX11EffectBlendVariable** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e5c9b-109">**ID3DX11EffectBlendVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="e5c9b-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="e5c9b-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e5c9b-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="e5c9b-111">Methods</span></span>

<span data-ttu-id="e5c9b-112">L'interfaccia **ID3DX11EffectBlendVariable** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e5c9b-112">The **ID3DX11EffectBlendVariable** interface has these methods.</span></span>



| <span data-ttu-id="e5c9b-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="e5c9b-113">Method</span></span>                                                                    | <span data-ttu-id="e5c9b-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5c9b-114">Description</span></span>                                          |
|:--------------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="e5c9b-115">**GetBackingStore**</span><span class="sxs-lookup"><span data-stu-id="e5c9b-115">**GetBackingStore**</span></span>](id3dx11effectblendvariable-getbackingstore.md)     | <span data-ttu-id="e5c9b-116">Ottenere un puntatore a una variabile di stato di Blend.</span><span class="sxs-lookup"><span data-stu-id="e5c9b-116">Get a pointer to a blend-state variable.</span></span><br/>  |
| [<span data-ttu-id="e5c9b-117">**GetBlendState**</span><span class="sxs-lookup"><span data-stu-id="e5c9b-117">**GetBlendState**</span></span>](id3dx11effectblendvariable-getblendstate.md)         | <span data-ttu-id="e5c9b-118">Ottenere un puntatore a un'interfaccia di stato di Blend.</span><span class="sxs-lookup"><span data-stu-id="e5c9b-118">Get a pointer to a blend-state interface.</span></span><br/> |
| [<span data-ttu-id="e5c9b-119">**SetBlendState**</span><span class="sxs-lookup"><span data-stu-id="e5c9b-119">**SetBlendState**</span></span>](id3dx11effectblendvariable-setblendstate.md)         | <span data-ttu-id="e5c9b-120">Imposta lo stato di Blend di un effetto.</span><span class="sxs-lookup"><span data-stu-id="e5c9b-120">Sets an effect's blend-state.</span></span><br/>             |
| [<span data-ttu-id="e5c9b-121">**UndoSetBlendState**</span><span class="sxs-lookup"><span data-stu-id="e5c9b-121">**UndoSetBlendState**</span></span>](id3dx11effectblendvariable-undosetblendstate.md) | <span data-ttu-id="e5c9b-122">Ripristina uno stato di Blend impostato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="e5c9b-122">Reverts a previously set blend-state.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="e5c9b-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5c9b-123">Remarks</span></span>

<span data-ttu-id="e5c9b-124">Un'interfaccia [**ID3DX11EffectVariable**](id3dx11effectvariable.md) viene creata quando un effetto viene letto in memoria.</span><span class="sxs-lookup"><span data-stu-id="e5c9b-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="e5c9b-125">Le variabili di effetto vengono salvate in memoria nell'archivio di backup; Quando viene applicata una tecnica, i valori nell'archivio di backup vengono copiati nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5c9b-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="e5c9b-126">È possibile usare uno di questi metodi per restituire lo stato.</span><span class="sxs-lookup"><span data-stu-id="e5c9b-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="e5c9b-127">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="e5c9b-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e5c9b-128">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="e5c9b-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e5c9b-129">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e5c9b-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e5c9b-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5c9b-130">Requirements</span></span>



| <span data-ttu-id="e5c9b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5c9b-131">Requirement</span></span> | <span data-ttu-id="e5c9b-132">Valore</span><span class="sxs-lookup"><span data-stu-id="e5c9b-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5c9b-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5c9b-133">Header</span></span><br/>  | <dl> <span data-ttu-id="e5c9b-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5c9b-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e5c9b-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="e5c9b-135">Library</span></span><br/> | <dl> <span data-ttu-id="e5c9b-136"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="e5c9b-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5c9b-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5c9b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5c9b-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="e5c9b-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="e5c9b-139">Interfacce Effects 11</span><span class="sxs-lookup"><span data-stu-id="e5c9b-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="e5c9b-140">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="e5c9b-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





