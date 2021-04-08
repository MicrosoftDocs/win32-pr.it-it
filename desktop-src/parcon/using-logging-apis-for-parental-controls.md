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
# <a name="using-logging-apis-for-parental-controls"></a>Uso delle API di registrazione per i controlli padre

### <a name="activity-reporting-logging"></a>Creazione di report attività (registrazione)

Il file di intestazione WpcEvent. h contiene le definizioni dei campi per ogni tipo di evento di attività predefinito e per il tipo personalizzato. In questo codice di esempio vengono illustrati i passaggi per la registrazione di un evento di invito di conversazione di messaggistica immediata mediante l'API di pubblicazione ETW:


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

Affinché un'applicazione estenda gli eventi registrati al di fuori del set di eventi predefiniti o di un tipo personalizzato, sarà necessario definire un provider per tale oggetto nel manifesto dell'applicazione. Il canale predefinito WPC può quindi essere importato e gli eventi definiti dall'applicazione possono essere registrati.

### <a name="logging-rights"></a>Diritti di registrazione

Il canale di registrazione WPC è controllato dall' [*elenco di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACL) per fornire accesso completo solo agli amministratori. Gli account non amministratore possono scrivere sul canale ma non dispongono di accesso in lettura o eliminazione. L'accesso al canale consiste nell'utilizzo dell'API ETW.

### <a name="parental-controls-logging-provider-details"></a>Dettagli del provider di registrazione dei controlli padre

Il provider WPC è denominato Microsoft.com/Windows/ParentalControls con GUID {01090065-B467-4503-9B28-533766761087}. Il canale di registrazione locale predefinito è Microsoft.com/Windows/ParentalControls/LocalEvents.

I file di log vengono archiviati nella \\ cartella Windows system32 \\ WPC \\ logs.

### <a name="notification-of-impending-time-limits-logout"></a>Notifica dei limiti di tempo imminenti per la disconnessione

Il sistema di controlli padre genera un evento di avviso a 15 minuti e di nuovo a 1 minuto prima della disconnessione di un utente controllato in base alle restrizioni temporali. Le applicazioni possono sottoscrivere questi eventi, soprattutto quando sono in esecuzione in modalità a schermo intero DirectX in cui non vengono visualizzate le notifiche standard di Windows. Viene fornito codice di esempio che illustra come sottoscrivere gli eventi, registrare una funzione di callback e ricevere gli eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Cenni preliminari sulle funzionalità di estensibilità dei controlli padre](parental-controls-extensibility-features-overview.md)
</dt> <dt>

[**\_descrittore dati evento \_**](/windows/desktop/api/evntprov/ns-evntprov-event_data_descriptor)
</dt> <dt>

[**EventDataDescCreate**](/windows/desktop/api/evntprov/nf-evntprov-eventdatadesccreate)
</dt> <dt>

[**\_argomenti \_ CONVERSATIONINITEVENT di WPC**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 
