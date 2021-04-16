---
title: Compilatore di messaggi (MC.exe)
description: Utilizzato per compilare manifesti di strumentazione e file di testo del messaggio.
ms.assetid: f9de35f1-6d31-4f4b-b2c4-8474d6fce9e0
keywords:
- Log eventi del compilatore di messaggi (MC.exe)
topic_type:
- apiref
api_name:
- Message Compiler (MC.exe)
api_type:
- NA
ms.topic: reference
ms.date: 06/03/2020
ms.openlocfilehash: 5eb852dcbb13800705db0a0f19d912de899f9b0f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524241"
---
# <a name="message-compiler-mcexe"></a><span data-ttu-id="52562-104">Compilatore di messaggi (MC.exe)</span><span class="sxs-lookup"><span data-stu-id="52562-104">Message Compiler (MC.exe)</span></span>

<span data-ttu-id="52562-105">Utilizzato per compilare manifesti di strumentazione e file di testo del messaggio.</span><span class="sxs-lookup"><span data-stu-id="52562-105">Used to compile instrumentation manifests and message text files.</span></span> <span data-ttu-id="52562-106">Il compilatore genera i file di risorse dei messaggi a cui è collegata l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="52562-106">The compiler generates the message resource files to which your application links.</span></span>

``` syntax
MC [-?aAbcdnouUv] [-m <length>] [-h <path>] [-e <extension>] [-r <path>]
   [-x <path>] [-w <file>] [-W <file>] [-z <basename> ] [-cp <encoding>]
   [-km | -um | -generateProjections | -cs <namespace>]
   [-mof] [-p <prefix>] [-P <prefix>]
   [<filename.man>] [<filename.mc>]
```

