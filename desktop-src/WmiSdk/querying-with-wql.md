---
description: Il WMI Query Language (WQL) è un subset di standard American National Standards Institute Structured Query Language (ANSI SQL) con modifiche semantiche secondarie per supportare WMI.
ms.assetid: 7e04ba37-c0e0-4304-b162-8b911f233f38
ms.tgt_platform: multiple
title: Esecuzione di query con WQL
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 737ae9505a0f775c26c5049eeb2f8500c9e3222d78181e18326ff53d39dfde01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554832"
---
# <a name="querying-with-wql"></a>Esecuzione di query con WQL

Il WMI Query Language (WQL) è un subset di standard American National Standards Institute Structured Query Language (ANSI SQL) con modifiche semantiche secondarie per supportare WMI.

Per un elenco completo delle parole chiave WQL supportate, vedere [WQL (SQL per WMI).](wql-sql-for-wmi.md) L SQL parole chiave per i nomi di oggetti o proprietà può limitare l'analisi di una query. Le parole SQL seguenti sono limitate: **NULL,** **TRUE** e **FALSE.**

> [!Note]  
> Esistono limiti al numero di parole chiave AND e OR che possono essere usate nelle query WQL. Un numero elevato di parole chiave WQL usate in una query complessa può causare la restituzione del codice di errore **WBEM \_ E \_ QUOTA \_ VIOLATION** da parte di WMI come **valore HRESULT.** Il limite delle parole chiave WQL dipende dalla complessità della query.

 

Le query possono usare la **clausola WHERE** per l'estensione e la personalizzazione, anche se non è necessaria. La **clausola WHERE** è costituito da una proprietà o una parola chiave, un operatore e una costante. Tutte le clausole **WHERE** devono specificare uno degli operatori predefiniti inclusi in WQL. Per altre informazioni sulla sintassi, vedere [Clausola WHERE](where-clause.md). Per altre informazioni sugli operatori WQL validi, vedere [Operatori WQL](wql-operators.md).

Come per altre stringhe SQL query, è possibile eseguire l'escape delle query.

> [!Note]  
> WQL non supporta le query o le associazioni tra spazi dei nomi. Non è possibile eseguire una query per tutte le istanze di una classe specificata che risiedono in tutti gli spazi dei nomi nel computer di destinazione.

 

WQL supporta i tipi di query seguenti:

-   Query di dati

    Le query di dati vengono usate per recuperare le istanze di classe e le associazioni dati. Si tratta del tipo di query più comunemente usato negli script e nelle applicazioni WMI. Per altre informazioni sulla sintassi delle query di dati, vedere [Richiesta dei dati dell'istanza della classe](requesting-class-instance-data.md). Per altre informazioni sulle associazioni, vedere [Dichiarazione di una classe di associazione](declaring-an-association-class.md).

    > [!Note]  
    > WQL non supporta le query di tipi di dati di matrice.

     

    L'esempio di query sui dati seguente richiede il file di log eventi denominato "Application" da tutte le istanze di [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set colItems = objWMIService.ExecQuery( _
        "SELECT * FROM Win32_NTLogEvent " _
        & "WHERE Logfile = 'Application'",,48)
    ```

    

-   Query di eventi

    I consumer usano query di eventi per registrarsi per ricevere notifiche di eventi. I provider di eventi usano query di eventi per la registrazione per supportare uno o più eventi. Per altre informazioni sulle query di evento, vedere [Ricezione di notifiche degli eventi](receiving-event-notifications.md).

    La query di evento di esempio seguente eseguita da un consumer di eventi temporaneo richiede una notifica quando viene creata una nuova istanza di una classe derivata da [**Win32 \_ NTLogEvent.**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent)

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set objEvents = objWMIService.ExecNotificationQuery _
    ("SELECT * FROM __InstanceModificationEvent WITHIN 10 WHERE " & _
        "TargetInstance ISA 'Win32_Service'" & _
        " AND TargetInstance._Class = 'win32_TerminalService'")

    i = TRUE
    Do While i = TRUE
        Set strReceivedEvent = objEvents.NextEvent

        'report an event
        Wscript.Echo "An event has occurred."
    Loop
    ```

    

-   Query dello schema

    Le query dello schema vengono usate per recuperare le definizioni di classe (anziché le istanze di classe) e le associazioni dello schema. I provider di classi usano query dello schema per specificare le classi supportate durante la registrazione. Per altre informazioni sulle query dello schema, vedere [Recupero di definizioni di classe](retrieving-class-definitions.md).

    La query dello schema di esempio seguente illustra la sintassi speciale.

    ```sql
    SELECT * FROM meta_class WHERE __this ISA "Win32_BaseService"
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato di data e ora WMI](date-and-time-format.md)
</dt> </dl>

 

 
