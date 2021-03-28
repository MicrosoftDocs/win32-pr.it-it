---
description: In questo argomento viene illustrato il modo in cui le applicazioni possono esporre le informazioni necessarie per abilitare determinati scenari.
ms.assetid: F88AA3E6-6F7B-442d-935A-7D2CB4958E6B
title: Registrazione dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857e96893d2fe717f1a4939d06c77af043ead318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966529"
---
# <a name="application-registration"></a><span data-ttu-id="ec105-103">Registrazione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="ec105-103">Application Registration</span></span>

<span data-ttu-id="ec105-104">In questo argomento viene illustrato il modo in cui le applicazioni possono esporre le informazioni necessarie per abilitare determinati scenari.</span><span class="sxs-lookup"><span data-stu-id="ec105-104">This topic discusses how applications can expose information about themselves necessary to enable certain scenarios.</span></span> <span data-ttu-id="ec105-105">Sono incluse le informazioni necessarie per individuare l'applicazione, i verbi supportati dall'applicazione e i tipi di file che possono essere gestiti da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ec105-105">This includes information needed to locate the application, the verbs that the application supports and the types of files that an application can handle.</span></span>

<span data-ttu-id="ec105-106">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="ec105-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="ec105-107">Ricerca di un eseguibile di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="ec105-107">Finding an Application Executable</span></span>](#finding-an-application-executable)
-   [<span data-ttu-id="ec105-108">Registrazione di applicazioni</span><span class="sxs-lookup"><span data-stu-id="ec105-108">Registering Applications</span></span>](#registering-applications)
    -   [<span data-ttu-id="ec105-109">Uso della sottochiave percorsi app</span><span class="sxs-lookup"><span data-stu-id="ec105-109">Using the App Paths Subkey</span></span>](#using-the-app-paths-subkey)
    -   [<span data-ttu-id="ec105-110">Uso della sottochiave Applications</span><span class="sxs-lookup"><span data-stu-id="ec105-110">Using the Applications Subkey</span></span>](#using-the-applications-subkey)
-   [<span data-ttu-id="ec105-111">Registrazione di verbi e altre informazioni sull'associazione di file</span><span class="sxs-lookup"><span data-stu-id="ec105-111">Registering Verbs and Other File Association Information</span></span>](#registering-verbs-and-other-file-association-information)
-   [<span data-ttu-id="ec105-112">Registrazione di un tipo percepito</span><span class="sxs-lookup"><span data-stu-id="ec105-112">Registering a Perceived Type</span></span>](#registering-a-perceived-type)
-   [<span data-ttu-id="ec105-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ec105-113">Related topics</span></span>](#related-topics)

> [!Note]  
> <span data-ttu-id="ec105-114">Le applicazioni possono anche essere registrate in Imposta accesso al programma e impostazioni predefinite computer (SPAD) e impostare le applicazioni del pannello di controllo programmi predefiniti (Imposta programmi predefiniti).</span><span class="sxs-lookup"><span data-stu-id="ec105-114">Applications can also be registered in the Set Program Access and Computer Defaults (SPAD) and Set Your Default Programs (SYDP) control panel applications.</span></span> <span data-ttu-id="ec105-115">Per informazioni sulla registrazione dell'applicazione SPAD e imposta programmi predefiniti, vedere [linee guida per le associazioni di file e programmi predefiniti](appguide-fa-defpro.md)e [impostare l'accesso ai programmi e le impostazioni predefinite del computer (SPAD)](cpl-setprogramaccess.md).</span><span class="sxs-lookup"><span data-stu-id="ec105-115">For information about SPAD and SYDP application registration, see [Guidelines for File Associations and Default Programs](appguide-fa-defpro.md), and [Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md).</span></span>

 

## <a name="finding-an-application-executable"></a><span data-ttu-id="ec105-116">Ricerca di un eseguibile di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="ec105-116">Finding an Application Executable</span></span>

<span data-ttu-id="ec105-117">Quando viene chiamata la funzione [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) con il nome di un file eseguibile nel parametro *lpFile* , la funzione Cerca il file in diverse posizioni.</span><span class="sxs-lookup"><span data-stu-id="ec105-117">When the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) function is called with the name of an executable file in its *lpFile* parameter, there are several places where the function looks for the file.</span></span> <span data-ttu-id="ec105-118">Si consiglia di registrare l'applicazione nella sottochiave del registro di sistema **percorsi app** .</span><span class="sxs-lookup"><span data-stu-id="ec105-118">We recommend registering your application in the **App Paths** registry subkey.</span></span> <span data-ttu-id="ec105-119">In questo modo si evita la necessità di modificare la variabile di ambiente percorso di sistema per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ec105-119">Doing so avoids the need for applications to modify the system PATH environment variable.</span></span>

<span data-ttu-id="ec105-120">Il file viene cercato nei percorsi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ec105-120">The file is sought in the following locations:</span></span>

-   <span data-ttu-id="ec105-121">Directory di lavoro corrente</span><span class="sxs-lookup"><span data-stu-id="ec105-121">The current working directory.</span></span>
-   <span data-ttu-id="ec105-122">Solo la directory **Windows** (nessuna sottodirectory cercata).</span><span class="sxs-lookup"><span data-stu-id="ec105-122">The **Windows** directory only (no subdirectories are searched).</span></span>
-   <span data-ttu-id="ec105-123">Directory **\\ System32 di Windows** .</span><span class="sxs-lookup"><span data-stu-id="ec105-123">The **Windows\\System32** directory.</span></span>
-   <span data-ttu-id="ec105-124">Directory elencate nella variabile di ambiente PATH.</span><span class="sxs-lookup"><span data-stu-id="ec105-124">Directories listed in the PATH environment variable.</span></span>
-   <span data-ttu-id="ec105-125">Consigliato: **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **App Paths**</span><span class="sxs-lookup"><span data-stu-id="ec105-125">Recommended: **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**App Paths**</span></span>

## <a name="registering-applications"></a><span data-ttu-id="ec105-126">Registrazione di applicazioni</span><span class="sxs-lookup"><span data-stu-id="ec105-126">Registering Applications</span></span>

<span data-ttu-id="ec105-127">Le sottochiavi del registro di sistema per le **applicazioni** e i **percorsi delle app** vengono usate per registrare e controllare il comportamento del sistema per conto delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ec105-127">Both the **App Paths** and **Applications** registry subkeys are used to register and control the behavior of the system on behalf of applications.</span></span> <span data-ttu-id="ec105-128">La sottochiave **percorsi dell'app** è la posizione preferita.</span><span class="sxs-lookup"><span data-stu-id="ec105-128">The **App Paths** subkey is the preferred location.</span></span>

### <a name="using-the-app-paths-subkey"></a><span data-ttu-id="ec105-129">Uso della sottochiave percorsi app</span><span class="sxs-lookup"><span data-stu-id="ec105-129">Using the App Paths Subkey</span></span>

<span data-ttu-id="ec105-130">In Windows 7 e versioni successive, si consiglia vivamente di installare le applicazioni per utente anziché per computer.</span><span class="sxs-lookup"><span data-stu-id="ec105-130">In Windows 7 and later, we strongly recommend you install applications per user rather than per machine.</span></span> <span data-ttu-id="ec105-131">Un'applicazione installata per ogni utente può essere registrata in **HKEY \_ Current \_ User** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **App Paths**.</span><span class="sxs-lookup"><span data-stu-id="ec105-131">An application that is installed for per user can be registered under **HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**App Paths**.</span></span> <span data-ttu-id="ec105-132">Un'applicazione installata per tutti gli utenti del computer può essere registrata in **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **App Paths**.</span><span class="sxs-lookup"><span data-stu-id="ec105-132">An application that is installed for all users of the computer can be registered under **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**App Paths**.</span></span>

<span data-ttu-id="ec105-133">Le voci trovate nei **percorsi delle app** vengono usate principalmente per gli scopi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ec105-133">The entries found under **App Paths** are used primarily for the following purposes:</span></span>

-   <span data-ttu-id="ec105-134">Per eseguire il mapping del nome del file eseguibile di un'applicazione al percorso completo di tale file.</span><span class="sxs-lookup"><span data-stu-id="ec105-134">To map an application's executable file name to that file's fully qualified path.</span></span>
-   <span data-ttu-id="ec105-135">Per pre-sospendere le informazioni sulla variabile di ambiente PATH per ogni singola applicazione, per processo.</span><span class="sxs-lookup"><span data-stu-id="ec105-135">To pre-pend information to the PATH environment variable on a per-application, per-process basis.</span></span>

<span data-ttu-id="ec105-136">Se il nome di una sottochiave dei **percorsi dell'app** corrisponde al nome del file, la shell esegue due azioni:</span><span class="sxs-lookup"><span data-stu-id="ec105-136">If the name of a subkey of **App Paths** matches the file name, the Shell performs two actions:</span></span>

-   <span data-ttu-id="ec105-137">La voce (predefinita) viene utilizzata come percorso completo del file.</span><span class="sxs-lookup"><span data-stu-id="ec105-137">The (Default) entry is used as the file's fully qualified path.</span></span>
-   <span data-ttu-id="ec105-138">La voce di percorso per la sottochiave è preceduto dalla variabile di ambiente PATH di tale processo.</span><span class="sxs-lookup"><span data-stu-id="ec105-138">The Path entry for that subkey is pre-pended to the PATH environment variable of that process.</span></span> <span data-ttu-id="ec105-139">Se questa operazione non è necessaria, il valore del percorso può essere omesso.</span><span class="sxs-lookup"><span data-stu-id="ec105-139">If this is not required, the Path value can be omitted.</span></span>

<span data-ttu-id="ec105-140">Di seguito sono riportati i potenziali problemi da tenere presente:</span><span class="sxs-lookup"><span data-stu-id="ec105-140">Potential issues to be aware of include:</span></span>

-   <span data-ttu-id="ec105-141">La shell limita la lunghezza di una riga di comando al numero massimo di \_ caratteri del percorso \* 2.</span><span class="sxs-lookup"><span data-stu-id="ec105-141">The Shell limits the length of a command line to MAX\_PATH \* 2 characters.</span></span> <span data-ttu-id="ec105-142">Se sono presenti molti file elencati come voci del registro di sistema o i relativi percorsi sono lunghi, i nomi di file più avanti nell'elenco potrebbero andare perduti perché la riga di comando è troncata.</span><span class="sxs-lookup"><span data-stu-id="ec105-142">If there are many files listed as registry entries or their paths are long, file names later in the list could be lost as the command line is truncated.</span></span>
-   <span data-ttu-id="ec105-143">Alcune applicazioni non accettano più nomi di file in una riga di comando.</span><span class="sxs-lookup"><span data-stu-id="ec105-143">Some applications do not accept multiple file names in a command line.</span></span>
-   <span data-ttu-id="ec105-144">Alcune applicazioni che accettano più nomi di file non riconoscono il formato in cui sono fornite dalla Shell.</span><span class="sxs-lookup"><span data-stu-id="ec105-144">Some applications that accept multiple file names do not recognize the format in which the Shell provides them.</span></span> <span data-ttu-id="ec105-145">La shell fornisce l'elenco di parametri come stringa tra virgolette, ma alcune applicazioni potrebbero richiedere stringhe senza virgolette.</span><span class="sxs-lookup"><span data-stu-id="ec105-145">The Shell provides the parameter list as a quoted string, but some applications might require strings without quotes.</span></span>
-   <span data-ttu-id="ec105-146">Non tutti gli elementi che possono essere trascinati fanno parte del file system; ad esempio, stampanti.</span><span class="sxs-lookup"><span data-stu-id="ec105-146">Not all items that can be dragged are part of the file system; for example, printers.</span></span> <span data-ttu-id="ec105-147">Questi elementi non hanno un percorso Win32 standard, quindi non esiste alcun modo per fornire un valore *lpParameters* significativo a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="ec105-147">These items do not have a standard Win32 path, so there is no way to provide a meaningful *lpParameters* value to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

<span data-ttu-id="ec105-148">L'utilizzo della voce DropTarget consente di evitare questi potenziali problemi fornendo l'accesso a tutti i formati degli Appunti, inclusi [CFSTR \_ SHELLIDLIST](clipboard.md) (per gli elenchi di file lunghi) e [CFSTR \_ fileContents](clipboard.md) (per gli oggetti non di file System).</span><span class="sxs-lookup"><span data-stu-id="ec105-148">Using the DropTarget entry avoids these potential issues by providing access to all of the clipboard formats, including [CFSTR\_SHELLIDLIST](clipboard.md) (for long file lists) and [CFSTR\_FILECONTENTS](clipboard.md) (for non-file-system objects).</span></span>

<span data-ttu-id="ec105-149">**Per registrare e controllare il comportamento delle applicazioni con la sottochiave percorsi dell'app**:</span><span class="sxs-lookup"><span data-stu-id="ec105-149">**To register and control the behavior of your applications with the App Paths subkey**:</span></span>

1.  <span data-ttu-id="ec105-150">Aggiungere una sottochiave con lo stesso nome del file eseguibile alla sottochiave **percorsi dell'app** , come illustrato nella voce del registro di sistema seguente.</span><span class="sxs-lookup"><span data-stu-id="ec105-150">Add a subkey with the same name as your executable file to the **App Paths** subkey, as shown in the following registry entry.</span></span>

    ```
    HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   App Paths
                      file.exe
                         (Default)
                         DontUseDesktopChangeRouter
                         DropTarget
                         Path
                         UseUrl
    ```

2.  <span data-ttu-id="ec105-151">Per informazioni dettagliate sulle voci delle sottochiavi dei **percorsi dell'app** , vedere la tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ec105-151">See the following table for details of the **App Paths** subkey entries.</span></span> 

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="ec105-152">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="ec105-152">Registry entry</span></span></th>
    <th><span data-ttu-id="ec105-153">Dettagli</span><span class="sxs-lookup"><span data-stu-id="ec105-153">Details</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="ec105-154">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="ec105-154">(Default)</span></span></td>
    <td><span data-ttu-id="ec105-155">È il percorso completo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ec105-155">Is the fully qualified path to the application.</span></span> <span data-ttu-id="ec105-156">Il nome dell'applicazione specificato nella voce (impostazione predefinita) può essere dichiarato con o senza la relativa estensione exe.</span><span class="sxs-lookup"><span data-stu-id="ec105-156">The application name provided in the (Default) entry can be stated with or without its .exe extension.</span></span> <span data-ttu-id="ec105-157">Se necessario, la funzione <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> aggiunge l'estensione durante la ricerca della sottochiave dei <strong>percorsi dell'applicazione</strong> .</span><span class="sxs-lookup"><span data-stu-id="ec105-157">If necessary, the <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> function adds the extension when searching <strong>App Paths</strong> subkey.</span></span> <span data-ttu-id="ec105-158">La voce è del tipo di <strong>REG_SZ</strong> .</span><span class="sxs-lookup"><span data-stu-id="ec105-158">The entry is of the <strong>REG_SZ</strong> type.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="ec105-159">DontUseDesktopChangeRouter</span><span class="sxs-lookup"><span data-stu-id="ec105-159">DontUseDesktopChangeRouter</span></span></td>
    <td><span data-ttu-id="ec105-160">È obbligatorio per le applicazioni del debugger evitare deadlock di finestra di dialogo dei file durante il debug del processo di Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="ec105-160">Is mandatory for debugger applications to avoid file dialog deadlocks when debugging the Windows Explorer process.</span></span> <span data-ttu-id="ec105-161">L'impostazione della voce DontUseDesktopChangeRouter produce tuttavia una gestione leggermente meno efficiente delle notifiche di modifica.</span><span class="sxs-lookup"><span data-stu-id="ec105-161">Setting the DontUseDesktopChangeRouter entry produces a slightly less efficient handling of the change notifications, however.</span></span> <span data-ttu-id="ec105-162">La voce è del tipo di <strong>REG_DWORD</strong> e il valore è 0x1.</span><span class="sxs-lookup"><span data-stu-id="ec105-162">The entry is of the <strong>REG_DWORD</strong> type and the value is 0x1.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="ec105-163">DropTarget</span><span class="sxs-lookup"><span data-stu-id="ec105-163">DropTarget</span></span></td>
    <td><span data-ttu-id="ec105-164">È un identificatore di classe (CLSID).</span><span class="sxs-lookup"><span data-stu-id="ec105-164">Is a class identifier (CLSID).</span></span> <span data-ttu-id="ec105-165">La voce DropTarget contiene il CLSID di un oggetto (in genere un server locale anziché un server in-process) che implementa <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ec105-165">The DropTarget entry contains the CLSID of an object (usually a local server rather than an in-process server) that implements <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a>.</span></span> <span data-ttu-id="ec105-166">Per impostazione predefinita, quando l'obiettivo di rilascio è un file eseguibile e non viene specificato alcun valore di DropTarget, la Shell converte l'elenco dei file eliminati in un parametro della riga di comando e lo passa a <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> tramite <em>lpParameters</em>.</span><span class="sxs-lookup"><span data-stu-id="ec105-166">By default, when the drop target is an executable file, and no DropTarget value is provided, the Shell converts the list of dropped files into a command-line parameter and passes it to <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> through <em>lpParameters</em>.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="ec105-167">Percorso</span><span class="sxs-lookup"><span data-stu-id="ec105-167">Path</span></span></td>
    <td><span data-ttu-id="ec105-168">Fornisce una stringa (sotto forma di elenco delimitato da punti e virgola di directory) da accodare alla variabile di ambiente PATH quando viene avviata un'applicazione chiamando <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ec105-168">Supplies a string (in the form of a semicolon-separated list of directories) to append to the PATH environment variable when an application is launched by calling <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>.</span></span> <span data-ttu-id="ec105-169">Si tratta del percorso completo del file con estensione exe.</span><span class="sxs-lookup"><span data-stu-id="ec105-169">It is the fully qualified path to the .exe.</span></span> <span data-ttu-id="ec105-170">È <strong>REG_SZ</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec105-170">It is of <strong>REG_SZ</strong>.</span></span> <span data-ttu-id="ec105-171">In <strong>Windows 7 e versioni successive</strong>, il tipo può essere <strong>REG_EXPAND_SZ</strong>ed è in genere <strong>REG_EXPAND_SZ</strong> % ProgramFiles%.</span><span class="sxs-lookup"><span data-stu-id="ec105-171">In <strong>Windows 7 and later</strong>, the type can be <strong>REG_EXPAND_SZ</strong>, and is commonly <strong>REG_EXPAND_SZ</strong> %ProgramFiles%.</span></span>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="ec105-172">Oltre alle voci (impostazione predefinita), percorso e DropTarget riconosciute dalla shell, un'applicazione può anche aggiungere valori personalizzati alla sottochiave dei <strong>percorsi delle app</strong> del file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="ec105-172">In addition to the (Default), Path, and DropTarget entries recognized by the Shell, an application can also add custom values to its executable file's <strong>App Paths</strong> subkey.</span></span> <span data-ttu-id="ec105-173">Si consiglia agli sviluppatori di applicazioni di usare la sottochiave <strong>percorsi app</strong> per fornire un percorso specifico dell'applicazione anziché aggiungere al percorso di sistema globale.</span><span class="sxs-lookup"><span data-stu-id="ec105-173">We encourage application developers to use the <strong>App Paths</strong> subkey to provide an application-specific path instead of making additions to the global system path.</span></span>
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="ec105-174">SupportedProtocols</span><span class="sxs-lookup"><span data-stu-id="ec105-174">SupportedProtocols</span></span></td>
    <td><span data-ttu-id="ec105-175">Crea una stringa che contiene gli schemi di protocollo URL per una chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="ec105-175">Creates a string that contains the URL protocol schemes for a given key.</span></span> <span data-ttu-id="ec105-176">Può contenere più valori del registro di sistema per indicare quali schemi sono supportati.</span><span class="sxs-lookup"><span data-stu-id="ec105-176">This can contain multiple registry values to indicate which schemes are supported.</span></span> <span data-ttu-id="ec105-177">Questa stringa segue il formato di <strong>scheme1: scheme2</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec105-177">This string follows the format of <strong>scheme1:scheme2</strong>.</span></span> <span data-ttu-id="ec105-178">Se l'elenco non è vuoto, <strong>file:</strong> verrà aggiunto alla stringa.</span><span class="sxs-lookup"><span data-stu-id="ec105-178">If this list is not empty, <strong>file:</strong> will be added to the string.</span></span> <span data-ttu-id="ec105-179">Questo protocollo è supportato in modo implicito quando viene definito <em>SupportedProtocols: Recupera</em> .</span><span class="sxs-lookup"><span data-stu-id="ec105-179">This protocol is implicitly supported when <em>SupportedProtocols</em> is defined.</span></span> <br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="ec105-180">UseUrl</span><span class="sxs-lookup"><span data-stu-id="ec105-180">UseUrl</span></span></td>
    <td><span data-ttu-id="ec105-181">Indica che l'applicazione può accettare un URL, anziché un nome di file, nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="ec105-181">Indicates that your application can accept a URL (instead of a file name) on the command line.</span></span> <span data-ttu-id="ec105-182">Le applicazioni che possono aprire documenti direttamente da Internet, come browser Web e lettori multimediali, devono impostare questa voce.</span><span class="sxs-lookup"><span data-stu-id="ec105-182">Applications that can open documents directly from the internet, like web browsers and media players, should set this entry.</span></span> <br/> <span data-ttu-id="ec105-183">Quando la funzione <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> avvia un'applicazione e il valore UseUrl = 1 non è impostato, <strong>ShellExecuteEx</strong> Scarica il documento in un file locale e richiama il gestore nella copia locale.</span><span class="sxs-lookup"><span data-stu-id="ec105-183">When the <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> function starts an application and the UseUrl=1 value is not set, <strong>ShellExecuteEx</strong> downloads the document to a local file and invokes the handler on the local copy.</span></span><br/> <span data-ttu-id="ec105-184">Se ad esempio l'applicazione dispone di questo set di voci e un utente fa clic con il pulsante destro del mouse su un file archiviato in un server Web, il verbo aperto verrà reso disponibile.</span><span class="sxs-lookup"><span data-stu-id="ec105-184">For example, if the application has this entry set and a user right-clicks on a file stored on a web server, the Open verb will be made available.</span></span> <span data-ttu-id="ec105-185">In caso contrario, l'utente dovrà scaricare il file e aprire la copia locale.</span><span class="sxs-lookup"><span data-stu-id="ec105-185">If not, the user will have to download the file and open the local copy.</span></span> <br/> <span data-ttu-id="ec105-186">La voce UseUrl è di tipo <strong>REG_DWORD</strong> e il valore è 0x1.</span><span class="sxs-lookup"><span data-stu-id="ec105-186">The UseUrl entry is of <strong>REG_DWORD</strong> type, and the value is 0x1.</span></span><br/> <span data-ttu-id="ec105-187">In Windows Vista e versioni precedenti, questa voce indica che l'URL deve essere passato all'applicazione insieme a un nome di file locale, quando viene chiamato tramite ShellExecuteEx.</span><span class="sxs-lookup"><span data-stu-id="ec105-187">In Windows Vista and earlier, this entry indicated that the URL should be passed to the application along with a local file name, when called via ShellExecuteEx.</span></span> <span data-ttu-id="ec105-188">In Windows 7 indica che l'applicazione può comprendere qualsiasi URL http o HTTPS passato, senza dover specificare anche il nome del file di cache.</span><span class="sxs-lookup"><span data-stu-id="ec105-188">In Windows 7, it indicates that the application can understand any http or https url that is passed to it, without having to supply the cache file name as well.</span></span> <span data-ttu-id="ec105-189">Questa chiave del registro di sistema è associata alla chiave <em>SupportedProtocols: Recupera</em> .</span><span class="sxs-lookup"><span data-stu-id="ec105-189">This registry key is associated with the <em>SupportedProtocols</em> key.</span></span><br/></td>
    </tr>
    </tbody>
    </table>

    

     

### <a name="using-the-applications-subkey"></a><span data-ttu-id="ec105-190">Uso della sottochiave Applications</span><span class="sxs-lookup"><span data-stu-id="ec105-190">Using the Applications Subkey</span></span>

<span data-ttu-id="ec105-191">Tramite l'inclusione delle voci del registro di sistema nelle applicazioni **\_ \_ radice delle classi HKEY** \\  \\ *ApplicationName.exe* sottochiave, le applicazioni possono fornire le informazioni specifiche dell'applicazione mostrate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ec105-191">Through the inclusion of registry entries under the **HKEY\_CLASSES\_ROOT**\\**Applications**\\*ApplicationName.exe* subkey, applications can provide the application-specific information shown in the following table.</span></span>



| <span data-ttu-id="ec105-192">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="ec105-192">Registry entry</span></span>                   | <span data-ttu-id="ec105-193">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec105-193">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec105-194">Verbo della shell \\</span><span class="sxs-lookup"><span data-stu-id="ec105-194">shell\\verb</span></span>                      | <span data-ttu-id="ec105-195">Fornisce il metodo Verb per chiamare l'applicazione da OpenWith.</span><span class="sxs-lookup"><span data-stu-id="ec105-195">Provides the verb method for calling the application from OpenWith.</span></span> <span data-ttu-id="ec105-196">Senza una definizione di verbo specificata in questo punto, il sistema presuppone che l'applicazione supporti [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)e passa il nome del file nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="ec105-196">Without a verb definition specified here, the system assumes that the application supports [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa), and passes the file name on the command line.</span></span> <span data-ttu-id="ec105-197">Questa funzionalità si applica a tutti i metodi verb, tra cui DropTarget, ExecuteCommand e Dynamic Data Exchange (DDE).</span><span class="sxs-lookup"><span data-stu-id="ec105-197">This functionality applies to all the verb methods, including DropTarget, ExecuteCommand, and Dynamic Data Exchange (DDE).</span></span>                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="ec105-198">DefaultIcon</span><span class="sxs-lookup"><span data-stu-id="ec105-198">DefaultIcon</span></span>                      | <span data-ttu-id="ec105-199">Consente a un'applicazione di fornire un'icona specifica per rappresentare l'applicazione anziché la prima icona archiviata nel file con estensione exe.</span><span class="sxs-lookup"><span data-stu-id="ec105-199">Enables an application to provide a specific icon to represent the application instead of the first icon stored in the .exe file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="ec105-200">FriendlyAppName</span><span class="sxs-lookup"><span data-stu-id="ec105-200">FriendlyAppName</span></span>                  | <span data-ttu-id="ec105-201">Fornisce un modo per ottenere un nome localizzabile da visualizzare per un'applicazione anziché solo le informazioni sulla versione visualizzate, che potrebbero non essere localizzabili.</span><span class="sxs-lookup"><span data-stu-id="ec105-201">Provides a way to get a localizable name to display for an application instead of just the version information appearing, which may not be localizable.</span></span> <span data-ttu-id="ec105-202">La query di associazione [**ASSOCSTR**](/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr) legge questo valore di voce del registro di sistema e esegue il fallback per usare il nome FileDescription nelle informazioni sulla versione.</span><span class="sxs-lookup"><span data-stu-id="ec105-202">The association query [**ASSOCSTR**](/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr) reads this registry entry value and falls back to use the FileDescription name in the version information.</span></span> <span data-ttu-id="ec105-203">Se tale nome non è presente, per impostazione predefinita la query di associazione corrisponde al nome visualizzato del file.</span><span class="sxs-lookup"><span data-stu-id="ec105-203">If that name is missing, the association query defaults to the display name of the file.</span></span> <span data-ttu-id="ec105-204">Le applicazioni devono usare **ASSOCSTR \_ FRIENDLYAPPNAME** per recuperare queste informazioni per ottenere il comportamento appropriato.</span><span class="sxs-lookup"><span data-stu-id="ec105-204">Applications should use **ASSOCSTR\_FRIENDLYAPPNAME** to retrieve this information to obtain the proper behavior.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="ec105-205">SupportedTypes</span><span class="sxs-lookup"><span data-stu-id="ec105-205">SupportedTypes</span></span>                   | <span data-ttu-id="ec105-206">Elenca i tipi di file supportati dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ec105-206">Lists the file types that the application supports.</span></span> <span data-ttu-id="ec105-207">Questa operazione consente di elencare l'applicazione nel menu a cascata della finestra di dialogo **Apri con** .</span><span class="sxs-lookup"><span data-stu-id="ec105-207">Doing so enables the application to be listed in the cascade menu of the **Open with** dialog box.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ec105-208">NoOpenWith</span><span class="sxs-lookup"><span data-stu-id="ec105-208">NoOpenWith</span></span>                       | <span data-ttu-id="ec105-209">Indica che per l'apertura di questo tipo di file non è specificata alcuna applicazione.</span><span class="sxs-lookup"><span data-stu-id="ec105-209">Indicates that no application is specified for opening this file type.</span></span> <span data-ttu-id="ec105-210">Tenere presente che se è stata impostata una sottochiave OpenWithProgIDs per un'applicazione in base al tipo di file e la sottochiave ProgID stessa non ha anche una voce NoOpenWith, l'applicazione verrà visualizzata nell'elenco delle applicazioni consigliate o disponibili anche se ha specificato la voce NoOpenWith.</span><span class="sxs-lookup"><span data-stu-id="ec105-210">Be aware that if an OpenWithProgIDs subkey has been set for an application by file type, and the ProgID subkey itself does not also have a NoOpenWith entry, that application will appear in the list of recommended or available applications even if it has specified the NoOpenWith entry.</span></span> <span data-ttu-id="ec105-211">Per ulteriori informazioni, vedere [come includere un'applicazione nella finestra di dialogo Apri con](how-to-include-an-application-on-the-open-with-dialog-box.md) e [come escludere un'applicazione dalla finestra di dialogo Apri con](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="ec105-211">For more information, see [How to How to Include an Application in the Open With Dialog Box](how-to-include-an-application-on-the-open-with-dialog-box.md) and [How to exclude an Application from the Open with Dialog Box](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md).</span></span><br/> |
| <span data-ttu-id="ec105-212">IsHostApp</span><span class="sxs-lookup"><span data-stu-id="ec105-212">IsHostApp</span></span>                        | <span data-ttu-id="ec105-213">Indica che il processo è un processo host, ad esempio Rundll32.exe o Dllhost.exe, e non deve essere preso in considerazione per l'aggiunta o l'inclusione del menu **Start** nell'elenco usato più di frequente (MFU).</span><span class="sxs-lookup"><span data-stu-id="ec105-213">Indicates that the process is a host process, such as Rundll32.exe or Dllhost.exe, and should not be considered for **Start** menu pinning or inclusion in the Most Frequently Used (MFU) list.</span></span> <span data-ttu-id="ec105-214">Quando viene avviato con un collegamento che contiene un elenco di argomenti non null o un [ID del modello utente dell'applicazione esplicito (AppUserModelIDs)](appids.md), il processo può essere aggiunto (come tale collegamento).</span><span class="sxs-lookup"><span data-stu-id="ec105-214">When launched with a shortcut that contains a non-null argument list or an explicit [Application User Model IDs (AppUserModelIDs)](appids.md), the process can be pinned (as that shortcut).</span></span> <span data-ttu-id="ec105-215">Questi tasti di scelta rapida sono candidati per l'inclusione nell'elenco MFU.</span><span class="sxs-lookup"><span data-stu-id="ec105-215">Such shortcuts are candidates for inclusion in the MFU list.</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ec105-216">NoStartPage</span><span class="sxs-lookup"><span data-stu-id="ec105-216">NoStartPage</span></span>                      | <span data-ttu-id="ec105-217">Indica che l'eseguibile dell'applicazione e i collegamenti devono essere esclusi dal menu **Start** e dall'aggiunta o dall'inclusione nell'elenco MFU.</span><span class="sxs-lookup"><span data-stu-id="ec105-217">Indicates that the application executable and shortcuts should be excluded from the **Start** menu and from pinning or inclusion in the MFU list.</span></span> <span data-ttu-id="ec105-218">Questa voce viene in genere usata per escludere gli strumenti di sistema, i programmi di installazione e i programmi di disinstallazione e i file Leggimi.</span><span class="sxs-lookup"><span data-stu-id="ec105-218">This entry is typically used to exclude system tools, installers and uninstallers, and readme files.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ec105-219">UseExecutableForTaskbarGroupIcon</span><span class="sxs-lookup"><span data-stu-id="ec105-219">UseExecutableForTaskbarGroupIcon</span></span> | <span data-ttu-id="ec105-220">Fa in modo che la barra delle applicazioni usi l'icona predefinita di questo eseguibile se non è presente alcun collegamento aggiungibili per questa applicazione e invece dell'icona della finestra che è stata rilevata per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="ec105-220">Causes the taskbar to use the default icon of this executable if there is no pinnable shortcut for this application, and instead of the icon of the window that was first encountered.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ec105-221">TaskbarGroupIcon</span><span class="sxs-lookup"><span data-stu-id="ec105-221">TaskbarGroupIcon</span></span>                 | <span data-ttu-id="ec105-222">Specifica l'icona utilizzata per eseguire l'override dell'icona della barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ec105-222">Specifies the icon used to override the taskbar icon.</span></span> <span data-ttu-id="ec105-223">L'icona della finestra viene in genere utilizzata per la barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ec105-223">The window icon is normally used for the taskbar.</span></span> <span data-ttu-id="ec105-224">Se si imposta la voce TaskbarGroupIcon, il sistema utilizzerà invece l'icona del file exe per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ec105-224">Setting the TaskbarGroupIcon entry causes the system to use the icon from the .exe for the application instead.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

### <a name="examples"></a><span data-ttu-id="ec105-225">Esempio</span><span class="sxs-lookup"><span data-stu-id="ec105-225">Examples</span></span>

<span data-ttu-id="ec105-226">Di seguito sono riportati alcuni esempi di registrazioni di applicazioni tramite le applicazioni **\_ \_ radice delle classi HKEY** \\  \\ *ApplicationName.exe* sottochiave.</span><span class="sxs-lookup"><span data-stu-id="ec105-226">Some examples of application registrations through the **HKEY\_CLASSES\_ROOT**\\**Applications**\\*ApplicationName.exe* subkey are as follows.</span></span> <span data-ttu-id="ec105-227">Tutti i valori delle voci del registro di sistema sono di tipo **reg \_ SZ** , ad eccezione di **DefaultIcon** , che è di tipo **reg \_ expand \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="ec105-227">All registry entry values are of **REG\_SZ** type, with the exception of **DefaultIcon** which is of **REG\_EXPAND\_SZ** type.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      wordpad.exe
         FriendlyAppName = @%SystemRoot%\System32\shell32.dll,-22069
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         SupportedTypes
            .3gp2
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         DefaultIcon
            (Default) = %SystemRoot%\system32\wmploc.dll,-730
```

```
HKEY_CLASSES_ROOT
   Applications
      WScript.exe
         NoOpenWith
```

```
HKEY_CLASSES_ROOT
   Applications
      photoviewer.dll
         shell
            open
               DropTarget
                  Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
```

```
HKEY_CLASSES_ROOT
   Applications
      mspaint.exe
         SupportedTypes
            .bmp
            .dib
            .rle
            .jpg
            .jpeg
            .jpe
            .jfif
            .gif
            .emf
            .wmf
            .tif
            .tiff
            .png
            .ico
```

## <a name="registering-verbs-and-other-file-association-information"></a><span data-ttu-id="ec105-228">Registrazione di verbi e altre informazioni sull'associazione di file</span><span class="sxs-lookup"><span data-stu-id="ec105-228">Registering Verbs and Other File Association Information</span></span>

<span data-ttu-id="ec105-229">Le sottochiavi registrate **nelle \_ classi HKEY \_ radice** \\ **SystemFileAssociations** consentono alla shell di definire il comportamento predefinito degli attributi per i tipi di file e di abilitare le associazioni di file condivisi.</span><span class="sxs-lookup"><span data-stu-id="ec105-229">Subkeys registered under **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** enable the Shell to define the default behavior of attributes for file types and enable shared file associations.</span></span> <span data-ttu-id="ec105-230">Quando gli utenti modificano l'applicazione predefinita per un tipo di file, il ProgID della nuova applicazione predefinita ha la priorità per fornire verbi e altre informazioni di associazione.</span><span class="sxs-lookup"><span data-stu-id="ec105-230">When users change the default application for a file type, the ProgID of the new default application has priority in providing verbs and other association information.</span></span> <span data-ttu-id="ec105-231">Questa priorità è dovuta al fatto che è la prima voce nella matrice di associazioni.</span><span class="sxs-lookup"><span data-stu-id="ec105-231">This priority is due to it being the first entry in the association array.</span></span> <span data-ttu-id="ec105-232">Se il programma predefinito viene modificato, le informazioni contenute nel ProgID precedente non sono più disponibili.</span><span class="sxs-lookup"><span data-stu-id="ec105-232">If the default program is changed, the information under the previous ProgID is no longer available.</span></span>

<span data-ttu-id="ec105-233">Per gestire in modo proattivo le conseguenze di una modifica ai programmi predefiniti, è possibile usare **\_ le classi HKEY \_ radice** \\ **SystemFileAssociations** per registrare i verbi e altre informazioni di associazione.</span><span class="sxs-lookup"><span data-stu-id="ec105-233">To deal proactively with the consequences of a change to default programs, you can use **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** to register verbs and other association information.</span></span> <span data-ttu-id="ec105-234">A causa della loro posizione dopo il ProgID nell'array di associazioni, queste registrazioni hanno una priorità inferiore.</span><span class="sxs-lookup"><span data-stu-id="ec105-234">Due to their location after the ProgID in the association array, these registrations are lower priority.</span></span> <span data-ttu-id="ec105-235">Questi SystemFileAssociationsregistrations sono stabili anche quando gli utenti modificano i programmi predefiniti e forniscono un percorso per registrare i verbi secondari che saranno sempre disponibili per un determinato tipo di file.</span><span class="sxs-lookup"><span data-stu-id="ec105-235">These SystemFileAssociationsregistrations are stable even when users change the default programs, and provide a location to register secondary verbs that will always be available for a particular file type.</span></span> <span data-ttu-id="ec105-236">Per un esempio di registro, vedere [registrazione di un tipo percepito](#registering-a-perceived-type) più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="ec105-236">For a registry example, see [Registering a Perceived Type](#registering-a-perceived-type) later in this topic.</span></span>

<span data-ttu-id="ec105-237">Nell'esempio di registro di sistema seguente viene illustrato cosa accade quando l'utente esegue l'elemento **programmi predefiniti** nel pannello di controllo per modificare il valore predefinito per i file con estensione MP3 in App2ProgID.</span><span class="sxs-lookup"><span data-stu-id="ec105-237">The following registry example shows what happens when the user runs the **Default Programs** item in Control Panel to change the default for .mp3 files to App2ProgID.</span></span> <span data-ttu-id="ec105-238">Dopo aver modificato l'impostazione predefinita, Verb1 non è più disponibile e Verb2 diventa il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="ec105-238">After changing the default, Verb1 is no longer available, and Verb2 becomes the default.</span></span>

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = App1ProgID
```

```
HKEY_CLASSES_ROOT
   App1ProgID
      shell
         Verb1
```

```
HKEY_CLASSES_ROOT
   App2ProgID
      shell
         Verb2
```

## <a name="registering-a-perceived-type"></a><span data-ttu-id="ec105-239">Registrazione di un tipo percepito</span><span class="sxs-lookup"><span data-stu-id="ec105-239">Registering a Perceived Type</span></span>

<span data-ttu-id="ec105-240">I valori del registro di sistema per i tipi percepiti vengono definiti come sottochiavi della sottochiave del registro di sistema **HKEY delle \_ classi \_ radice** \\ **SystemFileAssociations**</span><span class="sxs-lookup"><span data-stu-id="ec105-240">Registry values for perceived types are defined as subkeys of the **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** registry subkey.</span></span> <span data-ttu-id="ec105-241">Il **testo** del tipo percepito, ad esempio, viene registrato come segue:</span><span class="sxs-lookup"><span data-stu-id="ec105-241">For example, the perceived type **text** is registered as follows:</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      text
         shell
            edit
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
            open
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
```

<span data-ttu-id="ec105-242">Il tipo percepito di un tipo di file è indicato includendo un valore PerceivedType nella sottochiave del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="ec105-242">A file type's perceived type is indicated by including a PerceivedType value in the file type's subkey.</span></span> <span data-ttu-id="ec105-243">Il valore PerceivedType è impostato sul nome del tipo percepito registrato nella sottochiave del registro di sistema **HKEY \_ classi \_ radice** \\ **SystemFileAssociations** , come illustrato nell'esempio di registro di sistema precedente.</span><span class="sxs-lookup"><span data-stu-id="ec105-243">The PerceivedType value is set to the name of the perceived type registered under **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** registry subkey, as shown in the previous registry example.</span></span> <span data-ttu-id="ec105-244">Per dichiarare i file con estensione cpp come di tipo "Text" percepito, ad esempio, aggiungere la seguente voce del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="ec105-244">To declare .cpp files as being of perceived type "text", for example, add the following registry entry:</span></span>

```
HKEY_CLASSES_ROOT
   .cpp
      PerceivedType = text
```

## <a name="related-topics"></a><span data-ttu-id="ec105-245">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ec105-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec105-246">Tipi di file</span><span class="sxs-lookup"><span data-stu-id="ec105-246">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="ec105-247">Funzionamento delle associazioni di file</span><span class="sxs-lookup"><span data-stu-id="ec105-247">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="ec105-248">Visualizzazione contenuto per tipo di file o tipo</span><span class="sxs-lookup"><span data-stu-id="ec105-248">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="ec105-249">Tipo di file Verifier</span><span class="sxs-lookup"><span data-stu-id="ec105-249">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="ec105-250">Gestori di tipi di file</span><span class="sxs-lookup"><span data-stu-id="ec105-250">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="ec105-251">Identificatori a livello di codice</span><span class="sxs-lookup"><span data-stu-id="ec105-251">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="ec105-252">Tipi percepiti</span><span class="sxs-lookup"><span data-stu-id="ec105-252">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="ec105-253">Matrici di associazione</span><span class="sxs-lookup"><span data-stu-id="ec105-253">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

