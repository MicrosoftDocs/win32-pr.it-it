---
description: Un consumer fisico è un oggetto COM che implementa l'interfaccia IWbemUnboundObjectSink.
ms.assetid: 497457dc-61ca-4527-89fd-2af0383de5e9
ms.tgt_platform: multiple
title: Implementazione di un consumer fisico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0a9530ed7a98ce19b3b39f2f5a1fe52f3b0631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315222"
---
# <a name="implementing-a-physical-consumer"></a>Implementazione di un consumer fisico

Un consumer fisico è un oggetto COM che implementa l'interfaccia [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) . WMI carica il consumer fisico e passa gli eventi tramite **IWbemUnboundObjectSink** in risposta a uno o più eventi, in base a quanto definito dal consumer logico associato. I consumer permanenti hanno requisiti di sicurezza speciali. Per ulteriori informazioni, vedere [protezione degli eventi WMI](securing-wmi-events.md).

Nella procedura seguente viene descritto come implementare un consumer fisico per un consumer di eventi permanenti.

**Per implementare un consumer fisico per un consumer di eventi permanenti**

1.  Creare un oggetto COM.

    È necessario implementare un consumer fisico come server locale o remoto utilizzando il protocollo COM.

2.  Determinare se si desidera supportare la notifica di eventi sincroni o asincroni.

    Con la notifica asincrona degli eventi, il thread di invio non è correlato al thread di destinazione. Pertanto, né WMI né il provider di eventi vengono bloccati mentre WMI invia una notifica a qualsiasi utente registrato per ricevere l'evento. Lo svantaggio del recapito asincrono è che si verifica un cambio di contesto tra il momento in cui il provider produce l'evento e il momento in cui il consumer riceve l'evento. Per ulteriori informazioni sull'utilizzo asincrono, vedere l'argomento [nozioni fondamentali su com](../com/guide.md) nella sezione com di Microsoft Windows Software Development Kit (SDK). Per ulteriori informazioni sulle opzioni di contesto, vedere l'argomento [cambi di contesto](../procthread/context-switches.md) nella sezione dll, processi e thread della Windows SDK.

    > [!Note]  
    > Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile utilizzare semisincrono anziché la comunicazione asincrona. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

     

    Con la notifica sincrona, WMI recapita la notifica sullo stesso thread utilizzato dal provider di eventi per recapitare l'evento a WMI. In questo caso, quando un provider di eventi invia una notifica, il provider di eventi viene bloccato da WMI finché WMI non recapita la notifica. Solo se il consumer è estremamente veloce ed è in grado di elaborare un evento in microsecondi 100 o meno, è consigliabile supportare la notifica sincrona. I consumer sincroni che importano troppo tempo per elaborare gli eventi possono rallentare seriamente il recapito degli eventi a tutti gli altri utenti. Inoltre, possono bloccare inavvertitamente il provider. Per ulteriori informazioni, vedere [associazione di un filtro eventi a un consumer logico](binding-an-event-filter-with-a-logical-consumer.md).

3.  Implementare la funzione [**IWbemUnboundObjectSink:: IndicateToConsumer**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemunboundobjectsink-indicatetoconsumer) .

    WMI utilizza la funzione [**IndicateToConsumer**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemunboundobjectsink-indicatetoconsumer) per passare i puntatori e gli eventi necessari al consumer fisico per le comunicazioni sincrone e asincrone. L'implementazione di **IndicateToConsumer** deve contenere tutto il codice necessario per rispondere a un evento.

    Diversamente da un consumer di eventi temporaneo, non è necessario chiamare l'interfaccia [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) per contattare WMI. Al contrario, WMI individua un puntatore al consumer tramite il provider di consumer di eventi. Per ulteriori informazioni, vedere [scrittura di un provider di consumer di eventi](writing-an-event-consumer-provider.md).

    Tuttavia, se si desidera richiamarlo in WMI, utilizzare le interfacce [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) e [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . Il metodo tradizionale per la connessione a WMI è durante il processo di inizializzazione dell'oggetto COM. Per ulteriori informazioni, vedere [creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md).

    Se il consumer fisico viene implementato come server COM in-process e si esegue la connessione a WMI separatamente dal processo di inizializzazione, è necessario utilizzare l'identificatore di classe **CLSID \_ WbemAdministrativeLocator** per accedere all'interfaccia [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) nella chiamata a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Nell'esempio seguente viene illustrato come utilizzare l'identificatore di classe **CLSID \_ WbemAdministrativeLocator** per accedere all'interfaccia [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) .

    ```C++
    IWbemLocator *pLoc = 0;

    DWORD dwRes = CoCreateInstance(CLSID_WbemAdministrativeLocator, 0, 
        CLSCTX_INPROC_SERVER, IID_IWbemLocator, (LPVOID *) &pLoc);
    ```

    

    L'interfaccia [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) ottiene il puntatore iniziale dello spazio dei nomi a WMI in un determinato computer host. Se non si utilizza l'identificatore **CLSID \_ WbemAdministrativeLocator** nella chiamata [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , viene restituito un errore di accesso negato.

    In circostanze normali, WMI recapita gli eventi asincroni al client uno alla volta. Tuttavia, se un client non è in grado di ricevere notifiche di eventi asincrone con la stessa velocità con cui arrivano gli eventi, WMI inizia a eseguire automaticamente il batch degli eventi in una singola chiamata. L'invio in batch automatico aiuta se i tempi di round trip rappresentano un problema, come spesso accade negli scenari con velocità effettiva elevata. Tuttavia, l'invio in batch non migliora le prestazioni del sistema se il client o la larghezza di banda di rete sono in errore.

 

 
