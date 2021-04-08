---
description: Il consumer standard implementato dalla classe ActiveScriptEventConsumer consente a un computer di eseguire uno script e di intervenire quando si verificano eventi importanti per garantire che un computer possa rilevare e risolvere automaticamente i problemi.
ms.assetid: 0d2ac139-3e2b-4089-ae9c-289d376e27a2
ms.tgt_platform: multiple
title: Esecuzione di uno script basato su un evento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4dbb1e55c7828a79d6541182eff5ce20147a82c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884777"
---
# <a name="running-a-script-based-on-an-event"></a>Esecuzione di uno script basato su un evento

Il consumer standard implementato dalla classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) consente a un computer di eseguire uno script e di intervenire quando si verificano eventi importanti per garantire che un computer possa rilevare e risolvere automaticamente i problemi.

Questo consumer viene caricato per impostazione predefinita nello spazio dei nomi della **\\ sottoscrizione radice** .

È possibile configurare le prestazioni di tutte le istanze di [**ActiveScriptEventConsumer**](activescripteventconsumer.md) in un sistema impostando i valori della proprietà **timeout** o **MaximumScripts** in una singola istanza di [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md).

La procedura di base per l'utilizzo di consumer standard è sempre la stessa ed è disponibile per il [monitoraggio e la risposta a eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md). La procedura seguente che aggiunge alla procedura di base è specifica della classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) e descrive come creare un consumer di eventi che esegue uno script.

> [!Caution]  
> La classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) presenta vincoli di sicurezza speciali. Questo consumer standard deve essere configurato da un membro locale del gruppo Administrators nel computer locale. Se si utilizza un account di dominio per creare la sottoscrizione, è necessario che l'account LocalSystem disponga delle autorizzazioni necessarie per il dominio per verificare che il creatore sia un membro del gruppo Administrators locale.

 

Nella procedura seguente viene descritto come creare un consumer di eventi per l'esecuzione di uno script.

**Per creare un consumer di eventi che esegue uno script**

1.  Scrivere lo script da eseguire quando si verifica un evento.

    È possibile scrivere lo script in qualsiasi linguaggio, ma assicurarsi che nel computer sia installato un motore di scripting per la lingua scelta. Lo script non deve usare oggetti di scripting WMI.

    Solo un amministratore può configurare un consumer di script e lo script viene eseguito con le credenziali LocalSystem, che offre ampie funzionalità al consumer, ad eccezione dell'accesso alla rete. Tuttavia, lo script non ha accesso a dati di accesso utente specifici, ad esempio le variabili di ambiente e le condivisioni di rete.

2.  Nel file Managed Object Format (MOF) creare un'istanza di [**ActiveScriptEventConsumer**](activescripteventconsumer.md) per ricevere gli eventi richiesti nella query.

    È possibile inserire il testo dello script in **ScriptText** oppure specificare il percorso e il nome file dello script in **ScriptFileName**. Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).

3.  Creare un'istanza di [**\_ \_ EventFilter**](--eventfilter.md), denominarla, quindi creare una query per specificare il tipo di evento che attiva l'esecuzione dello script.

    Per ulteriori informazioni, vedere [esecuzione di query con WQL](querying-with-wql.md).

4.  Creare un'istanza di [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) per associare il filtro all'istanza di [**ActiveScriptEventConsumer**](activescripteventconsumer.md).
5.  Compilare il file MOF utilizzando [**Mofcomp.exe**](mofcomp.md).

Gli esempi nella sezione seguente illustrano due modi per implementare uno script basato su eventi. Nel primo esempio viene utilizzato uno script definito in un file esterno, mentre nel secondo viene utilizzato uno script incorporato nel codice MOF. Gli esempi sono disponibili nel codice MOF, ma è possibile creare le istanze a livello di programmazione usando l' [API di scripting per WMI](scripting-api-for-wmi.md) o l' [API com per WMI](com-api-for-wmi.md).

## <a name="example-using-an-external-script"></a>Esempio di utilizzo di uno script esterno

Nella procedura seguente viene descritto come utilizzare l'esempio di script esterno.

**Per usare l'esempio di script esterno**

1.  Creare un file denominato c: \\Asec.vbs, quindi copiare lo script in questo esempio.
2.  Copiare l'elenco MOF in un file di testo e salvarlo con un'estensione MOF.
3.  In una finestra del prompt dei comandi compilare il file MOF usando il comando seguente.

    **Mofcomp** *nomefile * * *. mof**

