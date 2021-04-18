---
description: L'interfaccia IAMTimelineVirtualTrack fornisce metodi per l'uso di tracce virtuali in servizi di modifica DirectShow (DES). Le composizioni e le tracce supportano questa interfaccia.
ms.assetid: 69d1d2ea-d33f-406d-a9ca-ddfb890bed34
title: Interfaccia IAMTimelineVirtualTrack (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineVirtualTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2295f1c336270818242f0d992a369e6a66f9237a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327424"
---
# <a name="iamtimelinevirtualtrack-interface"></a><span data-ttu-id="61327-104">Interfaccia IAMTimelineVirtualTrack</span><span class="sxs-lookup"><span data-stu-id="61327-104">IAMTimelineVirtualTrack interface</span></span>

> [!Note]  
> <span data-ttu-id="61327-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="61327-105">\[Deprecated.</span></span> <span data-ttu-id="61327-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="61327-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="61327-107">L' `IAMTimelineVirtualTrack` interfaccia fornisce metodi per l'utilizzo di tracce virtuali in [servizi di modifica DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="61327-107">The `IAMTimelineVirtualTrack` interface provides methods for working with virtual tracks in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="61327-108">Le composizioni e le tracce supportano questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="61327-108">Compositions and tracks support this interface.</span></span>

## <a name="members"></a><span data-ttu-id="61327-109">Membri</span><span class="sxs-lookup"><span data-stu-id="61327-109">Members</span></span>

<span data-ttu-id="61327-110">L'interfaccia **IAMTimelineVirtualTrack** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="61327-110">The **IAMTimelineVirtualTrack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="61327-111">**IAMTimelineVirtualTrack** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="61327-111">**IAMTimelineVirtualTrack** also has these types of members:</span></span>

-   [<span data-ttu-id="61327-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="61327-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="61327-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="61327-113">Methods</span></span>

<span data-ttu-id="61327-114">L'interfaccia **IAMTimelineVirtualTrack** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="61327-114">The **IAMTimelineVirtualTrack** interface has these methods.</span></span>



| <span data-ttu-id="61327-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="61327-115">Method</span></span>                                                               | <span data-ttu-id="61327-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61327-116">Description</span></span>                                       |
|:---------------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="61327-117">**SetTrackDirty**</span><span class="sxs-lookup"><span data-stu-id="61327-117">**SetTrackDirty**</span></span>](iamtimelinevirtualtrack-settrackdirty.md)       | <span data-ttu-id="61327-118">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="61327-118">Not supported.</span></span><br/>                         |
| [<span data-ttu-id="61327-119">**TrackGetPriority**</span><span class="sxs-lookup"><span data-stu-id="61327-119">**TrackGetPriority**</span></span>](iamtimelinevirtualtrack-trackgetpriority.md) | <span data-ttu-id="61327-120">Recupera il livello di priorità dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="61327-120">Retrieves the object's priority level.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="61327-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="61327-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="61327-122">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="61327-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="61327-123">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="61327-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="61327-124">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="61327-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="61327-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61327-125">Requirements</span></span>



| <span data-ttu-id="61327-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="61327-126">Requirement</span></span> | <span data-ttu-id="61327-127">Valore</span><span class="sxs-lookup"><span data-stu-id="61327-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61327-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="61327-128">Header</span></span><br/>  | <dl> <span data-ttu-id="61327-129"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="61327-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="61327-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="61327-130">Library</span></span><br/> | <dl> <span data-ttu-id="61327-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="61327-131"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
