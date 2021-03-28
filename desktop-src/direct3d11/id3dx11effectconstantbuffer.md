---
title: Interfaccia ID3DX11EffectConstantBuffer (D3dx11effect. h)
description: Un'interfaccia con buffer costante accede a buffer costanti o a buffer di trama.
ms.assetid: 2106cb51-dc0a-4ab6-adb6-2deb06922af1
keywords:
- Interfaccia ID3DX11EffectConstantBuffer Direct3D 11
- Interfaccia ID3DX11EffectConstantBuffer Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfea2e8e67af30075990d6643b10bb86cf3021ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355254"
---
# <a name="id3dx11effectconstantbuffer-interface"></a><span data-ttu-id="8b685-105">Interfaccia ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="8b685-105">ID3DX11EffectConstantBuffer interface</span></span>

<span data-ttu-id="8b685-106">Un'interfaccia con buffer costante accede a buffer costanti o a buffer di trama.</span><span class="sxs-lookup"><span data-stu-id="8b685-106">A constant-buffer interface accesses constant buffers or texture buffers.</span></span>

## <a name="members"></a><span data-ttu-id="8b685-107">Membri</span><span class="sxs-lookup"><span data-stu-id="8b685-107">Members</span></span>

<span data-ttu-id="8b685-108">L'interfaccia **ID3DX11EffectConstantBuffer** eredita da [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="8b685-108">The **ID3DX11EffectConstantBuffer** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="8b685-109">**ID3DX11EffectConstantBuffer** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8b685-109">**ID3DX11EffectConstantBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="8b685-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="8b685-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8b685-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="8b685-111">Methods</span></span>

<span data-ttu-id="8b685-112">L'interfaccia **ID3DX11EffectConstantBuffer** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="8b685-112">The **ID3DX11EffectConstantBuffer** interface has these methods.</span></span>



| <span data-ttu-id="8b685-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="8b685-113">Method</span></span>                                                                             | <span data-ttu-id="8b685-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b685-114">Description</span></span>                                          |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="8b685-115">**GetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="8b685-115">**GetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-getconstantbuffer.md)         | <span data-ttu-id="8b685-116">Ottenere un buffer costante.</span><span class="sxs-lookup"><span data-stu-id="8b685-116">Get a constant-buffer.</span></span><br/>                    |
| [<span data-ttu-id="8b685-117">**GetTextureBuffer**</span><span class="sxs-lookup"><span data-stu-id="8b685-117">**GetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-gettexturebuffer.md)           | <span data-ttu-id="8b685-118">Ottenere un buffer di trama.</span><span class="sxs-lookup"><span data-stu-id="8b685-118">Get a texture-buffer.</span></span><br/>                     |
| [<span data-ttu-id="8b685-119">**SetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="8b685-119">**SetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-setconstantbuffer.md)         | <span data-ttu-id="8b685-120">Impostare un buffer di costanti.</span><span class="sxs-lookup"><span data-stu-id="8b685-120">Set a constant-buffer.</span></span><br/>                    |
| [<span data-ttu-id="8b685-121">**SetTextureBuffer**</span><span class="sxs-lookup"><span data-stu-id="8b685-121">**SetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-settexturebuffer.md)           | <span data-ttu-id="8b685-122">Impostare un buffer di trama.</span><span class="sxs-lookup"><span data-stu-id="8b685-122">Set a texture-buffer.</span></span><br/>                     |
| [<span data-ttu-id="8b685-123">**UndoSetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="8b685-123">**UndoSetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-undosetconstantbuffer.md) | <span data-ttu-id="8b685-124">Ripristina un buffer costante impostato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="8b685-124">Reverts a previously set constant buffer.</span></span><br/> |
| [<span data-ttu-id="8b685-125">**UndoSetTextureBuffer**</span><span class="sxs-lookup"><span data-stu-id="8b685-125">**UndoSetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-undosettexturebuffer.md)   | <span data-ttu-id="8b685-126">Ripristina un buffer di trama impostato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="8b685-126">Reverts a previously set texture buffer.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="8b685-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="8b685-127">Remarks</span></span>

<span data-ttu-id="8b685-128">Usare i buffer costanti per archiviare molte costanti di effetto; raggruppamento di costanti in buffer in base alla relativa frequenza di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8b685-128">Use constant buffers to store many effect constants; grouping constants into buffers based on their frequency of update.</span></span> <span data-ttu-id="8b685-129">Questo consente di ridurre al minimo il numero di modifiche allo stato e di effettuare il minor numero di chiamate API per modificare lo stato.</span><span class="sxs-lookup"><span data-stu-id="8b685-129">This allows you to minimize the number of state changes as well as make the fewest API calls to change state.</span></span> <span data-ttu-id="8b685-130">Entrambi questi fattori consentono di ottenere prestazioni migliori.</span><span class="sxs-lookup"><span data-stu-id="8b685-130">Both of these factors lead to better performance.</span></span>

> [!Note]  
> <span data-ttu-id="8b685-131">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="8b685-131">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="8b685-132">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="8b685-132">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="8b685-133">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="8b685-133">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8b685-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b685-134">Requirements</span></span>



| <span data-ttu-id="8b685-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b685-135">Requirement</span></span> | <span data-ttu-id="8b685-136">Valore</span><span class="sxs-lookup"><span data-stu-id="8b685-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b685-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b685-137">Header</span></span><br/>  | <dl> <span data-ttu-id="8b685-138"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b685-138"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="8b685-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="8b685-139">Library</span></span><br/> | <dl> <span data-ttu-id="8b685-140"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="8b685-140"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b685-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b685-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b685-142">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="8b685-142">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="8b685-143">Interfacce Effects 11</span><span class="sxs-lookup"><span data-stu-id="8b685-143">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="8b685-144">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="8b685-144">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





