---
title: Evento External. OnLoginChange
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | Evento External. OnLoginChange
ms.assetid: 096794d5-977a-414f-8a98-b7998674c268
keywords:
- Media Player di Windows dell'evento External. OnLoginChange
topic_type:
- apiref
api_name:
- External.OnLoginChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b7d54da86ffdde896a44580567b0cd381725d5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324559"
---
# <a name="externalonloginchange-event"></a><span data-ttu-id="3b095-105">Evento External. OnLoginChange</span><span class="sxs-lookup"><span data-stu-id="3b095-105">External.OnLoginChange Event</span></span>

> [!Note]  
> <span data-ttu-id="3b095-106">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="3b095-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="3b095-107">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3b095-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="3b095-108">L'evento **OnLoginChange** si verifica quando lo stato di accesso dell'utente cambia o quando un tentativo di accesso ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="3b095-108">The **OnLoginChange** event occurs when the user's log-in status changes or when an attempt to log in fails.</span></span>

``` syntax
window.external.OnLoginChange = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="3b095-109">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="3b095-109">Possible Values</span></span>

<span data-ttu-id="3b095-110">Si tratta di una proprietà di sola scrittura che specifica il nome della funzione nello script che Windows Media Player chiama quando si verifica l'evento.</span><span class="sxs-lookup"><span data-stu-id="3b095-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="3b095-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="3b095-111">Parameters</span></span>

<span data-ttu-id="3b095-112">La funzione che gestisce questo evento non accetta parametri.</span><span class="sxs-lookup"><span data-stu-id="3b095-112">The function that handles this event takes no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b095-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b095-113">Remarks</span></span>

<span data-ttu-id="3b095-114">Questo evento si verifica ogni volta che il plug-in Online Store chiama [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passando wmpcnLoginStateChange nel parametro di *tipo* .</span><span class="sxs-lookup"><span data-stu-id="3b095-114">This event occurs every time the online store's plug-in calls [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passing wmpcnLoginStateChange in the *type* parameter.</span></span> <span data-ttu-id="3b095-115">A volte il plug-in effettua questa chiamata per notificare a Windows Media Player che si è verificata una modifica nello stato di accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3b095-115">Sometimes the plug-in makes this call to notify Windows Media Player that there was a change in the user's log-in state.</span></span> <span data-ttu-id="3b095-116">In altri casi, il plug-in effettua questa chiamata per notificare al lettore che un tentativo di accesso non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="3b095-116">Other times, the plug-in makes this call to notify the Player that an attempt to log in failed.</span></span> <span data-ttu-id="3b095-117">Il parametro *pContext* del metodo **Notify** specifica se la notifica è relativa a una modifica dello stato di accesso o a un tentativo di accesso non riuscito.</span><span class="sxs-lookup"><span data-stu-id="3b095-117">The *pContext* parameter of the **Notify** method specifies whether the notification is for a change of log-in state or for a failed log-in attempt.</span></span>

<span data-ttu-id="3b095-118">Poiché ogni chiamata a `Notify(wmpcnLoginStateChange, ...)` fa in modo che Windows Media Player generi l'evento **OnLoginChange** , il gestore eventi **OnLoginChange** viene chiamato a volte come il risultato di una modifica nello stato di accesso e talvolta come il risultato di un tentativo di accesso non riuscito.</span><span class="sxs-lookup"><span data-stu-id="3b095-118">Because every call to `Notify(wmpcnLoginStateChange, ...)` causes Windows Media Player to raise the **OnLoginChange** event, the **OnLoginChange** event handler is called sometimes as the result of a change in log-in state and sometimes as the result of a failed log-in attempt.</span></span> <span data-ttu-id="3b095-119">Per determinare lo stato di accesso corrente dell'utente, è necessario che il gestore dell'evento **OnLoginChange** chiami [External. userLoggedIn](external-userloggedin.md).</span><span class="sxs-lookup"><span data-stu-id="3b095-119">To determine the user's current log-in state, the **OnLoginChange** event handler must call [External.userLoggedIn](external-userloggedin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b095-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b095-120">Requirements</span></span>



| <span data-ttu-id="3b095-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b095-121">Requirement</span></span> | <span data-ttu-id="3b095-122">Valore</span><span class="sxs-lookup"><span data-stu-id="3b095-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3b095-123">Versione</span><span class="sxs-lookup"><span data-stu-id="3b095-123">Version</span></span><br/> | <span data-ttu-id="3b095-124">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="3b095-124">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="3b095-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3b095-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="3b095-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b095-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b095-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b095-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b095-128">**Oggetto esterno per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="3b095-128">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="3b095-129">**External. attemptLogin**</span><span class="sxs-lookup"><span data-stu-id="3b095-129">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="3b095-130">**External. userLoggedIn**</span><span class="sxs-lookup"><span data-stu-id="3b095-130">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> </dl>

 

 





