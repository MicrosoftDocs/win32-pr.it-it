---
description: Usando la classe SMTPEventConsumer, è possibile inviare messaggi di posta elettronica a un utente designato quando si verifica un evento specificato. Questa classe è un consumer di eventi standard fornito da WMI.
ms.assetid: ed10e6f7-8e18-4cde-bd46-a7791547c7da
ms.tgt_platform: multiple
title: Invio di messaggi di posta elettronica in base a un evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68bcef0858f7022fcb36006f038b20dedc940da60ee6c61e0372f5a74663093a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860419"
---
# <a name="sending-email-based-on-an-event"></a>Invio di messaggi di posta elettronica in base a un evento

Usando la [classe SMTPEventConsumer,](smtpeventconsumer.md) è possibile inviare messaggi di posta elettronica a un utente designato quando si verifica un evento specificato. Questa classe è un [consumer di eventi standard](standard-consumer-classes.md) fornito da WMI.

La [classe SMTPEventConsumer](smtpeventconsumer.md) richiede le condizioni seguenti per inviare un messaggio di posta elettronica in risposta a un evento:

-   La [classe SMTPEventConsumer](smtpeventconsumer.md) deve essere compilata nello spazio dei nomi corretto. Per altre informazioni, vedere [Monitoraggio e risposta agli eventi con consumer standard.](monitoring-and-responding-to-events-with-standard-consumers.md)
-   Nella rete deve esistere un server SMTP.
-   Il messaggio di posta elettronica non può avere un allegato.
-   Il messaggio di posta elettronica deve essere codificato in US-ASCII.

La procedura di base per l'uso di consumer standard è sempre la stessa e si trova in Monitoraggio e risposta [agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md). La procedura seguente aggiunge alla procedura di base. è specifico della [classe SMTPEventConsumer.](smtpeventconsumer.md) e descrive come creare un consumer di eventi che invia messaggi di posta elettronica.

La procedura seguente descrive come creare un consumer di eventi che invia messaggi di posta elettronica.

**Per creare un consumer di eventi che invia messaggi di posta elettronica**

1.  Installare e registrare la [classe SMTPEventConsumer,](smtpeventconsumer.md) se necessario.

    La [classe SMTPEventConsumer](smtpeventconsumer.md) viene compilata nello spazio dei nomi della \\ sottoscrizione radice dal programma di installazione WMI.

2.  Identificare l'evento che si desidera monitorare e creare la query di eventi.

    Potrebbe essere presente un evento intrinseco esistente che usa per monitorare l'evento. La maggior parte degli eventi intrinseci è associata alle modifiche alle istanze della classe nello spazio \\ dei nomi "cimv2 radice". Analizzando le classi nel riferimento alle classi [WMI,](wmi-classes.md) è probabilmente possibile trovare una classe che identifica l'evento da monitorare. Ad esempio, usare la [**classe \_ LogicalDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) per monitorare le modifiche apportate a un'unità disco rigido.

    Se non sono presenti eventi intrinseci esistenti che usano , potrebbe essere disponibile un provider di eventi estensivi che può funzionare. Ad esempio, usare la [**classe RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) del provider del Registro di sistema per monitorare le modifiche al Registro di sistema.

    Se non esiste una classe che identifica l'evento da monitorare, è necessario creare un provider di eventi personalizzato e definire nuove classi di evento estensivi. Per altre informazioni, vedere [Scrittura di un provider di eventi](writing-an-event-provider.md).

3.  Nel file Managed Object Format (MOF) creare un'istanza di [SMTPEventConsumer](smtpeventconsumer.md) per ricevere eventi.

    Usare le proprietà dell'istanza di per definire il messaggio di posta elettronica da inviare quando si verifica un evento. Ad esempio, la **proprietà ToLine** definisce l'indirizzo di posta elettronica e la **proprietà Message** definisce il testo del messaggio di posta elettronica. È necessario definire l'indirizzo di posta elettronica, l'oggetto e il testo di un messaggio, ma un messaggio di posta elettronica non può avere un allegato. Per altre informazioni, vedere [Progettazione di Managed Object Format (MOF).](designing-managed-object-format--mof--classes.md)

4.  Creare una query di eventi che specifica gli eventi da monitorare.

    Per altre informazioni, vedere [Esecuzione di query con WQL.](querying-with-wql.md)

5.  Creare un'istanza di [**\_ \_ EventFilter**](--eventfilter.md) e archiviare la query nella **proprietà Query.**

    Per altre informazioni, vedere [Esecuzione di query con WQL.](querying-with-wql.md)

6.  Creare un'istanza [**\_ \_ di FilterToConsumerBinding**](--filtertoconsumerbinding.md) per associare il filtro e il consumer.
7.  Compilare il file MOF [**usando**](mofcomp.md)Mofcomp.exe.


## <a name="example"></a>Esempio

L'esempio in questa sezione è in codice MOF, ma è possibile creare le istanze a livello di codice usando [l'API scripting](scripting-api-for-wmi.md) per WMI o [l'API COM per WMI.](com-api-for-wmi.md)

La procedura seguente descrive come usare l'esempio.

**Per usare l'esempio**

1.  Copiare il file MOF seguente in un file di testo e salvarlo con estensione mof.
2.  In una finestra del prompt dei comandi compilare il file MOF usando il comando seguente:

    **Nome file Mofcomp***.mof** *

> [!Note]  
> Quando il codice MOF viene compilato nello spazio dei nomi della \\ sottoscrizione radice, [SMTPEventConsumer](smtpeventconsumer.md) viene compilato nello stesso spazio dei nomi.

 

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of __EventFilter as $FILTER
{
    Name = "LowDiskspaceFilter";
    
    EventNamespace = "\\\\.\\root\\cimv2";  

    Query = "SELECT * FROM __InstanceModificationEvent WITHIN 10 "
            "WHERE TargetInstance ISA \"Win32_LogicalDisk\" "
            "AND TargetInstance.FreeSpace < 846000000 "
            "AND PreviousInstance.FreeSpace >= 846000000 "
            "AND (TargetInstance.DeviceID = \"C:\" "
            "OR TargetInstance.DeviceID = \"D:\")";
    QueryLanguage = "WQL";
};


instance of SMTPEventConsumer as $CONSUMER
{
    Name = "LowDisk";
    ToLine = "SysAd@MyCompany.com, MyAlias@MyCompany.com";
    CcLine = "MyHome@MyISP.com";
    ReplyToLine = "MyAlias@MyCompany.com";
    SMTPServer = "SmartHost";
    Subject = "WARNING: Low disk space";
    Message = "WARNING: Your %TargetInstance.DeviceID% is"
        " getting dangerously low.";
};

instance of __FilterToConsumerBinding
{
    Consumer = $CONSUMER ;
    Filter = $FILTER ;
};
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
