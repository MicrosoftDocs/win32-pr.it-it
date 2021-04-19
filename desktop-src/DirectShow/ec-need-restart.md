---
description: Un filtro richiede che il grafico venga riavviato.
ms.assetid: 58f17338-dd60-4b77-80d3-b6b6a76af9b2
title: EC_NEED_RESTART (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9651ae51b8dd8969a95b4f5e9d5093ec2e879f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324168"
---
# <a name="ec_need_restart"></a><span data-ttu-id="a56b7-103">EC \_ necessario \_ riavvio</span><span class="sxs-lookup"><span data-stu-id="a56b7-103">EC\_NEED\_RESTART</span></span>

<span data-ttu-id="a56b7-104">Un filtro richiede che il grafico venga riavviato.</span><span class="sxs-lookup"><span data-stu-id="a56b7-104">A filter is requesting that the graph be restarted.</span></span>

## <a name="parameters"></a><span data-ttu-id="a56b7-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="a56b7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a56b7-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="a56b7-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="a56b7-107">Zero.</span><span class="sxs-lookup"><span data-stu-id="a56b7-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="a56b7-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="a56b7-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a56b7-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="a56b7-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="a56b7-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="a56b7-110">Default Action</span></span>

<span data-ttu-id="a56b7-111">Il gestore del grafico del filtro sospende e riavvia il grafo.</span><span class="sxs-lookup"><span data-stu-id="a56b7-111">The filter graph manager pauses and restarts the graph.</span></span> <span data-ttu-id="a56b7-112">L'evento non viene passato all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a56b7-112">It does not pass the event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="a56b7-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a56b7-113">Remarks</span></span>

<span data-ttu-id="a56b7-114">Se un filtro rifiuta un campione al centro di un flusso, il pin upstream interrompe la distribuzione degli esempi.</span><span class="sxs-lookup"><span data-stu-id="a56b7-114">If a filter rejects a sample in the middle of a stream, the upstream pin will stop delivering samples.</span></span> <span data-ttu-id="a56b7-115">Il filtro può riavviare il flusso inviando questo evento.</span><span class="sxs-lookup"><span data-stu-id="a56b7-115">The filter can restart the stream by sending this event.</span></span> <span data-ttu-id="a56b7-116">Ad esempio, il renderer audio potrebbe perdere l'accesso al dispositivo audio, perché una finestra video ha perso lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="a56b7-116">For example, the audio renderer might lose access to the sound device, because a video window has lost focus.</span></span> <span data-ttu-id="a56b7-117">A questo punto, il renderer audio inizia a rifiutare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="a56b7-117">At that point, the audio renderer starts rejecting samples.</span></span> <span data-ttu-id="a56b7-118">Quando viene riacquisito l'accesso al dispositivo audio, questo evento viene inviato per riavviare il flusso audio.</span><span class="sxs-lookup"><span data-stu-id="a56b7-118">When it regains access to the sound device, it sends this event to restart the audio stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="a56b7-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a56b7-119">Requirements</span></span>



| <span data-ttu-id="a56b7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a56b7-120">Requirement</span></span> | <span data-ttu-id="a56b7-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a56b7-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a56b7-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a56b7-122">Header</span></span><br/> | <dl> <span data-ttu-id="a56b7-123"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="a56b7-123"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a56b7-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a56b7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a56b7-125">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="a56b7-125">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="a56b7-126">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="a56b7-126">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




