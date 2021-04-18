---
description: Inviato quando un'applicazione usa il filtro del writer ASF WM per indicizzare i file di Windows Media Video.
ms.assetid: e5f69aa1-f9b0-4403-acab-25d1f971a876
title: EC_WMT_INDEX_EVENT (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28e10b1d0e4a559bb10fbc521e232d08e08b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327827"
---
# <a name="ec_wmt_index_event-dshowh"></a><span data-ttu-id="b7154-103">EC_WMT_INDEX_EVENT (dshow. h)</span><span class="sxs-lookup"><span data-stu-id="b7154-103">EC_WMT_INDEX_EVENT (Dshow.h)</span></span>

<span data-ttu-id="b7154-104">Inviato quando un'applicazione usa il filtro del [writer ASF WM](wm-asf-writer-filter.md) per indicizzare i file di Windows Media video.</span><span class="sxs-lookup"><span data-stu-id="b7154-104">Sent when an application uses the [WM ASF Writer](wm-asf-writer-filter.md) filter to index Windows Media Video files.</span></span>

## <a name="parameters"></a><span data-ttu-id="b7154-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7154-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7154-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="b7154-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b7154-107">Può essere uno dei seguenti messaggi **di \_ stato di WMT** .</span><span class="sxs-lookup"><span data-stu-id="b7154-107">Can be one of the following **WMT\_STATUS** messages.</span></span>



| <span data-ttu-id="b7154-108">Valore</span><span class="sxs-lookup"><span data-stu-id="b7154-108">Value</span></span>                | <span data-ttu-id="b7154-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7154-109">Description</span></span>              |
|----------------------|--------------------------|
| <span data-ttu-id="b7154-110">WMT \_ avviato</span><span class="sxs-lookup"><span data-stu-id="b7154-110">WMT\_STARTED</span></span>         | <span data-ttu-id="b7154-111">L'indicizzazione è iniziata.</span><span class="sxs-lookup"><span data-stu-id="b7154-111">Indexing has begun.</span></span>      |
| <span data-ttu-id="b7154-112">WMT \_ chiuso</span><span class="sxs-lookup"><span data-stu-id="b7154-112">WMT\_CLOSED</span></span>          | <span data-ttu-id="b7154-113">L'indicizzazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="b7154-113">Indexing has completed.</span></span>  |
| <span data-ttu-id="b7154-114">\_stato dell'indice WMT \_</span><span class="sxs-lookup"><span data-stu-id="b7154-114">WMT\_INDEX\_PROGRESS</span></span> | <span data-ttu-id="b7154-115">L'indicizzazione è in corso.</span><span class="sxs-lookup"><span data-stu-id="b7154-115">Indexing is in progress.</span></span> |



 

</dd> <dt>

<span data-ttu-id="b7154-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="b7154-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b7154-117">Se *lParam1* è WMT \_ Closed o WMT \_ Started, *lParam2* è zero.</span><span class="sxs-lookup"><span data-stu-id="b7154-117">If *lParam1* is WMT\_CLOSED or WMT\_STARTED, then *lParam2* is zero.</span></span> <span data-ttu-id="b7154-118">Se *lParam1* è \_ \_ lo stato di avanzamento dell'indice WMT, *lParam2* è un **valore DWORD** che specifica lo stato di avanzamento corrente come percentuale delle dimensioni totali del download.</span><span class="sxs-lookup"><span data-stu-id="b7154-118">If *lParam1* is WMT\_INDEX\_PROGRESS, then *lParam2* is a **DWORD** that specifies the current progress as a percentage of the total download size.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7154-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7154-119">Requirements</span></span>



| <span data-ttu-id="b7154-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7154-120">Requirement</span></span> | <span data-ttu-id="b7154-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b7154-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b7154-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7154-122">Header</span></span><br/> | <dl> <span data-ttu-id="b7154-123"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7154-123"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7154-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7154-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7154-125">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="b7154-125">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="b7154-126">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="b7154-126">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




