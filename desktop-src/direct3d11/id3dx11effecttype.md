---
title: Interfaccia ID3DX11EffectType (D3dx11effect. h)
description: L'interfaccia ID3DX11EffectType accede alle variabili di effetto per tipo. La durata di un oggetto ID3DX11EffectType è uguale alla durata del relativo oggetto ID3DX11Effect padre.
ms.assetid: 700076ee-a5fe-4af2-a5f4-053c05d8ddf0
keywords:
- Interfaccia ID3DX11EffectType Direct3D 11
- Interfaccia ID3DX11EffectType Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectType
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e3c210ca60abc9e55b8864a2b121cf92be369a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761981"
---
# <a name="id3dx11effecttype-interface"></a><span data-ttu-id="a6de4-105">Interfaccia ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="a6de4-105">ID3DX11EffectType interface</span></span>

<span data-ttu-id="a6de4-106">L'interfaccia **ID3DX11EffectType** accede alle variabili di effetto per tipo.</span><span class="sxs-lookup"><span data-stu-id="a6de4-106">The **ID3DX11EffectType** interface accesses effect variables by type.</span></span>

<span data-ttu-id="a6de4-107">La durata di un oggetto **ID3DX11EffectType** è uguale alla durata del relativo oggetto [**ID3DX11Effect**](id3dx11effect.md) padre.</span><span class="sxs-lookup"><span data-stu-id="a6de4-107">The lifetime of an **ID3DX11EffectType** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="a6de4-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="a6de4-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a6de4-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="a6de4-109">Methods</span></span>

<span data-ttu-id="a6de4-110">L'interfaccia **ID3DX11EffectType** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a6de4-110">The **ID3DX11EffectType** interface has these methods.</span></span>



| <span data-ttu-id="a6de4-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="a6de4-111">Method</span></span>                                                                       | <span data-ttu-id="a6de4-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6de4-112">Description</span></span>                                       |
|:-----------------------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="a6de4-113">**Getdesc**</span><span class="sxs-lookup"><span data-stu-id="a6de4-113">**GetDesc**</span></span>](id3dx11effecttype-getdesc.md)                                 | <span data-ttu-id="a6de4-114">Ottenere una descrizione del tipo di effetto.</span><span class="sxs-lookup"><span data-stu-id="a6de4-114">Get an effect-type description.</span></span><br/>        |
| [<span data-ttu-id="a6de4-115">**GetMemberName**</span><span class="sxs-lookup"><span data-stu-id="a6de4-115">**GetMemberName**</span></span>](id3dx11effecttype-getmembername.md)                     | <span data-ttu-id="a6de4-116">Ottiene il nome di un membro.</span><span class="sxs-lookup"><span data-stu-id="a6de4-116">Get the name of a member.</span></span><br/>              |
| [<span data-ttu-id="a6de4-117">**GetMemberSemantic**</span><span class="sxs-lookup"><span data-stu-id="a6de4-117">**GetMemberSemantic**</span></span>](id3dx11effecttype-getmembersemantic.md)             | <span data-ttu-id="a6de4-118">Ottenere la semantica collegata a un membro.</span><span class="sxs-lookup"><span data-stu-id="a6de4-118">Get the semantic attached to a member.</span></span><br/> |
| [<span data-ttu-id="a6de4-119">**GetMemberTypeByIndex**</span><span class="sxs-lookup"><span data-stu-id="a6de4-119">**GetMemberTypeByIndex**</span></span>](id3dx11effecttype-getmembertypebyindex.md)       | <span data-ttu-id="a6de4-120">Ottenere un tipo di membro in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="a6de4-120">Get a member type by index.</span></span><br/>            |
| [<span data-ttu-id="a6de4-121">**GetMemberTypeByName**</span><span class="sxs-lookup"><span data-stu-id="a6de4-121">**GetMemberTypeByName**</span></span>](id3dx11effecttype-getmembertypebyname.md)         | <span data-ttu-id="a6de4-122">Ottenere un tipo di membro in base al nome.</span><span class="sxs-lookup"><span data-stu-id="a6de4-122">Get an member type by name.</span></span><br/>            |
| [<span data-ttu-id="a6de4-123">**GetMemberTypeBySemantic**</span><span class="sxs-lookup"><span data-stu-id="a6de4-123">**GetMemberTypeBySemantic**</span></span>](id3dx11effecttype-getmembertypebysemantic.md) | <span data-ttu-id="a6de4-124">Ottenere un tipo di membro in base alla semantica.</span><span class="sxs-lookup"><span data-stu-id="a6de4-124">Get a member type by semantic.</span></span><br/>         |
| [<span data-ttu-id="a6de4-125">**isValid**</span><span class="sxs-lookup"><span data-stu-id="a6de4-125">**IsValid**</span></span>](id3dx11effecttype-isvalid.md)                                 | <span data-ttu-id="a6de4-126">Verifica che il tipo di effetto sia valido.</span><span class="sxs-lookup"><span data-stu-id="a6de4-126">Tests that the effect type is valid.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="a6de4-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="a6de4-127">Remarks</span></span>

<span data-ttu-id="a6de4-128">Per ottenere informazioni su un tipo di effetto da una variabile Effect, chiamare [**ID3DX11EffectVariable:: GetType**](id3dx11effectvariable-gettype.md).</span><span class="sxs-lookup"><span data-stu-id="a6de4-128">To get information about an effect type from an effect variable, call [**ID3DX11EffectVariable::GetType**](id3dx11effectvariable-gettype.md).</span></span>

> [!Note]  
> <span data-ttu-id="a6de4-129">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="a6de4-129">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a6de4-130">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="a6de4-130">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a6de4-131">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a6de4-131">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a6de4-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6de4-132">Requirements</span></span>



| <span data-ttu-id="a6de4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6de4-133">Requirement</span></span> | <span data-ttu-id="a6de4-134">Valore</span><span class="sxs-lookup"><span data-stu-id="a6de4-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6de4-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a6de4-135">Header</span></span><br/>  | <dl> <span data-ttu-id="a6de4-136"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6de4-136"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a6de4-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="a6de4-137">Library</span></span><br/> | <dl> <span data-ttu-id="a6de4-138"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="a6de4-138"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6de4-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6de4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6de4-140">Interfacce Effects 11</span><span class="sxs-lookup"><span data-stu-id="a6de4-140">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="a6de4-141">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="a6de4-141">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





