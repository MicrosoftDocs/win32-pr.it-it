---
title: Metodo External. sendMessage
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. Il metodo sendMessage Invia un messaggio al plug-in del negozio online.
ms.assetid: 72d34dcc-3284-4446-804f-0fc93a7d8dab
keywords:
- Metodo sendMessage Media Player Windows
- Metodo sendMessage Media Player Windows, classe esterna
- Classe esterna Media Player Windows, metodo sendMessage
topic_type:
- apiref
api_name:
- External.sendMessage
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4648f3cf433a2828d3c97604ebf9ee6e7223b7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328410"
---
# <a name="externalsendmessage-method"></a><span data-ttu-id="02f50-108">Metodo External. sendMessage</span><span class="sxs-lookup"><span data-stu-id="02f50-108">External.sendMessage method</span></span>

> [!Note]  
> <span data-ttu-id="02f50-109">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="02f50-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="02f50-110">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="02f50-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="02f50-111">Il metodo **SendMessage** Invia un messaggio al plug-in del negozio online.</span><span class="sxs-lookup"><span data-stu-id="02f50-111">The **sendMessage** method sends a message to the online store's plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="02f50-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02f50-112">Syntax</span></span>


```JScript
External.sendMessage(
  Msg,
  Param
)
```



## <a name="parameters"></a><span data-ttu-id="02f50-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="02f50-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02f50-114">*Messaggio* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02f50-114">*Msg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02f50-115">**Stringa** che contiene il messaggio.</span><span class="sxs-lookup"><span data-stu-id="02f50-115">**String** containing the message.</span></span>

</dd> <dt>

<span data-ttu-id="02f50-116">*Param* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02f50-116">*Param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02f50-117">**Stringa** contenente i parametri associati al messaggio.</span><span class="sxs-lookup"><span data-stu-id="02f50-117">**String** containing parameters associated with the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02f50-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02f50-118">Return value</span></span>

<span data-ttu-id="02f50-119">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="02f50-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="02f50-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="02f50-120">Remarks</span></span>

<span data-ttu-id="02f50-121">Il messaggio viene inviato in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="02f50-121">The message is sent asynchronously.</span></span> <span data-ttu-id="02f50-122">Questo metodo viene restituito immediatamente anziché attendere l'elaborazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="02f50-122">That is, this method returns immediately rather than waiting for the message to be processed.</span></span> <span data-ttu-id="02f50-123">Al termine dell'elaborazione del messaggio, il plug-in chiama il metodo [IWMPContentPartnerCallback:: SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) , che a sua volta chiama il gestore dell'evento [OnSendMessageComplete](external-onsendmessagecomplete-event.md) dello script.</span><span class="sxs-lookup"><span data-stu-id="02f50-123">When the plug-in finishes processing the message, it calls the [IWMPContentPartnerCallback::SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) method, which in turn calls the script's [OnSendMessageComplete](external-onsendmessagecomplete-event.md) event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="02f50-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02f50-124">Requirements</span></span>



| <span data-ttu-id="02f50-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="02f50-125">Requirement</span></span> | <span data-ttu-id="02f50-126">Valore</span><span class="sxs-lookup"><span data-stu-id="02f50-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="02f50-127">Versione</span><span class="sxs-lookup"><span data-stu-id="02f50-127">Version</span></span><br/> | <span data-ttu-id="02f50-128">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="02f50-128">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="02f50-129">DLL</span><span class="sxs-lookup"><span data-stu-id="02f50-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="02f50-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02f50-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02f50-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02f50-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02f50-132">**Oggetto esterno per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="02f50-132">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="02f50-133">**External. OnSendMessageComplete**</span><span class="sxs-lookup"><span data-stu-id="02f50-133">**External.OnSendMessageComplete**</span></span>](external-onsendmessagecomplete-event.md)
</dt> <dt>

[<span data-ttu-id="02f50-134">**IWMPContentPartner:: SendMessage**</span><span class="sxs-lookup"><span data-stu-id="02f50-134">**IWMPContentPartner::SendMessage**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[<span data-ttu-id="02f50-135">**IWMPContentPartnerCallback::SendMessageComplete**</span><span class="sxs-lookup"><span data-stu-id="02f50-135">**IWMPContentPartnerCallback::SendMessageComplete**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





