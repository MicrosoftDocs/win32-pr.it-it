---
title: Evento External. OnSendMessageComplete
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | Evento External. OnSendMessageComplete
ms.assetid: 9ae60aa5-4ecd-41dd-aeb0-afb1a3686982
keywords:
- Media Player di Windows dell'evento External. OnSendMessageComplete
topic_type:
- apiref
api_name:
- External.OnSendMessageComplete Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05d4de69a753811537f60ae8a3244cfaf012f60d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324558"
---
# <a name="externalonsendmessagecomplete-event"></a><span data-ttu-id="ae1d1-105">Evento External. OnSendMessageComplete</span><span class="sxs-lookup"><span data-stu-id="ae1d1-105">External.OnSendMessageComplete Event</span></span>

> [!Note]  
> <span data-ttu-id="ae1d1-106">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="ae1d1-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="ae1d1-107">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ae1d1-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="ae1d1-108">L'evento **OnSendMessageComplete** si verifica al termine dell'elaborazione di un messaggio da parte del negozio online.</span><span class="sxs-lookup"><span data-stu-id="ae1d1-108">The **OnSendMessageComplete** event occurs when the online store has finished processing a message.</span></span> <span data-ttu-id="ae1d1-109">Script nella pagina di individuazione ha inviato in precedenza il messaggio chiamando [External. SendMessage](external-sendmessage.md).</span><span class="sxs-lookup"><span data-stu-id="ae1d1-109">Script on the discovery page previously sent the message by calling [External.sendMessage](external-sendmessage.md).</span></span>

