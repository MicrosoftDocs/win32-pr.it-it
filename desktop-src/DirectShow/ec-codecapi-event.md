---
description: "L' \\_ evento di evento CODEcapite EC \\_ viene inviato da un codificatore per segnalare un evento di codifica. Il client esegue la registrazione per l'evento del codificatore chiamando il metodo ICodecAPI:: RegisterForEvent."
ms.assetid: 88924ba9-707b-41a7-9bca-c630b4a9c4c8
title: EC_CODECAPI_EVENT (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c24ece20a0c729b251c56b50b5b44fc9f7fa98f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328463"
---
# <a name="ec_codecapi_event"></a><span data-ttu-id="c631c-104">\_evento CODEcapite EC \_</span><span class="sxs-lookup"><span data-stu-id="c631c-104">EC\_CODECAPI\_EVENT</span></span>

<span data-ttu-id="c631c-105">L' \_ evento di evento CODEcapite EC \_ viene inviato da un codificatore per segnalare un evento di codifica.</span><span class="sxs-lookup"><span data-stu-id="c631c-105">The EC\_CODECAPI\_EVENT event is sent by an encoder to signal an encoding event.</span></span> <span data-ttu-id="c631c-106">Il client esegue la registrazione per l'evento del codificatore chiamando il metodo [**ICodecAPI:: RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) .</span><span class="sxs-lookup"><span data-stu-id="c631c-106">The client registers for encoder event by calling the [**ICodecAPI::RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) method.</span></span>

## <a name="parameters"></a><span data-ttu-id="c631c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c631c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c631c-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="c631c-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="c631c-109">Dati utente.</span><span class="sxs-lookup"><span data-stu-id="c631c-109">User data.</span></span> <span data-ttu-id="c631c-110">Il valore di questo parametro è il puntatore specificato dal chiamante nel parametro *UserData* del metodo [**RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) .</span><span class="sxs-lookup"><span data-stu-id="c631c-110">The value of this parameter is the pointer that the caller specified in the *userData* parameter of the [**RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) method.</span></span>

</dd> <dt>

<span data-ttu-id="c631c-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="c631c-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="c631c-112">Puntatore ai dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="c631c-112">Pointer to the event data.</span></span> <span data-ttu-id="c631c-113">Questi dati vengono allocati dal codificatore e devono essere liberati dall'applicazione mediante la funzione **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="c631c-113">This data is allocated by the encoder and must be freed by the application, using the **CoTaskMemFree** function.</span></span> <span data-ttu-id="c631c-114">Il blocco di dati inizia con una struttura [**CodecAPIEventData**](/windows/desktop/api/strmif/ns-strmif-codecapieventdata) ; eseguire il cast del parametro *lParam2* a un puntatore a questa struttura.</span><span class="sxs-lookup"><span data-stu-id="c631c-114">The data block starts with a [**CodecAPIEventData**](/windows/desktop/api/strmif/ns-strmif-codecapieventdata) structure; cast the *lParam2* parameter to a pointer to this structure.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="c631c-115">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="c631c-115">Default Action</span></span>

<span data-ttu-id="c631c-116">Nessuna azione predefinita.</span><span class="sxs-lookup"><span data-stu-id="c631c-116">No default action.</span></span>

## <a name="requirements"></a><span data-ttu-id="c631c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c631c-117">Requirements</span></span>



| <span data-ttu-id="c631c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c631c-118">Requirement</span></span> | <span data-ttu-id="c631c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c631c-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c631c-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c631c-120">Header</span></span><br/> | <dl> <span data-ttu-id="c631c-121"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="c631c-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c631c-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c631c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c631c-123">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="c631c-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="c631c-124">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="c631c-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




