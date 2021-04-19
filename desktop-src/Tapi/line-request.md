---
description: Il messaggio di richiesta della linea TAPI \_ viene inviato per segnalare l'arrivo di una nuova richiesta da un'altra applicazione.
ms.assetid: d4dbba0d-8225-48d7-a66b-b189fdae70a8
title: Messaggio di LINE_REQUEST (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23987e370d5ae9c8eeb579780c5659f8075ac865
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326625"
---
# <a name="line_request-message"></a><span data-ttu-id="9b694-103">Messaggio di richiesta di riga \_</span><span class="sxs-lookup"><span data-stu-id="9b694-103">LINE\_REQUEST message</span></span>

<span data-ttu-id="9b694-104">Il messaggio **di \_ richiesta della linea** TAPI viene inviato per segnalare l'arrivo di una nuova richiesta da un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b694-104">The TAPI **LINE\_REQUEST** message is sent to report the arrival of a new request from another application.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="9b694-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="9b694-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b694-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="9b694-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="9b694-107">Non usato.</span><span class="sxs-lookup"><span data-stu-id="9b694-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="9b694-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="9b694-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="9b694-109">Istanza di registrazione dell'applicazione specificata in [**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient).</span><span class="sxs-lookup"><span data-stu-id="9b694-109">The registration instance of the application specified on [**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient).</span></span>

</dd> <dt>

<span data-ttu-id="9b694-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="9b694-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="9b694-111">Modalità di richiesta della richiesta appena in sospeso.</span><span class="sxs-lookup"><span data-stu-id="9b694-111">The request mode of the newly pending request.</span></span> <span data-ttu-id="9b694-112">Questo parametro usa le [**\_ costanti LINEREQUESTMODE**](linerequestmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="9b694-112">This parameter uses the [**LINEREQUESTMODE\_ constants**](linerequestmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b694-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="9b694-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="9b694-114">Le condizioni per questo parametro sono, se *dwParam1* è impostato su LINEREQUESTMODE \_ Drop, *dwParam2* contiene l' *HWND* dell'applicazione che richiede l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="9b694-114">The conditions for this parameter are, if *dwParam1* is set to LINEREQUESTMODE\_DROP, *dwParam2* contains the *hWnd* of the application requesting the drop.</span></span> <span data-ttu-id="9b694-115">In caso contrario, *dwParam2* è inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="9b694-115">Otherwise, *dwParam2* is unused.</span></span>

</dd> <dt>

<span data-ttu-id="9b694-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="9b694-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="9b694-117">Se *dwParam1* è impostato su LINEREQUESTMODE \_ Drop, la parola di ordine inferiore di *dwParam3* contiene il *wRequestID* come specificato dall'applicazione che ha richiesto l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="9b694-117">If *dwParam1* is set to LINEREQUESTMODE\_DROP, the low-order word of *dwParam3* contains the *wRequestID* as specified by the application that requested the drop.</span></span> <span data-ttu-id="9b694-118">In caso contrario, *dwParam3* è inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="9b694-118">Otherwise, *dwParam3* is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b694-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9b694-119">Return value</span></span>

<span data-ttu-id="9b694-120">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="9b694-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b694-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="9b694-121">Remarks</span></span>

<span data-ttu-id="9b694-122">Il messaggio di **\_ richiesta di riga** viene inviato all'applicazione con priorità più elevata registrata per la modalità di richiesta corrispondente.</span><span class="sxs-lookup"><span data-stu-id="9b694-122">The **LINE\_REQUEST** message is sent to the highest priority application that has registered for the corresponding request mode.</span></span> <span data-ttu-id="9b694-123">Questo messaggio indica l'arrivo di una richiesta di telefonia assistita della modalità di richiesta specificata.</span><span class="sxs-lookup"><span data-stu-id="9b694-123">This message indicates the arrival of an Assisted Telephony request of the specified request mode.</span></span> <span data-ttu-id="9b694-124">Se *dwParam1* è LINEREQUESTMODE \_ MAKECALL, l'applicazione può richiamare [**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest) usando la modalità di richiesta corrispondente per ricevere la richiesta.</span><span class="sxs-lookup"><span data-stu-id="9b694-124">If *dwParam1* is LINEREQUESTMODE\_MAKECALL, the application can invoke [**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest) using the corresponding request mode to receive the request.</span></span> <span data-ttu-id="9b694-125">Se *dwParam1* è LINEREQUESTMODE \_ Drop, il messaggio contiene tutti i dati necessari al destinatario della richiesta per eseguire la richiesta.</span><span class="sxs-lookup"><span data-stu-id="9b694-125">If *dwParam1* is LINEREQUESTMODE\_DROP, the message contains all of the data the request recipient requires to perform the request.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b694-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b694-126">Requirements</span></span>



| <span data-ttu-id="9b694-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b694-127">Requirement</span></span> | <span data-ttu-id="9b694-128">Valore</span><span class="sxs-lookup"><span data-stu-id="9b694-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9b694-129">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="9b694-129">TAPI version</span></span><br/> | <span data-ttu-id="9b694-130">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="9b694-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="9b694-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9b694-131">Header</span></span><br/>       | <dl> <span data-ttu-id="9b694-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b694-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b694-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b694-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b694-134">**lineGetRequest**</span><span class="sxs-lookup"><span data-stu-id="9b694-134">**lineGetRequest**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)
</dt> <dt>

[<span data-ttu-id="9b694-135">**lineRegisterRequestRecipient**</span><span class="sxs-lookup"><span data-stu-id="9b694-135">**lineRegisterRequestRecipient**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient)
</dt> <dt>

[<span data-ttu-id="9b694-136">**tapiRequestMakeCall**</span><span class="sxs-lookup"><span data-stu-id="9b694-136">**tapiRequestMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-tapirequestmakecall)
</dt> </dl>

 

 




