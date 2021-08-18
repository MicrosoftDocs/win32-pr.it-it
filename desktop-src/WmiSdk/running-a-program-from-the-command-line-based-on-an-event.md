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
ms.openlocfilehash: 9c499713b3c6496759d94229e291138b0cb07de9e9f35d116eb19b4a7aeb3829
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553970"
---
# <a name="running-a-program-from-the-command-line-based-on-an-event"></a>Esecuzione di un programma dalla riga di comando in base a un evento

La [**classe CommandLineEventConsumer**](commandlineeventconsumer.md) esegue un programma eseguibile specificato da una riga di comando quando si verifica un evento specificato. Questa classe è un consumer di eventi standard fornito da WMI.

Quando si usa [**CommandLineEventConsumer**](commandlineeventconsumer.md), è necessario proteggere l'eseguibile da avviare. Se l'eseguibile non si trova in una posizione sicura o non è protetto con un elenco di controllo di accesso sicuro , un utente senza privilegi di accesso può sostituire l'eseguibile con un file eseguibile diverso. È possibile usare le [**classi \_ LogicalFileSecuritySetting Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) o [**\_ Win32 LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) per modificare a livello di codice la sicurezza di un file o di una condivisione. Per altre informazioni, vedere [Creazione di un descrittore di sicurezza per un nuovo oggetto in C++.](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--)

La procedura di base per usare i consumer standard è sempre la stessa e si trova in Monitoraggio e risposta [agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md). La procedura seguente aggiunge alla routine di base, è specifica della classe [**CommandLineEventConsumer**](commandlineeventconsumer.md) e descrive come creare un consumer di eventi che esegue un programma.

> [!Caution]
>
> La [**classe CommandLineEventConsumer**](commandlineeventconsumer.md) ha vincoli di sicurezza speciali. Questo consumer standard deve essere configurato da un membro locale del gruppo Administrators nel computer locale. Se si usa un account di dominio per creare la sottoscrizione, l'account LocalSystem deve disporre delle autorizzazioni necessarie per il dominio per verificare che l'autore sia membro del gruppo Administrators locale.
>
> [**CommandLineEventConsumer**](commandlineeventconsumer.md) non può essere usato per avviare un processo eseguito in modo interattivo.

 

La procedura seguente descrive come creare un consumer di eventi che esegue un processo da una riga di comando.

**Per creare un consumer di eventi che esegue un processo da una riga di comando**

1.  Nel file Managed Object Format (MOF) creare un'istanza di [**CommandLineEventConsumer**](commandlineeventconsumer.md) per ricevere gli eventi richiesta nella query. Per altre informazioni, vedere [Progettazione di Managed Object Format (MOF).](designing-managed-object-format--mof--classes.md)
2.  Creare un'istanza di [**\_ \_ EventFilter**](--eventfilter.md) e assegnargli un nome.
3.  Creare una query per specificare il tipo di evento. Per altre informazioni, vedere [Esecuzione di query con WQL.](querying-with-wql.md)
4.  Creare [**\_ \_ un'istanza di FilterToConsumerBinding**](--filtertoconsumerbinding.md) per associare il filtro all'istanza di [**CommandLineEventConsumer**](commandlineeventconsumer.md).
5.  Compilare il file MOF [**usando**](mofcomp.md)Mofcomp.exe.

## <a name="example"></a>Esempio

Nell'esempio di codice seguente viene creata una nuova classe denominata "MyCmdLineConsumer" per generare eventi quando viene creata un'istanza della nuova classe alla fine di un file MOF. L'esempio è in codice MOF, ma è possibile creare le istanze a livello di codice usando [l'API scripting](scripting-api-for-wmi.md) per WMI o [l'API COM per WMI](com-api-for-wmi.md).

La procedura seguente descrive come creare una nuova classe denominata MyCmdLineConsumer.

**Per creare una nuova classe denominata MyCmdLineConsumer**

1.  Creare il file c: cmdlinetest.bat con un comando che esegue un programma visibile, ad esempio \\ \_ "calc.exe".
2.  Copiare il file MOF in un file di testo e salvarlo con estensione mof.
3.  In un finestra di comando compilare il file MOF usando il comando seguente: **Mofcomp filename.mof**.

> [!Note]  
> Il programma specificato nella riga di comando \_test.bat deve essere eseguito.

 

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

 

 
