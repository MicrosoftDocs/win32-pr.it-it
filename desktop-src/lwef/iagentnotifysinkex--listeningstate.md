---
title: IAgentNotifySinkEx ListeningState
description: IAgentNotifySinkEx ListeningState
ms.assetid: e303b299-0dd0-419a-87a9-1490fe6cf54a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fee8f931030cbd68cd148fc57360d8b0ccf7624
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515829"
---
# <a name="iagentnotifysinkexlisteningstate"></a><span data-ttu-id="8deb9-103">IAgentNotifySinkEx::ListeningState</span><span class="sxs-lookup"><span data-stu-id="8deb9-103">IAgentNotifySinkEx::ListeningState</span></span>

<span data-ttu-id="8deb9-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8deb9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ListeningState(
   long dwCharacterID,  // character ID
   long bListening,     // listening mode state
   long dwCause         // cause  
);
```

<span data-ttu-id="8deb9-105">Notifica a un'applicazione client quando viene modificata la modalità di ascolto.</span><span class="sxs-lookup"><span data-stu-id="8deb9-105">Notifies a client application when the Listening mode changes.</span></span>

-   <span data-ttu-id="8deb9-106">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="8deb9-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="8deb9-107"><span id="dwCharacterID"></span><span id="dwcharacterid"></span><span id="DWCHARACTERID"></span>*dwCharacterID*</span><span class="sxs-lookup"><span data-stu-id="8deb9-107"><span id="dwCharacterID"></span><span id="dwcharacterid"></span><span id="DWCHARACTERID"></span>*dwCharacterID*</span></span>
</dt> <dd>

<span data-ttu-id="8deb9-108">Carattere per il quale è stato modificato lo stato di ascolto.</span><span class="sxs-lookup"><span data-stu-id="8deb9-108">The character for which the listening state changed.</span></span>

</dd> <dt>

<span data-ttu-id="8deb9-109"><span id="bListening"></span><span id="blistening"></span><span id="BLISTENING"></span>*bListening*</span><span class="sxs-lookup"><span data-stu-id="8deb9-109"><span id="bListening"></span><span id="blistening"></span><span id="BLISTENING"></span>*bListening*</span></span>
</dt> <dd>

<span data-ttu-id="8deb9-110">Stato della modalità di ascolto.</span><span class="sxs-lookup"><span data-stu-id="8deb9-110">The Listening mode state.</span></span> <span data-ttu-id="8deb9-111">**True** indica che la modalità di ascolto è stata avviata. **False**, la modalità di ascolto è terminata.</span><span class="sxs-lookup"><span data-stu-id="8deb9-111">**True** indicates that Listening mode has started; **False**, that Listening mode has ended.</span></span>

</dd> <dt>

<span data-ttu-id="8deb9-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span><span class="sxs-lookup"><span data-stu-id="8deb9-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="8deb9-113">Motivo dell'evento, che può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="8deb9-113">The cause for the event, which may be one of the following values.</span></span>



| <span data-ttu-id="8deb9-114">Valore</span><span class="sxs-lookup"><span data-stu-id="8deb9-114">Value</span></span>                                                                             | <span data-ttu-id="8deb9-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8deb9-115">Description</span></span>                                                                    |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="8deb9-116">**const unsigned long** **LSCOMPLETE \_ cause \_ PROGRAMDISABLED = 1;**</span><span class="sxs-lookup"><span data-stu-id="8deb9-116">**const unsigned long** **LSCOMPLETE\_CAUSE\_PROGRAMDISABLED = 1;**</span></span><br/>    | <span data-ttu-id="8deb9-117">La modalità di ascolto è stata disattivata dal codice del programma.</span><span class="sxs-lookup"><span data-stu-id="8deb9-117">Listening mode was turned off by program code.</span></span>                                 |
| <span data-ttu-id="8deb9-118">**const unsigned long** **LSCOMPLETE \_ causare \_ PROGRAMTIMEDOUT = 2;**</span><span class="sxs-lookup"><span data-stu-id="8deb9-118">**const unsigned long** **LSCOMPLETE\_CAUSE\_PROGRAMTIMEDOUT = 2;**</span></span><br/>    | <span data-ttu-id="8deb9-119">Timeout della modalità di ascolto (attivata dal codice del programma).</span><span class="sxs-lookup"><span data-stu-id="8deb9-119">Listening mode (turned on by program code) timed out.</span></span>                          |
| <span data-ttu-id="8deb9-120">**const unsigned long** **LSCOMPLETE \_ causare \_ USERTIMEDOUT = 3;**</span><span class="sxs-lookup"><span data-stu-id="8deb9-120">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERTIMEDOUT = 3;**</span></span><br/>       | <span data-ttu-id="8deb9-121">Timeout della modalità di ascolto (attivata dal tasto di attesa).</span><span class="sxs-lookup"><span data-stu-id="8deb9-121">Listening mode (turned on by the Listening key) timed out.</span></span>                     |
| <span data-ttu-id="8deb9-122">**const unsigned long** **LSCOMPLETE \_ causare \_ USERRELEASEDKEY = 4;**</span><span class="sxs-lookup"><span data-stu-id="8deb9-122">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERRELEASEDKEY = 4;**</span></span><br/>    | <span data-ttu-id="8deb9-123">La modalità di ascolto è stata disattivata perché l'utente ha rilasciato il tasto di attesa.</span><span class="sxs-lookup"><span data-stu-id="8deb9-123">Listening mode was turned off because the user released the Listening key.</span></span>     |
| <span data-ttu-id="8deb9-124">**const unsigned long** **LSCOMPLETE \_ causare \_ USERUTTERANCEENDED = 5;**</span><span class="sxs-lookup"><span data-stu-id="8deb9-124">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERUTTERANCEENDED = 5;**</span></span><br/> | <span data-ttu-id="8deb9-125">La modalità di ascolto è stata disattivata perché l'utente ha terminato di parlare.</span><span class="sxs-lookup"><span data-stu-id="8deb9-125">Listening mode was turned off because the user finished speaking.</span></span>              |
| <span data-ttu-id="8deb9-126">**const unsigned long** **LSCOMPLETE \_ causare \_ CLIENTDEACTIVATED = 6;**</span><span class="sxs-lookup"><span data-stu-id="8deb9-126">**const unsigned long** **LSCOMPLETE\_CAUSE\_CLIENTDEACTIVATED = 6;**</span></span><br/>  | <span data-ttu-id="8deb9-127">La modalità di ascolto è stata disabilitata perché il client attivo di input è stato disattivato.</span><span class="sxs-lookup"><span data-stu-id="8deb9-127">Listening mode was turned off because the input active client was deactivated.</span></span> |
| <span data-ttu-id="8deb9-128">**const unsigned long** **LSCOMPLETE \_ cause \_ DEFAULTCHARCHANGE = 7**</span><span class="sxs-lookup"><span data-stu-id="8deb9-128">**const unsigned long** **LSCOMPLETE\_CAUSE\_DEFAULTCHARCHANGE = 7**</span></span><br/>   | <span data-ttu-id="8deb9-129">La modalità di ascolto è stata disattivata perché il carattere predefinito è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="8deb9-129">Listening mode was turned off because the default character was changed.</span></span>       |
| <span data-ttu-id="8deb9-130">**const unsigned long** **LSCOMPLETE \_ cause \_ USERDISABLED = 8**</span><span class="sxs-lookup"><span data-stu-id="8deb9-130">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERDISABLED = 8**</span></span><br/>        | <span data-ttu-id="8deb9-131">La modalità di ascolto è stata disattivata perché l'utente ha disabilitato l'input vocale.</span><span class="sxs-lookup"><span data-stu-id="8deb9-131">Listening mode was turned off because the user disabled speech input.</span></span>          |



 

</dd> </dl>

<span data-ttu-id="8deb9-132">Questo evento viene inviato a tutti i client quando la modalità di ascolto viene avviata dopo che l'utente ha premuto il tasto ascolto o quando è terminato il timeout oppure quando il client di input-attivo chiama il metodo [**IAgentCharacterEx:: Listen**](iagentcharacterex--listen.md) con **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="8deb9-132">This event is sent to all clients when the Listening mode begins after the user presses the Listening key or when its time-out ends, or when the input-active client calls the [**IAgentCharacterEx::Listen**](iagentcharacterex--listen.md) method with **True** or **False**.</span></span>

<span data-ttu-id="8deb9-133">L'evento restituisce i valori ai client attualmente caricati da questo carattere.</span><span class="sxs-lookup"><span data-stu-id="8deb9-133">The event returns values to the clients that currently have this character loaded.</span></span> <span data-ttu-id="8deb9-134">Tutti gli altri client ricevono un carattere null (stringa vuota).</span><span class="sxs-lookup"><span data-stu-id="8deb9-134">All other clients receive a null character (empty string).</span></span>

## <a name="see-also"></a><span data-ttu-id="8deb9-135">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8deb9-135">See Also</span></span>

[<span data-ttu-id="8deb9-136">**IAgentCharacterEx:: Listen**</span><span class="sxs-lookup"><span data-stu-id="8deb9-136">**IAgentCharacterEx::Listen**</span></span>](iagentcharacterex--listen.md)


 

 





