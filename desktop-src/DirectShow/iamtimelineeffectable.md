---
description: L'interfaccia IAMTimelineEffectable fornisce metodi per l'aggiunta di effetti a un oggetto Timeline nei servizi di modifica DirectShow (DES) e per la modifica degli effetti su un oggetto.
ms.assetid: 70f2da64-e16a-4d4d-9522-042b5fa2855c
title: Interfaccia IAMTimelineEffectable (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bc67483f44515c2ce18825de5b6657d51e2c3826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328155"
---
# <a name="iamtimelineeffectable-interface"></a><span data-ttu-id="b1774-103">Interfaccia IAMTimelineEffectable</span><span class="sxs-lookup"><span data-stu-id="b1774-103">IAMTimelineEffectable interface</span></span>

> [!Note]  
> <span data-ttu-id="b1774-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="b1774-104">\[Deprecated.</span></span> <span data-ttu-id="b1774-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b1774-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b1774-106">L' `IAMTimelineEffectable` interfaccia fornisce metodi per l'aggiunta di effetti a un oggetto Timeline in [servizi di modifica DirectShow](directshow-editing-services.md) (des) e per la modifica degli effetti su un oggetto.</span><span class="sxs-lookup"><span data-stu-id="b1774-106">The `IAMTimelineEffectable` interface provides methods for adding effects to a timeline object in [DirectShow Editing Services](directshow-editing-services.md) (DES), and for manipulating the effects on an object.</span></span> <span data-ttu-id="b1774-107">Tutti gli oggetti che possono avere effetti applicati implementano questa interfaccia; sono incluse origini, tracce e composizioni.</span><span class="sxs-lookup"><span data-stu-id="b1774-107">All objects that can have effects applied to them implement this interface; this includes sources, tracks, and compositions.</span></span>

<span data-ttu-id="b1774-108">Un oggetto che implementa questa interfaccia può avere un numero qualsiasi di effetti.</span><span class="sxs-lookup"><span data-stu-id="b1774-108">An object that implements this interface can have any number of effects.</span></span> <span data-ttu-id="b1774-109">Per ogni oggetto, il motore di rendering applica gli effetti in ordine di priorità, a partire dal livello di priorità 0.</span><span class="sxs-lookup"><span data-stu-id="b1774-109">For each object, the render engine applies its effects in order of priority, starting with priority level 0.</span></span>

## <a name="members"></a><span data-ttu-id="b1774-110">Membri</span><span class="sxs-lookup"><span data-stu-id="b1774-110">Members</span></span>

<span data-ttu-id="b1774-111">L'interfaccia **IAMTimelineEffectable** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b1774-111">The **IAMTimelineEffectable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b1774-112">**IAMTimelineEffectable** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b1774-112">**IAMTimelineEffectable** also has these types of members:</span></span>

-   [<span data-ttu-id="b1774-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="b1774-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b1774-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="b1774-114">Methods</span></span>

<span data-ttu-id="b1774-115">L'interfaccia **IAMTimelineEffectable** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b1774-115">The **IAMTimelineEffectable** interface has these methods.</span></span>



| <span data-ttu-id="b1774-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="b1774-116">Method</span></span>                                                                     | <span data-ttu-id="b1774-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1774-117">Description</span></span>                                                                   |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="b1774-118">**EffectGetCount**</span><span class="sxs-lookup"><span data-stu-id="b1774-118">**EffectGetCount**</span></span>](iamtimelineeffectable-effectgetcount.md)             | <span data-ttu-id="b1774-119">Recupera il numero di effetti su questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="b1774-119">Retrieves the number of effects on this object.</span></span><br/>                    |
| [<span data-ttu-id="b1774-120">**EffectInsBefore**</span><span class="sxs-lookup"><span data-stu-id="b1774-120">**EffectInsBefore**</span></span>](iamtimelineeffectable-effectinsbefore.md)           | <span data-ttu-id="b1774-121">Inserisce un effetto nell'oggetto al livello di priorità specificato.</span><span class="sxs-lookup"><span data-stu-id="b1774-121">Inserts an effect into the object at the specified priority level.</span></span><br/> |
| [<span data-ttu-id="b1774-122">**EffectSwapPriorities**</span><span class="sxs-lookup"><span data-stu-id="b1774-122">**EffectSwapPriorities**</span></span>](iamtimelineeffectable-effectswappriorities.md) | <span data-ttu-id="b1774-123">Passa i livelli di priorità di due effetti.</span><span class="sxs-lookup"><span data-stu-id="b1774-123">Switches the priority levels of two effects.</span></span><br/>                       |
| [<span data-ttu-id="b1774-124">**GetEffect**</span><span class="sxs-lookup"><span data-stu-id="b1774-124">**GetEffect**</span></span>](iamtimelineeffectable-geteffect.md)                       | <span data-ttu-id="b1774-125">Recupera l'effetto al livello di priorità specificato.</span><span class="sxs-lookup"><span data-stu-id="b1774-125">Retrieves the effect at the specified priority level.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="b1774-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1774-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b1774-127">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="b1774-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b1774-128">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b1774-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b1774-129">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b1774-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b1774-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1774-130">Requirements</span></span>



| <span data-ttu-id="b1774-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1774-131">Requirement</span></span> | <span data-ttu-id="b1774-132">Valore</span><span class="sxs-lookup"><span data-stu-id="b1774-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1774-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1774-133">Header</span></span><br/>  | <dl> <span data-ttu-id="b1774-134"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1774-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b1774-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="b1774-135">Library</span></span><br/> | <dl> <span data-ttu-id="b1774-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1774-136"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
