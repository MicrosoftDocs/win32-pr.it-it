---
description: I consumer temporanei e permanenti hanno metodi diversi per proteggere il recapito degli eventi.
ms.assetid: cd02e5db-f9e2-438b-9632-0a1387a6d4e3
ms.tgt_platform: multiple
title: Ricezione di eventi in modo sicuro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64db5b0289abd9a43caee6ddb3b68da94a9560b0ea8f591d95ee472cf900b4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316528"
---
# <a name="receiving-events-securely"></a>Ricezione di eventi in modo sicuro

I consumer temporanei e permanenti hanno metodi diversi per proteggere il recapito degli eventi.

In questo argomento vengono illustrate le sezioni seguenti:

-   [Protezione dei consumer temporanei](#securing-temporary-consumers)
-   [Protezione dei consumer permanenti](#securing-permanent-consumers)
-   [Protezione della sottoscrizione permanente](#securing-the-permanent-subscription)
-   [Impostazione di una Administrator-Only SD](#setting-an-administrator-only-sd)
-   [Rappresentazione dell'identità del provider di eventi](#impersonating-the-event-provider-identity)
-   [SID e sottoscrizioni permanenti](#sids-and-permanent-subscriptions)
-   [Creazione di sottoscrizioni permanenti tramite account di dominio](#creating-permanent-subscriptions-using-domain-accounts)
-   [Argomenti correlati](#related-topics)

## <a name="securing-temporary-consumers"></a>Protezione dei consumer temporanei

Un [*consumer temporaneo*](gloss-t.md) viene eseguito fino al riavvio del sistema o all'arresto di WMI, ma non può essere avviato se viene generato un evento specifico. Ad esempio, una chiamata a [**SWbemServices.ExecNotificationQueryAsync crea**](swbemservices-execnotificationqueryasync.md) un consumer temporaneo.

Le chiamate [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) o [**IWbemServices::ExecNotificationQuery creano**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) consumer di eventi temporanei. I consumer temporanei non possono controllare chi fornisce eventi al [*sink di evento*](gloss-s.md) creato.

Le chiamate [**ai metodi ExecNotificationQuery**](swbemservices-execnotificationquery.md) possono essere effettuate in modo sincrono, [*semisincronousamente*](gloss-s.md)o in modo asincrono. Ad esempio, [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) è un metodo sincrono che può essere chiamato in modo semisincronous, a seconda della modalità di impostazione del parametro *iflags.* [**SWbemServices.ExecNotificationQueryAsync è**](swbemservices-execnotificationqueryasync.md) una chiamata asincrona.

Tenere presente che il callback al sink per le versioni asincrone di queste chiamate potrebbe non essere restituito allo stesso livello di autenticazione della chiamata effettuata dallo script. È pertanto consigliabile usare chiamate semisincrono anziché asincrone. Se è necessaria la comunicazione asincrona, vedere [Chiamata di un metodo e](calling-a-method.md) Impostazione della sicurezza in una chiamata [asincrona.](setting-security-on-an-asynchronous-call.md)

I sottoscrittori di script non possono controllare i diritti di accesso di un provider di eventi per fornire eventi al sink creato dallo script. Pertanto, è consigliabile che le [**chiamateSWbemServices.ExecNotificationQuery usino**](swbemservices-execnotificationquery.md) la forma semisincrono della chiamata e usino impostazioni di sicurezza specifiche. Per altre informazioni, vedere [Esecuzione di una chiamata semisincrono con VBScript.](making-a-semisynchronous-call-with-vbscript.md)

## <a name="securing-permanent-consumers"></a>Protezione dei consumer permanenti

Un [*consumer permanente*](gloss-p.md) ha una sottoscrizione permanente agli eventi di un provider di eventi che verranno mantenuti dopo il riavvio del sistema operativo. Un provider di eventi che supporta consumer permanenti è un [*provider di consumer di eventi*](gloss-e.md). Se il provider di eventi non è in esecuzione quando si verifica un evento, WMI avvia il provider quando deve recapitare gli eventi. WMI identifica il provider di consumer a cui devono essere recapitati gli eventi, in base all'istanza [**\_ \_ EventConsumerProviderRegistration,**](--eventconsumerproviderregistration.md) che associa l'istanza [**\_ \_ Win32Provider**](--win32provider.md) del provider di consumer a una classe [*consumer*](gloss-l.md) logica definita dal provider di consumer. Per altre informazioni sul ruolo dei provider di consumer, vedere [Scrittura di un provider di consumer di eventi.](writing-an-event-consumer-provider.md)

I consumer permanenti possono controllare chi invia gli eventi e i provider di eventi possono controllare chi accede ai propri eventi.

Le applicazioni e gli script client creano istanze della classe consumer logica come parte di una sottoscrizione. La classe consumer logica definisce le informazioni contenute nell'evento, le operazioni che il client può eseguire con l'evento e la modalità di recapito dell'evento.

Le classi [consumer standard](standard-consumer-classes.md) WMI forniscono esempi del ruolo delle classi consumer logiche. Per altre informazioni, vedere [Monitoraggio e risposta agli eventi con consumer standard.](monitoring-and-responding-to-events-with-standard-consumers.md)

## <a name="securing-the-permanent-subscription"></a>Protezione della sottoscrizione permanente

Le sottoscrizioni permanenti hanno maggiori potenzialità di causare problemi di sicurezza in WMI e pertanto hanno i requisiti di sicurezza seguenti:

-   Le istanze del consumer logico, [**\_ \_ EventFilter**](--eventfilter.md)e [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) devono avere lo stesso ID di sicurezza (SID) nella **proprietà CreatorSID.** Per altre informazioni, vedere [Mantenimento dello stesso SID in tutte le istanze di una sottoscrizione permanente.](#sids-and-permanent-subscriptions)
-   L'account che crea la sottoscrizione deve essere un account di dominio con privilegi di amministratore locale o l'account del gruppo Administrators locale. L'uso del SID del gruppo Administrators consente alla sottoscrizione di continuare a funzionare nel computer locale, anche se è disconnessa dalla rete. L'uso di un account di dominio consente l'identificazione esatta dell'utente.

    Tuttavia, se il computer non è connesso e l'account di creazione è un account di dominio, il consumer ha esito negativo perché WMI non è in grado di verificare l'identità dell'account. Per evitare errori di sottoscrizione se il computer è disconnesso dalla rete, usare il SID del gruppo Administrators per una sottoscrizione. In questo caso, è necessario assicurarsi che l'account LocalSystem possa accedere ai dati di appartenenza ai gruppi nel dominio. Alcuni provider di consumer di eventi hanno requisiti di sicurezza particolarmente elevati, poiché una sottoscrizione non autorizzata può causare gravi danni. Ad esempio, i consumer standard [**ActiveScriptEventConsumer**](activescripteventconsumer.md) [**e CommandLineEventConsumer.**](commandlineeventconsumer.md)

-   È possibile configurare la sottoscrizione permanente in modo che accetti solo eventi da identità specifiche del provider di eventi. Impostare il descrittore di sicurezza nella **proprietà EventAccess** dell'istanza [**\_ \_ di EventFilter**](--eventfilter.md) sull'identità del provider di eventi. WMI confronta l'identità del provider di eventi con il descrittore di sicurezza per determinare se il provider dispone **dell'accesso WBEM \_ RIGHT \_ PUBLISH.** Per altre informazioni, vedere [Costanti di sicurezza WMI.](wmi-security-constants.md)

    Se il filtro consente l'accesso all'identità del provider di eventi, considera attendibile anche l'evento. In questo modo il consumer che ha ricevuto l'evento può generare un evento delegato.

    **Nota**  Il valore predefinito per il descrittore di sicurezza in **EventAccess** è **NULL,** che consente l'accesso a tutti gli utenti. È consigliabile limitare l'accesso nell'istanza della sottoscrizione di [**\_ \_ EventFilter**](--eventfilter.md) per una migliore sicurezza degli eventi.

## <a name="setting-an-administrator-only-sd"></a>Impostazione di una Administrator-Only SD

L'esempio di codice C++ seguente crea un descrittore di sicurezza solo amministratore [**\_ \_ nell'istanza eventFilter.**](--eventfilter.md) Questo esempio crea il descrittore di sicurezza usando [SDDL (Security Descriptor Definition Language).](/windows/desktop/SecAuthZ/security-descriptor-definition-language) Per altre informazioni su **WBEM \_ RIGHT \_ SUBSCRIBE,** vedere [Costanti di sicurezza WMI.](wmi-security-constants.md)


```C++
// Create SD that allows only administrators 
//    to send events to this filter. 
// The SDDL settings are O:BAG:BAD:(A;;0x80;;;BA)
// Set the EventAccess property in the 
//    IWbemClassObject of the __EventFilter instance. 
   long lMask = WBEM_RIGHT_PUBLISH;
     WCHAR wBuf[MAX_PATH];
     _ltow( lMask, wBuf, 16 );
 
HRESULT hRes = pEventFilterInstance->Put( L"EventAccess", 0,
    &_variant_t( L"O:BAG:BAD:(A;;0x80;;;BA)" ), NULL );
```



L'esempio di codice precedente richiede il riferimento seguente e \# le istruzioni include.


```C++
#define _WIN32_DCOM
#include <wbemidl.h>
#include <comdef.h>

#pragma comment(lib, "wbemuuid.lib")
```



## <a name="impersonating-the-event-provider-identity"></a>Rappresentazione dell'identità del provider di eventi

Un consumer permanente potrebbe dover rappresentare il provider di eventi per elaborare l'evento. I consumer permanenti possono rappresentare il provider di eventi solo quando si verificano le condizioni seguenti:

-   L'istanza [**\_ \_ di FilterToConsumerBinding**](--filtertoconsumerbinding.md) ha la **proprietà MaintainSecurityContext** impostata su **True.**
-   Un evento viene recapitato nello stesso contesto di sicurezza in cui si trova il provider quando ha generato l'evento. Solo un consumer implementato come DLL, un consumer in-process, può ricevere eventi nel contesto di sicurezza del provider. Per altre informazioni sulla sicurezza di provider e consumer in-process, vedere [Hosting e sicurezza dei provider.](provider-hosting-and-security.md)
-   Il provider di eventi è in esecuzione in un processo che consente la rappresentazione.

L'account che esegue il processo consumer deve avere accesso **\_ FULL WRITE** al repository WMI (noto anche come repository CIM). Nella sottoscrizione, le istanze [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md), [**\_ \_ EventConsumer**](--eventconsumer.md)ed [**\_ \_ EventFilter**](--eventfilter.md) devono avere lo stesso valore di ID di sicurezza (SID) singolo nella **proprietà CreatorSID** . WMI archivia il SID in **CreatorSID** per ogni istanza.

## <a name="sids-and-permanent-subscriptions"></a>SID e sottoscrizioni permanenti

Una sottoscrizione permanente non funziona quando l'associazione, il consumer e il filtro non vengono creati dallo stesso utente, il che significa che [**\_ \_ FilterToConsumerBinding,**](--filtertoconsumerbinding.md) [**\_ \_ EventConsumer**](--eventconsumer.md)e [**\_ \_ EventFilter**](--eventfilter.md) devono avere lo stesso valore di ID di sicurezza (SID) singolo nella proprietà **CreatorSID.** Windows Strumentazione gestione (WMI) archivia questo valore.

## <a name="creating-permanent-subscriptions-using-domain-accounts"></a>Creazione di sottoscrizioni permanenti tramite account di dominio

Quando si usano account di dominio per creare sottoscrizioni permanenti, è necessario considerare diversi problemi. Ogni sottoscrizione permanente dovrebbe comunque funzionare quando nessun utente è connesso, ovvero funziona con l'account LocalSystem predefinito.

Se un utente di dominio è l'autore di una sottoscrizione permanente per i consumer sensibili alla sicurezza ([**ActiveScriptEventConsumer**](activescripteventconsumer.md), [**CommandLineEventConsumer**](commandlineeventconsumer.md)), WMI verifica se la proprietà **CreatorSID** della classe [**\_ \_ EventFilter,**](--eventfilter.md) [**\_ \_ della classe FilterToConsumerBinding**](--filtertoconsumerbinding.md) e delle istanze del consumer appartiene a un utente membro del gruppo Administrators locale.

L'esempio di codice seguente illustra come specificare la **proprietà CreatorSID.**

``` syntax
 instance of __EventFilter as $FILTER
    {
        // this is the Administrators SID in array of bytes format
        CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};    
        // Add filter code here ...
    }

    instance of ActiveScriptEventConsumer as $CONSUMER
    {
       CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};
       // Add consumer code here ...
    }

    instance of __FilterToConsumerBinding
    {
       CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};
       Consumer = $CONSUMER;
       Filter = $FILTER;
       // Add binding code here ...
    }
```

Per le situazioni tra domini, aggiungere Authenticated Users al "Windows authorization access group".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Protezione degli eventi WMI](securing-wmi-events.md)
</dt> <dt>

[Ricezione di un evento WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
