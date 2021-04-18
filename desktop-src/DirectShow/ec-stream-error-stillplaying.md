---
description: Si è verificato un errore in un flusso, ma il flusso è ancora in riproduzione.
ms.assetid: ff155c01-22ba-46dd-85b8-05eabf956908
title: EC_STREAM_ERROR_STILLPLAYING (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db74a9f16a0ca01ce74e6d94df50cc402221aaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327114"
---
# <a name="ec_stream_error_stillplaying"></a><span data-ttu-id="203d6-103">\_errore di flusso EC \_ \_ STILLPLAYING</span><span class="sxs-lookup"><span data-stu-id="203d6-103">EC\_STREAM\_ERROR\_STILLPLAYING</span></span>

<span data-ttu-id="203d6-104">Si è verificato un errore in un flusso, ma il flusso è ancora in riproduzione.</span><span class="sxs-lookup"><span data-stu-id="203d6-104">An error occurred in a stream, but the stream is still playing.</span></span>

## <a name="parameters"></a><span data-ttu-id="203d6-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="203d6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="203d6-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="203d6-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="203d6-107">(**HRESULT**) Codice di errore dell'operazione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="203d6-107">(**HRESULT**) Failure code of the operation that failed.</span></span>

</dd> <dt>

<span data-ttu-id="203d6-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="203d6-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="203d6-109">(**DWORD**) Codice di errore secondario.</span><span class="sxs-lookup"><span data-stu-id="203d6-109">(**DWORD**) Minor error code.</span></span> <span data-ttu-id="203d6-110">Questo valore è in genere pari a zero.</span><span class="sxs-lookup"><span data-stu-id="203d6-110">This value is usually zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="203d6-111">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="203d6-111">Default Action</span></span>

<span data-ttu-id="203d6-112">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="203d6-112">None.</span></span> <span data-ttu-id="203d6-113">L'applicazione deve decidere se arrestare il grafo.</span><span class="sxs-lookup"><span data-stu-id="203d6-113">The application must decide whether to stop the graph.</span></span>

## <a name="requirements"></a><span data-ttu-id="203d6-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="203d6-114">Requirements</span></span>



| <span data-ttu-id="203d6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="203d6-115">Requirement</span></span> | <span data-ttu-id="203d6-116">Valore</span><span class="sxs-lookup"><span data-stu-id="203d6-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="203d6-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="203d6-117">Header</span></span><br/> | <dl> <span data-ttu-id="203d6-118"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="203d6-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="203d6-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="203d6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="203d6-120">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="203d6-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="203d6-121">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="203d6-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




