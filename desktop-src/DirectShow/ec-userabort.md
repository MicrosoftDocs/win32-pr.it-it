---
description: L'utente ha terminato la riproduzione.
ms.assetid: 974a9c3e-cfc9-4608-9f98-732aeaa0a752
title: EC_USERABORT (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bab4f76e90d7e5f51655eda6dc72834053df87b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328335"
---
# <a name="ec_userabort"></a><span data-ttu-id="11040-103">\_USERABORT EC</span><span class="sxs-lookup"><span data-stu-id="11040-103">EC\_USERABORT</span></span>

<span data-ttu-id="11040-104">L'utente ha terminato la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="11040-104">The user has terminated playback.</span></span>

## <a name="parameters"></a><span data-ttu-id="11040-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="11040-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11040-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="11040-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="11040-107">Zero.</span><span class="sxs-lookup"><span data-stu-id="11040-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="11040-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="11040-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="11040-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="11040-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="11040-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="11040-110">Default Action</span></span>

<span data-ttu-id="11040-111">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="11040-111">None.</span></span> <span data-ttu-id="11040-112">L'applicazione deve decidere se arrestare il grafo.</span><span class="sxs-lookup"><span data-stu-id="11040-112">The application must decide whether to stop the graph.</span></span>

## <a name="remarks"></a><span data-ttu-id="11040-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="11040-113">Remarks</span></span>

<span data-ttu-id="11040-114">Questo codice di evento segnala che l'utente ha terminato la riproduzione normale dei grafici.</span><span class="sxs-lookup"><span data-stu-id="11040-114">This event code signals that the user has terminated normal graph playback.</span></span> <span data-ttu-id="11040-115">Ad esempio, i renderer video inviano questo evento se l'utente chiude la finestra del video.</span><span class="sxs-lookup"><span data-stu-id="11040-115">For example, video renderers send this event if the user closes the video window.</span></span>

<span data-ttu-id="11040-116">Dopo l'invio di questo evento, il filtro deve rifiutare tutti gli esempi e non inviare alcun evento di [**\_ ridisegno EC**](ec-repaint.md) , fino a quando il filtro non viene interrotto e non viene reimpostato.</span><span class="sxs-lookup"><span data-stu-id="11040-116">After sending this event, the filter should reject all samples and not send any [**EC\_REPAINT**](ec-repaint.md) events, until the filter stops and is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="11040-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11040-117">Requirements</span></span>



| <span data-ttu-id="11040-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="11040-118">Requirement</span></span> | <span data-ttu-id="11040-119">Valore</span><span class="sxs-lookup"><span data-stu-id="11040-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="11040-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11040-120">Header</span></span><br/> | <dl> <span data-ttu-id="11040-121"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="11040-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11040-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11040-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11040-123">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="11040-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="11040-124">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="11040-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




