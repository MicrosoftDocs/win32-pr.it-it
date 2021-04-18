---
description: Il WMI Query Language (WQL) è un subset di standard American National Standards Institute Structured Query Language (ANSI SQL) con modifiche semantiche secondarie per il supporto di WMI.
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
ms.openlocfilehash: 8e2d3f68f4d7384781110958070b33b67a78405f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309924"
---
# <a name="querying-with-wql"></a>Esecuzione di query con WQL

Il WMI Query Language (WQL) è un subset di standard American National Standards Institute Structured Query Language (ANSI SQL) con modifiche semantiche secondarie per il supporto di WMI.

Per un elenco completo delle parole chiave WQL supportate, vedere [WQL (SQL per WMI)](wql-sql-for-wmi.md). L'utilizzo di parole chiave SQL per i nomi di oggetti o proprietà può impedire l'analisi di una query. Le seguenti parole chiave SQL sono limitate: **null**, **true** e **false**.

> [!Note]  
> Esistono limiti al numero di parole chiave AND e OR che possono essere utilizzate nelle query WQL. Un numero elevato di parole chiave WQL utilizzate in una query complessa può causare la restituzione del codice di errore di **\_ \_ \_ violazione della quota E di WBEM** come valore **HRESULT** . Il limite di parole chiave WQL dipende dalla complessità della query.

 

Le query possono utilizzare la clausola **where** per l'estensione e la personalizzazione, sebbene non sia obbligatoria. La clausola **where** è costituita da una proprietà o una parola chiave, da un operatore e da una costante. Tutte le clausole **where** devono specificare uno degli operatori predefiniti inclusi in WQL. Per ulteriori informazioni sulla sintassi, vedere [clausola WHERE](where-clause.md). Per ulteriori informazioni sugli operatori WQL validi, vedere [operatori WQL](wql-operators.md).

Come per le altre stringhe di query SQL, è possibile usare caratteri di escape per le query.

> [!Note]  
> WQL non supporta le query o le associazioni tra gli spazi dei nomi. Non è possibile eseguire una query per tutte le istanze di una classe specificata che risiede in tutti gli spazi dei nomi nel computer di destinazione.

 

WQL supporta i tipi di query seguenti:

-   Query di dati

    Le query sui dati vengono utilizzate per recuperare le istanze di classe e le associazioni dati. Si tratta del tipo di query usato più di frequente in applicazioni e script WMI. Per ulteriori informazioni sulla sintassi delle query di dati, vedere [richiesta di dati dell'istanza di classe](requesting-class-instance-data.md). Per ulteriori informazioni sulle associazioni, vedere [dichiarazione di una classe di associazione](declaring-an-association-class.md).

    > [!Note]  
    > WQL non supporta query di tipi di oggetto di tipo matrice.

     

    Nell'esempio di query dei dati seguente viene richiesto il file di registro eventi denominato "Application" da tutte le istanze di [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set colItems = objWMIService.ExecQuery( _
        "SELECT * FROM Win32_NTLogEvent " _
        & "WHERE Logfile = 'Application'",,48)
    ```

    

-   Query di eventi

    I consumer usano le query di eventi per eseguire la registrazione per ricevere la notifica degli eventi. I provider di eventi utilizzano le query di eventi per eseguire la registrazione per supportare uno o più eventi. Per ulteriori informazioni sulle query di eventi, vedere [ricezione di notifiche degli eventi](receiving-event-notifications.md).

    La query di eventi di esempio seguente da parte di un consumer di eventi temporanei richiede una notifica quando viene creata una nuova istanza di una classe derivata da [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) .

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

    Le query di schema vengono utilizzate per recuperare le definizioni delle classi, anziché le istanze di classe, e le associazioni di schema. I provider di classi utilizzano query dello schema per specificare le classi supportate durante la registrazione. Per ulteriori informazioni sulle query dello schema, vedere [recupero di definizioni di classe](retrieving-class-definitions.md).

    Nella query dello schema di esempio seguente viene illustrata la sintassi speciale.

    ```sql
    SELECT * FROM meta_class WHERE __this ISA "Win32_BaseService"
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato data e ora WMI](date-and-time-format.md)
</dt> </dl>

 

 
