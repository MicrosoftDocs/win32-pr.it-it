---
description: Notifica all'applicazione lo stato di avanzamento all'apertura di un file di rete.
ms.assetid: 022b87e5-76af-4253-9485-97140f294938
title: EC_LOADSTATUS (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc06022a9774d851cabff6a18c0f8808f62f14f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332204"
---
# <a name="ec_loadstatus"></a><span data-ttu-id="6b60d-103">\_LOADSTATUS EC</span><span class="sxs-lookup"><span data-stu-id="6b60d-103">EC\_LOADSTATUS</span></span>

<span data-ttu-id="6b60d-104">Notifica all'applicazione lo stato di avanzamento all'apertura di un file di rete.</span><span class="sxs-lookup"><span data-stu-id="6b60d-104">Notifies the application of progress when opening a network file.</span></span>

## <a name="parameters"></a><span data-ttu-id="6b60d-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b60d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b60d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="6b60d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="6b60d-107">Codice di stato.</span><span class="sxs-lookup"><span data-stu-id="6b60d-107">Status code.</span></span> <span data-ttu-id="6b60d-108">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="6b60d-108">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6b60d-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="6b60d-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="6b60d-110">Zero.</span><span class="sxs-lookup"><span data-stu-id="6b60d-110">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="6b60d-111">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="6b60d-111">Default Action</span></span>

<span data-ttu-id="6b60d-112">No.</span><span class="sxs-lookup"><span data-stu-id="6b60d-112">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b60d-113">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="6b60d-113">Remarks</span></span>

<span data-ttu-id="6b60d-114">Il filtro [WM ASF Reader](wm-asf-reader-filter.md) e il filtro legacy [Windows Media Source](windows-media-source-filter.md) inviano questo evento.</span><span class="sxs-lookup"><span data-stu-id="6b60d-114">The [WM ASF Reader](wm-asf-reader-filter.md) filter and the legacy [Windows Media Source](windows-media-source-filter.md) filter send this event.</span></span> <span data-ttu-id="6b60d-115">Il primo parametro dell'evento ha uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6b60d-115">The first event parameter has one of the following values.</span></span>



| <span data-ttu-id="6b60d-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6b60d-116">Value</span></span>                        | <span data-ttu-id="6b60d-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b60d-117">Description</span></span>                                    |
|------------------------------|------------------------------------------------|
| <span data-ttu-id="6b60d-118">AM \_ LOADSTATUS \_ chiuso</span><span class="sxs-lookup"><span data-stu-id="6b60d-118">AM\_LOADSTATUS\_CLOSED</span></span>       | <span data-ttu-id="6b60d-119">Il filtro di origine ha chiuso il file.</span><span class="sxs-lookup"><span data-stu-id="6b60d-119">The source filter has closed the file.</span></span>         |
| <span data-ttu-id="6b60d-120">\_connessione LOADSTATUS \_</span><span class="sxs-lookup"><span data-stu-id="6b60d-120">AM\_LOADSTATUS\_CONNECTING</span></span>   | <span data-ttu-id="6b60d-121">Il filtro di origine si connette al server.</span><span class="sxs-lookup"><span data-stu-id="6b60d-121">The source filter is connecting to the server.</span></span> |
| <span data-ttu-id="6b60d-122">\_LOADINGDESCR LOADSTATUS \_</span><span class="sxs-lookup"><span data-stu-id="6b60d-122">AM\_LOADSTATUS\_LOADINGDESCR</span></span> | <span data-ttu-id="6b60d-123">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6b60d-123">Not used.</span></span>                                      |
| <span data-ttu-id="6b60d-124">\_LOADINGMCAST LOADSTATUS \_</span><span class="sxs-lookup"><span data-stu-id="6b60d-124">AM\_LOADSTATUS\_LOADINGMCAST</span></span> | <span data-ttu-id="6b60d-125">Non usato</span><span class="sxs-lookup"><span data-stu-id="6b60d-125">Not used</span></span>                                       |
| <span data-ttu-id="6b60d-126">\_individuazione LOADSTATUS \_</span><span class="sxs-lookup"><span data-stu-id="6b60d-126">AM\_LOADSTATUS\_LOCATING</span></span>     | <span data-ttu-id="6b60d-127">Il filtro di origine sta individuando i dati richiesti.</span><span class="sxs-lookup"><span data-stu-id="6b60d-127">The source filter is locating requested data.</span></span>  |
| <span data-ttu-id="6b60d-128">AM \_ LOADSTATUS \_ aperto</span><span class="sxs-lookup"><span data-stu-id="6b60d-128">AM\_LOADSTATUS\_OPEN</span></span>         | <span data-ttu-id="6b60d-129">Il filtro di origine ha aperto il file.</span><span class="sxs-lookup"><span data-stu-id="6b60d-129">The source filter has opened the file.</span></span>         |
| <span data-ttu-id="6b60d-130">\_apertura LOADSTATUS \_</span><span class="sxs-lookup"><span data-stu-id="6b60d-130">AM\_LOADSTATUS\_OPENING</span></span>      | <span data-ttu-id="6b60d-131">Il filtro di origine sta aprendo il file.</span><span class="sxs-lookup"><span data-stu-id="6b60d-131">The source filter is opening the file.</span></span>         |



 

## <a name="requirements"></a><span data-ttu-id="6b60d-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b60d-132">Requirements</span></span>



| <span data-ttu-id="6b60d-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b60d-133">Requirement</span></span> | <span data-ttu-id="6b60d-134">Valore</span><span class="sxs-lookup"><span data-stu-id="6b60d-134">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6b60d-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b60d-135">Header</span></span><br/> | <dl> <span data-ttu-id="6b60d-136"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b60d-136"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b60d-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b60d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b60d-138">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="6b60d-138">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="6b60d-139">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="6b60d-139">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




