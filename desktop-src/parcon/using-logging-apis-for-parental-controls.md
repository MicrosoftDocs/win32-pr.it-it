---
description: Uso delle API di registrazione per i controlli padre
ms.assetid: 6c38a634-53ba-4e76-83bf-1a3f36efb0bc
title: Uso delle API di registrazione per i controlli padre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d1cedb9ff02856be6ea1ae2069d8635b980681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882213"
---
# <a name="using-logging-apis-for-parental-controls"></a><span data-ttu-id="6ed5f-103">Uso delle API di registrazione per i controlli padre</span><span class="sxs-lookup"><span data-stu-id="6ed5f-103">Using Logging APIs for Parental Controls</span></span>

### <a name="activity-reporting-logging"></a><span data-ttu-id="6ed5f-104">Creazione di report attività (registrazione)</span><span class="sxs-lookup"><span data-stu-id="6ed5f-104">Activity Reporting (Logging)</span></span>

<span data-ttu-id="6ed5f-105">Il file di intestazione WpcEvent. h contiene le definizioni dei campi per ogni tipo di evento di attività predefinito e per il tipo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="6ed5f-105">The WpcEvent.h header file contains definitions of the fields for each predefined activity event type and the custom type.</span></span> <span data-ttu-id="6ed5f-106">In questo codice di esempio vengono illustrati i passaggi per la registrazione di un evento di invito di conversazione di messaggistica immediata mediante l'API di pubblicazione ETW:</span><span class="sxs-lookup"><span data-stu-id="6ed5f-106">This sample code shows the steps for logging an instant messaging conversation invitation event using the ETW publishing API:</span></span>


```C++
#include <windows.h>
#include <evntprov.h>
#include <wpcevent.h>

#pragma comment(lib, "advapi32.lib")

#define BYTELEN(x) ((wcslen(x) + 1) * sizeof(WCHAR))

void main()
{
    REGHANDLE hWpc = 0;

    // Register
    ULONG res = EventRegister(&WPCPROV, NULL, NULL, &hWpc);

    // Log an event
    PCWSTR pcszAppName = L"SuperIM";
    PCWSTR pcszAppVersion = L"7.0";
    PCWSTR pcszAccountName = L"Kate";
    PCWSTR pcszConvID = L"102";
    PCWSTR pcszRequestingIP = L"192.168.2.100";
    PCWSTR pcszSender = L"imperson@isp.com";
    const DWORD dwReason = WPCFLAG_ISBLOCKED_NOTBLOCKED;
    const DWORD dwRecipCount = 1;
    PCWSTR pcszRecipient = L"otherim@isp.com";

    EVENT_DATA_DESCRIPTOR eventData[WPC_ARGS_CONVERSATIONINITEVENT_CARGS];

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_APPNAME],
        (const PVOID)pcszAppName, (ULONG)BYTELEN(pcszAppName));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_APPVERSION],
        (const PVOID)pcszAppVersion,(ULONG)BYTELEN(pcszAppVersion));

    EventDataDescCreate(
        &eventData[WPC_ARGS_CONVERSATIONINITEVENT_ACCOUNTNAME], 
        (const PVOID)pcszAccountName, (ULONG)BYTELEN(pcszAccountName));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_CONVID], 
        (const PVOID)pcszConvID, (ULONG)BYTELEN(pcszConvID));

    EventDataDescCreate(
        &eventData[WPC_ARGS_CONVERSATIONINITEVENT_REQUESTINGIP], 
        (const PVOID)pcszRequestingIP, (ULONG)BYTELEN(pcszRequestingIP));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_SENDER],
        (const PVOID)pcszSender, (ULONG)BYTELEN(pcszSender));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_REASON],
        (const PVOID)&dwReason, sizeof(dwReason));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_RECIPCOUNT],
        (const PVOID)&dwRecipCount, sizeof(dwRecipCount));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_RECIPIENT],
        (const PVOID)pcszRecipient, (ULONG)BYTELEN(pcszRecipient));


    ULONG lRet = EventWrite(hWpc, &WPCEVENT_IM_INVITATION, ARRAYSIZE(eventData), eventData);

    // Unregister
    EventUnregister(hWpc);
}
```



### <a name="custom-logging"></a><span data-ttu-id="6ed5f-107">Registrazione personalizzata</span><span class="sxs-lookup"><span data-stu-id="6ed5f-107">Custom Logging</span></span>

<span data-ttu-id="6ed5f-108">Affinché un'applicazione estenda gli eventi registrati al di fuori del set di eventi predefiniti o di un tipo personalizzato, sarà necessario definire un provider per tale oggetto nel manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6ed5f-108">For an application to extend the events logged outside the set of predefined events or the one custom type, you will need to define a provider for that in the application manifest.</span></span> <span data-ttu-id="6ed5f-109">Il canale predefinito WPC può quindi essere importato e gli eventi definiti dall'applicazione possono essere registrati.</span><span class="sxs-lookup"><span data-stu-id="6ed5f-109">The WPC default channel can then be imported and application-defined events can then be logged.</span></span>