4.  Eseguire la calcolatrice, che consente di creare un processo di calc.exe. Attendere più di cinque secondi, chiudere la finestra del calcolatore e cercare \\ un file denominato ASEC. log nella directory C:.

    Il testo seguente è simile al testo che sarà contenuto nel file ASEC. log.

    ``` syntax
    Time: 12/31/2002 2:56:33 PM; Entry made by: ASEC
    Application closed. UserModeTime:  1562500; 
    KernelModeTime: 3125000 [hundreds of nanoseconds]
    ```

Nell'esempio di codice VBScript riportato di seguito viene illustrato lo script che viene chiamato quando un evento viene ricevuto dall'utente permanente. L'oggetto **TargetEvent** è un'istanza di [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md) in modo che disponga di una proprietà denominata **TargetInstance**, ovvero un'istanza di [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) utilizzata per generare l'evento. La classe di **\_ processo Win32** dispone delle proprietà **UserModeTime** e **KernelModeTime** inserite nel file di log creato dallo script.


```VB
' asec.vbs script
Dim objFS, objFile
Set objFS = CreateObject("Scripting.FileSystemObject")
Set objFile = objFS.OpenTextFile("C:\ASEC.log", 8, true)
objFile.WriteLine "Time: " & Now & "; Entry made by: ASEC"

objFile.WriteLine "Application closed. UserModeTime:  " & _
    TargetEvent.TargetInstance.UserModeTime & _
    "; KernelModeTime: " & _
    TargetEvent.TargetInstance.KernelModeTime & _
    " [hundreds of nanoseconds]"
objFile.Close
```



Nell'esempio di codice MOF seguente viene chiamato lo script quando viene ricevuto un evento. Crea il filtro, il consumer e l'associazione tra di essi nello spazio dei nomi della **\\ sottoscrizione radice** .

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $Cons
{
    Name = "ASEC";
    ScriptingEngine = "VBScript";
    ScriptFileName = "c:\\asec2.vbs";
};

instance of __EventFilter as $Filt
{
    Name = "EF";
    Query = "SELECT * FROM __InstanceDeletionEvent WITHIN 5 "
        "WHERE TargetInstance ISA \"Win32_Process\" "
        "AND TargetInstance.Name = \"calc.exe\"";
    QueryLanguage = "WQL";
    EventNamespace = "root\\cimv2";
};

instance of __FilterToConsumerBinding
{
    Filter = $Filt;
    Consumer = $Cons;
};
```

## <a name="example-using-inline-script"></a>Esempio di utilizzo di script inline

Nella procedura seguente viene descritto come utilizzare l'esempio di script inline.

**Per utilizzare l'esempio di script inline**

1.  Copiare l'elenco MOF in questa sezione in un file di testo e salvarlo con un'estensione MOF.
2.  In una finestra del prompt dei comandi compilare il file MOF usando il comando seguente.

    **Mofcomp** *nomefile * * *. mof**

L'esempio di codice MOF seguente crea il filtro, il consumer e l'associazione tra di essi e contiene anche lo script inline.

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $Cons
{
    Name = "ASEC";
    ScriptingEngine = "VBScript";
    
    ScriptText =
        "Dim objFS, objFile\n"
        "Set objFS = CreateObject(\"Scripting.FileSystemObject\")\n"
        "Set objFile = objFS.OpenTextFile(\"C:\\ASEC.log\","
        " 8, true)\nobjFile.WriteLine \"Time: \" & Now & \";"
        " Entry made by: ASEC\"\nobjFile.WriteLine"
        " \"Application closed. UserModeTime:  \" & "
        "TargetEvent.TargetInstance.UserModeTime &_\n"
        "\"; KernelModeTime: \" & "
        "TargetEvent.TargetInstance.KernelModeTime "
        "& \" [hundreds of nanoseconds]\"\n"
        "objFile.Close\n";
};

instance of __EventFilter as $Filt
{
    Name = "EF";
    Query = "SELECT * FROM __InstanceDeletionEvent WITHIN 5 "
        "WHERE TargetInstance ISA \"Win32_Process\" "
        "AND TargetInstance.Name = \"calc.exe\"";
    QueryLanguage = "WQL";
    EventNamespace = "root\\cimv2";
};

instance of __FilterToConsumerBinding
{
    Filter = $Filt;
    Consumer = $Cons;
};
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
