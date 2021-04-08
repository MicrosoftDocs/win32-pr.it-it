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
# <a name="running-a-script-based-on-an-event"></a><span data-ttu-id="bfcb3-103">Esecuzione di uno script basato su un evento</span><span class="sxs-lookup"><span data-stu-id="bfcb3-103">Running a Script Based on an Event</span></span>

<span data-ttu-id="bfcb3-104">Il consumer standard implementato dalla classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) consente a un computer di eseguire uno script e di intervenire quando si verificano eventi importanti per garantire che un computer possa rilevare e risolvere automaticamente i problemi.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-104">The standard consumer that is implemented by the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class allows a computer to run a script and take action when important events occur to ensure that a computer can detect and resolve problems automatically.</span></span>

<span data-ttu-id="bfcb3-105">Questo consumer viene caricato per impostazione predefinita nello spazio dei nomi della **\\ sottoscrizione radice** .</span><span class="sxs-lookup"><span data-stu-id="bfcb3-105">This consumer is loaded by default in the **root\\subscription** namespace.</span></span>

<span data-ttu-id="bfcb3-106">È possibile configurare le prestazioni di tutte le istanze di [**ActiveScriptEventConsumer**](activescripteventconsumer.md) in un sistema impostando i valori della proprietà **timeout** o **MaximumScripts** in una singola istanza di [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md).</span><span class="sxs-lookup"><span data-stu-id="bfcb3-106">You can configure the performance of all instances of [**ActiveScriptEventConsumer**](activescripteventconsumer.md) on a system by setting the values of the **Timeout** or **MaximumScripts** property in a single instance of [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md).</span></span>

<span data-ttu-id="bfcb3-107">La procedura di base per l'utilizzo di consumer standard è sempre la stessa ed è disponibile per il [monitoraggio e la risposta a eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="bfcb3-107">The basic procedure for using standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="bfcb3-108">La procedura seguente che aggiunge alla procedura di base è specifica della classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) e descrive come creare un consumer di eventi che esegue uno script.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-108">The following procedure that adds to the basic procedure, is specific to the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class, and describes how to create an event consumer that runs a script.</span></span>

> [!Caution]  
> <span data-ttu-id="bfcb3-109">La classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) presenta vincoli di sicurezza speciali.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-109">The [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class has special security constraints.</span></span> <span data-ttu-id="bfcb3-110">Questo consumer standard deve essere configurato da un membro locale del gruppo Administrators nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-110">This standard consumer must be configured by a local member of the Administrators group on the local computer.</span></span> <span data-ttu-id="bfcb3-111">Se si utilizza un account di dominio per creare la sottoscrizione, è necessario che l'account LocalSystem disponga delle autorizzazioni necessarie per il dominio per verificare che il creatore sia un membro del gruppo Administrators locale.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-111">If you use a domain account to create the subscription, the LocalSystem account must have the necessary permissions on the domain to verify that the creator is a member of the local Administrators group.</span></span>

 

<span data-ttu-id="bfcb3-112">Nella procedura seguente viene descritto come creare un consumer di eventi per l'esecuzione di uno script.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-112">The following procedure describes how to create an event consumer that executes a script.</span></span>

<span data-ttu-id="bfcb3-113">**Per creare un consumer di eventi che esegue uno script**</span><span class="sxs-lookup"><span data-stu-id="bfcb3-113">**To create an event consumer that executes a script**</span></span>

1.  <span data-ttu-id="bfcb3-114">Scrivere lo script da eseguire quando si verifica un evento.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-114">Write the script to run when an event takes place.</span></span>

    <span data-ttu-id="bfcb3-115">È possibile scrivere lo script in qualsiasi linguaggio, ma assicurarsi che nel computer sia installato un motore di scripting per la lingua scelta.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-115">You can write the script in any language, but ensure that a scripting engine for the language that you choose is installed on your machine.</span></span> <span data-ttu-id="bfcb3-116">Lo script non deve usare oggetti di scripting WMI.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-116">The script does not have to use WMI scripting objects.</span></span>

    <span data-ttu-id="bfcb3-117">Solo un amministratore può configurare un consumer di script e lo script viene eseguito con le credenziali LocalSystem, che offre ampie funzionalità al consumer, ad eccezione dell'accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-117">Only an administrator can set up a script consumer, and the script runs under LocalSystem credentials, which gives broad capabilities to the consumer except for network access.</span></span> <span data-ttu-id="bfcb3-118">Tuttavia, lo script non ha accesso a dati di accesso utente specifici, ad esempio le variabili di ambiente e le condivisioni di rete.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-118">However, the script does not have access to specific user logon data, for example, environment variables and network shares.</span></span>

