---
description: È stato applicato un comando di interruzione del controllo del flusso.
ms.assetid: a2f7a959-fafd-47ff-9b3d-1a898fdb1f81
title: EC_STREAM_CONTROL_STOPPED (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8c5488ba400d90623955c3e9adcba0dde07e04a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327115"
---
# <a name="ec_stream_control_stopped"></a><span data-ttu-id="a5849-103">\_controllo flusso \_ EC \_ arrestato</span><span class="sxs-lookup"><span data-stu-id="a5849-103">EC\_STREAM\_CONTROL\_STOPPED</span></span>

<span data-ttu-id="a5849-104">È stato applicato un comando di interruzione del controllo del flusso.</span><span class="sxs-lookup"><span data-stu-id="a5849-104">A stream-control stop command has taken effect.</span></span>

## <a name="parameters"></a><span data-ttu-id="a5849-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="a5849-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5849-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*</span><span class="sxs-lookup"><span data-stu-id="a5849-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*</span></span>
</dt> <dd>

<span data-ttu-id="a5849-107">(**IUnknown** \* ) Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN che ha interrotto il flusso.</span><span class="sxs-lookup"><span data-stu-id="a5849-107">(**IUnknown**\*) Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the pin that stopped the stream.</span></span>

</dd> <dt>

<span data-ttu-id="a5849-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*</span><span class="sxs-lookup"><span data-stu-id="a5849-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*</span></span>
</dt> <dd>

<span data-ttu-id="a5849-109">(**DWORD**) Valore definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a5849-109">(**DWORD**) User-defined value.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="a5849-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="a5849-110">Default Action</span></span>

<span data-ttu-id="a5849-111">No.</span><span class="sxs-lookup"><span data-stu-id="a5849-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5849-112">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="a5849-112">Remarks</span></span>

<span data-ttu-id="a5849-113">I filtri inviano questo evento in risposta al metodo [**IAMStreamControl:: STOPAT**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .</span><span class="sxs-lookup"><span data-stu-id="a5849-113">Filters send this event in response to the [**IAMStreamControl::StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) method.</span></span> <span data-ttu-id="a5849-114">Il metodo **STOPAT** specifica un'ora di riferimento per l'arresto del flusso da parte di un PIN.</span><span class="sxs-lookup"><span data-stu-id="a5849-114">The **StopAt** method specifies a reference time for a pin to stop streaming.</span></span> <span data-ttu-id="a5849-115">Quando il flusso si interrompe, il filtro Invia questo evento.</span><span class="sxs-lookup"><span data-stu-id="a5849-115">When streaming does halt, the filter sends this event.</span></span>

<span data-ttu-id="a5849-116">Il parametro *pSender* specifica il pin che esegue il comando stop.</span><span class="sxs-lookup"><span data-stu-id="a5849-116">The *pSender* parameter specifies the pin that executes the stop command.</span></span> <span data-ttu-id="a5849-117">A seconda dell'implementazione, potrebbe non corrispondere al pin che ha ricevuto la chiamata [**STOPAT**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .</span><span class="sxs-lookup"><span data-stu-id="a5849-117">Depending on the implementation, it might not be the pin that received the [**StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) call.</span></span>

<span data-ttu-id="a5849-118">Il parametro *dwCookie* viene specificato dall'applicazione nel metodo [**STOPAT**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .</span><span class="sxs-lookup"><span data-stu-id="a5849-118">The *dwCookie* parameter is specified by the application in the [**StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) method.</span></span> <span data-ttu-id="a5849-119">Questo parametro consente all'applicazione di tenere traccia di più chiamate al metodo.</span><span class="sxs-lookup"><span data-stu-id="a5849-119">This parameter enables the application to track multiple calls to the method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5849-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5849-120">Requirements</span></span>



| <span data-ttu-id="a5849-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5849-121">Requirement</span></span> | <span data-ttu-id="a5849-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a5849-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a5849-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a5849-123">Header</span></span><br/> | <dl> <span data-ttu-id="a5849-124"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5849-124"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5849-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a5849-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5849-126">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="a5849-126">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="a5849-127">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="a5849-127">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




