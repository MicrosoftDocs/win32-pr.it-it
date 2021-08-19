---
description: Uso delle API di registrazione per Controllo genitori
ms.assetid: 6c38a634-53ba-4e76-83bf-1a3f36efb0bc
title: Uso delle API di registrazione per Controllo genitori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 571a24f8bdbf687f8c1975cfc29057035ac56747edc0459682512531194c55a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869063"
---
# <a name="using-logging-apis-for-parental-controls"></a>Uso delle API di registrazione per Controllo genitori

### <a name="activity-reporting-logging"></a>Rapporto attività (registrazione)

Il file di intestazione WpcEvent.h contiene le definizioni dei campi per ogni tipo di evento di attività predefinito e il tipo personalizzato. Questo codice di esempio illustra i passaggi per registrare un evento di invito alla conversazione di messaggistica immediata usando l'API di pubblicazione ETW:


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



### <a name="custom-logging"></a>Registrazione personalizzata

Per estendere gli eventi registrati all'esterno del set di eventi predefiniti o di un tipo personalizzato, è necessario definire un provider per tale evento nel manifesto dell'applicazione. Il canale predefinito WPC può quindi essere importato e gli eventi definiti dall'applicazione possono essere registrati.

### <a name="logging-rights"></a>Diritti di registrazione

Il canale di registrazione WPC è controllato [*dall'elenco*](/windows/desktop/SecGloss/a-gly) di controllo di accesso (ACL) per fornire l'accesso completo solo agli amministratori. Gli account non amministratori possono scrivere nel canale ma non hanno accesso in lettura o eliminazione. L'accesso al canale è tramite l'API ETW.

### <a name="parental-controls-logging-provider-details"></a>Dettagli del provider di registrazione di Controllo genitori

Il provider WPC è denominato Microsoft.com/Windows/ParentalControls con GUID {01090065-B467-4503-9B28-533766761087}. Il canale di registrazione locale predefinito è Microsoft.com/Windows/ParentalControls/LocalEvents.

I file di log vengono archiviati nella Windows \\ System32 \\ Wpc \\ Logs.

### <a name="notification-of-impending-time-limits-logout"></a>Notifica della disconnessione dei limiti di tempo imminenti

Il sistema Controllo genitori genera un evento di avviso a 15 minuti e di nuovo a 1 minuto prima della disconnessione di un utente controllato in base alle restrizioni di tempo. Le applicazioni possono sottoscrivere questi eventi, soprattutto quando sono in esecuzione in modalità schermo intero DirectX in cui le notifiche Windows standard non vengono visualizzate. Viene fornito il codice di esempio che illustra come sottoscrivere gli eventi, registrare una funzione di callback e ricevere gli eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Cenni preliminari sulle funzionalità di estendibilità di Controllo genitori](parental-controls-extensibility-features-overview.md)
</dt> <dt>

[**DESCRITTORE \_ DEI \_ DATI DEGLI EVENTI**](/windows/desktop/api/evntprov/ns-evntprov-event_data_descriptor)
</dt> <dt>

[**EventDataDescCreate**](/windows/desktop/api/evntprov/nf-evntprov-eventdatadesccreate)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 
