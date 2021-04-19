---
description: È stato applicato un comando di avvio del controllo di flusso.
ms.assetid: e2f8d9a2-c96c-457c-8a88-7c86d4405928
title: EC_STREAM_CONTROL_STARTED (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 984562fde9001de14067e5865d5583636b264852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326162"
---
# <a name="ec_stream_control_started"></a><span data-ttu-id="bcc02-103">\_controllo flusso \_ EC \_ avviato</span><span class="sxs-lookup"><span data-stu-id="bcc02-103">EC\_STREAM\_CONTROL\_STARTED</span></span>

<span data-ttu-id="bcc02-104">È stato applicato un comando di avvio del controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="bcc02-104">A stream-control start command has taken effect.</span></span>

## <a name="parameters"></a><span data-ttu-id="bcc02-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="bcc02-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcc02-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*</span><span class="sxs-lookup"><span data-stu-id="bcc02-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*</span></span>
</dt> <dd>

<span data-ttu-id="bcc02-107">(**IUnknown** \* ) Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN che ha avviato il flusso.</span><span class="sxs-lookup"><span data-stu-id="bcc02-107">(**IUnknown**\*) Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the pin that started the stream.</span></span>

</dd> <dt>

<span data-ttu-id="bcc02-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*</span><span class="sxs-lookup"><span data-stu-id="bcc02-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*</span></span>
</dt> <dd>

<span data-ttu-id="bcc02-109">(**DWORD**) Valore definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="bcc02-109">(**DWORD**) User-defined value.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="bcc02-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="bcc02-110">Default Action</span></span>

<span data-ttu-id="bcc02-111">No.</span><span class="sxs-lookup"><span data-stu-id="bcc02-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcc02-112">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="bcc02-112">Remarks</span></span>

<span data-ttu-id="bcc02-113">I filtri inviano questo evento in risposta al metodo [**IAMStreamControl:: startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .</span><span class="sxs-lookup"><span data-stu-id="bcc02-113">Filters send this event in response to the [**IAMStreamControl::StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) method.</span></span> <span data-ttu-id="bcc02-114">Questo metodo specifica un'ora di riferimento per avviare lo streaming di un PIN.</span><span class="sxs-lookup"><span data-stu-id="bcc02-114">This method specifies a reference time for a pin to begin streaming.</span></span> <span data-ttu-id="bcc02-115">Quando il flusso inizia, il filtro Invia questo evento.</span><span class="sxs-lookup"><span data-stu-id="bcc02-115">When streaming does begin, the filter sends this event.</span></span>

<span data-ttu-id="bcc02-116">Il parametro *pSender* specifica il pin che esegue il comando di avvio.</span><span class="sxs-lookup"><span data-stu-id="bcc02-116">The *pSender* parameter specifies the pin that executes the start command.</span></span> <span data-ttu-id="bcc02-117">A seconda dell'implementazione, potrebbe non corrispondere al pin che ha ricevuto la chiamata [**startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .</span><span class="sxs-lookup"><span data-stu-id="bcc02-117">Depending on the implementation, it might not be the pin that received the [**StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) call.</span></span>

<span data-ttu-id="bcc02-118">Il parametro *dwCookie* viene specificato dall'applicazione nel metodo [**startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .</span><span class="sxs-lookup"><span data-stu-id="bcc02-118">The *dwCookie* parameter is specified by the application in the [**StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) method.</span></span> <span data-ttu-id="bcc02-119">Questo parametro consente all'applicazione di tenere traccia di più chiamate al metodo.</span><span class="sxs-lookup"><span data-stu-id="bcc02-119">This parameter enables the application to track multiple calls to the method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcc02-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bcc02-120">Requirements</span></span>



| <span data-ttu-id="bcc02-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcc02-121">Requirement</span></span> | <span data-ttu-id="bcc02-122">Valore</span><span class="sxs-lookup"><span data-stu-id="bcc02-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bcc02-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bcc02-123">Header</span></span><br/> | <dl> <span data-ttu-id="bcc02-124"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcc02-124"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcc02-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bcc02-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcc02-126">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="bcc02-126">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="bcc02-127">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="bcc02-127">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




