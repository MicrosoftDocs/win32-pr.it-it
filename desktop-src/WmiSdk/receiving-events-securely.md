---
description: I consumer temporanei e permanenti hanno metodi diversi per proteggere il recapito degli eventi.
ms.assetid: cd02e5db-f9e2-438b-9632-0a1387a6d4e3
ms.tgt_platform: multiple
title: Ricezione di eventi in modo sicuro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27d156213553ee17a346d780cbea0ff82beca83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314586"
---
# <a name="receiving-events-securely"></a>Ricezione di eventi in modo sicuro

I consumer temporanei e permanenti hanno metodi diversi per proteggere il recapito degli eventi.

Le sezioni seguenti sono illustrate in questo argomento:

-   [Protezione di consumer temporanei](#securing-temporary-consumers)
-   [Protezione di consumer permanenti](#securing-permanent-consumers)
-   [Protezione della sottoscrizione permanente](#securing-the-permanent-subscription)
-   [Impostazione di un Administrator-Only SD](#setting-an-administrator-only-sd)
-   [Rappresentazione dell'identità del provider di eventi](#impersonating-the-event-provider-identity)
-   [SID e sottoscrizioni permanenti](#sids-and-permanent-subscriptions)
-   [Creazione di sottoscrizioni permanenti tramite account di dominio](#creating-permanent-subscriptions-using-domain-accounts)
-   [Argomenti correlati](#related-topics)

## <a name="securing-temporary-consumers"></a>Protezione di consumer temporanei

Un [*consumer temporaneo*](gloss-t.md) viene eseguito fino al riavvio del sistema o all'arresto di WMI, ma non può essere avviato se viene generato un evento specifico. Ad esempio, una chiamata a [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) crea un consumer temporaneo.

Chiama [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) o [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) crea consumer di eventi temporanei. I consumer temporanei non possono controllare chi fornisce eventi al [*sink*](gloss-s.md) di evento che crea.

Le chiamate ai metodi [**ExecNotificationQuery**](swbemservices-execnotificationquery.md) possono essere eseguite in modo sincrono, [*semisincrona*](gloss-s.md)o in modo asincrono. Ad esempio, [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) è un metodo sincrono che può essere chiamato semisincrona, a seconda della modalità con cui viene impostato il parametro *iFlags* . [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) è una chiamata asincrona.

Tenere presente che il callback al sink per le versioni asincrone di queste chiamate potrebbe non essere restituito allo stesso livello di autenticazione della chiamata eseguita dallo script. È pertanto consigliabile utilizzare semisincrono anziché le chiamate asincrone. Se è necessaria la comunicazione asincrona, vedere [chiamata di un metodo](calling-a-method.md) e [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).

I sottoscrittori di scripting non possono verificare i diritti di accesso di un provider di eventi per fornire eventi al sink creato dallo script. È quindi consigliabile che le chiamate a [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) usino il form semisincrono della chiamata e usino impostazioni di sicurezza specifiche. Per ulteriori informazioni, vedere [creazione di una chiamata semisincrono con VBScript](making-a-semisynchronous-call-with-vbscript.md).

## <a name="securing-permanent-consumers"></a>Protezione di consumer permanenti

Un [*consumer permanente*](gloss-p.md) ha una sottoscrizione permanente agli eventi di un provider di eventi che verrà mantenuto dopo il riavvio del sistema operativo. Un provider di eventi che supporta gli utenti permanenti è un [*provider di consumer di eventi*](gloss-e.md). Se il provider di eventi non è in esecuzione quando si verifica un evento, WMI avvia il provider quando è necessario recapitare gli eventi. WMI identifica il provider di consumer a cui devono essere recapitati gli eventi, in base all'istanza di [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) , che associa l'istanza [**\_ \_ Win32Provider**](--win32provider.md) del provider consumer a una [*classe consumer logica*](gloss-l.md) definita dal provider consumer. Per ulteriori informazioni sul ruolo dei provider di consumer, vedere [scrittura di un provider di consumer di eventi](writing-an-event-consumer-provider.md).

I consumer permanenti possono controllare chi li invia e i provider di eventi possono controllare chi accede agli eventi.

Gli script client e le applicazioni creano istanze della classe consumer logica come parte di una sottoscrizione. La classe consumer logica definisce le informazioni contenute nell'evento, le operazioni che il client può eseguire con l'evento e il modo in cui viene recapitato l'evento.

Le [classi consumer standard](standard-consumer-classes.md) WMI forniscono esempi del ruolo delle classi consumer logiche. Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).

## <a name="securing-the-permanent-subscription"></a>Protezione della sottoscrizione permanente

Le sottoscrizioni permanenti hanno maggiori possibilità di causare problemi di sicurezza in WMI e pertanto presentano i requisiti di sicurezza seguenti:

-   L'istanza del consumer logico, le istanze [**\_ \_ EventFilter**](--eventfilter.md)e [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) devono avere lo stesso ID di sicurezza (SID) singolo nella proprietà **CreatorSID** . Per altre informazioni, vedere [mantenere lo stesso SID in tutte le istanze di una sottoscrizione permanente](#sids-and-permanent-subscriptions).
-   L'account che crea la sottoscrizione deve essere un account di dominio con privilegi di amministratore locale o l'account del gruppo Administrators locale. L'utilizzo del SID del gruppo Administrators consente alla sottoscrizione di continuare a lavorare nel computer locale, anche se è disconnesso dalla rete. L'utilizzo di un account di dominio consente l'identificazione esatta dell'utente.

    Tuttavia, se il computer non è connesso e l'account di creazione è un account di dominio, il consumer non riesce perché WMI non è in grado di verificare l'identità dell'account. Per evitare errori di sottoscrizione se il computer è disconnesso dalla rete, utilizzare il SID del gruppo Administrators per una sottoscrizione. In tal caso, è necessario assicurarsi che l'account LocalSystem possa accedere ai dati di appartenenza a gruppi nel dominio. Alcuni provider di consumer di eventi hanno requisiti di sicurezza particolarmente elevati, perché una sottoscrizione non autorizzata può causare gravi danni. Gli esempi sono gli utenti standard, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) e [**CommandLineEventConsumer**](commandlineeventconsumer.md).

-   È possibile configurare la sottoscrizione permanente in modo da accettare solo gli eventi da identità specifiche del provider di eventi. Impostare il descrittore di sicurezza nella proprietà **EventAccess** dell'istanza [**\_ \_ EventFilter**](--eventfilter.md) sulle identità del provider di eventi. Tramite WMI viene confrontata l'identità del provider di eventi con il descrittore di sicurezza per determinare se il provider ha l'accesso a destra per la **\_ \_ pubblicazione** . Per ulteriori informazioni, vedere la pagina relativa alle [costanti di sicurezza WMI](wmi-security-constants.md).

    Se il filtro consente l'accesso all'identità del provider di eventi, viene considerato attendibile anche l'evento. Ciò consente al consumer che ha ricevuto l'evento di generare un evento delegato.

    **Nota**  Il valore predefinito per il descrittore di sicurezza in **EventAccess** è **null**, che consente l'accesso a tutti gli utenti. La limitazione dell'accesso nell'istanza di sottoscrizione di [**\_ \_ EventFilter**](--eventfilter.md) è consigliata per una migliore sicurezza degli eventi.

## <a name="setting-an-administrator-only-sd"></a>Impostazione di un Administrator-Only SD

Nell'esempio di codice C++ riportato di seguito viene creato un descrittore di sicurezza solo amministratore nell'istanza [**\_ \_ EventFilter**](--eventfilter.md) . In questo esempio viene creato il descrittore di sicurezza utilizzando il linguaggio SDDL ( [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) ). Per ulteriori informazioni sulla **\_ \_ sottoscrizione a destra di WBEM**, vedere la pagina relativa alle costanti di [sicurezza WMI](wmi-security-constants.md).


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



Nell'esempio di codice precedente sono richieste le seguenti \# istruzioni Reference e include.


```C++
#define _WIN32_DCOM
#include <wbemidl.h>
#include <comdef.h>

#pragma comment(lib, "wbemuuid.lib")
```



## <a name="impersonating-the-event-provider-identity"></a>Rappresentazione dell'identità del provider di eventi

Un consumer permanente potrebbe dover rappresentare il provider di eventi per elaborare l'evento. I consumer permanenti possono rappresentare il provider di eventi solo quando sussistono le condizioni seguenti:

-   L'istanza di [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) ha la proprietà **MaintainSecurityContext** impostata su **true**.
-   Un evento viene recapitato nello stesso contesto di sicurezza in cui si trovava il provider durante la generazione dell'evento. Solo un consumer implementato come DLL, un consumer in-process, può ricevere eventi nel contesto di sicurezza del provider. Per ulteriori informazioni sulla sicurezza dei provider e dei consumer in-process, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md).
-   Il provider di eventi viene eseguito in un processo che consente la rappresentazione.

L'account che esegue il processo consumer deve avere accesso in **\_ scrittura completo** al repository WMI (noto anche come repository CIM). Nella sottoscrizione, le istanze [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md), [**\_ \_ EventConsumer**](--eventconsumer.md)e [**\_ \_ EventFilter**](--eventfilter.md) devono avere lo stesso valore SID (Single Security Identifier) nella proprietà **CreatorSID** . WMI archivia il SID in **CreatorSID** per ogni istanza.

## <a name="sids-and-permanent-subscriptions"></a>SID e sottoscrizioni permanenti

Una sottoscrizione permanente non funziona quando l'associazione, il consumer e il filtro non vengono creati dallo stesso utente, il che significa che [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md), [**\_ \_ EventConsumer**](--eventconsumer.md)e [**\_ \_ EventFilter**](--eventfilter.md) devono avere lo stesso valore SID (Single Security Identifier) della proprietà **CreatorSID** . In Strumentazione gestione Windows (WMI) viene archiviato questo valore.

## <a name="creating-permanent-subscriptions-using-domain-accounts"></a>Creazione di sottoscrizioni permanenti tramite account di dominio

Quando si utilizzano account di dominio per creare sottoscrizioni permanenti, è necessario considerare diversi problemi. Ogni sottoscrizione permanente dovrebbe continuare a funzionare quando nessun utente è connesso, il che significa che funzionano con l'account LocalSystem incorporato.

Se un utente di dominio è il creatore di una sottoscrizione permanente per i consumer sensibili alla sicurezza ([**ActiveScriptEventConsumer**](activescripteventconsumer.md), [**CommandLineEventConsumer**](commandlineeventconsumer.md)), WMI verifica se la proprietà **CreatorSID** della classe [**\_ \_ EventFilter**](--eventfilter.md) , la classe [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) e le istanze del consumer appartengono a un utente che è membro del gruppo Administrators locale.

Nell'esempio di codice riportato di seguito viene illustrato come è possibile specificare la proprietà **CreatorSID** .

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

Per le situazioni tra domini, aggiungere utenti autenticati al gruppo di accesso di autorizzazione Windows.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Protezione degli eventi WMI](securing-wmi-events.md)
</dt> <dt>

[Ricezione di un evento WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
