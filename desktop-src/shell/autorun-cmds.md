---
description: Questo argomento è un riferimento per le voci che possono essere usate in un file Autorun. inf. Una voce è costituita da una chiave e un valore.
ms.assetid: 5b8fd559-b1be-4552-a7be-19ad107855af
title: Voci Autorun. inf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56d93244f177d107bddc720fab1d0c774fd94735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225936"
---
# <a name="autoruninf-entries"></a><span data-ttu-id="37ab3-104">Voci Autorun. inf</span><span class="sxs-lookup"><span data-stu-id="37ab3-104">Autorun.inf Entries</span></span>

<span data-ttu-id="37ab3-105">Questo argomento è un riferimento per le voci che possono essere usate in un file Autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="37ab3-105">This topic is a reference for the entries that can be used in an Autorun.inf file.</span></span> <span data-ttu-id="37ab3-106">Una voce è costituita da una chiave e un valore.</span><span class="sxs-lookup"><span data-stu-id="37ab3-106">An entry consists of a key and a value.</span></span>

-   <span data-ttu-id="37ab3-107">[\[\]Chiavi Autorun](#autorun-keys)</span><span class="sxs-lookup"><span data-stu-id="37ab3-107">[\[AutoRun\] Keys](#autorun-keys)</span></span>
    -   [<span data-ttu-id="37ab3-108">action</span><span class="sxs-lookup"><span data-stu-id="37ab3-108">action</span></span>](#parameters)
    -   [<span data-ttu-id="37ab3-109">CustomEvent</span><span class="sxs-lookup"><span data-stu-id="37ab3-109">CustomEvent</span></span>](#customevent)
    -   [<span data-ttu-id="37ab3-110">icona</span><span class="sxs-lookup"><span data-stu-id="37ab3-110">icon</span></span>](#parameters)
    -   [<span data-ttu-id="37ab3-111">label</span><span class="sxs-lookup"><span data-stu-id="37ab3-111">label</span></span>](#parameters)
    -   [<span data-ttu-id="37ab3-112">open</span><span class="sxs-lookup"><span data-stu-id="37ab3-112">open</span></span>](#parameters)
    -   [<span data-ttu-id="37ab3-113">UseAutoPlay</span><span class="sxs-lookup"><span data-stu-id="37ab3-113">UseAutoPlay</span></span>](#parameters)
    -   [<span data-ttu-id="37ab3-114">ShellExecute</span><span class="sxs-lookup"><span data-stu-id="37ab3-114">shellexecute</span></span>](#shellexecute)
    -   [<span data-ttu-id="37ab3-115">Shell</span><span class="sxs-lookup"><span data-stu-id="37ab3-115">shell</span></span>](#autoruninf-entries)
    -   [<span data-ttu-id="37ab3-116">Verbo della shell \\</span><span class="sxs-lookup"><span data-stu-id="37ab3-116">shell\\verb</span></span>](#shellverb)
-   <span data-ttu-id="37ab3-117">[\[\]Chiavi simmetriche](#content-keys)</span><span class="sxs-lookup"><span data-stu-id="37ab3-117">[\[Content\] Keys](#content-keys)</span></span>
-   <span data-ttu-id="37ab3-118">[\[Chiavi di ExclusiveContentPaths \]](#exclusivecontentpaths-keys)</span><span class="sxs-lookup"><span data-stu-id="37ab3-118">[\[ExclusiveContentPaths\] Keys](#exclusivecontentpaths-keys)</span></span>
-   <span data-ttu-id="37ab3-119">[\[Chiavi di IgnoreContentPaths \]](#ignorecontentpaths-keys)</span><span class="sxs-lookup"><span data-stu-id="37ab3-119">[\[IgnoreContentPaths\] Keys](#ignorecontentpaths-keys)</span></span>
-   <span data-ttu-id="37ab3-120">[\[Chiavi di DeviceInstall \]](#deviceinstall-keys)</span><span class="sxs-lookup"><span data-stu-id="37ab3-120">[\[DeviceInstall\] Keys](#deviceinstall-keys)</span></span>
    -   [<span data-ttu-id="37ab3-121">DriverPath</span><span class="sxs-lookup"><span data-stu-id="37ab3-121">DriverPath</span></span>](#driverpath)

## <a name="autorun-keys"></a><span data-ttu-id="37ab3-122">\[\]Chiavi Autorun</span><span class="sxs-lookup"><span data-stu-id="37ab3-122">\[AutoRun\] Keys</span></span>

-   [<span data-ttu-id="37ab3-123">action</span><span class="sxs-lookup"><span data-stu-id="37ab3-123">action</span></span>](#parameters)
-   [<span data-ttu-id="37ab3-124">CustomEvent</span><span class="sxs-lookup"><span data-stu-id="37ab3-124">CustomEvent</span></span>](#customevent)
-   [<span data-ttu-id="37ab3-125">icona</span><span class="sxs-lookup"><span data-stu-id="37ab3-125">icon</span></span>](#parameters)
-   [<span data-ttu-id="37ab3-126">label</span><span class="sxs-lookup"><span data-stu-id="37ab3-126">label</span></span>](#parameters)
-   [<span data-ttu-id="37ab3-127">open</span><span class="sxs-lookup"><span data-stu-id="37ab3-127">open</span></span>](#parameters)
-   [<span data-ttu-id="37ab3-128">UseAutoPlay</span><span class="sxs-lookup"><span data-stu-id="37ab3-128">UseAutoPlay</span></span>](#parameters)
-   [<span data-ttu-id="37ab3-129">ShellExecute</span><span class="sxs-lookup"><span data-stu-id="37ab3-129">shellexecute</span></span>](#shellexecute)
-   [<span data-ttu-id="37ab3-130">Shell</span><span class="sxs-lookup"><span data-stu-id="37ab3-130">shell</span></span>](#autoruninf-entries)
-   [<span data-ttu-id="37ab3-131">Verbo della shell \\</span><span class="sxs-lookup"><span data-stu-id="37ab3-131">shell\\verb</span></span>](#shellverb)

### <a name="action"></a><span data-ttu-id="37ab3-132">azione</span><span class="sxs-lookup"><span data-stu-id="37ab3-132">action</span></span>

<span data-ttu-id="37ab3-133">La voce **Action** specifica il testo usato nella finestra di dialogo AutoPlay per il gestore che rappresenta il programma specificato nella voce [Open](#parameters) o [ShellExecute](#shellexecute) nel file Autorun. inf del supporto.</span><span class="sxs-lookup"><span data-stu-id="37ab3-133">The **action** entry specifies the text that is used in the Autoplay dialog for the handler representing the program specified in the [open](#parameters) or [shellexecute](#shellexecute) entry in the media's Autorun.inf file.</span></span> <span data-ttu-id="37ab3-134">Il valore può essere espresso come testo o come risorsa archiviata in un file binario.</span><span class="sxs-lookup"><span data-stu-id="37ab3-134">The value can be expressed as either text or as a resource stored in a binary.</span></span>


```
action=ActionText
```




```
action=@[filepath\]filename,-resourceID
```



### <a name="parameters"></a><span data-ttu-id="37ab3-135">Parametri</span><span class="sxs-lookup"><span data-stu-id="37ab3-135">Parameters</span></span>

-   <span data-ttu-id="37ab3-136">*ActionText*</span><span class="sxs-lookup"><span data-stu-id="37ab3-136">*ActionText*</span></span>

    <span data-ttu-id="37ab3-137">Testo utilizzato nella finestra di dialogo AutoPlay per il gestore che rappresenta il programma specificato nella voce [Open](#parameters) o [ShellExecute](#shellexecute) nel file Autorun. inf del supporto.</span><span class="sxs-lookup"><span data-stu-id="37ab3-137">Text that is used in the Autoplay dialog for the handler representing the program specified in the [open](#parameters) or [shellexecute](#shellexecute) entry in the media's Autorun.inf file.</span></span>

-   <span data-ttu-id="37ab3-138">*FilePath*</span><span class="sxs-lookup"><span data-stu-id="37ab3-138">*filepath*</span></span>

    <span data-ttu-id="37ab3-139">Stringa che contiene il percorso completo della directory che contiene il file binario contenente la stringa.</span><span class="sxs-lookup"><span data-stu-id="37ab3-139">A string that contains the fully qualified path of the directory that contains the binary file containing the string.</span></span> <span data-ttu-id="37ab3-140">Se non viene specificato alcun percorso, il file deve trovarsi nella directory radice dell'unità.</span><span class="sxs-lookup"><span data-stu-id="37ab3-140">If no path is specified, the file must be in the drive's root directory.</span></span>

-   <span data-ttu-id="37ab3-141">*filename*</span><span class="sxs-lookup"><span data-stu-id="37ab3-141">*filename*</span></span>

    <span data-ttu-id="37ab3-142">Stringa che contiene il nome del file binario.</span><span class="sxs-lookup"><span data-stu-id="37ab3-142">A string that contains the binary file's name.</span></span>

-   <span data-ttu-id="37ab3-143">*resourceID*</span><span class="sxs-lookup"><span data-stu-id="37ab3-143">*resourceID*</span></span>

    <span data-ttu-id="37ab3-144">ID della stringa nel file binario.</span><span class="sxs-lookup"><span data-stu-id="37ab3-144">The ID of the string within the binary file.</span></span>

### <a name="remarks"></a><span data-ttu-id="37ab3-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="37ab3-145">Remarks</span></span>

<span data-ttu-id="37ab3-146">La chiave **Action** viene utilizzata solo in Windows XP Service Pack 2 (SP2) o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="37ab3-146">The **action** key is only used in Windows XP Service Pack 2 (SP2) or later.</span></span> <span data-ttu-id="37ab3-147">È supportato solo per le unità di tipo unità \_ rimovibili e unità \_ fisse.</span><span class="sxs-lookup"><span data-stu-id="37ab3-147">It is only supported for drives of type DRIVE\_REMOVABLE and DRIVE\_FIXED.</span></span> <span data-ttu-id="37ab3-148">Nel caso di un'unità \_ rimovibile, la chiave dell' **azione** è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="37ab3-148">In the case of DRIVE\_REMOVABLE, the **action** key is required.</span></span> <span data-ttu-id="37ab3-149">Un comando di **azione** nel file Autorun. inf di un CD audio o di un DVD di film viene ignorato e questi supporti continuano a funzionare come in Windows XP Service Pack 1 (SP1) e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="37ab3-149">An **action** command in the Autorun.inf file of an audio CD or movie DVD is ignored, and these media continue to behave as in Windows XP Service Pack 1 (SP1) and earlier.</span></span>

<span data-ttu-id="37ab3-150">La stringa visualizzata nella finestra di dialogo AutoPlay viene costruita combinando il testo specificato nella voce di **azione** con un testo hardcoded che denomina il provider, fornito dalla Shell.</span><span class="sxs-lookup"><span data-stu-id="37ab3-150">The string displayed in the Autoplay dialog is constructed by combining the text specified in the **action** entry with hard-coded text naming the provider, provided by the Shell.</span></span> <span data-ttu-id="37ab3-151">L' [icona](#parameters) viene visualizzata accanto a essa.</span><span class="sxs-lookup"><span data-stu-id="37ab3-151">The [icon](#parameters) is displayed next to it.</span></span> <span data-ttu-id="37ab3-152">Questa voce viene sempre visualizzata come prima opzione nella finestra di dialogo AutoPlay ed è selezionata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="37ab3-152">This entry always appears as the first option in the Autoplay dialog and is selected by default.</span></span> <span data-ttu-id="37ab3-153">Se l'utente accetta l'opzione, viene avviata l'applicazione specificata dalla voce [Open](#parameters) o [ShellExecute](#shellexecute) nel file Autorun. inf del supporto.</span><span class="sxs-lookup"><span data-stu-id="37ab3-153">If the user accepts the option, the application specified by the [open](#parameters) or [shellexecute](#shellexecute) entry in the media's Autorun.inf file is launched.</span></span> <span data-ttu-id="37ab3-154">L'opzione **Esegui sempre l'azione selezionata** non è disponibile in questa situazione.</span><span class="sxs-lookup"><span data-stu-id="37ab3-154">The **Always do the selected action** option is not available in this situation.</span></span>

<span data-ttu-id="37ab3-155">I tasti [Action](#parameters) e [Icon](#parameters) definiscono insieme la rappresentazione dell'applicazione visualizzata dall'utente finale nella finestra di dialogo AutoPlay.</span><span class="sxs-lookup"><span data-stu-id="37ab3-155">The [action](#parameters) and [icon](#parameters) keys together define the representation of the application that is seen by the end user in the Autoplay dialog.</span></span> <span data-ttu-id="37ab3-156">Devono essere composte in modo che gli utenti possano identificarle facilmente.</span><span class="sxs-lookup"><span data-stu-id="37ab3-156">They should be composed in such a way that users can easily identify them.</span></span> <span data-ttu-id="37ab3-157">Devono indicare che l'applicazione deve essere eseguita, la società che la ha creata ed eventuali personalizzazioni associate.</span><span class="sxs-lookup"><span data-stu-id="37ab3-157">They should indicate the application to be run, the company that created it, and any associated branding.</span></span>

<span data-ttu-id="37ab3-158">Per compatibilità con le versioni precedenti, la voce **azione** è facoltativa per i dispositivi di tipo unità \_ fisse.</span><span class="sxs-lookup"><span data-stu-id="37ab3-158">For backward compatibility, the **action** entry is optional for devices of type DRIVE\_FIXED.</span></span> <span data-ttu-id="37ab3-159">Per questo tipo, nella finestra di dialogo AutoPlay viene utilizzata una voce predefinita se nel file Autorun. inf non è presente alcuna voce di **azione** .</span><span class="sxs-lookup"><span data-stu-id="37ab3-159">For this type, a default entry is used in the Autoplay dialog if no **action** entry is present in the Autorun.inf file.</span></span>

<span data-ttu-id="37ab3-160">La voce di **azione** è obbligatoria per i dispositivi di tipo unità \_ rimovibile, che fino a questo momento non dispone del supporto Autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="37ab3-160">The **action** entry is mandatory for devices of type DRIVE\_REMOVABLE, which until now did not have Autorun.inf support.</span></span> <span data-ttu-id="37ab3-161">Se non è presente alcuna voce di **azione** , viene visualizzata la finestra di dialogo AutoPlay, ma senza l'opzione per avviare il contenuto aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="37ab3-161">If no **action** entry is present, the Autoplay dialog is displayed but with no option to launch the additional content.</span></span>

### <a name="customevent"></a><span data-ttu-id="37ab3-162">CustomEvent</span><span class="sxs-lookup"><span data-stu-id="37ab3-162">CustomEvent</span></span>

<span data-ttu-id="37ab3-163">La voce **CustomEvent** specifica un evento di contenuto AutoPlay personalizzato.</span><span class="sxs-lookup"><span data-stu-id="37ab3-163">The **CustomEvent** entry specifies a custom AutoPlay content event.</span></span>


```
CustomEvent=CustomEventName
```



### <a name="parameters"></a><span data-ttu-id="37ab3-164">Parametri</span><span class="sxs-lookup"><span data-stu-id="37ab3-164">Parameters</span></span>

-   <span data-ttu-id="37ab3-165">*CustomEventName*</span><span class="sxs-lookup"><span data-stu-id="37ab3-165">*CustomEventName*</span></span>

    <span data-ttu-id="37ab3-166">Stringa di testo contenente il nome dell'evento di contenuto AutoPlay.</span><span class="sxs-lookup"><span data-stu-id="37ab3-166">A text string containing the name of the AutoPlay content event.</span></span> <span data-ttu-id="37ab3-167">Il nome non deve contenere più di 100 caratteri alfanumerici.</span><span class="sxs-lookup"><span data-stu-id="37ab3-167">The name must be no more than 100 alphanumeric characters.</span></span>

### <a name="remarks"></a><span data-ttu-id="37ab3-168">Commenti</span><span class="sxs-lookup"><span data-stu-id="37ab3-168">Remarks</span></span>

<span data-ttu-id="37ab3-169">È possibile includere un nome di evento personalizzato nel file Autorun. inf di un volume.</span><span class="sxs-lookup"><span data-stu-id="37ab3-169">You can include a custom event name in the Autorun.inf file of a volume.</span></span> <span data-ttu-id="37ab3-170">Quando AutoPlay chiede all'utente l'uso di un'applicazione con il volume, Visualizza solo le applicazioni che hanno effettuato la registrazione per il nome dell'evento personalizzato specificato.</span><span class="sxs-lookup"><span data-stu-id="37ab3-170">When AutoPlay prompts the user for an application to use with the volume, it displays only applications that have registered for the specified custom event name.</span></span> <span data-ttu-id="37ab3-171">Per informazioni su come registrare un'applicazione come gestore per l'evento di contenuto AutoPlay personalizzato, vedere [avvio automatico con AutoPlay](/previous-versions/windows/apps/hh452731(v=win.10)) o [come registrare un gestore eventi](how-to-register-an-event-handler.md).</span><span class="sxs-lookup"><span data-stu-id="37ab3-171">For information on how you can register an application as a handler for your custom AutoPlay content event, see [Auto-launching with AutoPlay](/previous-versions/windows/apps/hh452731(v=win.10)) or [How to Register an Event Handler](how-to-register-an-event-handler.md).</span></span>

<span data-ttu-id="37ab3-172">Nell'esempio seguente viene specificato il valore "MyContentOnArrival" come nuovo evento di contenuto AutoPlay.</span><span class="sxs-lookup"><span data-stu-id="37ab3-172">The following example specifies the value "MyContentOnArrival" as a new AutoPlay content event.</span></span>


```
CustomEvent=MyContentOnArrival
```



### <a name="icon"></a><span data-ttu-id="37ab3-173">icon</span><span class="sxs-lookup"><span data-stu-id="37ab3-173">icon</span></span>

<span data-ttu-id="37ab3-174">La voce **icona** specifica un'icona che rappresenta l'unità abilitata per l'esecuzione automatica nell'interfaccia utente di Windows.</span><span class="sxs-lookup"><span data-stu-id="37ab3-174">The **icon** entry specifies an icon which represents the AutoRun-enabled drive in the Windows user interface.</span></span>


```
icon=iconfilename[,index]
```



### <a name="parameters"></a><span data-ttu-id="37ab3-175">Parametri</span><span class="sxs-lookup"><span data-stu-id="37ab3-175">Parameters</span></span>

-   <span data-ttu-id="37ab3-176">*IconFileName*</span><span class="sxs-lookup"><span data-stu-id="37ab3-176">*iconfilename*</span></span>

    <span data-ttu-id="37ab3-177">Nome di un file con estensione ICO, BMP, exe o dll contenente le informazioni sull'icona.</span><span class="sxs-lookup"><span data-stu-id="37ab3-177">Name of an .ico, .bmp, .exe, or .dll file containing the icon information.</span></span> <span data-ttu-id="37ab3-178">Se un file contiene più di un'icona, è necessario specificare anche un indice in base zero dell'icona.</span><span class="sxs-lookup"><span data-stu-id="37ab3-178">If a file contains more than one icon, you must also specify zero-based index of the icon.</span></span>

### <a name="remarks"></a><span data-ttu-id="37ab3-179">Commenti</span><span class="sxs-lookup"><span data-stu-id="37ab3-179">Remarks</span></span>

<span data-ttu-id="37ab3-180">L'icona, insieme all'etichetta, rappresenta l'unità abilitata per l'esecuzione automatica nell'interfaccia utente di Windows.</span><span class="sxs-lookup"><span data-stu-id="37ab3-180">The icon, together with the label, represents the AutoRun-enabled drive in the Windows user interface.</span></span> <span data-ttu-id="37ab3-181">Ad esempio, in Esplora risorse l'unità viene rappresentata da questa icona anziché dall'icona dell'unità standard.</span><span class="sxs-lookup"><span data-stu-id="37ab3-181">For instance, in Windows Explorer, the drive is represented by this icon instead of the standard drive icon.</span></span> <span data-ttu-id="37ab3-182">Il file dell'icona deve trovarsi nella stessa directory del file specificato dal comando [Apri](#parameters) .</span><span class="sxs-lookup"><span data-stu-id="37ab3-182">The icon's file must be in the same directory as the file specified by the [open](#parameters) command.</span></span>

<span data-ttu-id="37ab3-183">Nell'esempio seguente viene specificata la seconda icona nel file di MyProg.exe.</span><span class="sxs-lookup"><span data-stu-id="37ab3-183">The following example specifies the second icon in the MyProg.exe file.</span></span>


```
icon=MyProg.exe,1
```



### <a name="label"></a><span data-ttu-id="37ab3-184">label</span><span class="sxs-lookup"><span data-stu-id="37ab3-184">label</span></span>

<span data-ttu-id="37ab3-185">La voce **etichetta** specifica un'etichetta di testo che rappresenta l'unità abilitata per l'esecuzione automatica nell'interfaccia utente di Windows.</span><span class="sxs-lookup"><span data-stu-id="37ab3-185">The **label** entry specifies a text label which represents the AutoRun-enabled drive in the Windows user interface.</span></span>


```
label=LabelText
```



### <a name="parameters"></a><span data-ttu-id="37ab3-186">Parametri</span><span class="sxs-lookup"><span data-stu-id="37ab3-186">Parameters</span></span>

-   <span data-ttu-id="37ab3-187">*LabelText*</span><span class="sxs-lookup"><span data-stu-id="37ab3-187">*LabelText*</span></span>

    <span data-ttu-id="37ab3-188">Stringa di testo contenente l'etichetta.</span><span class="sxs-lookup"><span data-stu-id="37ab3-188">A text string containing the label.</span></span> <span data-ttu-id="37ab3-189">Può contenere spazi e non deve contenere più di 32 caratteri.</span><span class="sxs-lookup"><span data-stu-id="37ab3-189">It can contain spaces and should be no longer than 32 characters.</span></span>

> [!Note]  
> <span data-ttu-id="37ab3-190">È possibile inserire un valore nel parametro **LabelText** che supera i 32 caratteri e non viene visualizzato alcun messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="37ab3-190">It is possible to put a value in the **LabelText** parameter which exceeds 32 characters and receive no error message.</span></span> <span data-ttu-id="37ab3-191">Tuttavia, nel sistema vengono visualizzati solo i primi 32 caratteri.</span><span class="sxs-lookup"><span data-stu-id="37ab3-191">However, the system only displays the first 32 characters.</span></span> <span data-ttu-id="37ab3-192">Qualsiasi carattere dopo la 32a viene troncato e non viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="37ab3-192">Any characters after the 32nd are truncated and not displayed.</span></span> <span data-ttu-id="37ab3-193">Ad esempio, se **LabelText** è il seguente: label = "questo CD è progettato per essere il CD musicale finale".</span><span class="sxs-lookup"><span data-stu-id="37ab3-193">For example, if the **LabelText** is as follows: label="This CD is designed to be the ultimate music CD."</span></span> <span data-ttu-id="37ab3-194">verrà visualizzato quanto segue: "questo CD è progettato per essere UL".</span><span class="sxs-lookup"><span data-stu-id="37ab3-194">the following will be displayed, "This CD is designed to be the ul".</span></span>

 

### <a name="remarks"></a><span data-ttu-id="37ab3-195">Commenti</span><span class="sxs-lookup"><span data-stu-id="37ab3-195">Remarks</span></span>

<span data-ttu-id="37ab3-196">L'etichetta, insieme a un'icona, rappresenta l'unità abilitata per l'esecuzione automatica nell'interfaccia utente di Windows.</span><span class="sxs-lookup"><span data-stu-id="37ab3-196">The label, together with an icon, represents the AutoRun-enabled drive in the Windows user interface.</span></span>

<span data-ttu-id="37ab3-197">Nell'esempio seguente viene specificato il valore "My Drive label" come etichetta dell'unità.</span><span class="sxs-lookup"><span data-stu-id="37ab3-197">The following example specifies the value "My Drive Label" as the drive's label.</span></span>


```
label=My Drive Label
```



### <a name="open"></a><span data-ttu-id="37ab3-198">apre</span><span class="sxs-lookup"><span data-stu-id="37ab3-198">open</span></span>

<span data-ttu-id="37ab3-199">La voce di **apertura** specifica il percorso e il nome file dell'applicazione avviata dall'avvio automatico quando un utente inserisce un disco nell'unità.</span><span class="sxs-lookup"><span data-stu-id="37ab3-199">The **open** entry specifies the path and file name of the application that AutoRun launches when a user inserts a disc in the drive.</span></span>


```
open=[exepath\]exefile [param1 [param2] ...] 
```



### <a name="parameters"></a><span data-ttu-id="37ab3-200">Parametri</span><span class="sxs-lookup"><span data-stu-id="37ab3-200">Parameters</span></span>

-   <span data-ttu-id="37ab3-201">*exefile*</span><span class="sxs-lookup"><span data-stu-id="37ab3-201">*exefile*</span></span>

    <span data-ttu-id="37ab3-202">Percorso completo di un file eseguibile che viene eseguito al momento dell'inserimento del CD.</span><span class="sxs-lookup"><span data-stu-id="37ab3-202">Fully qualified path of an executable file that runs when the CD is inserted.</span></span> <span data-ttu-id="37ab3-203">Se viene specificato solo un nome file, deve trovarsi nella directory radice dell'unità.</span><span class="sxs-lookup"><span data-stu-id="37ab3-203">If only a file name is specified, it must be in drive's root directory.</span></span> <span data-ttu-id="37ab3-204">Per individuare il file in una sottodirectory, è necessario specificare un percorso.</span><span class="sxs-lookup"><span data-stu-id="37ab3-204">To locate the file in a subdirectory, you must specify a path.</span></span> <span data-ttu-id="37ab3-205">È inoltre possibile includere uno o più parametri della riga di comando da passare all'applicazione di avvio.</span><span class="sxs-lookup"><span data-stu-id="37ab3-205">You can also include one or more command-line parameters to pass to the startup application.</span></span>

### <a name="useautoplay"></a><span data-ttu-id="37ab3-206">UseAutoPlay</span><span class="sxs-lookup"><span data-stu-id="37ab3-206">UseAutoPlay</span></span>

<span data-ttu-id="37ab3-207">In Windows XP, la voce **UseAutoPlay** specifica che è necessario usare AutoPlay anziché Autorun.</span><span class="sxs-lookup"><span data-stu-id="37ab3-207">On Windows XP, the **UseAutoPlay** entry specifies that AutoPlay should be used instead of AutoRun.</span></span>

<span data-ttu-id="37ab3-208">In Windows Vista e versioni successive, questa voce provoca l'eliminazione di tutte le azioni specificate per l'esecuzione automatica (usando le voci **Open** o **ShellExecute** ) dalla finestra di dialogo AutoPlay.</span><span class="sxs-lookup"><span data-stu-id="37ab3-208">On Windows Vista and later, this entry causes any actions specified for AutoRun (by using either the **open** or **shellexecute** entries) to be suppressed from the AutoPlay dialog.</span></span> <span data-ttu-id="37ab3-209">Questa voce non ha alcun effetto sulle versioni di Windows precedenti a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="37ab3-209">This entry has no effect on versions of Windows earlier than Windows XP.</span></span>

<span data-ttu-id="37ab3-210">In Windows 8 e versioni successive, se si specifica il valore 0 verrà disabilitato AutoPlay per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37ab3-210">On Windows 8 and later, specifying a value of 0 will disable autoplay for this device.</span></span>

### <a name="parameters"></a><span data-ttu-id="37ab3-211">Parametri</span><span class="sxs-lookup"><span data-stu-id="37ab3-211">Parameters</span></span>

<span data-ttu-id="37ab3-212">Per usare questa opzione, aggiungere una voce per **UseAutoPlay** al file Autorun. inf e impostare la voce uguale a 1.</span><span class="sxs-lookup"><span data-stu-id="37ab3-212">To use this option, add an entry for **UseAutoPlay** to the Autorun.inf file and set the entry equal to 1.</span></span> <span data-ttu-id="37ab3-213">Nessun altro valore è supportato nelle versioni di Windows precedenti a Windows 8.</span><span class="sxs-lookup"><span data-stu-id="37ab3-213">No other value is supported on versions of Windows earlier than Windows 8.</span></span>

<span data-ttu-id="37ab3-214">In Windows 8 e versioni successive, specificare il valore 0 per disabilitare AutoPlay per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37ab3-214">On Windows 8 and later, specify a value of 0 to disable autoplay for this device.</span></span>


```
UseAutoPlay=1
```



### <a name="remarks"></a><span data-ttu-id="37ab3-215">Commenti</span><span class="sxs-lookup"><span data-stu-id="37ab3-215">Remarks</span></span>

<span data-ttu-id="37ab3-216">Attualmente, **UseAutoPlay** è applicabile solo in Windows XP o versioni successive e solo in un'unità che [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea) determina di essere di tipo **unità \_ CDROM**.</span><span class="sxs-lookup"><span data-stu-id="37ab3-216">Currently, **UseAutoPlay** is applicable only on Windows XP or later and only on a drive that [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea) determines to be of type **DRIVE\_CDROM**.</span></span>

<span data-ttu-id="37ab3-217">Quando si utilizza **UseAutoPlay** , qualsiasi azione specificata dalle voci **aperte** o **ShellExecute** in autorun. inf viene ignorata in Windows XP e omessa dalla finestra di dialogo AutoPlay in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="37ab3-217">When **UseAutoPlay** is used, any action specified by the **open** or **shellexecute** entries in Autorun.inf is ignored on Windows XP and omitted from the AutoPlay dialog on Windows Vista.</span></span>

<span data-ttu-id="37ab3-218">AutoRun viene in genere usato per eseguire automaticamente o caricare elementi contenuti nel supporto inserito, mentre AutoPlay visualizza una finestra di dialogo che include un elenco di azioni rilevanti che possono essere eseguite e consente all'utente di scegliere l'azione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="37ab3-218">AutoRun is typically used to automatically run or load something contained on the inserted media, whereas AutoPlay presents a dialog that includes a list of relevant actions that may be taken and enables the user to choose which action to take.</span></span> <span data-ttu-id="37ab3-219">Per ulteriori informazioni sulla differenza tra AutoRun e AutoPlay, vedere [creazione di un'applicazione CD-ROM abilitata per l'autorun](autoplay.md) e [utilizzo e configurazione di AutoPlay](autoplay2k-using.md), rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="37ab3-219">For more information about the difference between AutoRun and AutoPlay, see [Creating an AutoRun-enabled CD-ROM Application](autoplay.md) and [Using and Configuring AutoPlay](autoplay2k-using.md), respectively.</span></span>

### <a name="usage-example"></a><span data-ttu-id="37ab3-220">Esempio di utilizzo</span><span class="sxs-lookup"><span data-stu-id="37ab3-220">Usage Example</span></span>

<span data-ttu-id="37ab3-221">Un CD contiene tre file: Autorun. inf, Readme.txt e Music. WMA.</span><span class="sxs-lookup"><span data-stu-id="37ab3-221">A CD contains three files: Autorun.inf, Readme.txt, and Music.wma.</span></span> <span data-ttu-id="37ab3-222">A seconda della versione di Windows in uso e delle opzioni specificate in autorun. inf, il CD può essere gestito da AutoRun o AutoPlay quando viene inserito (presupponendo che AutoRun/AutoPlay sia abilitato per l'unità in cui viene inserito il CD).</span><span class="sxs-lookup"><span data-stu-id="37ab3-222">Depending on the version of Windows in use and options specified in Autorun.inf, the CD may be handled by either AutoRun or AutoPlay when it is inserted (assuming AutoRun/AutoPlay is enabled for the drive into which the CD is inserted).</span></span>

<span data-ttu-id="37ab3-223">In primo luogo, si consideri un file Autorun. inf con il contenuto seguente, notando che **UseAutoPlay = 1** non è specificato:</span><span class="sxs-lookup"><span data-stu-id="37ab3-223">First, consider an Autorun.inf file with the following contents, noting that **UseAutoPlay=1** is not specified:</span></span>


```
[AutoRun]
shellexecute="Readme.txt"
```



<span data-ttu-id="37ab3-224">L'azione eseguita dalla shell quando questo CD viene inserito dipende dalla versione di Windows in uso:</span><span class="sxs-lookup"><span data-stu-id="37ab3-224">The action taken by the Shell when this CD is inserted depends on the version of Windows in use:</span></span>

-   <span data-ttu-id="37ab3-225">In Windows XP o versioni precedenti, questo CD viene gestito da AutoRun quando viene inserito.</span><span class="sxs-lookup"><span data-stu-id="37ab3-225">On Windows XP or earlier, this CD is handled by AutoRun when it is inserted.</span></span> <span data-ttu-id="37ab3-226">In questo caso, viene letta la voce **ShellExecute** e la shell richiama il gestore di file associato ai file con estensione txt; in genere, questo si apre Readme.txt nel blocco note.</span><span class="sxs-lookup"><span data-stu-id="37ab3-226">In this case, the **shellexecute** entry is read, and the Shell invokes the file handler associated with .txt files; typically this would open Readme.txt in Notepad.</span></span>
-   <span data-ttu-id="37ab3-227">In Windows Vista, la presenza di un file Autorun. inf con una voce **ShellExecute** fa sì che il supporto venga identificato come AutoPlay di tipo "software e giochi".</span><span class="sxs-lookup"><span data-stu-id="37ab3-227">On Windows Vista, the presence of an Autorun.inf file with a **shellexecute** entry causes the media to be identified as AutoPlay type "Software and games".</span></span> <span data-ttu-id="37ab3-228">In questo caso l'utente viene visualizzato con una finestra di dialogo AutoPlay che include l'azione specificata dalla voce **ShellExecute** (visualizzata come "Load Readme.txt" nella finestra di dialogo), insieme a azioni predefinite associate a supporti di tipo "software e giochi".</span><span class="sxs-lookup"><span data-stu-id="37ab3-228">In this case the user is presented with an AutoPlay dialog that includes the action specified by the **shellexecute** entry (presented as "Load Readme.txt" in the dialog), along with default actions associated with media of type "Software and games".</span></span>

<span data-ttu-id="37ab3-229">Per indicare che è necessario utilizzare AutoPlay anziché l'esecuzione automatica in Windows XP e che l'azione specificata dalla voce ShellExecute di AutoRun debba essere eliminata dalla finestra di dialogo AutoPlay in Windows Vista, inserire **UseAutoPlay** nel file Autorun. inf come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="37ab3-229">To indicate that AutoPlay should be used rather than AutoRun on Windows XP, and that the action specified by the AutoRun shellexecute entry should be suppressed from the AutoPlay dialog on Windows Vista, insert **UseAutoPlay** into the Autorun.inf file as follows:</span></span>


```
[AutoRun]
shellexecute="Readme.txt"
UseAutoPlay=1
```



<span data-ttu-id="37ab3-230">Ancora una volta, l'azione eseguita dalla shell quando questo CD viene inserito dipende dalla versione di Windows in uso.</span><span class="sxs-lookup"><span data-stu-id="37ab3-230">Once again, the action taken by the Shell when this CD is inserted depends on the version of Windows in use.</span></span>

-   <span data-ttu-id="37ab3-231">Nelle versioni di Windows precedenti a Windows XP, viene ancora utilizzato l'esecuzione automatica e viene eseguita l'azione specificata da **ShellExecute** , come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="37ab3-231">On versions of Windows earlier than Windows XP, AutoRun is still used and the action specified by **shellexecute** is performed, as described previously.</span></span> <span data-ttu-id="37ab3-232">Si noti che solo l'esecuzione automatica è disponibile nelle versioni di Windows precedenti a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="37ab3-232">(Note that only AutoRun is available on versions of Windows earlier than Windows XP.)</span></span>
-   <span data-ttu-id="37ab3-233">In Windows XP, la voce **UseAutoPlay** fa sì che AutoPlay venga usato al posto dell'autorun.</span><span class="sxs-lookup"><span data-stu-id="37ab3-233">On Windows XP, the **UseAutoPlay** entry causes AutoPlay to be used in place of AutoRun.</span></span> <span data-ttu-id="37ab3-234">In questo caso, AutoPlay determina che il supporto contiene un file di Windows Media Audio (WMA) e categorizza il contenuto come "file musicali".</span><span class="sxs-lookup"><span data-stu-id="37ab3-234">In this case, AutoPlay determines that the media contains a Windows Media Audio (.wma) file and categorizes the content as "Music files".</span></span> <span data-ttu-id="37ab3-235">L'utente viene visualizzato con una finestra di dialogo AutoPlay contenente i gestori registrati per il tipo di supporto AutoPlay "Music Files"; la voce ShellExecute AutoRun viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="37ab3-235">The user is presented with an AutoPlay dialog containing registered handlers for the "Music files" AutoPlay media type; the AutoRun shellexecute entry is ignored.</span></span>

### <a name="shellexecute"></a><span data-ttu-id="37ab3-236">ShellExecute</span><span class="sxs-lookup"><span data-stu-id="37ab3-236">shellexecute</span></span>

[<span data-ttu-id="37ab3-237">Versione 5,0.</span><span class="sxs-lookup"><span data-stu-id="37ab3-237">Version 5.0.</span></span>](versions.md) <span data-ttu-id="37ab3-238">La voce **ShellExecute** specifica un'applicazione o un file di dati che l'esecuzione automatica userà per chiamare [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="37ab3-238">The **shellexecute** entry specifies an application or data file that AutoRun will use to call [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>


```
shellexecute=[filepath\]filename[param1, [param2]...] 
```



### <a name="parameters"></a><span data-ttu-id="37ab3-239">Parametri</span><span class="sxs-lookup"><span data-stu-id="37ab3-239">Parameters</span></span>

-   <span data-ttu-id="37ab3-240">*FilePath*</span><span class="sxs-lookup"><span data-stu-id="37ab3-240">*filepath*</span></span>

    <span data-ttu-id="37ab3-241">Stringa che contiene il percorso completo della directory che contiene i dati o il file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="37ab3-241">A string that contains the fully qualified path of the directory that contains the data or executable file.</span></span> <span data-ttu-id="37ab3-242">Se non viene specificato alcun percorso, il file deve trovarsi nella directory radice dell'unità.</span><span class="sxs-lookup"><span data-stu-id="37ab3-242">If no path is specified, the file must be in the drive's root directory.</span></span>

-   <span data-ttu-id="37ab3-243">*filename*</span><span class="sxs-lookup"><span data-stu-id="37ab3-243">*filename*</span></span>

    <span data-ttu-id="37ab3-244">Stringa che contiene il nome del file.</span><span class="sxs-lookup"><span data-stu-id="37ab3-244">A string that contains the file's name.</span></span> <span data-ttu-id="37ab3-245">Se è un file eseguibile, viene avviato.</span><span class="sxs-lookup"><span data-stu-id="37ab3-245">If it is an executable file, it is launched.</span></span> <span data-ttu-id="37ab3-246">Se è un file di dati, deve essere un membro di un [tipo di file](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="37ab3-246">If it is a data file, it must be a member of a [file type](fa-file-types.md).</span></span> <span data-ttu-id="37ab3-247">[**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) avvia il comando predefinito associato al tipo di file.</span><span class="sxs-lookup"><span data-stu-id="37ab3-247">[**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) launches the default command associated with the file type.</span></span>

-   <span data-ttu-id="37ab3-248">*paramx*</span><span class="sxs-lookup"><span data-stu-id="37ab3-248">*paramx*</span></span>

    <span data-ttu-id="37ab3-249">Contiene eventuali parametri aggiuntivi che devono essere passati a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="37ab3-249">Contains any additional parameters that should be passed to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

### <a name="remarks"></a><span data-ttu-id="37ab3-250">Commenti</span><span class="sxs-lookup"><span data-stu-id="37ab3-250">Remarks</span></span>

<span data-ttu-id="37ab3-251">Questa voce è simile a [Apri](#parameters), ma consente di usare le informazioni di [associazione file](fa-intro.md) per eseguire l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37ab3-251">This entry is similar to [open](#parameters), but it allows you to use [file association](fa-intro.md) information to run the application.</span></span>

### <a name="shell"></a><span data-ttu-id="37ab3-252">shell</span><span class="sxs-lookup"><span data-stu-id="37ab3-252">shell</span></span>

<span data-ttu-id="37ab3-253">La voce della **Shell** specifica un comando predefinito per il menu di scelta rapida dell'unità.</span><span class="sxs-lookup"><span data-stu-id="37ab3-253">The **shell** entry specifies a default command for the drive's shortcut menu.</span></span>


```
shell=verb
```



### <a name="parameters"></a><span data-ttu-id="37ab3-254">Parametri</span><span class="sxs-lookup"><span data-stu-id="37ab3-254">Parameters</span></span>

-   <span data-ttu-id="37ab3-255">*verb*</span><span class="sxs-lookup"><span data-stu-id="37ab3-255">*verb*</span></span>

    <span data-ttu-id="37ab3-256">Verbo che corrisponde al comando di menu.</span><span class="sxs-lookup"><span data-stu-id="37ab3-256">The verb that corresponds to the menu command.</span></span> <span data-ttu-id="37ab3-257">Il verbo e il relativo comando di menu associato devono essere definiti nel file Autorun. inf con una voce del [ \\ verbo della shell](#shellverb) .</span><span class="sxs-lookup"><span data-stu-id="37ab3-257">The verb and its associated menu command must be defined in the Autorun.inf file with a [shell\\verb](#shellverb) entry.</span></span>

### <a name="remarks"></a><span data-ttu-id="37ab3-258">Commenti</span><span class="sxs-lookup"><span data-stu-id="37ab3-258">Remarks</span></span>

<span data-ttu-id="37ab3-259">Quando si fa clic con il pulsante destro del mouse sull'icona dell'unità, viene visualizzato un menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="37ab3-259">When a user right-clicks the drive icon, a shortcut menu appears.</span></span> <span data-ttu-id="37ab3-260">Se è presente un file Autorun. inf, viene sottratto il comando di menu di scelta rapida predefinito.</span><span class="sxs-lookup"><span data-stu-id="37ab3-260">If an Autorun.inf file is present, the default shortcut menu command is taken from it.</span></span> <span data-ttu-id="37ab3-261">Questo comando viene eseguito anche quando l'utente fa doppio clic sull'icona dell'unità.</span><span class="sxs-lookup"><span data-stu-id="37ab3-261">This command also executes when the user double-clicks the drive's icon.</span></span>

<span data-ttu-id="37ab3-262">Per specificare il comando di menu di scelta rapida predefinito, definirne innanzitutto il verbo, la stringa di comando e il testo del menu con il [ \\ verbo della shell](#shellverb).</span><span class="sxs-lookup"><span data-stu-id="37ab3-262">To specify the default shortcut menu command, first define its verb, command string, and menu text with [shell\\verb](#shellverb).</span></span> <span data-ttu-id="37ab3-263">Usare quindi Shell per impostarlo come comando di menu di scelta rapida predefinito.</span><span class="sxs-lookup"><span data-stu-id="37ab3-263">Then use shell to make it the default shortcut menu command.</span></span> <span data-ttu-id="37ab3-264">In caso contrario, il testo predefinito della voce di menu sarà "AutoPlay", che avvia l'applicazione specificata dalla voce di [apertura](#parameters) .</span><span class="sxs-lookup"><span data-stu-id="37ab3-264">Otherwise, the default menu item text will be "AutoPlay", which launches the application specified by the [open](#parameters) entry.</span></span>

### <a name="shellverb"></a><span data-ttu-id="37ab3-265">Verbo della shell \\</span><span class="sxs-lookup"><span data-stu-id="37ab3-265">shell\\verb</span></span>

<span data-ttu-id="37ab3-266">La voce del **\\ verbo della shell** aggiunge un comando personalizzato al menu di scelta rapida dell'unità.</span><span class="sxs-lookup"><span data-stu-id="37ab3-266">The **shell\\verb** entry adds a custom command to the drive's shortcut menu.</span></span>


```
shell\verb\command=Filename.exe 
shell\verb=MenuText
```



### <a name="parameters"></a><span data-ttu-id="37ab3-267">Parametri</span><span class="sxs-lookup"><span data-stu-id="37ab3-267">Parameters</span></span>

-   <span data-ttu-id="37ab3-268">*verb*</span><span class="sxs-lookup"><span data-stu-id="37ab3-268">*verb*</span></span>

    <span data-ttu-id="37ab3-269">Verbo del comando di menu.</span><span class="sxs-lookup"><span data-stu-id="37ab3-269">The menu command's verb.</span></span> <span data-ttu-id="37ab3-270">La voce di *_\\ comando_* del _verbo_ della **Shell \\** associa il verbo a un file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="37ab3-270">The **shell\\**_verb_*_\\command_* entry associates the verb with an executable file.</span></span> <span data-ttu-id="37ab3-271">I verbi non devono contenere spazi incorporati.</span><span class="sxs-lookup"><span data-stu-id="37ab3-271">Verbs must not contain embedded spaces.</span></span> <span data-ttu-id="37ab3-272">Per impostazione predefinita, *Verb* è il testo visualizzato nel menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="37ab3-272">By default, *verb* is the text that is displayed in the shortcut menu.</span></span>

-   <span data-ttu-id="37ab3-273">*Filename.exe*</span><span class="sxs-lookup"><span data-stu-id="37ab3-273">*Filename.exe*</span></span>

    <span data-ttu-id="37ab3-274">Il percorso e il nome file dell'applicazione che esegue l'azione.</span><span class="sxs-lookup"><span data-stu-id="37ab3-274">The path and file name of the application that performs the action.</span></span>

-   <span data-ttu-id="37ab3-275">*MenuText*</span><span class="sxs-lookup"><span data-stu-id="37ab3-275">*MenuText*</span></span>

    <span data-ttu-id="37ab3-276">Questo parametro specifica il testo visualizzato nel menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="37ab3-276">This parameter specifies the text that is displayed in the shortcut menu.</span></span> <span data-ttu-id="37ab3-277">Se viene omesso, viene visualizzato il *verbo* .</span><span class="sxs-lookup"><span data-stu-id="37ab3-277">If it is omitted, *verb* is displayed.</span></span> <span data-ttu-id="37ab3-278">*MenuText* può essere costituito da maiuscole e minuscole e può contenere spazi.</span><span class="sxs-lookup"><span data-stu-id="37ab3-278">*MenuText* can be mixed-case and can contain spaces.</span></span> <span data-ttu-id="37ab3-279">È possibile impostare un tasto di scelta rapida per la voce di menu inserendo una e commerciale (&) davanti alla lettera.</span><span class="sxs-lookup"><span data-stu-id="37ab3-279">You can set a shortcut key for the menu item by putting an ampersand (&) in front of the letter.</span></span>

### <a name="remarks"></a><span data-ttu-id="37ab3-280">Commenti</span><span class="sxs-lookup"><span data-stu-id="37ab3-280">Remarks</span></span>

<span data-ttu-id="37ab3-281">Quando si fa clic con il pulsante destro del mouse sull'icona dell'unità, viene visualizzato un menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="37ab3-281">When a user right-clicks the drive icon, a shortcut menu appears.</span></span> <span data-ttu-id="37ab3-282">L'aggiunta di voci di **\\ verbi Shell** al file Autorun. inf dell'unità consente di aggiungere comandi a questo menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="37ab3-282">Adding **shell\\verb** entries to the drive's Autorun.inf file allows you to add commands to this shortcut menu.</span></span>

<span data-ttu-id="37ab3-283">Questa voce è costituita da due parti, che devono essere su righe separate.</span><span class="sxs-lookup"><span data-stu-id="37ab3-283">There are two parts to this entry, which must be on separate lines.</span></span> <span data-ttu-id="37ab3-284">La prima parte è il *_\\ comando_* del _verbo_ della **Shell \\**.</span><span class="sxs-lookup"><span data-stu-id="37ab3-284">The first part is **shell\\**_verb_*_\\command_*.</span></span> <span data-ttu-id="37ab3-285">Questo argomento è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="37ab3-285">It is required.</span></span> <span data-ttu-id="37ab3-286">Associa una stringa, denominata *verbo*, con l'applicazione da avviare quando viene eseguito il comando.</span><span class="sxs-lookup"><span data-stu-id="37ab3-286">It associates a string, called a *verb*, with the application to launch when the command runs.</span></span> <span data-ttu-id="37ab3-287">La seconda parte è la voce del _verbo_ della **Shell \\**.</span><span class="sxs-lookup"><span data-stu-id="37ab3-287">The second part is the **shell\\**_verb_ entry.</span></span> <span data-ttu-id="37ab3-288">Questo passaggio è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="37ab3-288">It is optional.</span></span> <span data-ttu-id="37ab3-289">È possibile includerlo per specificare il testo visualizzato nel menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="37ab3-289">You can include it to specify the text that displays in the shortcut menu.</span></span>

<span data-ttu-id="37ab3-290">Per specificare un comando di menu di scelta rapida predefinito, definire il verbo con il **\\ verbo della shell** e impostarlo come comando predefinito con la voce della [Shell](#autoruninf-entries) .</span><span class="sxs-lookup"><span data-stu-id="37ab3-290">To specify a default shortcut menu command, define the verb with **shell\\verb**, and make it the default command with the [shell](#autoruninf-entries) entry.</span></span>

<span data-ttu-id="37ab3-291">Il frammento di autorun. inf di esempio seguente associa il verbo *pronto* con la stringa di comando "Notepad ABC \\readme.txt".</span><span class="sxs-lookup"><span data-stu-id="37ab3-291">The following sample Autorun.inf fragment associates the *readit* verb with the command string "Notepad abc\\readme.txt".</span></span> <span data-ttu-id="37ab3-292">Il testo del menu è "Read me" è m'è definito come il tasto di scelta rapida dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="37ab3-292">The menu text is "Read Me", and 'M' is defined as the item's shortcut key.</span></span> <span data-ttu-id="37ab3-293">Quando l'utente seleziona questo comando, \\ viene aperto il file abcreadme.txt dell'unità con il blocco note di Microsoft.</span><span class="sxs-lookup"><span data-stu-id="37ab3-293">When the user selects this command, the drive's abc\\readme.txt file opens with Microsoft Notepad.</span></span>


```
shell\readit\command=notepad abc\readme.txt 
shell\readit=Read &Me
```



## <a name="content-keys"></a><span data-ttu-id="37ab3-294">\[\]Chiavi simmetriche</span><span class="sxs-lookup"><span data-stu-id="37ab3-294">\[Content\] Keys</span></span>

<span data-ttu-id="37ab3-295">Sono disponibili tre chiavi di tipo file: **MusicFiles**, **PictureFiles** e **VideoFiles**.</span><span class="sxs-lookup"><span data-stu-id="37ab3-295">There are three file type keys: **MusicFiles**, **PictureFiles**, and **VideoFiles**.</span></span>

<span data-ttu-id="37ab3-296">Se uno di questi contenuti viene impostato su true tramite uno dei valori 1, y, Yes, t o true senza distinzione tra maiuscole e minuscole, l'interfaccia utente di AutoPlay Visualizza i gestori associati a tale tipo di contenuto, indipendentemente dal fatto che il contenuto del tipo esista sul supporto.</span><span class="sxs-lookup"><span data-stu-id="37ab3-296">If one of these contents is set to true through one the case-insensitive values 1, y, yes, t, or true, the Autoplay UI displays the handlers associated with that content type regardless of whether content of that type exists on the media.</span></span>

<span data-ttu-id="37ab3-297">Se uno di questi contenuti viene impostato su false tramite uno dei valori 0, n, no, f o false senza distinzione tra maiuscole e minuscole, l'interfaccia utente di AutoPlay non Visualizza i gestori associati a tale tipo di contenuto anche se il contenuto del tipo viene rilevato sul supporto.</span><span class="sxs-lookup"><span data-stu-id="37ab3-297">If one of these contents is set to false through one the case-insensitive values 0, n, no, f, or false, the Autoplay UI does not display the handlers associated with that content type even if content of that type is detected on the media.</span></span>

<span data-ttu-id="37ab3-298">L'uso di questa sezione consente agli autori di contenuti di comunicare lo scopo del contenuto a AutoPlay.</span><span class="sxs-lookup"><span data-stu-id="37ab3-298">Use of this section is intended to allow content authors to communicate the intent of content to Autoplay.</span></span> <span data-ttu-id="37ab3-299">Ad esempio, un CD può essere categorizzato in modo da contenere solo contenuto musicale anche se contiene anche immagini e video e altrimenti verrebbe visualizzato come contenuto misto.</span><span class="sxs-lookup"><span data-stu-id="37ab3-299">For instance, a CD can be categorized as containing only music content even though it also has pictures and videos and would otherwise be seen as having mixed content.</span></span>

<span data-ttu-id="37ab3-300">La sezione **\[ Content \]** è supportata solo in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="37ab3-300">The **\[Content\]** section is only supported under Windows Vista and later.</span></span>


```
[Content]
MusicFiles=Y
PictureFiles=0
VideoFiles=false
```



## <a name="exclusivecontentpaths-keys"></a><span data-ttu-id="37ab3-301">\[Chiavi di ExclusiveContentPaths \]</span><span class="sxs-lookup"><span data-stu-id="37ab3-301">\[ExclusiveContentPaths\] Keys</span></span>

<span data-ttu-id="37ab3-302">Le cartelle elencate in questa sezione limitano AutoPlay alla ricerca di contenuto solo nelle cartelle e nelle relative sottocartelle.</span><span class="sxs-lookup"><span data-stu-id="37ab3-302">Folders listed in this section limit Autoplay to searching only those folders and their subfolders for content.</span></span> <span data-ttu-id="37ab3-303">Possono essere specificati con o senza una barra rovesciata principale ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="37ab3-303">They can be given with or without a leading backslash (\\).</span></span> <span data-ttu-id="37ab3-304">In entrambi i casi vengono considerati percorsi assoluti dalla directory radice del supporto.</span><span class="sxs-lookup"><span data-stu-id="37ab3-304">In either case they are taken as absolute paths from the root directory of the media.</span></span> <span data-ttu-id="37ab3-305">Nel caso di cartelle con spazi nei nomi, non racchiuderle tra virgolette poiché le virgolette vengono eseguite letteralmente come parte del percorso.</span><span class="sxs-lookup"><span data-stu-id="37ab3-305">In the case of folders with spaces in their names, do not enclose them in quotes as the quotes are taken literally as part of the path.</span></span>

<span data-ttu-id="37ab3-306">L'uso di questa sezione ha lo scopo di consentire agli autori di contenuti di comunicare lo scopo del contenuto a AutoPlay e di abbreviare il tempo di analisi limitando l'analisi a determinate aree significative del supporto.</span><span class="sxs-lookup"><span data-stu-id="37ab3-306">Use of this section is intended to allow content authors both to communicate the intent of content to Autoplay and to shorten its scan time by limiting the scan to certain significant areas of the media.</span></span>

<span data-ttu-id="37ab3-307">Di seguito sono riportati tutti i percorsi validi</span><span class="sxs-lookup"><span data-stu-id="37ab3-307">The following are all valid paths</span></span>


```
[ExclusiveContentPaths]
\music
\music\more music
music2
```



<span data-ttu-id="37ab3-308">La sezione **\[ ExclusiveContentPaths \]** è supportata solo in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="37ab3-308">The **\[ExclusiveContentPaths\]** section is only supported under Windows Vista and later.</span></span>

## <a name="ignorecontentpaths-keys"></a><span data-ttu-id="37ab3-309">\[Chiavi di IgnoreContentPaths \]</span><span class="sxs-lookup"><span data-stu-id="37ab3-309">\[IgnoreContentPaths\] Keys</span></span>

<span data-ttu-id="37ab3-310">Le cartelle elencate in questa sezione e le relative sottocartelle vengono ignorate da AutoPlay durante la ricerca di contenuto in un supporto.</span><span class="sxs-lookup"><span data-stu-id="37ab3-310">Folders listed in this section, and their subfolders, are ignored by Autoplay when searching a media for content.</span></span> <span data-ttu-id="37ab3-311">Possono essere specificati con o senza una barra rovesciata principale ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="37ab3-311">They can be given with or without a leading backslash (\\).</span></span> <span data-ttu-id="37ab3-312">In entrambi i casi vengono considerati percorsi assoluti dalla directory radice del supporto.</span><span class="sxs-lookup"><span data-stu-id="37ab3-312">In either case they are taken as absolute paths from the root directory of the media.</span></span> <span data-ttu-id="37ab3-313">Nel caso di cartelle con spazi nei nomi, non racchiuderle tra virgolette poiché le virgolette vengono eseguite letteralmente come parte del percorso.</span><span class="sxs-lookup"><span data-stu-id="37ab3-313">In the case of folders with spaces in their names, do not enclose them in quotes as the quotes are taken literally as part of the path.</span></span>

<span data-ttu-id="37ab3-314">I percorsi in questa sezione hanno la precedenza sui percorsi nella sezione **\[ ExclusiveContentPaths \]** .</span><span class="sxs-lookup"><span data-stu-id="37ab3-314">Paths in this section take precedence over paths in the **\[ExclusiveContentPaths\]** section.</span></span> <span data-ttu-id="37ab3-315">Se un percorso specificato in **\[ IgnoreContentPaths \]** è una sottocartella di un percorso specificato in **\[ ExclusiveContentPaths \]**, viene comunque ignorato.</span><span class="sxs-lookup"><span data-stu-id="37ab3-315">If a path given in **\[IgnoreContentPaths\]** is a subfolder of a path given in **\[ExclusiveContentPaths\]**, it is still ignored.</span></span>

<span data-ttu-id="37ab3-316">L'uso di questa sezione ha lo scopo di consentire agli autori di contenuti di comunicare lo scopo del contenuto a AutoPlay e di abbreviare il tempo di analisi limitando l'analisi a determinate aree significative del supporto.</span><span class="sxs-lookup"><span data-stu-id="37ab3-316">Use of this section is intended to allow content authors both to communicate the intent of content to Autoplay and to shorten its scan time by limiting the scan to certain significant areas of the media.</span></span>

<span data-ttu-id="37ab3-317">Di seguito sono riportati tutti i percorsi validi</span><span class="sxs-lookup"><span data-stu-id="37ab3-317">The following are all valid paths</span></span>


```
[IgnoreContentPaths]
\music
\music\more music
music2
```



<span data-ttu-id="37ab3-318">La sezione **\[ IgnoreContentPaths \]** è supportata solo in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="37ab3-318">The **\[IgnoreContentPaths\]** section is only supported under Windows Vista and later.</span></span>

## <a name="deviceinstall-keys"></a><span data-ttu-id="37ab3-319">\[Chiavi di DeviceInstall \]</span><span class="sxs-lookup"><span data-stu-id="37ab3-319">\[DeviceInstall\] Keys</span></span>

### <a name="driverpath"></a><span data-ttu-id="37ab3-320">DriverPath</span><span class="sxs-lookup"><span data-stu-id="37ab3-320">DriverPath</span></span>

<span data-ttu-id="37ab3-321">La voce **DriverPath** specifica una directory in cui eseguire la ricerca in modo ricorsivo per i file del driver.</span><span class="sxs-lookup"><span data-stu-id="37ab3-321">The **DriverPath** entry specifies a directory to search recursively for driver files.</span></span> <span data-ttu-id="37ab3-322">Questo comando viene usato durante l'installazione di un driver e non fa parte di un'operazione di esecuzione automatica.</span><span class="sxs-lookup"><span data-stu-id="37ab3-322">This command is used during a driver installation and is not part of an AutoRun operation.</span></span> <span data-ttu-id="37ab3-323">La sezione **\[ DeviceInstall \]** è supportata solo in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="37ab3-323">The **\[DeviceInstall\]** section is only supported under Windows XP.</span></span>


```
[DeviceInstall]
DriverPath=directorypath
```



### <a name="parameters"></a><span data-ttu-id="37ab3-324">Parametri</span><span class="sxs-lookup"><span data-stu-id="37ab3-324">Parameters</span></span>

-   <span data-ttu-id="37ab3-325">*DirectoryPath*</span><span class="sxs-lookup"><span data-stu-id="37ab3-325">*directorypath*</span></span>

    <span data-ttu-id="37ab3-326">Percorso di una directory in cui Windows cerca i file del driver, insieme a tutte le relative sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="37ab3-326">A path to a directory that Windows searches for driver files, along with all of its subdirectories.</span></span>

### <a name="remarks"></a><span data-ttu-id="37ab3-327">Commenti</span><span class="sxs-lookup"><span data-stu-id="37ab3-327">Remarks</span></span>

<span data-ttu-id="37ab3-328">Non usare lettere di unità in *DirectoryPath* quando cambiano da un computer a quello successivo.</span><span class="sxs-lookup"><span data-stu-id="37ab3-328">Do not use drive letters in *directorypath* as they change from one computer to the next.</span></span>

<span data-ttu-id="37ab3-329">Per eseguire la ricerca in più directory, aggiungere una voce **DriverPath** per ogni directory come in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="37ab3-329">To search multiple directories, add a **DriverPath** entry for each directory as in this example.</span></span>


```
[DeviceInstall]
DriverPath=drivers\video 
DriverPath=drivers\audio
```



<span data-ttu-id="37ab3-330">Se nella sezione **\[ DeviceInstall \]** non è specificata alcuna voce **DriverPath** o la voce **DriverPath** non ha alcun valore, l'unità viene ignorata durante la ricerca dei file del driver.</span><span class="sxs-lookup"><span data-stu-id="37ab3-330">If no **DriverPath** entry is provided in the **\[DeviceInstall\]** section or the **DriverPath** entry has no value, then that drive is skipped during a search for driver files.</span></span>

 

 