``` syntax
window.external.OnSendMessageComplete = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="ae1d1-110">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="ae1d1-110">Possible Values</span></span>

<span data-ttu-id="ae1d1-111">Si tratta di una proprietà di sola scrittura che specifica il nome della funzione nello script che Windows Media Player chiama quando si verifica l'evento.</span><span class="sxs-lookup"><span data-stu-id="ae1d1-111">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="ae1d1-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae1d1-112">Parameters</span></span>

<span data-ttu-id="ae1d1-113">La funzione che gestisce questo evento presenta i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="ae1d1-113">The function that handles this event has the following parameters.</span></span>

<dl> <dt>

<span data-ttu-id="ae1d1-114"><span id="Msg"></span><span id="msg"></span><span id="MSG"></span>*Messaggio*</span><span class="sxs-lookup"><span data-stu-id="ae1d1-114"><span id="Msg"></span><span id="msg"></span><span id="MSG"></span>*Msg*</span></span>
</dt> <dd>

<span data-ttu-id="ae1d1-115">La stessa stringa passata nel parametro **msg** di **SendMessage**.</span><span class="sxs-lookup"><span data-stu-id="ae1d1-115">The same string that was passed in the **Msg** parameter of **sendMessage**.</span></span>

</dd> <dt>

<span data-ttu-id="ae1d1-116"><span id="Param"></span><span id="param"></span><span id="PARAM"></span>*Param*</span><span class="sxs-lookup"><span data-stu-id="ae1d1-116"><span id="Param"></span><span id="param"></span><span id="PARAM"></span>*Param*</span></span>
</dt> <dd>

<span data-ttu-id="ae1d1-117">La stessa stringa passata nel parametro **param** di **SendMessage**.</span><span class="sxs-lookup"><span data-stu-id="ae1d1-117">The same string that was passed in the **Param** parameter of **sendMessage**.</span></span>

</dd> <dt>

<span data-ttu-id="ae1d1-118"><span id="Result"></span><span id="result"></span><span id="RESULT"></span>*Risultato*</span><span class="sxs-lookup"><span data-stu-id="ae1d1-118"><span id="Result"></span><span id="result"></span><span id="RESULT"></span>*Result*</span></span>
</dt> <dd>

<span data-ttu-id="ae1d1-119">**Stringa** che contiene il risultato della gestione dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="ae1d1-119">**String** that contains the result of the message handling.</span></span> <span data-ttu-id="ae1d1-120">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="ae1d1-120">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae1d1-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae1d1-121">Remarks</span></span>

<span data-ttu-id="ae1d1-122">Il metodo **SendMessage** chiama [IWMPContentPartner:: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage), che restituisce in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="ae1d1-122">The **sendMessage** method calls [IWMPContentPartner::SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage), which returns asynchronously.</span></span> <span data-ttu-id="ae1d1-123">Ovvero, viene restituito prima del completamento dell'elaborazione del messaggio da parte del negozio online.</span><span class="sxs-lookup"><span data-stu-id="ae1d1-123">That is, it returns before the online store finishes processing the message.</span></span> <span data-ttu-id="ae1d1-124">Al termine dell'elaborazione del messaggio da parte del negozio online, viene chiamato [IWMPContentPartnerCallback:: SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete), che a sua volta chiama il gestore dell'evento **OnSendMessageComplete** dello script.</span><span class="sxs-lookup"><span data-stu-id="ae1d1-124">When the online store finishes processing the message, it calls [IWMPContentPartnerCallback::SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete), which in turn calls the script's **OnSendMessageComplete** event handler.</span></span>

<span data-ttu-id="ae1d1-125">Quando l'archivio online chiama **IWMPContentPartnerCallback:: SendMessageComplete**, fornisce un codice risultato nel parametro *bstrResult* .</span><span class="sxs-lookup"><span data-stu-id="ae1d1-125">When the online store calls **IWMPContentPartnerCallback::SendMessageComplete**, it supplies a result code in the *bstrResult* parameter.</span></span> <span data-ttu-id="ae1d1-126">Windows Media Player non interpreta il codice risultante.</span><span class="sxs-lookup"><span data-stu-id="ae1d1-126">Windows Media Player does not interpret that result code.</span></span> <span data-ttu-id="ae1d1-127">Al contrario, Windows Media Player passa il codice risultato insieme al gestore eventi **OnSendMessageComplete** nel parametro *result* .</span><span class="sxs-lookup"><span data-stu-id="ae1d1-127">Instead, Windows Media Player passes the result code along to the **OnSendMessageComplete** event handler in the *Result* parameter.</span></span>

<span data-ttu-id="ae1d1-128">Nessuno dei parametri (*msg*, *param*, *result*) del gestore dell'evento **OnSendMessageComplete** viene interpretato da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="ae1d1-128">None of the parameters (*Msg*, *Param*, *Result*) of the **OnSendMessageComplete** event handler is interpreted by Windows Media Player.</span></span> <span data-ttu-id="ae1d1-129">I parametri hanno un significato solo per il negozio online.</span><span class="sxs-lookup"><span data-stu-id="ae1d1-129">The parameters have meaning only to the online store.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae1d1-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae1d1-130">Requirements</span></span>



| <span data-ttu-id="ae1d1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae1d1-131">Requirement</span></span> | <span data-ttu-id="ae1d1-132">Valore</span><span class="sxs-lookup"><span data-stu-id="ae1d1-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ae1d1-133">Versione</span><span class="sxs-lookup"><span data-stu-id="ae1d1-133">Version</span></span><br/> | <span data-ttu-id="ae1d1-134">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="ae1d1-134">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="ae1d1-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ae1d1-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="ae1d1-136"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae1d1-136"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae1d1-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae1d1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae1d1-138">**Oggetto esterno per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="ae1d1-138">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="ae1d1-139">**SendMessage esterno**</span><span class="sxs-lookup"><span data-stu-id="ae1d1-139">**External.sendMessage**</span></span>](external-sendmessage.md)
</dt> <dt>

[<span data-ttu-id="ae1d1-140">**IWMPContentPartner:: SendMessage**</span><span class="sxs-lookup"><span data-stu-id="ae1d1-140">**IWMPContentPartner::SendMessage**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[<span data-ttu-id="ae1d1-141">**IWMPContentPartnerCallback::SendMessageComplete**</span><span class="sxs-lookup"><span data-stu-id="ae1d1-141">**IWMPContentPartnerCallback::SendMessageComplete**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





