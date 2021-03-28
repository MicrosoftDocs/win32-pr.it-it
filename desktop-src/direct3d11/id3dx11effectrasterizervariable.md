---
title: Interfaccia ID3DX11EffectRasterizerVariable (D3dx11effect. h)
description: Un'interfaccia di rasterizzatore-variabile accede allo stato di rasterizzazione.
ms.assetid: d039e3c5-c066-4658-bead-92a5d705ed89
keywords:
- Interfaccia ID3DX11EffectRasterizerVariable Direct3D 11
- Interfaccia ID3DX11EffectRasterizerVariable Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a19c5d529d6134ebad238be6e7c6195dc628a7f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996260"
---
# <a name="id3dx11effectrasterizervariable-interface"></a><span data-ttu-id="6ba72-105">Interfaccia ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="6ba72-105">ID3DX11EffectRasterizerVariable interface</span></span>

<span data-ttu-id="6ba72-106">Un'interfaccia di rasterizzatore-variabile accede allo stato di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="6ba72-106">A rasterizer-variable interface accesses rasterizer state.</span></span>

## <a name="members"></a><span data-ttu-id="6ba72-107">Membri</span><span class="sxs-lookup"><span data-stu-id="6ba72-107">Members</span></span>

<span data-ttu-id="6ba72-108">L'interfaccia **ID3DX11EffectRasterizerVariable** eredita da [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="6ba72-108">The **ID3DX11EffectRasterizerVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="6ba72-109">**ID3DX11EffectRasterizerVariable** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6ba72-109">**ID3DX11EffectRasterizerVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="6ba72-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="6ba72-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6ba72-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="6ba72-111">Methods</span></span>

<span data-ttu-id="6ba72-112">L'interfaccia **ID3DX11EffectRasterizerVariable** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6ba72-112">The **ID3DX11EffectRasterizerVariable** interface has these methods.</span></span>



| <span data-ttu-id="6ba72-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="6ba72-113">Method</span></span>                                                                                   | <span data-ttu-id="6ba72-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ba72-114">Description</span></span>                                                            |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="6ba72-115">**GetBackingStore**</span><span class="sxs-lookup"><span data-stu-id="6ba72-115">**GetBackingStore**</span></span>](id3dx11effectrasterizervariable-getbackingstore.md)               | <span data-ttu-id="6ba72-116">Ottiene un puntatore a una variabile che contiene lo stato rasteriser.</span><span class="sxs-lookup"><span data-stu-id="6ba72-116">Get a pointer to a variable that contains rasteriser state.</span></span><br/> |
| [<span data-ttu-id="6ba72-117">**GetRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="6ba72-117">**GetRasterizerState**</span></span>](id3dx11effectrasterizervariable-getrasterizerstate.md)         | <span data-ttu-id="6ba72-118">Ottenere un puntatore a un'interfaccia di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="6ba72-118">Get a pointer to a rasterizer interface.</span></span><br/>                    |
| [<span data-ttu-id="6ba72-119">**SetRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="6ba72-119">**SetRasterizerState**</span></span>](id3dx11effectrasterizervariable-setrasterizerstate.md)         | <span data-ttu-id="6ba72-120">Imposta lo stato del rasterizzatore.</span><span class="sxs-lookup"><span data-stu-id="6ba72-120">Sets the rasterizer state.</span></span><br/>                                  |
| [<span data-ttu-id="6ba72-121">**UndoSetRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="6ba72-121">**UndoSetRasterizerState**</span></span>](id3dx11effectrasterizervariable-undosetrasterizerstate.md) | <span data-ttu-id="6ba72-122">Ripristina uno stato di rasterizzazione impostato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="6ba72-122">Reverts a previously set rasterizer state.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="6ba72-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ba72-123">Remarks</span></span>

<span data-ttu-id="6ba72-124">Un'interfaccia [**ID3DX11EffectVariable**](id3dx11effectvariable.md) viene creata quando un effetto viene letto in memoria.</span><span class="sxs-lookup"><span data-stu-id="6ba72-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="6ba72-125">Le variabili di effetto vengono salvate in memoria nell'archivio di backup; Quando viene applicata una tecnica, i valori nell'archivio di backup vengono copiati nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ba72-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="6ba72-126">È possibile usare uno di questi metodi per restituire lo stato.</span><span class="sxs-lookup"><span data-stu-id="6ba72-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="6ba72-127">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="6ba72-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6ba72-128">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="6ba72-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6ba72-129">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="6ba72-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6ba72-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ba72-130">Requirements</span></span>



| <span data-ttu-id="6ba72-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ba72-131">Requirement</span></span> | <span data-ttu-id="6ba72-132">Valore</span><span class="sxs-lookup"><span data-stu-id="6ba72-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ba72-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6ba72-133">Header</span></span><br/>  | <dl> <span data-ttu-id="6ba72-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ba72-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6ba72-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="6ba72-135">Library</span></span><br/> | <dl> <span data-ttu-id="6ba72-136"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="6ba72-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ba72-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ba72-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ba72-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="6ba72-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="6ba72-139">Interfacce Effects 11</span><span class="sxs-lookup"><span data-stu-id="6ba72-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="6ba72-140">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="6ba72-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





