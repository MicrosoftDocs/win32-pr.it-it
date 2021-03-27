---
title: Interfaccia ID3DX11EffectSamplerVariable (D3dx11effect. h)
description: Un'interfaccia del campionatore accede allo stato del campionatore.
ms.assetid: 8d21f829-2145-45f2-a9b4-2fdc06e0a879
keywords:
- Interfaccia ID3DX11EffectSamplerVariable Direct3D 11
- Interfaccia ID3DX11EffectSamplerVariable Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5019022cea823566611410cd6e8fd5013380b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132410"
---
# <a name="id3dx11effectsamplervariable-interface"></a><span data-ttu-id="a11b1-105">Interfaccia ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="a11b1-105">ID3DX11EffectSamplerVariable interface</span></span>

<span data-ttu-id="a11b1-106">Un'interfaccia del campionatore accede allo stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="a11b1-106">A sampler interface accesses sampler state.</span></span>

## <a name="members"></a><span data-ttu-id="a11b1-107">Membri</span><span class="sxs-lookup"><span data-stu-id="a11b1-107">Members</span></span>

<span data-ttu-id="a11b1-108">L'interfaccia **ID3DX11EffectSamplerVariable** eredita da [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="a11b1-108">The **ID3DX11EffectSamplerVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="a11b1-109">**ID3DX11EffectSamplerVariable** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a11b1-109">**ID3DX11EffectSamplerVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="a11b1-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="a11b1-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a11b1-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="a11b1-111">Methods</span></span>

<span data-ttu-id="a11b1-112">L'interfaccia **ID3DX11EffectSamplerVariable** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a11b1-112">The **ID3DX11EffectSamplerVariable** interface has these methods.</span></span>



| <span data-ttu-id="a11b1-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="a11b1-113">Method</span></span>                                                                  | <span data-ttu-id="a11b1-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a11b1-114">Description</span></span>                                                         |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="a11b1-115">**GetBackingStore**</span><span class="sxs-lookup"><span data-stu-id="a11b1-115">**GetBackingStore**</span></span>](id3dx11effectsamplervariable-getbackingstore.md) | <span data-ttu-id="a11b1-116">Ottiene un puntatore a una variabile che contiene lo stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="a11b1-116">Get a pointer to a variable that contains sampler state.</span></span><br/> |
| [<span data-ttu-id="a11b1-117">**Getsampler**</span><span class="sxs-lookup"><span data-stu-id="a11b1-117">**GetSampler**</span></span>](id3dx11effectsamplervariable-getsampler.md)           | <span data-ttu-id="a11b1-118">Ottenere un puntatore a un'interfaccia del campionatore.</span><span class="sxs-lookup"><span data-stu-id="a11b1-118">Get a pointer to a sampler interface.</span></span><br/>                    |
| [<span data-ttu-id="a11b1-119">**Sesampler**</span><span class="sxs-lookup"><span data-stu-id="a11b1-119">**SetSampler**</span></span>](id3dx11effectsamplervariable-setsampler.md)           | <span data-ttu-id="a11b1-120">Impostare lo stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="a11b1-120">Set sampler state.</span></span><br/>                                       |
| [<span data-ttu-id="a11b1-121">**UndoSetSampler**</span><span class="sxs-lookup"><span data-stu-id="a11b1-121">**UndoSetSampler**</span></span>](id3dx11effectsamplervariable-undosetsampler.md)   | <span data-ttu-id="a11b1-122">Ripristinare uno stato del campionatore impostato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="a11b1-122">Revert a previously set sampler state.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="a11b1-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="a11b1-123">Remarks</span></span>

<span data-ttu-id="a11b1-124">Un'interfaccia [**ID3DX11EffectVariable**](id3dx11effectvariable.md) viene creata quando un effetto viene letto in memoria.</span><span class="sxs-lookup"><span data-stu-id="a11b1-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="a11b1-125">Le variabili di effetto vengono salvate in memoria nell'archivio di backup; Quando viene applicata una tecnica, i valori nell'archivio di backup vengono copiati nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a11b1-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="a11b1-126">È possibile usare uno di questi metodi per restituire lo stato.</span><span class="sxs-lookup"><span data-stu-id="a11b1-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="a11b1-127">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="a11b1-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a11b1-128">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="a11b1-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a11b1-129">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a11b1-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a11b1-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a11b1-130">Requirements</span></span>



| <span data-ttu-id="a11b1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a11b1-131">Requirement</span></span> | <span data-ttu-id="a11b1-132">Valore</span><span class="sxs-lookup"><span data-stu-id="a11b1-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a11b1-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a11b1-133">Header</span></span><br/>  | <dl> <span data-ttu-id="a11b1-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a11b1-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a11b1-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="a11b1-135">Library</span></span><br/> | <dl> <span data-ttu-id="a11b1-136"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="a11b1-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a11b1-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a11b1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a11b1-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="a11b1-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="a11b1-139">Interfacce Effects 11</span><span class="sxs-lookup"><span data-stu-id="a11b1-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="a11b1-140">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="a11b1-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





