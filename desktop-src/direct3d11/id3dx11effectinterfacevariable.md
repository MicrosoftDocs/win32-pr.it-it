---
title: Interfaccia ID3DX11EffectInterfaceVariable (D3dx11effect. h)
description: Accede a una variabile di interfaccia.
ms.assetid: c1d1f564-c7b8-4108-9988-972255662000
keywords:
- Interfaccia ID3DX11EffectInterfaceVariable Direct3D 11
- Interfaccia ID3DX11EffectInterfaceVariable Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectInterfaceVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8169afc18e6974168e9196962b3e0cf87e860e4c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982271"
---
# <a name="id3dx11effectinterfacevariable-interface"></a><span data-ttu-id="0a2fa-105">Interfaccia ID3DX11EffectInterfaceVariable</span><span class="sxs-lookup"><span data-stu-id="0a2fa-105">ID3DX11EffectInterfaceVariable interface</span></span>

<span data-ttu-id="0a2fa-106">Accede a una variabile di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="0a2fa-106">Accesses an interface variable.</span></span>

## <a name="members"></a><span data-ttu-id="0a2fa-107">Membri</span><span class="sxs-lookup"><span data-stu-id="0a2fa-107">Members</span></span>

<span data-ttu-id="0a2fa-108">L'interfaccia **ID3DX11EffectInterfaceVariable** eredita da [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="0a2fa-108">The **ID3DX11EffectInterfaceVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="0a2fa-109">**ID3DX11EffectInterfaceVariable** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0a2fa-109">**ID3DX11EffectInterfaceVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="0a2fa-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="0a2fa-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0a2fa-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="0a2fa-111">Methods</span></span>

<span data-ttu-id="0a2fa-112">L'interfaccia **ID3DX11EffectInterfaceVariable** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="0a2fa-112">The **ID3DX11EffectInterfaceVariable** interface has these methods.</span></span>



| <span data-ttu-id="0a2fa-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="0a2fa-113">Method</span></span>                                                                      | <span data-ttu-id="0a2fa-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a2fa-114">Description</span></span>                       |
|:----------------------------------------------------------------------------|:----------------------------------|
| [<span data-ttu-id="0a2fa-115">**GetClassInstance**</span><span class="sxs-lookup"><span data-stu-id="0a2fa-115">**GetClassInstance**</span></span>](id3dx11effectinterfacevariable-getclassinstance.md) | <span data-ttu-id="0a2fa-116">Ottenere un'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="0a2fa-116">Get a class instance.</span></span><br/>  |
| [<span data-ttu-id="0a2fa-117">**SetClassInstance**</span><span class="sxs-lookup"><span data-stu-id="0a2fa-117">**SetClassInstance**</span></span>](id3dx11effectinterfacevariable-setclassinstance.md) | <span data-ttu-id="0a2fa-118">Imposta un'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="0a2fa-118">Sets a class instance.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0a2fa-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a2fa-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0a2fa-120">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="0a2fa-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0a2fa-121">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="0a2fa-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0a2fa-122">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0a2fa-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0a2fa-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a2fa-123">Requirements</span></span>



| <span data-ttu-id="0a2fa-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a2fa-124">Requirement</span></span> | <span data-ttu-id="0a2fa-125">Valore</span><span class="sxs-lookup"><span data-stu-id="0a2fa-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a2fa-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a2fa-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0a2fa-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a2fa-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0a2fa-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="0a2fa-128">Library</span></span><br/> | <dl> <span data-ttu-id="0a2fa-129"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="0a2fa-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a2fa-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a2fa-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a2fa-131">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="0a2fa-131">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="0a2fa-132">Interfacce Effects 11</span><span class="sxs-lookup"><span data-stu-id="0a2fa-132">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="0a2fa-133">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="0a2fa-133">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





