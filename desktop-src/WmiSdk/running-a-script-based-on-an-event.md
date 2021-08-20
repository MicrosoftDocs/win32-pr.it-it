---
description: Il consumer standard implementato dalla classe ActiveScriptEventConsumer consente a un computer di eseguire uno script ed eseguire azioni quando si verificano eventi importanti per garantire che un computer possa rilevare e risolvere automaticamente i problemi.
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
ms.openlocfilehash: b5950ae8a4e7260932fd4df559a73f3abea2bfaf7722444db0b92470649dd312
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816739"
---
# <a name="running-a-script-based-on-an-event"></a>Esecuzione di uno script basato su un evento

Il consumer standard implementato dalla classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) consente a un computer di eseguire uno script ed eseguire azioni quando si verificano eventi importanti per garantire che un computer possa rilevare e risolvere automaticamente i problemi.

Questo consumer viene caricato per impostazione predefinita nello spazio dei nomi **della \\ sottoscrizione** radice.

È possibile configurare le prestazioni di tutte le istanze di [**ActiveScriptEventConsumer**](activescripteventconsumer.md) in un sistema impostando i valori della proprietà **Timeout** o **MaximumScripts** in una singola istanza di [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md).

La procedura di base per l'uso di consumer standard è sempre la stessa e si trova in Monitoraggio e risposta [agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md). La procedura seguente che aggiunge alla routine di base è specifica della [**classe ActiveScriptEventConsumer**](activescripteventconsumer.md) e descrive come creare un consumer di eventi che esegue uno script.

> [!Caution]  
> La [**classe ActiveScriptEventConsumer**](activescripteventconsumer.md) ha vincoli di sicurezza speciali. Questo consumer standard deve essere configurato da un membro locale del gruppo Administrators nel computer locale. Se si usa un account di dominio per creare la sottoscrizione, l'account LocalSystem deve disporre delle autorizzazioni necessarie per il dominio per verificare che l'autore sia membro del gruppo Administrators locale.

 

La procedura seguente descrive come creare un consumer di eventi che esegue uno script.

**Per creare un consumer di eventi che esegue uno script**

1.  Scrivere lo script da eseguire quando si verifica un evento.

    È possibile scrivere lo script in qualsiasi linguaggio, ma assicurarsi che nel computer sia installato un motore di scripting per il linguaggio scelto. Lo script non deve usare oggetti di scripting WMI.

    Solo un amministratore può configurare un consumer di script e lo script viene eseguito con credenziali LocalSystem, che offre funzionalità generali al consumer, ad eccezione dell'accesso alla rete. Tuttavia, lo script non ha accesso a dati di accesso utente specifici, ad esempio variabili di ambiente e condivisioni di rete.

2.  Nel file Managed Object Format (MOF) creare un'istanza di [**ActiveScriptEventConsumer**](activescripteventconsumer.md) per ricevere gli eventi richiesta nella query.

    È possibile inserire il testo dello script in **ScriptText** oppure specificare il percorso e il nome file dello script in **ScriptFileName**. Per altre informazioni, vedere [Progettazione di Managed Object Format (MOF).](designing-managed-object-format--mof--classes.md)

3.  Creare un'istanza di [**\_ \_ EventFilter**](--eventfilter.md), assegnare un nome e quindi creare una query per specificare il tipo di evento, che attiva l'esecuzione dello script.

    Per altre informazioni, vedere [Esecuzione di query con WQL.](querying-with-wql.md)

4.  Creare [**\_ \_ un'istanza di FilterToConsumerBinding**](--filtertoconsumerbinding.md) per associare il filtro all'istanza di [**ActiveScriptEventConsumer**](activescripteventconsumer.md).
5.  Compilare il file MOF [**usando**](mofcomp.md)Mofcomp.exe.

Gli esempi nella sezione seguente illustrano due modi per implementare uno script basato su eventi. Il primo esempio usa uno script definito in un file esterno e il secondo usa uno script incorporato nel codice MOF. Gli esempi sono nel codice MOF, ma è possibile creare le istanze a livello di codice usando [l'API scripting](scripting-api-for-wmi.md) per WMI o [l'API COM per WMI.](com-api-for-wmi.md)

## <a name="example-using-an-external-script"></a>Esempio di uso di uno script esterno

La procedura seguente descrive come usare l'esempio di script esterno.

**Per usare l'esempio di script esterno**

1.  Creare un file denominato c:Asec.vbs e quindi copiare al suo interno lo \\ script in questo esempio.
2.  Copiare l'elenco MOF in un file di testo e salvarlo con estensione mof.
3.  In una finestra del prompt dei comandi compilare il file MOF usando il comando seguente.

    **Nome file Mofcomp***.mof** *

4.  Eseguire la calcolatrice, che crea un calc.exe processo. Attendere più di cinque secondi, chiudere la finestra calcolatrice e cercare nella directory C: un \\ file denominato ASEC.log.

    Il testo seguente è simile al testo che sarà contenuto nel file ASEC.log.

    ``` syntax
    Time: 12/31/2002 2:56:33 PM; Entry made by: ASEC
    Application closed. UserModeTime:  1562500; 
    KernelModeTime: 3125000 [hundreds of nanoseconds]
    ```

Nell'esempio di codice VBScript seguente viene illustrato lo script chiamato quando un evento viene ricevuto dal consumer permanente. **L'oggetto TargetEvent** è [**\_ \_ un'istanza di InstanceDeletionEvent,**](--instancedeletionevent.md) quindi ha una proprietà denominata **TargetInstance**, ovvero un'istanza [**di processo Win32 \_**](/windows/desktop/CIMWin32Prov/win32-process) usata per l'evento. La **classe Win32 \_ Process** ha le **proprietà UserModeTime** e **KernelModeTime** che vengono inserite nel file di log creato dallo script.


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



L'esempio di codice MOF seguente chiama lo script quando viene ricevuto un evento. Crea il filtro, il consumer e l'associazione tra di essi nello spazio dei nomi **\\ della sottoscrizione** radice.

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

## <a name="example-using-inline-script"></a>Esempio di uso di script inline

La procedura seguente descrive come usare l'esempio di script inline.

**Per usare l'esempio di script inline**

1.  Copiare l'elenco MOF in questa sezione in un file di testo e salvarlo con estensione mof.
2.  In una finestra del prompt dei comandi compilare il file MOF usando il comando seguente.

    **Nome file Mofcomp***.mof** *

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

 

 
