---
description: L'interfaccia IAMTimelineTransable aggiunge transizioni a un oggetto in DirectShow editing Services (DES).
ms.assetid: 1be9adaa-4145-447c-b307-dabb4419c86c
title: Interfaccia IAMTimelineTransable (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d083b768e8dcf54236945755f4b26ecf13409b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332960"
---
# <a name="iamtimelinetransable-interface"></a><span data-ttu-id="b0eac-103">Interfaccia IAMTimelineTransable</span><span class="sxs-lookup"><span data-stu-id="b0eac-103">IAMTimelineTransable interface</span></span>

> [!Note]  
> <span data-ttu-id="b0eac-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="b0eac-104">\[Deprecated.</span></span> <span data-ttu-id="b0eac-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b0eac-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b0eac-106">L' `IAMTimelineTransable` interfaccia aggiunge transizioni a un oggetto in [DirectShow editing Services](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="b0eac-106">The `IAMTimelineTransable` interface adds transitions to an object in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="b0eac-107">Questa interfaccia è esposta da qualsiasi oggetto a cui possono essere applicate transizioni, tra cui tracce, composizioni e gruppi.</span><span class="sxs-lookup"><span data-stu-id="b0eac-107">This interface is exposed by any object that can have transitions applied to it, including tracks, compositions, and groups.</span></span> <span data-ttu-id="b0eac-108">Un oggetto che implementa questa interfaccia può avere un numero qualsiasi di transizioni, ma le transizioni non devono sovrapporsi nel tempo.</span><span class="sxs-lookup"><span data-stu-id="b0eac-108">An object that implements this interface can have any number of transitions, but the transitions must not overlap in time.</span></span>

> [!Note]  
> <span data-ttu-id="b0eac-109">L'audio non supporta le transizioni.</span><span class="sxs-lookup"><span data-stu-id="b0eac-109">Audio does not support transitions.</span></span> <span data-ttu-id="b0eac-110">Gli oggetti all'interno di gruppi audio possono esporre l' `IAMTimelineTransable` interfaccia, ma l'applicazione non deve aggiungere transizioni.</span><span class="sxs-lookup"><span data-stu-id="b0eac-110">Objects within audio groups can expose the `IAMTimelineTransable` interface, but the application should not add transitions to them.</span></span>

 

## <a name="members"></a><span data-ttu-id="b0eac-111">Membri</span><span class="sxs-lookup"><span data-stu-id="b0eac-111">Members</span></span>

<span data-ttu-id="b0eac-112">L'interfaccia **IAMTimelineTransable** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b0eac-112">The **IAMTimelineTransable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b0eac-113">**IAMTimelineTransable** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b0eac-113">**IAMTimelineTransable** also has these types of members:</span></span>

-   [<span data-ttu-id="b0eac-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="b0eac-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b0eac-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="b0eac-115">Methods</span></span>

<span data-ttu-id="b0eac-116">L'interfaccia **IAMTimelineTransable** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b0eac-116">The **IAMTimelineTransable** interface has these methods.</span></span>



| <span data-ttu-id="b0eac-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="b0eac-117">Method</span></span>                                                          | <span data-ttu-id="b0eac-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0eac-118">Description</span></span>                                                                                                                        |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0eac-119">**GetNextTrans**</span><span class="sxs-lookup"><span data-stu-id="b0eac-119">**GetNextTrans**</span></span>](iamtimelinetransable-getnexttrans.md)       | <span data-ttu-id="b0eac-120">Recupera la prima transizione visualizzata all'ora specificata o successiva.</span><span class="sxs-lookup"><span data-stu-id="b0eac-120">Retrieves the first transition that appears at the specified time or later.</span></span><br/>                                             |
| [<span data-ttu-id="b0eac-121">**GetNextTrans2**</span><span class="sxs-lookup"><span data-stu-id="b0eac-121">**GetNextTrans2**</span></span>](iamtimelinetransable-getnexttrans2.md)     | <span data-ttu-id="b0eac-122">Recupera la prima transizione visualizzata all'ora specificata o in una versione successiva, con l'ora specificata come valore **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="b0eac-122">Retrieves the first transition that appears at the specified time or later, with the time given as a **REFTIME** value.</span></span><br/> |
| [<span data-ttu-id="b0eac-123">**GetTransAtTime**</span><span class="sxs-lookup"><span data-stu-id="b0eac-123">**GetTransAtTime**</span></span>](iamtimelinetransable-gettransattime.md)   | <span data-ttu-id="b0eac-124">Recupera la transizione più vicina all'ora specificata.</span><span class="sxs-lookup"><span data-stu-id="b0eac-124">Retrieves the transition nearest to the specified time.</span></span><br/>                                                                 |
| [<span data-ttu-id="b0eac-125">**GetTransAtTime2**</span><span class="sxs-lookup"><span data-stu-id="b0eac-125">**GetTransAtTime2**</span></span>](iamtimelinetransable-gettransattime2.md) | <span data-ttu-id="b0eac-126">Recupera la transizione più vicina all'ora specificata, specificata come valore **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="b0eac-126">Retrieves the transition nearest to the specified time, given as a **REFTIME** value.</span></span><br/>                                   |
| [<span data-ttu-id="b0eac-127">**TransAdd**</span><span class="sxs-lookup"><span data-stu-id="b0eac-127">**TransAdd**</span></span>](iamtimelinetransable-transadd.md)               | <span data-ttu-id="b0eac-128">Aggiunge una transizione all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b0eac-128">Adds a transition to the object.</span></span><br/>                                                                                        |
| [<span data-ttu-id="b0eac-129">**TransGetCount**</span><span class="sxs-lookup"><span data-stu-id="b0eac-129">**TransGetCount**</span></span>](iamtimelinetransable-transgetcount.md)     | <span data-ttu-id="b0eac-130">Recupera il numero di transizioni in questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="b0eac-130">Retrieves the number of transitions on this object.</span></span><br/>                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="b0eac-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="b0eac-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b0eac-132">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="b0eac-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b0eac-133">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b0eac-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b0eac-134">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b0eac-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b0eac-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0eac-135">Requirements</span></span>



| <span data-ttu-id="b0eac-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0eac-136">Requirement</span></span> | <span data-ttu-id="b0eac-137">Valore</span><span class="sxs-lookup"><span data-stu-id="b0eac-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0eac-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b0eac-138">Header</span></span><br/>  | <dl> <span data-ttu-id="b0eac-139"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0eac-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b0eac-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="b0eac-140">Library</span></span><br/> | <dl> <span data-ttu-id="b0eac-141"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0eac-141"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
