---
description: La classe CommandLineEventConsumer esegue un programma eseguibile specificato da una riga di comando quando si verifica un evento specificato. Questa classe è un consumer di eventi standard fornito da WMI.
ms.assetid: b912a4a1-7b1c-43a9-b098-fcfd62a2c2db
ms.tgt_platform: multiple
title: Esecuzione di un programma dalla riga di comando in base a un evento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: de7f4fb5e679a6b5767635c70e2ffb5eda3ba800
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309901"
---
# <a name="running-a-program-from-the-command-line-based-on-an-event"></a>Esecuzione di un programma dalla riga di comando in base a un evento

La classe [**CommandLineEventConsumer**](commandlineeventconsumer.md) esegue un programma eseguibile specificato da una riga di comando quando si verifica un evento specificato. Questa classe è un consumer di eventi standard fornito da WMI.

Quando si usa [**CommandLineEventConsumer**](commandlineeventconsumer.md), è necessario proteggere il file eseguibile che si vuole avviare. Se il file eseguibile non si trova in una posizione sicura o non è protetto con un elenco di controllo di accesso (ACL) sicuro, un utente senza privilegi di accesso può sostituire l'eseguibile con un file eseguibile diverso. È possibile utilizzare le classi [**Win32 \_ LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) o [**Win32 \_ LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) per modificare a livello di codice la sicurezza di un file o di una condivisione. Per ulteriori informazioni, vedere [creazione di un descrittore di sicurezza per un nuovo oggetto in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

La procedura di base per l'uso di consumer standard è sempre la stessa e si trova nel [monitoraggio e nella risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md). La procedura seguente aggiunge alla procedura di base, è specifica della classe [**CommandLineEventConsumer**](commandlineeventconsumer.md) e descrive come creare un consumer di eventi che esegue un programma.

> [!Caution]
>
> La classe [**CommandLineEventConsumer**](commandlineeventconsumer.md) presenta vincoli di sicurezza speciali. Questo consumer standard deve essere configurato da un membro locale del gruppo Administrators nel computer locale. Se si utilizza un account di dominio per creare la sottoscrizione, è necessario che l'account LocalSystem disponga delle autorizzazioni necessarie per il dominio per verificare che il creatore sia un membro del gruppo Administrators locale.
>
> Non è possibile usare [**CommandLineEventConsumer**](commandlineeventconsumer.md) per avviare un processo che viene eseguito in modo interattivo.

 

Nella procedura seguente viene descritto come creare un consumer di eventi che esegue un processo da una riga di comando.

**Per creare un consumer di eventi che esegue un processo da una riga di comando**

1.  Nel file Managed Object Format (MOF) creare un'istanza di [**CommandLineEventConsumer**](commandlineeventconsumer.md) per ricevere gli eventi richiesti nella query. Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).
2.  Creare un'istanza di [**\_ \_ EventFilter**](--eventfilter.md) e assegnarle un nome.
3.  Creare una query per specificare il tipo di evento. Per ulteriori informazioni, vedere [esecuzione di query con WQL](querying-with-wql.md).
4.  Creare un'istanza di [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) per associare il filtro all'istanza di [**CommandLineEventConsumer**](commandlineeventconsumer.md).
5.  Compilare il file MOF usando [**Mofcomp.exe**](mofcomp.md).

## <a name="example"></a>Esempio

Nell'esempio di codice seguente viene creata una nuova classe denominata "MyCmdLineConsumer" per generare eventi quando viene creata un'istanza della nuova classe alla fine di un file MOF. L'esempio è nel codice MOF, ma è possibile creare le istanze a livello di programmazione usando l' [API di scripting per WMI](scripting-api-for-wmi.md) o l' [API com per WMI](com-api-for-wmi.md).

Nella procedura seguente viene descritto come creare una nuova classe denominata MyCmdLineConsumer.

**Per creare una nuova classe denominata MyCmdLineConsumer**

1.  Creare il \\ \_ file ditest.bat c: cmdline con un comando che esegue un programma visibile, ad esempio "calc.exe".
2.  Copiare il file MOF in un file di testo e salvarlo con un'estensione MOF.
3.  In una finestra di comando compilare il file MOF usando il comando seguente: **mofcomp nomefile. mof**.

> [!Note]  
> Il programma specificato in cmdline \_test.bat deve essere eseguito.

 

``` syntax
// Set the namespace as root\subscription.
// The CommandLineEventConsumer is already compiled
// in the root\subscription namespace. 
#pragma namespace ("\\\\.\\Root\\subscription")

class MyCmdLineConsumer
{
 [key]string Name;
};

// Create an instance of the command line consumer
// and give it the alias $CMDLINECONSUMER

instance of CommandLineEventConsumer as $CMDLINECONSUMER
{
 Name = "CmdLineConsumer_Example";
 CommandLineTemplate = "c:\\cmdline_test.bat";
 RunInteractively = True;
 WorkingDirectory = "c:\\";
};    

// Create an instance of the event filter
// and give it the alias $CMDLINEFILTER
// The filter queries for instance creation event
// for instances of the MyCmdLineConsumer class

instance of __EventFilter as $CMDLINEFILTER
{
    Name = "CmdLineFilter";
    Query = "SELECT * FROM __InstanceCreationEvent"
        " WHERE TargetInstance.__class = \"MyCmdLineConsumer\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding
// between filter and consumer instances.

instance of __FilterToConsumerBinding
{
     Consumer = $CMDLINECONSUMER;
     Filter = $CMDLINEFILTER;
};

// Create an instance of this class right now. 
// The commands in c:\\cmdline_test.bat execute
// as the result of creating the instance
// of MyCmdLineConsumer.
 
instance of MyCmdLineConsumer
{
     Name = "CmdLineEventConsumer test";
};
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
