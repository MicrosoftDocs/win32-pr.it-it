---
title: Interfaccia ID3DX11EffectStringVariable (D3dx11effect. h)
description: Un'interfaccia a variabili di stringa accede a una variabile di stringa.
ms.assetid: 8304d7cc-de30-41fe-af12-e11bf7ae32ce
keywords:
- Interfaccia ID3DX11EffectStringVariable Direct3D 11
- Interfaccia ID3DX11EffectStringVariable Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a45eb5e0825bd8487396ed850c9d79665e5f1044
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995810"
---
# <a name="id3dx11effectstringvariable-interface"></a><span data-ttu-id="54357-105">Interfaccia ID3DX11EffectStringVariable</span><span class="sxs-lookup"><span data-stu-id="54357-105">ID3DX11EffectStringVariable interface</span></span>

<span data-ttu-id="54357-106">Un'interfaccia a variabili di stringa accede a una variabile di stringa.</span><span class="sxs-lookup"><span data-stu-id="54357-106">A string-variable interface accesses a string variable.</span></span>

## <a name="members"></a><span data-ttu-id="54357-107">Membri</span><span class="sxs-lookup"><span data-stu-id="54357-107">Members</span></span>

<span data-ttu-id="54357-108">L'interfaccia **ID3DX11EffectStringVariable** eredita da [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="54357-108">The **ID3DX11EffectStringVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="54357-109">**ID3DX11EffectStringVariable** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="54357-109">**ID3DX11EffectStringVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="54357-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="54357-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="54357-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="54357-111">Methods</span></span>

<span data-ttu-id="54357-112">L'interfaccia **ID3DX11EffectStringVariable** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="54357-112">The **ID3DX11EffectStringVariable** interface has these methods.</span></span>



| <span data-ttu-id="54357-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="54357-113">Method</span></span>                                                               | <span data-ttu-id="54357-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54357-114">Description</span></span>                         |
|:---------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="54357-115">**GetString**</span><span class="sxs-lookup"><span data-stu-id="54357-115">**GetString**</span></span>](id3dx11effectstringvariable-getstring.md)           | <span data-ttu-id="54357-116">Ottiene la stringa.</span><span class="sxs-lookup"><span data-stu-id="54357-116">Get the string.</span></span><br/>          |
| [<span data-ttu-id="54357-117">**GetStringArray**</span><span class="sxs-lookup"><span data-stu-id="54357-117">**GetStringArray**</span></span>](id3dx11effectstringvariable-getstringarray.md) | <span data-ttu-id="54357-118">Ottiene una matrice di stringhe.</span><span class="sxs-lookup"><span data-stu-id="54357-118">Get an array of strings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="54357-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="54357-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="54357-120">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="54357-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="54357-121">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="54357-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="54357-122">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="54357-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="54357-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54357-123">Requirements</span></span>



| <span data-ttu-id="54357-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="54357-124">Requirement</span></span> | <span data-ttu-id="54357-125">Valore</span><span class="sxs-lookup"><span data-stu-id="54357-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54357-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54357-126">Header</span></span><br/>  | <dl> <span data-ttu-id="54357-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="54357-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="54357-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="54357-128">Library</span></span><br/> | <dl> <span data-ttu-id="54357-129"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="54357-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54357-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54357-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54357-131">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="54357-131">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="54357-132">Interfacce Effects 11</span><span class="sxs-lookup"><span data-stu-id="54357-132">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="54357-133">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="54357-133">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