-   [<span data-ttu-id="52562-107">Argomenti comuni a entrambi i file di testo dei messaggi e i file manifesto</span><span class="sxs-lookup"><span data-stu-id="52562-107">Arguments common to both message text files and manifest files</span></span>](#arguments-common-to-both-message-text-files-and-manifest-files)
-   [<span data-ttu-id="52562-108">Argomenti specifici dei file manifesto</span><span class="sxs-lookup"><span data-stu-id="52562-108">Arguments specific to manifest files</span></span>](#arguments-specific-to-manifest-files)
-   [<span data-ttu-id="52562-109">Argomenti specifici della generazione di codice che il provider utilizzerebbe per registrare gli eventi</span><span class="sxs-lookup"><span data-stu-id="52562-109">Arguments specific to generating code that your provider would use to log events</span></span>](#arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events)
-   [<span data-ttu-id="52562-110">Argomenti specifici dei file di testo del messaggio</span><span class="sxs-lookup"><span data-stu-id="52562-110">Arguments specific to message text files</span></span>](#arguments-specific-to-message-text-files)

## <a name="arguments-common-to-both-message-text-files-and-manifest-files"></a><span data-ttu-id="52562-111">Argomenti comuni a entrambi i file di testo dei messaggi e i file manifesto</span><span class="sxs-lookup"><span data-stu-id="52562-111">Arguments common to both message text files and manifest files</span></span>

<dl> <dt>

<span data-ttu-id="52562-112"><span id="-_"></span>**-?**</span><span class="sxs-lookup"><span data-stu-id="52562-112"><span id="-_"></span>**-?**</span></span>
</dt> <dd>

<span data-ttu-id="52562-113">Visualizza le informazioni sull'utilizzo del compilatore di messaggi.</span><span class="sxs-lookup"><span data-stu-id="52562-113">Displays the usage information for the Message Compiler.</span></span>

</dd> <dt>

<span data-ttu-id="52562-114"><span id="-c"></span><span id="-C"></span>**-c**</span><span class="sxs-lookup"><span data-stu-id="52562-114"><span id="-c"></span><span id="-C"></span>**-c**</span></span>
</dt> <dd>

<span data-ttu-id="52562-115">Usare questo argomento per fare in modo che il compilatore imposti il bit Customer (bit 28) in tutti gli ID messaggio.</span><span class="sxs-lookup"><span data-stu-id="52562-115">Use this argument to have the compiler set the customer bit (bit 28) in all message IDs.</span></span> <span data-ttu-id="52562-116">Per informazioni sul bit del cliente, vedere Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="52562-116">For information on the customer bit, see winerror.h.</span></span>

</dd> <dt>

<span data-ttu-id="52562-117"><span id="-cp"></span><span id="-CP"></span>**-** *codifica* CP</span><span class="sxs-lookup"><span data-stu-id="52562-117"><span id="-cp"></span><span id="-CP"></span>**-cp** *encoding*</span></span>
</dt> <dd>

<span data-ttu-id="52562-118">Utilizzare questo argomento per specificare la codifica dei caratteri utilizzata per tutti i file di testo generati.</span><span class="sxs-lookup"><span data-stu-id="52562-118">Use this argument to specify the character encoding used for all generated text files.</span></span> <span data-ttu-id="52562-119">I nomi validi includono "ANSI" (impostazione predefinita), "UTF-8" e "UTF-16".</span><span class="sxs-lookup"><span data-stu-id="52562-119">Valid names include "ansi" (default), "utf-8", and "utf-16".</span></span> <span data-ttu-id="52562-120">Con le codifiche Unicode viene aggiunto un byte order mark.</span><span class="sxs-lookup"><span data-stu-id="52562-120">The Unicode encodings will add a byte order mark.</span></span>

</dd> <dt>

<span data-ttu-id="52562-121"><span id="-e_extension"></span><span id="-E_EXTENSION"></span>*estensione* **-e**</span><span class="sxs-lookup"><span data-stu-id="52562-121"><span id="-e_extension"></span><span id="-E_EXTENSION"></span>**-e** *extension*</span></span>
</dt> <dd>

<span data-ttu-id="52562-122">Utilizzare questo argomento per specificare l'estensione da utilizzare per il file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="52562-122">Use this argument to specify the extension to use for the header file.</span></span> <span data-ttu-id="52562-123">È possibile specificare fino a un'estensione di tre caratteri, escluso il punto.</span><span class="sxs-lookup"><span data-stu-id="52562-123">You can specify up to a three characters extension, not including the period.</span></span> <span data-ttu-id="52562-124">Il valore predefinito è. h.</span><span class="sxs-lookup"><span data-stu-id="52562-124">The default is .h.</span></span>

</dd> <dt>

<span data-ttu-id="52562-125"><span id="-h_path"></span><span id="-H_PATH"></span>**-h** *percorso*</span><span class="sxs-lookup"><span data-stu-id="52562-125"><span id="-h_path"></span><span id="-H_PATH"></span>**-h** *path*</span></span>
</dt> <dd>

<span data-ttu-id="52562-126">Utilizzare questo argomento per specificare la cartella in cui si desidera che il compilatore inserisca il file di intestazione generato.</span><span class="sxs-lookup"><span data-stu-id="52562-126">Use this argument to specify the folder into which you want the compiler to place the generated header file.</span></span> <span data-ttu-id="52562-127">Il valore predefinito è la directory corrente.</span><span class="sxs-lookup"><span data-stu-id="52562-127">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="52562-128"><span id="-m_length"></span><span id="-M_LENGTH"></span>*lunghezza* **-m**</span><span class="sxs-lookup"><span data-stu-id="52562-128"><span id="-m_length"></span><span id="-M_LENGTH"></span>**-m** *length*</span></span>
</dt> <dd>

<span data-ttu-id="52562-129">Usare questo argomento per fare in modo che il compilatore generi un avviso se il messaggio supera i caratteri di *lunghezza* .</span><span class="sxs-lookup"><span data-stu-id="52562-129">Use this argument to have the compiler generate a warning if the any message exceeds *length* characters.</span></span>

</dd> <dt>

<span data-ttu-id="52562-130"><span id="-r_path"></span><span id="-R_PATH"></span>**-r** *percorso*</span><span class="sxs-lookup"><span data-stu-id="52562-130"><span id="-r_path"></span><span id="-R_PATH"></span>**-r** *path*</span></span>
</dt> <dd>

<span data-ttu-id="52562-131">Usare questo argomento per specificare la cartella in cui si vuole che il compilatore inserisca lo script del compilatore di risorse generato (file RC) e i file. bin generati (risorse binarie) inclusi nello script del compilatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="52562-131">Use this argument to specify the folder into which you want the compiler to place the generated resource compiler script (.rc file) and the generated .bin files (binary resources) that the resource compiler script includes.</span></span> <span data-ttu-id="52562-132">Il valore predefinito è la directory corrente.</span><span class="sxs-lookup"><span data-stu-id="52562-132">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="52562-133"><span id="-z_name"></span><span id="-Z_NAME"></span>**-z** *nome*</span><span class="sxs-lookup"><span data-stu-id="52562-133"><span id="-z_name"></span><span id="-Z_NAME"></span>**-z** *name*</span></span>
</dt> <dd>

<span data-ttu-id="52562-134">Utilizzare questo argomento per eseguire l'override del nome di base predefinito utilizzato dal compilatore per i file generati.</span><span class="sxs-lookup"><span data-stu-id="52562-134">Use this argument to override the default base name that the compiler uses for the files that it generates.</span></span> <span data-ttu-id="52562-135">Per impostazione predefinita, viene utilizzato il nome di base del file di input del *nome* file.</span><span class="sxs-lookup"><span data-stu-id="52562-135">The default is to use the base name of the *filename* input file.</span></span>

</dd> <dt>

<span data-ttu-id="52562-136"><span id="filename"></span><span id="FILENAME"></span>*filename*</span><span class="sxs-lookup"><span data-stu-id="52562-136"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="52562-137">Il file manifesto di strumentazione o il file di testo del messaggio.</span><span class="sxs-lookup"><span data-stu-id="52562-137">The instrumentation manifest file or message text file.</span></span> <span data-ttu-id="52562-138">Il file deve essere presente nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="52562-138">The file must exist in the current directory.</span></span> <span data-ttu-id="52562-139">È possibile specificare un file manifesto, un file di testo del messaggio o entrambi.</span><span class="sxs-lookup"><span data-stu-id="52562-139">You can specify a manifest file, message text file, or both.</span></span> <span data-ttu-id="52562-140">Il nome del file deve includere l'estensione.</span><span class="sxs-lookup"><span data-stu-id="52562-140">The file name must include the extension.</span></span> <span data-ttu-id="52562-141">La convenzione prevede l'uso di un'estensione. Man per i file manifesto e di un'estensione MC per i file di testo del messaggio.</span><span class="sxs-lookup"><span data-stu-id="52562-141">The convention is to use a .man extension for manifest files and a .mc extension for message text files.</span></span>

</dd> </dl>

### <a name="arguments-specific-to-manifest-files"></a><span data-ttu-id="52562-142">Argomenti specifici dei file manifesto</span><span class="sxs-lookup"><span data-stu-id="52562-142">Arguments specific to manifest files</span></span>

<dl> <dt>

<span data-ttu-id="52562-143"><span id="-s_path"></span><span id="-S_PATH"></span>**-s** *percorso*</span><span class="sxs-lookup"><span data-stu-id="52562-143"><span id="-s_path"></span><span id="-S_PATH"></span>**-s** *path*</span></span>
</dt> <dd>

<span data-ttu-id="52562-144">Usare questo argomento per creare una linea di base della strumentazione.</span><span class="sxs-lookup"><span data-stu-id="52562-144">Use this argument to create a baseline of your instrumentation.</span></span> <span data-ttu-id="52562-145">Specificare il percorso della cartella che contiene i file manifesto di base.</span><span class="sxs-lookup"><span data-stu-id="52562-145">Specify the path to the folder that contains your baseline manifest files.</span></span> <span data-ttu-id="52562-146">Per le versioni successive, si userà quindi l'argomento **-t** per verificare il nuovo manifesto rispetto alla linea di base per i problemi di compatibilità.</span><span class="sxs-lookup"><span data-stu-id="52562-146">For subsequent releases, you would then use the **-t** argument to check the new manifest against the baseline for compatibility issues.</span></span>

<span data-ttu-id="52562-147">**Prima della versione MC 1.12.7051:** Non disponibile</span><span class="sxs-lookup"><span data-stu-id="52562-147">**Prior to MC version 1.12.7051:** Not available</span></span>

</dd> <dt>

<span data-ttu-id="52562-148"><span id="-t_path"></span><span id="-T_PATH"></span>**-t** *percorso*</span><span class="sxs-lookup"><span data-stu-id="52562-148"><span id="-t_path"></span><span id="-T_PATH"></span>**-t** *path*</span></span>
</dt> <dd>

<span data-ttu-id="52562-149">Usare questo argomento quando si crea una nuova versione del manifesto e si vuole controllare la compatibilità delle applicazioni con la linea di base creata con l'argomento **-s** .</span><span class="sxs-lookup"><span data-stu-id="52562-149">Use this argument when you create a new version of your manifest and want to check it for application compatibility against the baseline that you created using the **-s** argument.</span></span> <span data-ttu-id="52562-150">Il percorso deve puntare alla cartella che contiene. File BIN creati dall'operazione di base (vedere l'opzione **-s** ).</span><span class="sxs-lookup"><span data-stu-id="52562-150">The path must point to the folder that contains the .BIN files that the baseline operation created (see the **-s** switch).</span></span>

<span data-ttu-id="52562-151">**Prima della versione MC 1.12.7051:** Non disponibile</span><span class="sxs-lookup"><span data-stu-id="52562-151">**Prior to MC version 1.12.7051:** Not available</span></span>

</dd> <dt>

<span data-ttu-id="52562-152"><span id="-w_path"></span><span id="-W_PATH"></span>**-w** *percorso*</span><span class="sxs-lookup"><span data-stu-id="52562-152"><span id="-w_path"></span><span id="-W_PATH"></span>**-w** *path*</span></span>
</dt> <dd>

<span data-ttu-id="52562-153">Il compilatore ignora questo argomento e convalida automaticamente il manifesto.</span><span class="sxs-lookup"><span data-stu-id="52562-153">The compiler ignores this argument and automatically validates the manifest.</span></span>

<span data-ttu-id="52562-154">**Prima della versione MC 1.12.7051:** Utilizzare questo argomento per specificare la cartella che contiene il file di schema EventName. xsd, utilizzato dal compilatore per convalidare il manifesto.</span><span class="sxs-lookup"><span data-stu-id="52562-154">**Prior to MC version 1.12.7051:** Use this argument to specify the folder that contains the Eventman.xsd schema file, which the compiler uses to validate your manifest.</span></span> <span data-ttu-id="52562-155">Il Windows SDK include il file di schema EventName. xsd nella \\ cartella di inclusione.</span><span class="sxs-lookup"><span data-stu-id="52562-155">The Windows SDK includes the Eventman.xsd schema file in the \\Include folder.</span></span> <span data-ttu-id="52562-156">Se non si specifica questo argomento, il compilatore non convalida il manifesto.</span><span class="sxs-lookup"><span data-stu-id="52562-156">If you do not specify this argument, the compiler does not validate your manifest.</span></span>

</dd> <dt>

<span data-ttu-id="52562-157"><span id="-W_path"></span><span id="-w_path"></span><span id="-W_PATH"></span>**-W** *percorso*</span><span class="sxs-lookup"><span data-stu-id="52562-157"><span id="-W_path"></span><span id="-w_path"></span><span id="-W_PATH"></span>**-W** *path*</span></span>
</dt> <dd>

<span data-ttu-id="52562-158">Il compilatore ignora questo argomento.</span><span class="sxs-lookup"><span data-stu-id="52562-158">The compiler ignores this argument.</span></span>

<span data-ttu-id="52562-159">**Prima della versione MC 1.12.7051:** Utilizzare questo argomento per specificare la cartella che contiene il file di Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="52562-159">**Prior to MC version 1.12.7051:** Use this argument to specify the folder that contains the Winmeta.xml file.</span></span> <span data-ttu-id="52562-160">Il file di Winmeta.xml contiene i tipi di input e output riconosciuti, nonché i canali, i livelli e i codici operativi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="52562-160">The Winmeta.xml file contains the recognized input and output types as well as the predefined channels, levels, and opcodes.</span></span> <span data-ttu-id="52562-161">Il Windows SDK include il file di Winmeta.xml nella \\ cartella di inclusione.</span><span class="sxs-lookup"><span data-stu-id="52562-161">The Windows SDK includes the Winmeta.xml file in the \\Include folder.</span></span>

</dd> </dl>

### <a name="arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events"></a><span data-ttu-id="52562-162">Argomenti specifici della generazione di codice che il provider utilizzerebbe per registrare gli eventi</span><span class="sxs-lookup"><span data-stu-id="52562-162">Arguments specific to generating code that your provider would use to log events</span></span>

<span data-ttu-id="52562-163">È possibile utilizzare gli argomenti del compilatore seguenti per generare codice in modalità kernel o utente che è possibile utilizzare per registrare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="52562-163">You can use the following compiler arguments to generate kernel-mode or user-mode code that you can use to log events.</span></span> <span data-ttu-id="52562-164">È inoltre possibile richiedere al compilatore di generare codice per supportare la scrittura di eventi nei computer precedenti a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="52562-164">You can also request that the compiler generate code to support writing events on computers prior to Windows Vista.</span></span> <span data-ttu-id="52562-165">Se l'applicazione è scritta in C#, il compilatore può generare una classe C# che può essere usata per registrare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="52562-165">If your application is written C#, the compiler can generate a C# class that you can use to log events.</span></span> <span data-ttu-id="52562-166">Questi argomenti sono disponibili a partire dalla versione MC 1.12.7051 fornita con la versione Windows 7 di Window SDK.</span><span class="sxs-lookup"><span data-stu-id="52562-166">These arguments are available beginning with MC version 1.12.7051 that ships with the Windows 7 version of the Window SDK.</span></span>

<dl> <dt>

<span data-ttu-id="52562-167"><span id="-co"></span><span id="-CO"></span>**-Co**</span><span class="sxs-lookup"><span data-stu-id="52562-167"><span id="-co"></span><span id="-CO"></span>**-co**</span></span>
</dt> <dd>

<span data-ttu-id="52562-168">Usare questo argomento per fare in modo che il servizio di registrazione chiami la funzione definita dall'utente per ogni evento registrato (la funzione viene chiamata dopo che l'evento è stato registrato).</span><span class="sxs-lookup"><span data-stu-id="52562-168">Use this argument to have the logging service call your user-defined function for each event that you log (the function is called after the event has been logged).</span></span> <span data-ttu-id="52562-169">La funzione definita dall'utente deve avere la firma seguente.</span><span class="sxs-lookup"><span data-stu-id="52562-169">Your user-defined function must have the following signature.</span></span>


```C++
VOID
pFnUserFunction(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR Descriptor,
    __in ULONG EventDataCount,
    __in_ecount(EventDataCount) PEVENT_DATA_DESCRIPTOR EventData
    );
```



<span data-ttu-id="52562-170">È inoltre necessario includere la direttiva seguente nel codice.</span><span class="sxs-lookup"><span data-stu-id="52562-170">You must also include the following directive in your code.</span></span>

`#define MCGEN_CALLOUT pFnUserFunction`

<span data-ttu-id="52562-171">Per evitare problemi di registrazione, è consigliabile tenere l'implementazione più breve possibile. il servizio non registrerà più gli eventi fino a quando la funzione non restituisce.</span><span class="sxs-lookup"><span data-stu-id="52562-171">You should keep your implementation as short as possible to prevent logging issues; the service will not log anymore of your events until the function returns.</span></span>

<span data-ttu-id="52562-172">È possibile usare questo argomento con l'argomento **-km** o **-um** .</span><span class="sxs-lookup"><span data-stu-id="52562-172">You can use this argument with the **-km** or **-um** argument.</span></span>

</dd> <dt>

<span data-ttu-id="52562-173"><span id="-cs_namespace"></span><span id="-CS_NAMESPACE"></span>**-cs (** *spazio dei nomi* )</span><span class="sxs-lookup"><span data-stu-id="52562-173"><span id="-cs_namespace"></span><span id="-CS_NAMESPACE"></span>**-cs** *namespace*</span></span>
</dt> <dd>

<span data-ttu-id="52562-174">Usare questo argomento per fare in modo che il compilatore generi una classe C# basata sulla classe [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) di .NET 3,5.</span><span class="sxs-lookup"><span data-stu-id="52562-174">Use this argument to have the compiler generate a C# class based on the .NET 3.5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) class.</span></span>

</dd> <dt>

<span data-ttu-id="52562-175"><span id="-css_namespace"></span><span id="-CSS_NAMESPACE"></span>**-** *spazio dei nomi* CSS</span><span class="sxs-lookup"><span data-stu-id="52562-175"><span id="-css_namespace"></span><span id="-CSS_NAMESPACE"></span>**-css** *namespace*</span></span>
</dt> <dd>

<span data-ttu-id="52562-176">Usare questo argomento per fare in modo che il compilatore generi una classe C# statica basata sulla classe [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) di .NET 3,5.</span><span class="sxs-lookup"><span data-stu-id="52562-176">Use this argument to have the compiler generate a static C# class based on the .NET 3.5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) class.</span></span>

</dd> <dt>

<span data-ttu-id="52562-177"><span id="-km"></span><span id="-KM"></span>**-km**</span><span class="sxs-lookup"><span data-stu-id="52562-177"><span id="-km"></span><span id="-KM"></span>**-km**</span></span>
</dt> <dd>

<span data-ttu-id="52562-178">Usare questo argomento per fare in modo che il compilatore generi il codice in modalità kernel da usare per registrare gli eventi definiti nel manifesto.</span><span class="sxs-lookup"><span data-stu-id="52562-178">Use this argument to have the compiler generate the kernel-mode code that you would use to log the events defined in your manifest.</span></span>

</dd> <dt>

<span data-ttu-id="52562-179"><span id="-mof"></span><span id="-MOF"></span>**-MOF**</span><span class="sxs-lookup"><span data-stu-id="52562-179"><span id="-mof"></span><span id="-MOF"></span>**-mof**</span></span>
</dt> <dd>

<span data-ttu-id="52562-180">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="52562-180">DEPRECATED.</span></span> <span data-ttu-id="52562-181">Utilizzare questo argomento per fare in modo che il compilatore generi codice che è possibile utilizzare per registrare gli eventi nei computer precedenti a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="52562-181">Use this argument to have the compiler generate code that you can use to log events on computers prior to Windows Vista.</span></span> <span data-ttu-id="52562-182">Questa opzione crea anche un file MOF che contiene le classi MOF per ogni evento definito nel manifesto.</span><span class="sxs-lookup"><span data-stu-id="52562-182">This option also creates a MOF file that contains the MOF classes for each event defined in the manifest.</span></span> <span data-ttu-id="52562-183">Per registrare le classi nel file MOF in modo che i consumer possano decodificare gli eventi, usare il compilatore MOF (Mofcomp.exe).</span><span class="sxs-lookup"><span data-stu-id="52562-183">To register the classes in the MOF file so that consumers can decode the events, use the MOF compiler (Mofcomp.exe).</span></span> <span data-ttu-id="52562-184">Per informazioni dettagliate sull'uso del compilatore MOF, vedere [Managed Object Format](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="52562-184">For details on using the MOF compiler, see [Managed Object Format](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

<span data-ttu-id="52562-185">Per usare questa opzione, è necessario rispettare le restrizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="52562-185">To use this switch, you must adhere to the following restrictions:</span></span>

-   <span data-ttu-id="52562-186">Ogni definizione di evento deve includere gli attributi Task e OpCode</span><span class="sxs-lookup"><span data-stu-id="52562-186">Every event definition must include the task and opcode attributes</span></span>
-   <span data-ttu-id="52562-187">Ogni attività deve includere l'attributo eventGuid</span><span class="sxs-lookup"><span data-stu-id="52562-187">Every task must include the eventGuid attribute</span></span>
-   <span data-ttu-id="52562-188">I dati del modello a cui fa riferimento l'evento non possono contenere:</span><span class="sxs-lookup"><span data-stu-id="52562-188">The template data that the event references cannot contain:</span></span>
    -   <span data-ttu-id="52562-189">Elementi di dati che specificano i tipi di input Win: Binary o Win: SYSTEMTIME</span><span class="sxs-lookup"><span data-stu-id="52562-189">Data items that specify the win:Binary or win:SYSTEMTIME input types</span></span>
    -   <span data-ttu-id="52562-190">Strutture</span><span class="sxs-lookup"><span data-stu-id="52562-190">Structures</span></span>
    -   <span data-ttu-id="52562-191">Matrici di dimensioni variabili; è tuttavia possibile specificare matrici a lunghezza fissa</span><span class="sxs-lookup"><span data-stu-id="52562-191">Variable sized arrays; however, you can specify fixed length arrays</span></span>
    -   <span data-ttu-id="52562-192">I tipi di dati stringa non possono specificare l'attributo length</span><span class="sxs-lookup"><span data-stu-id="52562-192">String data types cannot specify the length attribute</span></span>

<span data-ttu-id="52562-193">È necessario utilizzare questo argomento con l'argomento **-um**, **-CS**, **-CSS** o **-km**</span><span class="sxs-lookup"><span data-stu-id="52562-193">You must use this argument with the **-um**, **-cs**, **-css**, or **-km** argument</span></span>

</dd> <dt>

<span data-ttu-id="52562-194"><span id="-p_prefix"></span><span id="-P_PREFIX"></span>*prefisso* **-p**</span><span class="sxs-lookup"><span data-stu-id="52562-194"><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-p** *prefix*</span></span>
</dt> <dd>

<span data-ttu-id="52562-195">Utilizzare questo argomento per sostituire il prefisso predefinito utilizzato dal compilatore per i nomi delle macro di registrazione e i nomi dei metodi.</span><span class="sxs-lookup"><span data-stu-id="52562-195">Use this argument to override the default prefix that the compiler uses for the logging macro names and method names.</span></span> <span data-ttu-id="52562-196">Il prefisso predefinito è "EventWrite".</span><span class="sxs-lookup"><span data-stu-id="52562-196">The default prefix is "EventWrite".</span></span> <span data-ttu-id="52562-197">Per la stringa viene fatta distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="52562-197">The string is case-sensitive.</span></span>

<span data-ttu-id="52562-198">È possibile utilizzare questo argomento con l'argomento **-um**, **-CS**, **-CSS** o **-km** .</span><span class="sxs-lookup"><span data-stu-id="52562-198">You can use this argument with the **-um**, **-cs**, **-css**, or **-km** argument.</span></span>

</dd> <dt>

<span data-ttu-id="52562-199"><span id="-P_prefix"></span><span id="-p_prefix"></span><span id="-P_PREFIX"></span>*Prefisso* **-P**</span><span class="sxs-lookup"><span data-stu-id="52562-199"><span id="-P_prefix"></span><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-P** *prefix*</span></span>
</dt> <dd>

<span data-ttu-id="52562-200">Usare questo argomento per rimuovere i caratteri dall'inizio del nome simbolico specificato per l'evento.</span><span class="sxs-lookup"><span data-stu-id="52562-200">Use this argument to remove characters from the beginning of the symbolic name that you specified for the event.</span></span> <span data-ttu-id="52562-201">Il confronto viene eseguito senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="52562-201">The comparison is case-insensitive.</span></span> <span data-ttu-id="52562-202">Il compilatore usa il nome simbolico per formare i nomi delle macro di registrazione e i nomi dei metodi.</span><span class="sxs-lookup"><span data-stu-id="52562-202">The compiler uses the symbolic name to form the logging macro names and method names.</span></span>

<span data-ttu-id="52562-203">Il nome predefinito di una macro di registrazione è EventWrite *symbolName*, dove *symbolName* è il nome simbolico specificato per l'evento.</span><span class="sxs-lookup"><span data-stu-id="52562-203">The default name for a logging macro is EventWrite *SymbolName*, where *SymbolName* is the symbolic name that you specified for the event.</span></span> <span data-ttu-id="52562-204">Se, ad esempio, si imposta l'attributo symbol dell'evento su PrinterConnection, il nome della macro sarà EventWritePrinterConnection.</span><span class="sxs-lookup"><span data-stu-id="52562-204">For example, if you set the symbol attribute of the event to PrinterConnection, the macro name would be EventWritePrinterConnection.</span></span> <span data-ttu-id="52562-205">Per rimuovere la stampante dal nome, usare **-P** **Printer**, che restituisce EventWriteConnection.</span><span class="sxs-lookup"><span data-stu-id="52562-205">To remove Printer from the name, use **-P** **Printer**, which results in EventWriteConnection.</span></span>

<span data-ttu-id="52562-206">È possibile utilizzare questo argomento con l'argomento **-um**, **-CS**, **-CSS** o **-km** .</span><span class="sxs-lookup"><span data-stu-id="52562-206">You can use this argument with the **-um**, **-cs**, **-css**, or **-km** argument.</span></span>

</dd> <dt>

<span data-ttu-id="52562-207"><span id="-um"></span><span id="-UM"></span>**-um**</span><span class="sxs-lookup"><span data-stu-id="52562-207"><span id="-um"></span><span id="-UM"></span>**-um**</span></span>
</dt> <dd>

<span data-ttu-id="52562-208">Usare questo argomento per fare in modo che il compilatore generi il codice in modalità utente da usare per registrare gli eventi definiti nel manifesto.</span><span class="sxs-lookup"><span data-stu-id="52562-208">Use this argument to have the compiler generate the user-mode code that you would use to log the events defined in your manifest.</span></span>

</dd> </dl>

<span data-ttu-id="52562-209">Per fare in modo che il compilatore generi il codice di registrazione, è necessario specificare l'argomento **-um**, **-CS**, **-CSS** o **-km** ; questi argomenti si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="52562-209">To have the compiler generate logging code, you must specify the **-um**, **-cs**, **-css**, or **-km** argument; these arguments are mutually exclusive.</span></span>

<span data-ttu-id="52562-210">Per specificare dove inserire i file con estensione h, CS e MOF generati dal compilatore, usare l'argomento **-h** .</span><span class="sxs-lookup"><span data-stu-id="52562-210">To specify where to place the .h, .cs, and .mof files that the compiler generates, use the **-h** argument.</span></span> <span data-ttu-id="52562-211">Se non si specifica l'argomento **-h** , i file vengono inseriti nella cartella corrente.</span><span class="sxs-lookup"><span data-stu-id="52562-211">If you do not specify the **-h** argument, the files are placed in the current folder.</span></span>

<span data-ttu-id="52562-212">Per specificare dove inserire il file RC e i file binari (contenenti le risorse di metadati) generati dal compilatore, usare l'argomento **-r** .</span><span class="sxs-lookup"><span data-stu-id="52562-212">To specify where to place the .rc file and binary files (that contain the metadata resources) that the compiler generates, use the **-r** argument.</span></span> <span data-ttu-id="52562-213">Se non si specifica l'argomento **-r** , i file vengono inseriti nella cartella corrente.</span><span class="sxs-lookup"><span data-stu-id="52562-213">If you do not specify the **-r** argument, the files are placed in the current folder.</span></span>

<span data-ttu-id="52562-214">Il compilatore usa il nome di base del file di input come nome di base dei file generati.</span><span class="sxs-lookup"><span data-stu-id="52562-214">The compiler uses the base name of the input file as the base name of the files that it generates.</span></span> <span data-ttu-id="52562-215">Per specificare un nome di base, usare l'argomento **-z** .</span><span class="sxs-lookup"><span data-stu-id="52562-215">To specify a base name, use the **-z** argument.</span></span>

### <a name="arguments-specific-to-message-text-files"></a><span data-ttu-id="52562-216">Argomenti specifici dei file di testo del messaggio</span><span class="sxs-lookup"><span data-stu-id="52562-216">Arguments specific to message text files</span></span>

<dl> <dt>

<span data-ttu-id="52562-217"><span id="-a"></span><span id="-A"></span>**-a**</span><span class="sxs-lookup"><span data-stu-id="52562-217"><span id="-a"></span><span id="-A"></span>**-a**</span></span>
</dt> <dd>

<span data-ttu-id="52562-218">Usare questo argomento per specificare che il file di input del *nome* file contiene contenuto nella tabella codici ANSI predefinita di sistema (CP_ACP).</span><span class="sxs-lookup"><span data-stu-id="52562-218">Use this argument to specify that the *filename* input file contains content in the system-default Windows ANSI code page (CP_ACP).</span></span> <span data-ttu-id="52562-219">Questo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="52562-219">This is the default.</span></span> <span data-ttu-id="52562-220">Usare **-u** per Unicode.</span><span class="sxs-lookup"><span data-stu-id="52562-220">Use **-u** for Unicode.</span></span> <span data-ttu-id="52562-221">Se il file di input contiene un BOM, questo argomento verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="52562-221">If the input file contains a BOM this argument will be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="52562-222"><span id="-A"></span><span id="-a"></span>**-A**</span><span class="sxs-lookup"><span data-stu-id="52562-222"><span id="-A"></span><span id="-a"></span>**-A**</span></span>
</dt> <dd>

<span data-ttu-id="52562-223">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="52562-223">DEPRECATED.</span></span> <span data-ttu-id="52562-224">Utilizzare questo argomento per specificare che i messaggi nel file. bin di output devono essere ANSI.</span><span class="sxs-lookup"><span data-stu-id="52562-224">Use this argument to specify that the messages in the output .bin file should be ANSI.</span></span>

</dd> <dt>

<span data-ttu-id="52562-225"><span id="-b"></span><span id="-B"></span>**-b**</span><span class="sxs-lookup"><span data-stu-id="52562-225"><span id="-b"></span><span id="-B"></span>**-b**</span></span>
</dt> <dd>

<span data-ttu-id="52562-226">Usare questo argomento per fare in modo che il compilatore usi il nome di base del file di input del *nome* file per i nomi di file con estensione bin.</span><span class="sxs-lookup"><span data-stu-id="52562-226">Use this argument to have the compiler use the base name of the *filename* input file for the .bin file names.</span></span> <span data-ttu-id="52562-227">Per impostazione predefinita, viene usato "MSG".</span><span class="sxs-lookup"><span data-stu-id="52562-227">The default is to use "MSG".</span></span>

</dd> <dt>

<span data-ttu-id="52562-228"><span id="-d"></span><span id="-D"></span>**-d**</span><span class="sxs-lookup"><span data-stu-id="52562-228"><span id="-d"></span><span id="-D"></span>**-d**</span></span>
</dt> <dd>

<span data-ttu-id="52562-229">Utilizzare questo argomento per utilizzare valori decimali per le costanti di gravità e di funzione nel file di intestazione anziché valori esadecimali.</span><span class="sxs-lookup"><span data-stu-id="52562-229">Use this argument to use decimal values for the Severity and Facility constants in the header file instead of hexadecimal values.</span></span>

</dd> <dt>

<span data-ttu-id="52562-230"><span id="-n"></span><span id="-N"></span>**-n**</span><span class="sxs-lookup"><span data-stu-id="52562-230"><span id="-n"></span><span id="-N"></span>**-n**</span></span>
</dt> <dd>

<span data-ttu-id="52562-231">Utilizzare questo argomento per specificare che i messaggi terminano immediatamente dopo il corpo del messaggio.</span><span class="sxs-lookup"><span data-stu-id="52562-231">Use this argument to specify that messages terminate immediately after the message body.</span></span> <span data-ttu-id="52562-232">Per impostazione predefinita, il corpo del messaggio viene terminato con CR/LF.</span><span class="sxs-lookup"><span data-stu-id="52562-232">The default is to terminate the message body with a CR/LF.</span></span>

</dd> <dt>

<span data-ttu-id="52562-233"><span id="-o"></span><span id="-O"></span>**-o**</span><span class="sxs-lookup"><span data-stu-id="52562-233"><span id="-o"></span><span id="-O"></span>**-o**</span></span>
</dt> <dd>

<span data-ttu-id="52562-234">Usare questo argomento per fare in modo che il compilatore generi un file di intestazione OLE2 usando le definizioni **HRESULT** anziché i codici di stato.</span><span class="sxs-lookup"><span data-stu-id="52562-234">Use this argument to have the compiler generate an OLE2 header file using **HRESULT** definitions instead of status codes.</span></span> <span data-ttu-id="52562-235">L'utilizzo dei codici di stato è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="52562-235">Using status codes is the default.</span></span>

</dd> <dt>

<span data-ttu-id="52562-236"><span id="-u"></span><span id="-U"></span>**-u**</span><span class="sxs-lookup"><span data-stu-id="52562-236"><span id="-u"></span><span id="-U"></span>**-u**</span></span>
</dt> <dd>

<span data-ttu-id="52562-237">Usare questo argomento per specificare che il file di input del *nome* file contiene contenuto UTF-16LE.</span><span class="sxs-lookup"><span data-stu-id="52562-237">Use this argument to specify that the *filename* input file contains UTF-16LE content.</span></span> <span data-ttu-id="52562-238">Il valore predefinito è contenuto ANSI.</span><span class="sxs-lookup"><span data-stu-id="52562-238">The default is ANSI content.</span></span> <span data-ttu-id="52562-239">Se il file di input contiene un BOM, questo argomento verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="52562-239">If the input file contains a BOM this argument will be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="52562-240"><span id="-U"></span><span id="-u"></span>**-U**</span><span class="sxs-lookup"><span data-stu-id="52562-240"><span id="-U"></span><span id="-u"></span>**-U**</span></span>
</dt> <dd>

<span data-ttu-id="52562-241">Utilizzare questo argomento per specificare che i messaggi nel file. bin di output devono essere Unicode.</span><span class="sxs-lookup"><span data-stu-id="52562-241">Use this argument to specify that the messages in the output .bin file should be Unicode.</span></span> <span data-ttu-id="52562-242">Questo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="52562-242">This is the default.</span></span>

</dd> <dt>

<span data-ttu-id="52562-243"><span id="-v"></span><span id="-V"></span>**-v**</span><span class="sxs-lookup"><span data-stu-id="52562-243"><span id="-v"></span><span id="-V"></span>**-v**</span></span>
</dt> <dd>

<span data-ttu-id="52562-244">Usare questo argomento per generare l'output dettagliato.</span><span class="sxs-lookup"><span data-stu-id="52562-244">Use this argument to generate verbose output.</span></span>

</dd> <dt>

<span data-ttu-id="52562-245"><span id="-x_path"></span><span id="-X_PATH"></span>**-x** *percorso*</span><span class="sxs-lookup"><span data-stu-id="52562-245"><span id="-x_path"></span><span id="-X_PATH"></span>**-x** *path*</span></span>
</dt> <dd>

<span data-ttu-id="52562-246">Utilizzare questo argomento per specificare la cartella in cui si desidera che il compilatore inserisca il file di inclusione. dbg C.</span><span class="sxs-lookup"><span data-stu-id="52562-246">Use this argument to specify the folder into which you want the compiler to place the .dbg C include file.</span></span> <span data-ttu-id="52562-247">Il file con estensione DBG esegue il mapping degli ID messaggio ai nomi simbolici.</span><span class="sxs-lookup"><span data-stu-id="52562-247">The .dbg file maps message IDs to their symbolic names.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52562-248">Commenti</span><span class="sxs-lookup"><span data-stu-id="52562-248">Remarks</span></span>

<span data-ttu-id="52562-249">Gli argomenti **-A** e **-MOF** sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="52562-249">The **-A** and **-mof** arguments are deprecated and will be removed in the future.</span></span>

<span data-ttu-id="52562-250">Il compilatore accetta come input un file manifesto (. Man) o un file di testo del messaggio (. MC) e genera i file seguenti:</span><span class="sxs-lookup"><span data-stu-id="52562-250">The compiler accepts as input a manifest (.man) file or a message text (.mc) file and generates the following files:</span></span>

-   <span data-ttu-id="52562-251">*nomefile*. h</span><span class="sxs-lookup"><span data-stu-id="52562-251">*filename*.h</span></span>

    <span data-ttu-id="52562-252">Un file di intestazione C/C++ che contiene i descrittori di evento, il GUID del provider e i nomi dei simboli a cui si fa riferimento nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="52562-252">A C/C++ header file that contains the event descriptors, provider GUID, and symbol names that you reference in your application.</span></span>

-   <span data-ttu-id="52562-253">*nome file* TEMP. bin</span><span class="sxs-lookup"><span data-stu-id="52562-253">*filename* TEMP.bin</span></span>

    <span data-ttu-id="52562-254">Un file di risorse binario che contiene i metadati dell'evento e del provider.</span><span class="sxs-lookup"><span data-stu-id="52562-254">A binary resource file that contains the provider and event metadata.</span></span> <span data-ttu-id="52562-255">Si tratta della risorsa modello, che è contraddistinta dal suffisso temporaneo del nome di base del file.</span><span class="sxs-lookup"><span data-stu-id="52562-255">This is the template resource, which is signified by the TEMP suffix of the base name of the file.</span></span>

-   <span data-ttu-id="52562-256">Msg00001. bin</span><span class="sxs-lookup"><span data-stu-id="52562-256">Msg00001.bin</span></span>

    <span data-ttu-id="52562-257">Un file di risorse binario per ogni lingua specificata (ad esempio, se il manifesto contiene stringhe di messaggio in en-US e fr-FR, il compilatore genererà Msg00001. bin e Msg00002. bin).</span><span class="sxs-lookup"><span data-stu-id="52562-257">A binary resource file for each language that you specify (for example, if your manifest contains message strings in en-US and fr-FR, the compiler would generate Msg00001.bin and Msg00002.bin).</span></span>

-   <span data-ttu-id="52562-258">*nomefile*. RC</span><span class="sxs-lookup"><span data-stu-id="52562-258">*filename*.rc</span></span>

    <span data-ttu-id="52562-259">Uno script del compilatore di risorse che contiene le istruzioni per includere ogni file con estensione bin come risorsa.</span><span class="sxs-lookup"><span data-stu-id="52562-259">A resource compiler script that contains the statements to include each .bin file as a resource.</span></span>

<span data-ttu-id="52562-260">Per gli argomenti che accettano un percorso, il percorso può essere un percorso assoluto, relativo o UNC e può contenere variabili di ambiente.</span><span class="sxs-lookup"><span data-stu-id="52562-260">For arguments that take a path, the path can be an absolute, relative, or UNC path and it can contain environment variables.</span></span>

<span data-ttu-id="52562-261">**Prima della versione MC 1.12.7051:** Il compilatore non consente percorsi relativi o variabili di ambiente.</span><span class="sxs-lookup"><span data-stu-id="52562-261">**Prior to MC version 1.12.7051:** The compiler does not allow relative paths or environment variables.</span></span>

<span data-ttu-id="52562-262">Il Windows SDK include il compilatore (mc.exe) nella \\ cartella bin.</span><span class="sxs-lookup"><span data-stu-id="52562-262">The Windows SDK includes the compiler (mc.exe) in the \\Bin folder.</span></span>

## <a name="examples"></a><span data-ttu-id="52562-263">Esempio</span><span class="sxs-lookup"><span data-stu-id="52562-263">Examples</span></span>

<span data-ttu-id="52562-264">Nell'esempio seguente viene compilato un manifesto usando le impostazioni predefinite del compilatore.</span><span class="sxs-lookup"><span data-stu-id="52562-264">The following example compiles a manifest using the compiler defaults.</span></span>

``` syntax
mc spooler.man
```

<span data-ttu-id="52562-265">Nell'esempio seguente viene compilato il manifesto e vengono posizionati i file di intestazione e di risorse nelle cartelle specificate.</span><span class="sxs-lookup"><span data-stu-id="52562-265">The following example compiles the manifest and places the header and resource files in the specified folders.</span></span>

``` syntax
mc -h <pathgoeshere> -r <pathgoeshere> spooler.man
```

## <a name="requirements"></a><span data-ttu-id="52562-266">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52562-266">Requirements</span></span>

| <span data-ttu-id="52562-267">Requisito</span><span class="sxs-lookup"><span data-stu-id="52562-267">Requirement</span></span> | <span data-ttu-id="52562-268">Valore</span><span class="sxs-lookup"><span data-stu-id="52562-268">Value</span></span> |
|--------------------------|-------------------------------------------------|
| <span data-ttu-id="52562-269">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52562-269">Minimum supported client</span></span> | <span data-ttu-id="52562-270">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="52562-270">Windows 2000 Professional \[desktop apps only\]</span></span> |
| <span data-ttu-id="52562-271">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52562-271">Minimum supported server</span></span> | <span data-ttu-id="52562-272">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="52562-272">Windows 2000 Server \[desktop apps only\]</span></span>       |
