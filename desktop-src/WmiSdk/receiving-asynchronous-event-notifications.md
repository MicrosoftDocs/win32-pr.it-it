---
description: La notifica asincrona degli eventi è una tecnica che consente a un'applicazione di monitorare costantemente gli eventi senza monopolizzare le risorse di sistema.
ms.assetid: 69ec8ead-9073-4689-bc66-5134728ab147
ms.tgt_platform: multiple
title: Ricezione di notifiche di eventi asincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d883908475c796a6bcf31895f2928345541c940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314587"
---
# <a name="receiving-asynchronous-event-notifications"></a>Ricezione di notifiche di eventi asincroni

La notifica asincrona degli eventi è una tecnica che consente a un'applicazione di monitorare costantemente gli eventi senza monopolizzare le risorse di sistema. Le notifiche degli eventi asincroni presentano le stesse limitazioni di sicurezza di altre chiamate asincrone. In alternativa, è possibile eseguire chiamate semisincrono. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

La coda di eventi asincroni indirizzati a un client può aumentare eccezionalmente le dimensioni. Pertanto, WMI implementa un criterio a livello di sistema per evitare di esaurire la memoria. WMI rallenta gli eventi o inizia a eliminare gli eventi dalla coda quando la coda cresce oltre una determinata dimensione.

WMI utilizza le proprietà [**LowThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) e [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) della classe [**\_ WMISetting Win32**](/windows/desktop/CIMWin32Prov/win32-wmisetting) per impostare limiti di prevenzione della memoria insufficiente. Il valore minimo indica quando WMI deve iniziare a rallentare la notifica degli eventi e il valore massimo indica quando iniziare a eliminare gli eventi. I valori predefiniti per le soglie bassa e massima sono 1 milione (10 MB) e 2 milioni (20 MB). Inoltre, è possibile impostare la proprietà [**MaxWaitOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) per descrivere l'intervallo di tempo in cui WMI deve attendere prima di eliminare gli eventi. Il valore predefinito per **MaxWaitOnEvents** è 2000 o 2 secondi.

## <a name="receiving-asynchronous-event-notifications-in-vbscript"></a>Ricezione di notifiche di eventi asincroni in VBScript

Le chiamate di scripting per ricevere notifiche degli eventi sono essenzialmente le stesse di tutte le chiamate asincrone con gli stessi problemi di sicurezza. Per ulteriori informazioni, vedere [creazione di una chiamata asincrona con VBScript](making-an-asynchronous-call-with-vbscript.md).

**Per ricevere notifiche di eventi asincroni in VBScript**