### <a name="logging-rights"></a><span data-ttu-id="6ed5f-110">Diritti di registrazione</span><span class="sxs-lookup"><span data-stu-id="6ed5f-110">Logging Rights</span></span>

<span data-ttu-id="6ed5f-111">Il canale di registrazione WPC è controllato dall' [*elenco di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACL) per fornire accesso completo solo agli amministratori.</span><span class="sxs-lookup"><span data-stu-id="6ed5f-111">The WPC logging channel is controlled by [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL) to provide full access for administrators only.</span></span> <span data-ttu-id="6ed5f-112">Gli account non amministratore possono scrivere sul canale ma non dispongono di accesso in lettura o eliminazione.</span><span class="sxs-lookup"><span data-stu-id="6ed5f-112">Non-administrator accounts may write to the channel but have no read or delete access.</span></span> <span data-ttu-id="6ed5f-113">L'accesso al canale consiste nell'utilizzo dell'API ETW.</span><span class="sxs-lookup"><span data-stu-id="6ed5f-113">Access to the channel is by using the ETW API.</span></span>

### <a name="parental-controls-logging-provider-details"></a><span data-ttu-id="6ed5f-114">Dettagli del provider di registrazione dei controlli padre</span><span class="sxs-lookup"><span data-stu-id="6ed5f-114">Parental Controls Logging Provider Details</span></span>

<span data-ttu-id="6ed5f-115">Il provider WPC è denominato Microsoft.com/Windows/ParentalControls con GUID {01090065-B467-4503-9B28-533766761087}.</span><span class="sxs-lookup"><span data-stu-id="6ed5f-115">The WPC provider is named Microsoft.com/Windows/ParentalControls with GUID {01090065-B467-4503-9B28-533766761087}.</span></span> <span data-ttu-id="6ed5f-116">Il canale di registrazione locale predefinito è Microsoft.com/Windows/ParentalControls/LocalEvents.</span><span class="sxs-lookup"><span data-stu-id="6ed5f-116">The default local logging channel is Microsoft.com/Windows/ParentalControls/LocalEvents.</span></span>

<span data-ttu-id="6ed5f-117">I file di log vengono archiviati nella \\ cartella Windows system32 \\ WPC \\ logs.</span><span class="sxs-lookup"><span data-stu-id="6ed5f-117">Log files are stored in the Windows\\System32\\Wpc\\Logs folder.</span></span>

### <a name="notification-of-impending-time-limits-logout"></a><span data-ttu-id="6ed5f-118">Notifica dei limiti di tempo imminenti per la disconnessione</span><span class="sxs-lookup"><span data-stu-id="6ed5f-118">Notification of Impending Time Limits Logout</span></span>

<span data-ttu-id="6ed5f-119">Il sistema di controlli padre genera un evento di avviso a 15 minuti e di nuovo a 1 minuto prima della disconnessione di un utente controllato in base alle restrizioni temporali.</span><span class="sxs-lookup"><span data-stu-id="6ed5f-119">The Parental Controls system will fire a warning event at 15 minutes and again at 1 minute before logout of a controlled user based on time restrictions.</span></span> <span data-ttu-id="6ed5f-120">Le applicazioni possono sottoscrivere questi eventi, soprattutto quando sono in esecuzione in modalità a schermo intero DirectX in cui non vengono visualizzate le notifiche standard di Windows.</span><span class="sxs-lookup"><span data-stu-id="6ed5f-120">Applications can subscribe to these events, especially when they are running in DirectX full-screen mode where standard Windows notifications are not displayed.</span></span> <span data-ttu-id="6ed5f-121">Viene fornito codice di esempio che illustra come sottoscrivere gli eventi, registrare una funzione di callback e ricevere gli eventi.</span><span class="sxs-lookup"><span data-stu-id="6ed5f-121">Sample code is provided that shows how to subscribe to the events, register a callback function, and receive the events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ed5f-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6ed5f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ed5f-123">Cenni preliminari sulle funzionalità di estensibilità dei controlli padre</span><span class="sxs-lookup"><span data-stu-id="6ed5f-123">Parental Controls Extensibility Features Overview</span></span>](parental-controls-extensibility-features-overview.md)
</dt> <dt>

[<span data-ttu-id="6ed5f-124">**\_descrittore dati evento \_**</span><span class="sxs-lookup"><span data-stu-id="6ed5f-124">**EVENT\_DATA\_DESCRIPTOR**</span></span>](/windows/desktop/api/evntprov/ns-evntprov-event_data_descriptor)
</dt> <dt>

[<span data-ttu-id="6ed5f-125">**EventDataDescCreate**</span><span class="sxs-lookup"><span data-stu-id="6ed5f-125">**EventDataDescCreate**</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventdatadesccreate)
</dt> <dt>

[<span data-ttu-id="6ed5f-126">**\_argomenti \_ CONVERSATIONINITEVENT di WPC**</span><span class="sxs-lookup"><span data-stu-id="6ed5f-126">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 
