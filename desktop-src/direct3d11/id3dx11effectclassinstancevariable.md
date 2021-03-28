---
title: Interfaccia ID3DX11EffectClassInstanceVariable (D3dx11effect. h)
description: Accede a un'istanza della classe.
ms.assetid: 64bbae01-1b54-4b3c-9115-80d7b8911ff8
keywords:
- Interfaccia ID3DX11EffectClassInstanceVariable Direct3D 11
- Interfaccia ID3DX11EffectClassInstanceVariable Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectClassInstanceVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56e8b6c7ca76dd595363fa0cd80753fce0b66b2e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355984"
---
# <a name="id3dx11effectclassinstancevariable-interface"></a><span data-ttu-id="3a218-105">Interfaccia ID3DX11EffectClassInstanceVariable</span><span class="sxs-lookup"><span data-stu-id="3a218-105">ID3DX11EffectClassInstanceVariable interface</span></span>

<span data-ttu-id="3a218-106">Accede a un'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="3a218-106">Accesses a class instance.</span></span>

## <a name="members"></a><span data-ttu-id="3a218-107">Membri</span><span class="sxs-lookup"><span data-stu-id="3a218-107">Members</span></span>

<span data-ttu-id="3a218-108">L'interfaccia **ID3DX11EffectClassInstanceVariable** eredita da [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="3a218-108">The **ID3DX11EffectClassInstanceVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="3a218-109">**ID3DX11EffectClassInstanceVariable** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3a218-109">**ID3DX11EffectClassInstanceVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="3a218-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="3a218-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3a218-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="3a218-111">Methods</span></span>

<span data-ttu-id="3a218-112">L'interfaccia **ID3DX11EffectClassInstanceVariable** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="3a218-112">The **ID3DX11EffectClassInstanceVariable** interface has these methods.</span></span>



| <span data-ttu-id="3a218-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="3a218-113">Method</span></span>                                                                          | <span data-ttu-id="3a218-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a218-114">Description</span></span>                       |
|:--------------------------------------------------------------------------------|:----------------------------------|
| [<span data-ttu-id="3a218-115">**GetClassInstance**</span><span class="sxs-lookup"><span data-stu-id="3a218-115">**GetClassInstance**</span></span>](id3dx11effectclassinstancevariable-getclassinstance.md) | <span data-ttu-id="3a218-116">Ottiene un'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="3a218-116">Gets a class instance.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3a218-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a218-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3a218-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="3a218-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3a218-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="3a218-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3a218-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3a218-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3a218-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a218-121">Requirements</span></span>



| <span data-ttu-id="3a218-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a218-122">Requirement</span></span> | <span data-ttu-id="3a218-123">Valore</span><span class="sxs-lookup"><span data-stu-id="3a218-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a218-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a218-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3a218-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a218-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3a218-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="3a218-126">Library</span></span><br/> | <dl> <span data-ttu-id="3a218-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="3a218-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a218-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a218-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a218-129">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="3a218-129">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="3a218-130">Interfacce Effects 11</span><span class="sxs-lookup"><span data-stu-id="3a218-130">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="3a218-131">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="3a218-131">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