1.  Creare un oggetto sink chiamando [WScript. CreateObject](/previous-versions//xzysf6hc(v=vs.85)) e specificando il ProgID di "WbemScripting" e il tipo di oggetto di [**SWbemSink**](swbemsink.md). L'oggetto sink riceve le notifiche.
2.  Scrivere una subroutine per ogni evento che si desidera gestire. La tabella seguente elenca gli eventi [**SWbemSink**](swbemsink.md) .

    

    | Evento                                            | Significato                                                                                                                         |
    |--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
    | [**OnObjectReady**](swbemsink-onobjectready.md) | Segnala i ritorni di un oggetto al sink. L'utilizzo di questa chiamata restituisce un oggetto ogni volta fino al completamento dell'operazione.     |
    | [**OnCompleted**](swbemsink-oncompleted.md)     | Segnala il completamento di una chiamata asincrona. Questo evento non si verifica mai se l'operazione è indefinita.                          |
    | [**OnObjectPut**](swbemsink-onobjectput.md)     | Segnala il completamento di un'operazione Put asincrona. Questo evento restituisce il percorso dell'oggetto dell'istanza o della classe salvata. |
    | [**OnProgress**](swbemsink-onprogress.md)       | Segnala lo stato di una chiamata asincrona in corso. Non tutti i provider supportano i report di stato provvisori.             |
    | [**Annulla**](swbemsink-cancel.md)               | Annulla tutte le operazioni asincrone in attesa associate a questo sink dell'oggetto.                                        |

    

     

Nell'esempio di codice VBScript seguente viene notificata l'eliminazione di processi con un intervallo di polling di 10 secondi. In questo script, il SINK della subroutine \_ OnObjectReady gestisce l'occorrenza dell'evento. Nell'esempio, l'oggetto sink è denominato "sink", tuttavia è possibile assegnare un nome a questo oggetto come scelto.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set MySink = WScript.CreateObject( _
    "WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, _
    "SELECT * FROM __InstanceDeletionEvent" _
    & " WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'"


WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    Wscript.Echo "__InstanceDeletionEvent event has occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub
```



## <a name="receiving-asynchronous-event-notifications-in-c"></a>Ricezione di notifiche di eventi asincroni in C++

Per eseguire una notifica asincrona, è necessario creare un thread separato esclusivamente per il monitoraggio e la ricezione di eventi da Strumentazione gestione Windows (WMI). Quando il thread riceve un messaggio, il thread invia una notifica all'applicazione principale.

Dedicando un thread separato, si consente al processo principale di eseguire altre attività in attesa dell'arrivo di un evento. Il recapito asincrono delle notifiche migliora le prestazioni, ma può garantire una minore sicurezza del necessario. In C++ è possibile usare l'interfaccia [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) o eseguire controlli di accesso sui descrittori di sicurezza. Per ulteriori informazioni, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).

**Per configurare le notifiche degli eventi asincroni**

1.  Prima di inizializzare le notifiche asincrone, assicurarsi che i parametri di prevenzione della memoria esaurita siano impostati correttamente in [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting).

2.  Determinare il tipo di eventi che si desidera ricevere.

    WMI supporta eventi intrinseci ed estrinseci. Un evento intrinseco è un evento predefinito da WMI, mentre un evento estrinseco è un evento definito da un provider di terze parti. Per ulteriori informazioni, vedere [determinazione del tipo di evento da ricevere](determining-the-type-of-event-to-receive.md).

Nella procedura seguente viene descritto come ricevere notifiche di eventi asincroni in C++.

**Per ricevere notifiche di eventi asincroni in C++**

1.  Configurare l'applicazione con le chiamate alle funzioni [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .

    La chiamata a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) Inizializza com, mentre [**COINITIALIZESECURITY**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) concede a WMI l'autorizzazione per chiamare il processo del consumer. La funzione **CoInitializeEx** offre inoltre la possibilità di programmare un'applicazione multithread, necessaria per la notifica asincrona. Per ulteriori informazioni, vedere [gestione della sicurezza WMI](maintaining-wmi-security.md).

    Il codice in questo argomento richiede i riferimenti seguenti e le \# istruzioni di inclusione per la compilazione corretta.

    ```C++
    #define _WIN32_DCOM
    #include <iostream>
    using namespace std;
    #include <wbemidl.h>
    ```

    

    Nell'esempio di codice seguente viene descritto come configurare il consumer di eventi temporanei con chiamate a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

    ```C++
    void main(int argc, char **argv)
    {
        HRESULT hr = 0;
        hr = CoInitializeEx (0, COINIT_MULTITHREADED);
        hr = CoInitializeSecurity (NULL, 
           -1, 
           NULL, 
           NULL,   
           RPC_C_AUTHN_LEVEL_NONE, 
           RPC_C_IMP_LEVEL_IMPERSONATE, 
           NULL,
           EOAC_NONE,
           NULL); 

        if (FAILED(hr))
        {
           CoUninitialize();
           cout << "Failed to initialize security. Error code = 0x"
               << hex << hr << endl;
           return;
        }

    // ...
    }
    ```

    

2.  Creare un oggetto sink tramite l'interfaccia [**IWbemObjectSink**](iwbemobjectsink.md) .

    WMI utilizza [**IWbemObjectSink**](iwbemobjectsink.md) per inviare notifiche degli eventi e per segnalare lo stato di un'operazione asincrona o di una notifica degli eventi.

3.  Registrare il consumer di eventi con una chiamata al metodo [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) .

    Verificare che il parametro *pResponseHandler* punti all'oggetto sink creato nel passaggio precedente.

    Lo scopo della registrazione è quello di ricevere solo le notifiche richieste. La ricezione di notifiche superflue spreca l'elaborazione e il tempo di recapito; e non usa la capacità di filtraggio di WMI al massimo del potenziale.

    Un consumer temporaneo può tuttavia ricevere più di un tipo di evento. In questo caso, un consumer temporaneo deve effettuare chiamate separate a [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) per ogni tipo di evento. Un consumer può, ad esempio, richiedere una notifica quando vengono creati nuovi processi (un evento di creazione dell'istanza o [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) e per le modifiche a determinate chiavi del registro di sistema (un evento del registro di sistema, ad esempio [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)). Pertanto, il consumer effettua una chiamata a [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) per registrare gli eventi di creazione dell'istanza e un'altra chiamata a **ExecNotificationQueryAsync** per la registrazione degli eventi del registro di sistema.

    Se si sceglie di creare un consumer di eventi che si registra per più eventi, è consigliabile evitare di registrare più classi con lo stesso sink. Usare invece un sink separato per ogni classe di evento registrato. Un sink dedicato semplifica l'elaborazione e favorisce la manutenzione, consentendo di annullare una registrazione senza influire sugli altri.

4.  Eseguire tutte le attività necessarie nel consumer di eventi.

    Questo passaggio deve contenere la maggior parte del codice e includere attività quali la visualizzazione di eventi in un'interfaccia utente.

5.  Al termine, annullare la registrazione del consumer di eventi temporanei con una chiamata all'evento [**IWbemServices:: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) .

    Indipendentemente dal fatto che la chiamata a [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) abbia esito positivo o negativo, non eliminare l'oggetto sink fino a quando il conteggio dei riferimenti all'oggetto non raggiunge lo zero. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

 

 
