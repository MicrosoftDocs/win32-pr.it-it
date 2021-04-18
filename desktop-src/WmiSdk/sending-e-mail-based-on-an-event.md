---
description: Utilizzando la classe SMTPEventConsumer, è possibile inviare un messaggio di posta elettronica a un utente designato quando si verifica un evento specifico. Questa classe è un consumer di eventi standard fornito da WMI.
ms.assetid: ed10e6f7-8e18-4cde-bd46-a7791547c7da
ms.tgt_platform: multiple
title: Invio di messaggi di posta elettronica in base a un evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4929b7c8c29d514d73a6e4c9d14049a19f306233
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313179"
---
# <a name="sending-email-based-on-an-event"></a>Invio di messaggi di posta elettronica in base a un evento

Utilizzando la classe [SMTPEventConsumer](smtpeventconsumer.md) , è possibile inviare un messaggio di posta elettronica a un utente designato quando si verifica un evento specifico. Questa classe è un [consumer di eventi standard](standard-consumer-classes.md) fornito da WMI.

Per inviare un messaggio di posta elettronica in risposta a un evento, la classe [SMTPEventConsumer](smtpeventconsumer.md) richiede le condizioni seguenti:

-   La classe [SMTPEventConsumer](smtpeventconsumer.md) deve essere compilata nello spazio dei nomi corretto. Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).
-   Un server SMTP deve esistere sulla rete.
-   Il messaggio di posta elettronica non può contenere un allegato.
-   Il messaggio di posta elettronica deve essere codificato in US-ASCII.

La procedura di base per l'utilizzo di consumer standard è sempre la stessa ed è disponibile per il [monitoraggio e la risposta a eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md). La procedura seguente consente di aggiungere alla procedura di base. è specifico della classe [SMTPEventConsumer](smtpeventconsumer.md) . e descrive come creare un consumer di eventi che invia un messaggio di posta elettronica.

Nella procedura seguente viene descritto come creare un consumer di eventi che invia un messaggio di posta elettronica.

**Per creare un consumer di eventi che invii un messaggio di posta elettronica**

1.  Installare e registrare la classe [SMTPEventConsumer](smtpeventconsumer.md) , se necessario.

    La classe [SMTPEventConsumer](smtpeventconsumer.md) viene compilata nello \\ spazio dei nomi della sottoscrizione radice dal programma di installazione di WMI.

2.  Identificare l'evento che si desidera monitorare e creare la query di eventi.

    Potrebbe esistere un evento intrinseco esistente che usa per monitorare l'evento. La maggior parte degli eventi intrinseci è associata alle modifiche apportate alle istanze di classe nello \\ spazio dei nomi "root cimv2". Analizzando le classi nel riferimento alle [classi WMI](wmi-classes.md) , probabilmente è possibile trovare una classe che identifichi l'evento che si desidera monitorare. Ad esempio, usare la classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) per monitorare le modifiche apportate a un'unità disco rigido.

    Se non sono presenti eventi intrinseci che usano, potrebbe essere disponibile un provider di eventi estrinseco che può funzionare. Utilizzare, ad esempio, la classe [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) del provider del registro di sistema per monitorare le modifiche apportate al registro di sistema.

    Se una classe non esiste che identifica l'evento che si desidera monitorare, è necessario creare un provider di eventi personalizzato e definire nuove classi di evento estrinseche. Per ulteriori informazioni, vedere [scrittura di un provider di eventi](writing-an-event-provider.md).

3.  Nel file Managed Object Format (MOF) creare un'istanza di [SMTPEventConsumer](smtpeventconsumer.md) per ricevere gli eventi.

    Utilizzare le proprietà dell'istanza per definire il messaggio di posta elettronica da inviare quando si verifica un evento. Ad esempio, la proprietà **ToLine** definisce l'indirizzo di posta elettronica e la proprietà **Message** definisce il testo del messaggio di posta elettronica. È necessario definire l'indirizzo di posta elettronica, l'oggetto e il testo di un messaggio, ma un messaggio di posta elettronica non può contenere un allegato. Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).

4.  Creare una query di eventi che specifichi gli eventi che si desidera monitorare.

    Per ulteriori informazioni, vedere [esecuzione di query con WQL](querying-with-wql.md).

5.  Creare un'istanza di [**\_ \_ EventFilter**](--eventfilter.md) e archiviare la query nella proprietà **query** .

    Per ulteriori informazioni, vedere [esecuzione di query con WQL](querying-with-wql.md).

6.  Creare un'istanza di [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) per associare il filtro e il consumer.
7.  Compilare il file MOF utilizzando [**Mofcomp.exe**](mofcomp.md).


## <a name="example"></a>Esempio

L'esempio in questa sezione è codice MOF, ma è possibile creare le istanze a livello di programmazione usando l' [API di scripting per WMI](scripting-api-for-wmi.md) o l' [API com per WMI](com-api-for-wmi.md).

Nella procedura riportata di seguito viene descritto come utilizzare l'esempio.

**Per usare l'esempio**

1.  Copiare il file MOF seguente in un file di testo e salvarlo con un'estensione MOF.
2.  In una finestra del prompt dei comandi compilare il file MOF usando il comando seguente:

    **Mofcomp** *nomefile * * *. mof**

> [!Note]  
> Quando il codice MOF viene compilato nello \\ spazio dei nomi della sottoscrizione radice, il [SMTPEventConsumer](smtpeventconsumer.md) viene compilato nello stesso spazio dei nomi.

 

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

 

 