2.  <span data-ttu-id="bfcb3-119">Nel file Managed Object Format (MOF) creare un'istanza di [**ActiveScriptEventConsumer**](activescripteventconsumer.md) per ricevere gli eventi richiesti nella query.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-119">In the Managed Object Format (MOF) file, create an instance of [**ActiveScriptEventConsumer**](activescripteventconsumer.md) to receive the events you request in the query.</span></span>

    <span data-ttu-id="bfcb3-120">È possibile inserire il testo dello script in **ScriptText** oppure specificare il percorso e il nome file dello script in **ScriptFileName**.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-120">You can put the text of the script in **ScriptText**, or you can specify the path and filename of the script in **ScriptFileName**.</span></span> <span data-ttu-id="bfcb3-121">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="bfcb3-121">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

3.  <span data-ttu-id="bfcb3-122">Creare un'istanza di [**\_ \_ EventFilter**](--eventfilter.md), denominarla, quindi creare una query per specificare il tipo di evento che attiva l'esecuzione dello script.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-122">Create an instance of [**\_\_EventFilter**](--eventfilter.md), name it, and then create a query to specify the type of event, which triggers executing the script.</span></span>

    <span data-ttu-id="bfcb3-123">Per ulteriori informazioni, vedere [esecuzione di query con WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="bfcb3-123">For more information see, [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="bfcb3-124">Creare un'istanza di [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) per associare il filtro all'istanza di [**ActiveScriptEventConsumer**](activescripteventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="bfcb3-124">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**ActiveScriptEventConsumer**](activescripteventconsumer.md).</span></span>
5.  <span data-ttu-id="bfcb3-125">Compilare il file MOF utilizzando [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="bfcb3-125">Compile the MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>

<span data-ttu-id="bfcb3-126">Gli esempi nella sezione seguente illustrano due modi per implementare uno script basato su eventi.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-126">The examples in the following section show two ways to implement an event-driven script.</span></span> <span data-ttu-id="bfcb3-127">Nel primo esempio viene utilizzato uno script definito in un file esterno, mentre nel secondo viene utilizzato uno script incorporato nel codice MOF.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-127">The first example uses a script that is defined in an external file, and the second example uses a script that is built into the MOF code.</span></span> <span data-ttu-id="bfcb3-128">Gli esempi sono disponibili nel codice MOF, ma è possibile creare le istanze a livello di programmazione usando l' [API di scripting per WMI](scripting-api-for-wmi.md) o l' [API com per WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="bfcb3-128">The examples are in MOF code, but you can create the instances programmatically by using either the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span>

## <a name="example-using-an-external-script"></a><span data-ttu-id="bfcb3-129">Esempio di utilizzo di uno script esterno</span><span class="sxs-lookup"><span data-stu-id="bfcb3-129">Example Using an External Script</span></span>

<span data-ttu-id="bfcb3-130">Nella procedura seguente viene descritto come utilizzare l'esempio di script esterno.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-130">The following procedure describes how to use the external script example.</span></span>

<span data-ttu-id="bfcb3-131">**Per usare l'esempio di script esterno**</span><span class="sxs-lookup"><span data-stu-id="bfcb3-131">**To use the external script example**</span></span>

1.  <span data-ttu-id="bfcb3-132">Creare un file denominato c: \\Asec.vbs, quindi copiare lo script in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-132">Create a file named c:\\Asec.vbs, and then copy the script in this example into it.</span></span>
2.  <span data-ttu-id="bfcb3-133">Copiare l'elenco MOF in un file di testo e salvarlo con un'estensione MOF.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-133">Copy the MOF list into a text file and save it with a .mof extension.</span></span>
3.  <span data-ttu-id="bfcb3-134">In una finestra del prompt dei comandi compilare il file MOF usando il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-134">In a command prompt window, compile the MOF file by using the following command.</span></span>

    <span data-ttu-id="bfcb3-135">**Mofcomp** *nomefile \* \* *. mof**</span><span class="sxs-lookup"><span data-stu-id="bfcb3-135">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

4.  <span data-ttu-id="bfcb3-136">Eseguire la calcolatrice, che consente di creare un processo di calc.exe.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-136">Run the Calculator, which creates a calc.exe process.</span></span> <span data-ttu-id="bfcb3-137">Attendere più di cinque secondi, chiudere la finestra del calcolatore e cercare \\ un file denominato ASEC. log nella directory C:.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-137">Wait for more than five seconds, close the Calculator window, and then look in the C:\\ directory for a file named ASEC.log.</span></span>

    <span data-ttu-id="bfcb3-138">Il testo seguente è simile al testo che sarà contenuto nel file ASEC. log.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-138">The following text is similar to the text that will be contained in the ASEC.log file.</span></span>

    ``` syntax
    Time: 12/31/2002 2:56:33 PM; Entry made by: ASEC
    Application closed. UserModeTime:  1562500; 
    KernelModeTime: 3125000 [hundreds of nanoseconds]
    ```

<span data-ttu-id="bfcb3-139">Nell'esempio di codice VBScript riportato di seguito viene illustrato lo script che viene chiamato quando un evento viene ricevuto dall'utente permanente.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-139">The following VBScript code example shows the script that is called when an event is received by the permanent consumer.</span></span> <span data-ttu-id="bfcb3-140">L'oggetto **TargetEvent** è un'istanza di [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md) in modo che disponga di una proprietà denominata **TargetInstance**, ovvero un'istanza di [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) utilizzata per generare l'evento.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-140">The **TargetEvent** object is an [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md) instance so it has a property named **TargetInstance**, which is a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) instance used to fire the event.</span></span> <span data-ttu-id="bfcb3-141">La classe di **\_ processo Win32** dispone delle proprietà **UserModeTime** e **KernelModeTime** inserite nel file di log creato dallo script.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-141">The **Win32\_Process** class has the **UserModeTime** and **KernelModeTime** properties that are put into the log file created by the script.</span></span>


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



<span data-ttu-id="bfcb3-142">Nell'esempio di codice MOF seguente viene chiamato lo script quando viene ricevuto un evento.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-142">The following MOF code example calls the script when an event is received.</span></span> <span data-ttu-id="bfcb3-143">Crea il filtro, il consumer e l'associazione tra di essi nello spazio dei nomi della **\\ sottoscrizione radice** .</span><span class="sxs-lookup"><span data-stu-id="bfcb3-143">It creates the filter, consumer, and the binding between them in the **root\\subscription** namespace.</span></span>

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

## <a name="example-using-inline-script"></a><span data-ttu-id="bfcb3-144">Esempio di utilizzo di script inline</span><span class="sxs-lookup"><span data-stu-id="bfcb3-144">Example Using Inline Script</span></span>

<span data-ttu-id="bfcb3-145">Nella procedura seguente viene descritto come utilizzare l'esempio di script inline.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-145">The following procedure describes how to use the inline script example.</span></span>

<span data-ttu-id="bfcb3-146">**Per utilizzare l'esempio di script inline**</span><span class="sxs-lookup"><span data-stu-id="bfcb3-146">**To use the inline script example**</span></span>

1.  <span data-ttu-id="bfcb3-147">Copiare l'elenco MOF in questa sezione in un file di testo e salvarlo con un'estensione MOF.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-147">Copy the MOF list in this section into a text file, and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="bfcb3-148">In una finestra del prompt dei comandi compilare il file MOF usando il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-148">In a command prompt window, compile the MOF file by using the following command.</span></span>

    <span data-ttu-id="bfcb3-149">**Mofcomp** *nomefile \* \* *. mof**</span><span class="sxs-lookup"><span data-stu-id="bfcb3-149">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

<span data-ttu-id="bfcb3-150">L'esempio di codice MOF seguente crea il filtro, il consumer e l'associazione tra di essi e contiene anche lo script inline.</span><span class="sxs-lookup"><span data-stu-id="bfcb3-150">The following MOF code example creates the filter, consumer, and the binding between them and also contains the script inline.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="bfcb3-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bfcb3-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfcb3-152">Monitoraggio e risposta agli eventi con consumer standard</span><span class="sxs-lookup"><span data-stu-id="bfcb3-152">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
