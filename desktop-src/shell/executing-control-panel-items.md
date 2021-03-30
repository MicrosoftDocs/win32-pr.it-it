---
description: Vengono illustrati i metodi di apertura di un elemento del pannello di controllo per i sistemi Windows Vista e versioni successive, nonché per i comandi del pannello di controllo legacy.
ms.assetid: c17167ab-e9a0-4290-955c-484d038b82af
title: Esecuzione degli elementi del pannello di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaaac4b782273e0b4444fb2b5b6d3cab0b3599ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994933"
---
# <a name="executing-control-panel-items"></a><span data-ttu-id="6f06c-103">Esecuzione degli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="6f06c-103">Executing Control Panel Items</span></span>

> [!Note]  
> <span data-ttu-id="6f06c-104">Se si cerca l'elenco di nomi di moduli e Canonical per gli elementi del pannello di controllo, vedere [nomi canonici degli elementi del pannello di controllo](controlpanel-canonical-names.md).</span><span class="sxs-lookup"><span data-stu-id="6f06c-104">If you are looking for the list of canonical and module names for Control Panel items, see [Canonical Names of Control Panel Items](controlpanel-canonical-names.md).</span></span>

 

<span data-ttu-id="6f06c-105">Esistono due modi per aprire un elemento del pannello di controllo:</span><span class="sxs-lookup"><span data-stu-id="6f06c-105">There are two ways to open a Control Panel item:</span></span>

-   <span data-ttu-id="6f06c-106">L'utente può aprire il pannello di controllo e quindi aprire un elemento facendo clic o facendo doppio clic sull'icona dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="6f06c-106">The user can open Control Panel and then open an item by clicking or double-clicking the item's icon.</span></span>
-   <span data-ttu-id="6f06c-107">L'utente o un'applicazione può avviare un elemento del pannello di controllo eseguendolo direttamente dal prompt della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="6f06c-107">The user or an application can start a Control Panel item by executing it directly from the command line prompt.</span></span>

<span data-ttu-id="6f06c-108">Un'applicazione può aprire il pannello di controllo a livello di codice tramite la funzione [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) .</span><span class="sxs-lookup"><span data-stu-id="6f06c-108">An application can open the Control Panel programmatically by using the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function.</span></span>


```
WinExec("c:\windows\system32\control.exe", SW_NORMAL);
```



<span data-ttu-id="6f06c-109">Nell'esempio seguente viene illustrato come un'applicazione può avviare l'elemento del pannello di controllo denominato **MyCpl.cpl** tramite la funzione [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) .</span><span class="sxs-lookup"><span data-stu-id="6f06c-109">The following example shows how an application can start the Control Panel item named **MyCpl.cpl** by using the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function.</span></span>


```
WinExec("c:\windows\system32\control.exe MyCpl.cpl", SW_NORMAL);
```



<span data-ttu-id="6f06c-110">Quando un elemento del pannello di controllo viene aperto tramite una riga di comando, è possibile indicarlo all'apertura di una particolare scheda nell'elemento.</span><span class="sxs-lookup"><span data-stu-id="6f06c-110">When a Control Panel item is opened through a command line, you can instruct it to open to a particular tab in the item.</span></span> <span data-ttu-id="6f06c-111">A causa dell'aggiunta e della rimozione di alcune schede in alcuni elementi del pannello di controllo di Windows Vista, è possibile che la numerazione delle schede sia cambiata rispetto a quella di Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6f06c-111">Due to the addition and removal of certain tabs in some Windows Vista Control Panel items, the numbering of the tabs might have changed from that in Windows XP.</span></span> <span data-ttu-id="6f06c-112">Nell'esempio seguente, ad esempio, viene avviata la quarta scheda dell'elemento di sistema in Windows XP e la terza scheda in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6f06c-112">For instance, the following example launches the fourth tab in the System item on Windows XP and the third tab on Windows Vista.</span></span>


```
control.exe sysdm.cpl,,3
```



<span data-ttu-id="6f06c-113">In questo argomento vengono trattati i seguenti temi:</span><span class="sxs-lookup"><span data-stu-id="6f06c-113">This topic discusses the following:</span></span>

-   [<span data-ttu-id="6f06c-114">Nomi canonici di Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f06c-114">Windows Vista Canonical Names</span></span>](#windows-vista-canonical-names)
-   [<span data-ttu-id="6f06c-115">Nuovi comandi per Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f06c-115">New Commands for Windows Vista</span></span>](#new-commands-for-windows-vista)
-   [<span data-ttu-id="6f06c-116">Comandi del pannello di controllo legacy</span><span class="sxs-lookup"><span data-stu-id="6f06c-116">Legacy Control Panel Commands</span></span>](#legacy-control-panel-commands)
-   [<span data-ttu-id="6f06c-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6f06c-117">Related topics</span></span>](#related-topics)

## <a name="windows-vista-canonical-names"></a><span data-ttu-id="6f06c-118">Nomi canonici di Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f06c-118">Windows Vista Canonical Names</span></span>

<span data-ttu-id="6f06c-119">In Windows Vista e versioni successive, il metodo preferito per l'avvio di un elemento del pannello di controllo da una riga di comando consiste nell'utilizzare il nome canonico dell'elemento del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="6f06c-119">In Windows Vista and later, the preferred method of launching a Control Panel item from a command line is to use the Control Panel item's canonical name.</span></span> <span data-ttu-id="6f06c-120">Un nome canonico è una stringa non localizzata dichiarata dall'elemento del pannello di controllo nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="6f06c-120">A canonical name is a non-localized string that the Control Panel item declares in the registry.</span></span> <span data-ttu-id="6f06c-121">Il valore di usando un nome canonico è che estrae il nome del modulo dell'elemento del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="6f06c-121">The value of using a canonical name is that it abstracts the module name of the Control Panel item.</span></span> <span data-ttu-id="6f06c-122">Un elemento può essere implementato in un file con estensione dll e successivamente reimplementato come file con estensione exe o modificare il nome del modulo.</span><span class="sxs-lookup"><span data-stu-id="6f06c-122">An item can be implemented in a .dll and later be reimplemented as a .exe or change its module name.</span></span> <span data-ttu-id="6f06c-123">Fino a quando il nome canonico rimane lo stesso, non è necessario aggiornare tutti i programmi che lo aprono usando tale nome canonico.</span><span class="sxs-lookup"><span data-stu-id="6f06c-123">As long as the canonical name remains the same, then any program that opens it by using that canonical name does not need to be updated.</span></span>

<span data-ttu-id="6f06c-124">Per convenzione, il nome canonico è formato "Corporationname. ControlPanelItemName".</span><span class="sxs-lookup"><span data-stu-id="6f06c-124">By convention, the canonical name is formed as "CorporationName.ControlPanelItemName".</span></span>

<span data-ttu-id="6f06c-125">Nell'esempio seguente viene illustrato come un'applicazione può avviare l'elemento del pannello di controllo **Windows Update** con [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec).</span><span class="sxs-lookup"><span data-stu-id="6f06c-125">The following example shows how an application can start the Control Panel item **Windows Update** with [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec).</span></span>


```
WinExec("%systemroot%\system32\control.exe /name Microsoft.WindowsUpdate", SW_NORMAL);
```



<span data-ttu-id="6f06c-126">Per avviare un elemento del pannello di controllo con il nome canonico, utilizzare: "% SystemRoot% \\ system32 \\control.exe/Name *CanonicalName*"</span><span class="sxs-lookup"><span data-stu-id="6f06c-126">To start a Control Panel item with its canonical name, use: "%systemroot%\\system32\\control.exe /name *canonicalName*"</span></span>

<span data-ttu-id="6f06c-127">Per aprire una pagina secondaria specifica in un elemento o per aprirla con parametri aggiuntivi, usare: "% SystemRoot% \\ system32 \\control.exe/Name **CanonicalName** /Page **pageName**"</span><span class="sxs-lookup"><span data-stu-id="6f06c-127">To open a specific sub-page in an item, or to open it with additional parameters, use: "%systemroot%\\system32\\control.exe /name **canonicalName** /page **pageName**"</span></span>

<span data-ttu-id="6f06c-128">Un'applicazione può inoltre implementare il metodo [**IOpenControlPanel:: Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) per avviare gli elementi del pannello di controllo, inclusa la possibilità di aprire una pagina secondaria specifica.</span><span class="sxs-lookup"><span data-stu-id="6f06c-128">An application can also implement the [**IOpenControlPanel::Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) method to launch Control Panel items, including the ability to open a specific sub-page.</span></span>

<span data-ttu-id="6f06c-129">Per un elenco completo dei nomi canonici degli elementi del pannello di controllo, vedere [nomi canonici degli elementi del pannello di controllo](controlpanel-canonical-names.md).</span><span class="sxs-lookup"><span data-stu-id="6f06c-129">For a complete list of Control Panel item canonical names, see [Canonical Names of Control Panel Items](controlpanel-canonical-names.md).</span></span>

## <a name="new-commands-for-windows-vista"></a><span data-ttu-id="6f06c-130">Nuovi comandi per Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f06c-130">New Commands for Windows Vista</span></span>

<span data-ttu-id="6f06c-131">In Windows Vista alcune opzioni a cui è stato eseguito l'accesso a un modulo. cpl in Windows XP sono ora implementate come file con estensione exe.</span><span class="sxs-lookup"><span data-stu-id="6f06c-131">On Windows Vista, some options that were accessed by a .cpl module on Windows XP are now implemented as .exe files.</span></span> <span data-ttu-id="6f06c-132">In questo modo viene fornita una maggiore sicurezza consentendo agli utenti standard di fornire le credenziali di amministratore quando si tenta di avviare i file.</span><span class="sxs-lookup"><span data-stu-id="6f06c-132">This provides added security by allowing standard users to be prompted to provide administrator credentials when trying to launch the files.</span></span> <span data-ttu-id="6f06c-133">Le stesse righe di comando utilizzate in Windows XP hanno accesso a opzioni che non richiedono una maggiore sicurezza.</span><span class="sxs-lookup"><span data-stu-id="6f06c-133">Options that do not require extra security are accessed by the same command lines that were used in Windows XP.</span></span> <span data-ttu-id="6f06c-134">Di seguito è riportato un elenco di comandi utilizzati in Windows Vista per accedere a schede specifiche degli elementi del pannello di controllo:</span><span class="sxs-lookup"><span data-stu-id="6f06c-134">The following is a list of commands used in Windows Vista to access specific tabs of Control Panel items:</span></span>

### <a name="personalization"></a><span data-ttu-id="6f06c-135">Personalization</span><span class="sxs-lookup"><span data-stu-id="6f06c-135">Personalization</span></span>

-   <span data-ttu-id="6f06c-136">Dimensioni del carattere e DPI:% windir% \\ system32 \\DpiScaling.exe</span><span class="sxs-lookup"><span data-stu-id="6f06c-136">Font size and DPI: %windir%\\system32\\DpiScaling.exe</span></span>
-   <span data-ttu-id="6f06c-137">Risoluzione dello schermo:% windir% \\ system32 \\control.exe desk.cpl, Settings,@Settings</span><span class="sxs-lookup"><span data-stu-id="6f06c-137">Screen resolution: %windir%\\system32\\control.exe desk.cpl,Settings,@Settings</span></span>
-   <span data-ttu-id="6f06c-138">Impostazioni di visualizzazione:% windir% \\ system32 \\control.exe desk.cpl, Settings,@Settings</span><span class="sxs-lookup"><span data-stu-id="6f06c-138">Display settings: %windir%\\system32\\control.exe desk.cpl,Settings,@Settings</span></span>
-   <span data-ttu-id="6f06c-139">Temi:% windir% \\ system32 \\control.exe desk.cpl, temi,@Themes</span><span class="sxs-lookup"><span data-stu-id="6f06c-139">Themes: %windir%\\system32\\control.exe desk.cpl,Themes,@Themes</span></span>
-   <span data-ttu-id="6f06c-140">Salvaschermo:% windir% \\ system32 \\control.exe desk.cpl, screensaver,@screensaver</span><span class="sxs-lookup"><span data-stu-id="6f06c-140">Screensaver: %windir%\\system32\\control.exe desk.cpl,screensaver,@screensaver</span></span>
-   <span data-ttu-id="6f06c-141">Multimonitor:% windir% \\ system32 \\control.exe desk.cpl, monitoraggio,@Monitor</span><span class="sxs-lookup"><span data-stu-id="6f06c-141">Multi-monitor: %windir%\\system32\\control.exe desk.cpl,Monitor,@Monitor</span></span>
-   <span data-ttu-id="6f06c-142">Combinazione colori:% windir% \\ system32 \\control.exe/name Microsoft. Personalizzazione/Page pageColorization</span><span class="sxs-lookup"><span data-stu-id="6f06c-142">Color Scheme: %windir%\\system32\\control.exe /name Microsoft.Personalization /page pageColorization</span></span>
-   <span data-ttu-id="6f06c-143">Sfondo del desktop:% windir% \\ system32 \\control.exe/name Microsoft. personalizzazione/page pageWallpaper</span><span class="sxs-lookup"><span data-stu-id="6f06c-143">Desktop background: %windir%\\system32\\control.exe /name Microsoft.Personalization /page pageWallpaper</span></span>

> [!Note]  
> <span data-ttu-id="6f06c-144">Le edizioni Starter e Basic non supportano control.exe comando/name Microsoft. personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="6f06c-144">Starter and Basic Editions do not support control.exe /name Microsoft.Personalization command.</span></span>

 

### <a name="system"></a><span data-ttu-id="6f06c-145">Sistema</span><span class="sxs-lookup"><span data-stu-id="6f06c-145">System</span></span>

-   <span data-ttu-id="6f06c-146">Prestazioni:% windir% \\ system32 \\SystemPropertiesPerformance.exe</span><span class="sxs-lookup"><span data-stu-id="6f06c-146">Performance: %windir%\\system32\\SystemPropertiesPerformance.exe</span></span>
-   <span data-ttu-id="6f06c-147">Accesso remoto:% windir% \\ system32 \\SystemPropertiesRemote.exe</span><span class="sxs-lookup"><span data-stu-id="6f06c-147">Remote access: %windir%\\system32\\SystemPropertiesRemote.exe</span></span>
-   <span data-ttu-id="6f06c-148">Nome computer:% windir% \\ system32 \\SystemPropertiesComputerName.exe</span><span class="sxs-lookup"><span data-stu-id="6f06c-148">Computer name: %windir%\\system32\\SystemPropertiesComputerName.exe</span></span>
-   <span data-ttu-id="6f06c-149">Protezione del sistema:% windir% \\ system32 \\SystemPropertiesProtection.exe</span><span class="sxs-lookup"><span data-stu-id="6f06c-149">System protection: %windir%\\system32\\SystemPropertiesProtection.exe</span></span>
-   <span data-ttu-id="6f06c-150">Proprietà di sistema avanzate:% windir% \\ system32 \\SystemPropertiesAdvanced.exe</span><span class="sxs-lookup"><span data-stu-id="6f06c-150">Advanced system properties: %windir%\\system32\\SystemPropertiesAdvanced.exe</span></span>

### <a name="programs-and-features"></a><span data-ttu-id="6f06c-151">Programmi e funzionalità</span><span class="sxs-lookup"><span data-stu-id="6f06c-151">Programs and Features</span></span>

-   <span data-ttu-id="6f06c-152">Aggiungere o rimuovere programmi:% windir% \\ system32 \\control.exe/name Microsoft. ProgramsAndFeatures</span><span class="sxs-lookup"><span data-stu-id="6f06c-152">Add or remove programs: %windir%\\system32\\control.exe /name Microsoft.ProgramsAndFeatures</span></span>
-   <span data-ttu-id="6f06c-153">Funzionalità di Windows:% windir% \\ system32 \\OptionalFeatures.exe</span><span class="sxs-lookup"><span data-stu-id="6f06c-153">Windows features: %windir%\\system32\\OptionalFeatures.exe</span></span>

### <a name="regional-and-language-options"></a><span data-ttu-id="6f06c-154">Opzioni internazionali e della lingua</span><span class="sxs-lookup"><span data-stu-id="6f06c-154">Regional and Language Options</span></span>

-   <span data-ttu-id="6f06c-155">Tastiera:% systemroot% \\ system32 \\control.exe/name Microsoft. RegionalAndLanguageOptions/page/p: "Keyboard"</span><span class="sxs-lookup"><span data-stu-id="6f06c-155">Keyboard: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"keyboard"</span></span>
-   <span data-ttu-id="6f06c-156">Percorso:% systemroot% \\ system32 \\control.exe/name Microsoft. RegionalAndLanguageOptions/page/p: "location"</span><span class="sxs-lookup"><span data-stu-id="6f06c-156">Location: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"location"</span></span>
-   <span data-ttu-id="6f06c-157">Amministrazione:% systemroot% \\ system32 \\control.exe/name Microsoft. RegionalAndLanguageOptions/page/p: "Administrative"</span><span class="sxs-lookup"><span data-stu-id="6f06c-157">Administrative: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"administrative"</span></span>

### <a name="folder-options"></a><span data-ttu-id="6f06c-158">Opzioni cartella</span><span class="sxs-lookup"><span data-stu-id="6f06c-158">Folder Options</span></span>

-   <span data-ttu-id="6f06c-159">Ricerca cartella:% windir% \\ system32 \\rundll32.exe shell32.dll, opzioni \_ rundll 2</span><span class="sxs-lookup"><span data-stu-id="6f06c-159">Folder searching: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 2</span></span>
-   <span data-ttu-id="6f06c-160">Associazioni file:% windir% \\ system32 \\control.exe/name Microsoft. DefaultPrograms/page pageFileAssoc</span><span class="sxs-lookup"><span data-stu-id="6f06c-160">File associations: %windir%\\system32\\control.exe /name Microsoft.DefaultPrograms /page pageFileAssoc</span></span>
-   <span data-ttu-id="6f06c-161">Visualizzazione:% windir% \\ system32 \\rundll32.exe shell32.dll, opzioni \_ rundll 7</span><span class="sxs-lookup"><span data-stu-id="6f06c-161">View: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 7</span></span>
-   <span data-ttu-id="6f06c-162">Generale:% windir% \\ system32 \\rundll32.exe shell32.dll, opzioni \_ rundll 0</span><span class="sxs-lookup"><span data-stu-id="6f06c-162">General: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 0</span></span>

### <a name="power-options"></a><span data-ttu-id="6f06c-163">Opzioni risparmio energia</span><span class="sxs-lookup"><span data-stu-id="6f06c-163">Power Options</span></span>

-   <span data-ttu-id="6f06c-164">Modifica le impostazioni del piano corrente:% windir% \\ system32 \\control.exe/name Microsoft. PowerOptions/page pagePlanSettings</span><span class="sxs-lookup"><span data-stu-id="6f06c-164">Edit current plan settings: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pagePlanSettings</span></span>
-   <span data-ttu-id="6f06c-165">Impostazioni di sistema:% windir% \\ system32 \\control.exe/name Microsoft. PowerOptions/page pageGlobalSettings</span><span class="sxs-lookup"><span data-stu-id="6f06c-165">System settings: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pageGlobalSettings</span></span>
-   <span data-ttu-id="6f06c-166">Creare una combinazione per il risparmio di energia:% windir% \\ system32 \\control.exe/name Microsoft. PowerOptions/page pageCreateNewPlan</span><span class="sxs-lookup"><span data-stu-id="6f06c-166">Create a power plan: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pageCreateNewPlan</span></span>
-   <span data-ttu-id="6f06c-167">Non esiste alcun comando canonico per la pagina Impostazioni avanzate, a cui è possibile accedere nel modo precedente:% windir% \\ system32 \\control.exe powercfg.cpl,, 3</span><span class="sxs-lookup"><span data-stu-id="6f06c-167">There is no canonical command for the Advanced Settings page, it is accessed in the older manner: %windir%\\system32\\control.exe powercfg.cpl,,3</span></span>

## <a name="legacy-control-panel-commands"></a><span data-ttu-id="6f06c-168">Comandi del pannello di controllo legacy</span><span class="sxs-lookup"><span data-stu-id="6f06c-168">Legacy Control Panel Commands</span></span>

<span data-ttu-id="6f06c-169">Quando si usa la funzione [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) , il sistema è in grado di riconoscere comandi speciali del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="6f06c-169">When you use the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function, the system can recognize special Control Panel commands.</span></span> <span data-ttu-id="6f06c-170">Questi comandi predatano Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6f06c-170">These commands predate Windows Vista.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f06c-171">control.exe desktop</span><span class="sxs-lookup"><span data-stu-id="6f06c-171">control.exe desktop</span></span></td>
<td><span data-ttu-id="6f06c-172">Avvia la finestra <strong>proprietà di visualizzazione</strong> .</span><span class="sxs-lookup"><span data-stu-id="6f06c-172">Launches the <strong>Display Properties</strong> window.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="6f06c-173">Le edizioni Starter e Basic non supportano questo comando.</span><span class="sxs-lookup"><span data-stu-id="6f06c-173">Starter and Basic Editions do not support this command.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f06c-174">Colore control.exe</span><span class="sxs-lookup"><span data-stu-id="6f06c-174">control.exe color</span></span></td>
<td><span data-ttu-id="6f06c-175">Apre la finestra <strong>proprietà di visualizzazione</strong> con la scheda <strong>aspetto</strong> preselezionata.</span><span class="sxs-lookup"><span data-stu-id="6f06c-175">Launches the <strong>Display Properties</strong> window with the <strong>Appearance</strong> tab preselected.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f06c-176">Data/ora control.exe</span><span class="sxs-lookup"><span data-stu-id="6f06c-176">control.exe date/time</span></span></td>
<td><span data-ttu-id="6f06c-177">Viene avviata la finestra <strong>Proprietà data e ora</strong> .</span><span class="sxs-lookup"><span data-stu-id="6f06c-177">Launches the <strong>Date and Time Properties</strong> window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f06c-178">control.exe internazionale</span><span class="sxs-lookup"><span data-stu-id="6f06c-178">control.exe international</span></span></td>
<td><span data-ttu-id="6f06c-179">Avvia la finestra <strong>Opzioni internazionali e della lingua</strong> .</span><span class="sxs-lookup"><span data-stu-id="6f06c-179">Launches the <strong>Regional and Language Options</strong> window.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f06c-180">Mouse control.exe</span><span class="sxs-lookup"><span data-stu-id="6f06c-180">control.exe mouse</span></span></td>
<td><span data-ttu-id="6f06c-181">Avvia la finestra <strong>proprietà del mouse</strong> .</span><span class="sxs-lookup"><span data-stu-id="6f06c-181">Launches the <strong>Mouse Properties</strong> window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f06c-182">Tastiera control.exe</span><span class="sxs-lookup"><span data-stu-id="6f06c-182">control.exe keyboard</span></span></td>
<td><span data-ttu-id="6f06c-183">Avvia la finestra <strong>Proprietà tastiera</strong> .</span><span class="sxs-lookup"><span data-stu-id="6f06c-183">Launches the <strong>Keyboard Properties</strong> window.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f06c-184">Stampanti control.exe</span><span class="sxs-lookup"><span data-stu-id="6f06c-184">control.exe printers</span></span></td>
<td><span data-ttu-id="6f06c-185">Consente di visualizzare la cartella <strong>stampanti e fax</strong> .</span><span class="sxs-lookup"><span data-stu-id="6f06c-185">Displays the <strong>Printers and Faxes</strong> folder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f06c-186">Tipi di carattere control.exe</span><span class="sxs-lookup"><span data-stu-id="6f06c-186">control.exe fonts</span></span></td>
<td><span data-ttu-id="6f06c-187">Consente di visualizzare la cartella <strong>Fonts</strong> .</span><span class="sxs-lookup"><span data-stu-id="6f06c-187">Displays the <strong>Fonts</strong> folder.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6f06c-188">Per i sistemi Windows 2000 e versioni successive:</span><span class="sxs-lookup"><span data-stu-id="6f06c-188">For Windows 2000 and later systems:</span></span>



|                            |                                                          |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="6f06c-189">Cartelle di control.exe</span><span class="sxs-lookup"><span data-stu-id="6f06c-189">control.exe folders</span></span>        | <span data-ttu-id="6f06c-190">Avvia la finestra **Opzioni cartella** .</span><span class="sxs-lookup"><span data-stu-id="6f06c-190">Launches the **Folder Options** window.</span></span>                  |
| <span data-ttu-id="6f06c-191">control.exe NetWare</span><span class="sxs-lookup"><span data-stu-id="6f06c-191">control.exe netware</span></span>        | <span data-ttu-id="6f06c-192">Avvia la finestra **Novell NetWare** (se installata).</span><span class="sxs-lookup"><span data-stu-id="6f06c-192">Launches the **Novell NetWare** window (if installed).</span></span>   |
| <span data-ttu-id="6f06c-193">Telefonia control.exe</span><span class="sxs-lookup"><span data-stu-id="6f06c-193">control.exe telephony</span></span>      | <span data-ttu-id="6f06c-194">Avvia la finestra **Opzioni telefono e modem** .</span><span class="sxs-lookup"><span data-stu-id="6f06c-194">Launches the **Phone and Modem Options** window.</span></span>         |
| <span data-ttu-id="6f06c-195">control.exe AdminTools</span><span class="sxs-lookup"><span data-stu-id="6f06c-195">control.exe admintools</span></span>     | <span data-ttu-id="6f06c-196">Consente di visualizzare la cartella **strumenti di amministrazione** .</span><span class="sxs-lookup"><span data-stu-id="6f06c-196">Displays the **Administrative Tools** folder.</span></span>            |
| <span data-ttu-id="6f06c-197">control.exe schedtasks</span><span class="sxs-lookup"><span data-stu-id="6f06c-197">control.exe schedtasks</span></span>     | <span data-ttu-id="6f06c-198">Consente di visualizzare la cartella **attività pianificate** .</span><span class="sxs-lookup"><span data-stu-id="6f06c-198">Displays the **Scheduled Tasks** folder.</span></span>                 |
| <span data-ttu-id="6f06c-199">control.exe netconnections</span><span class="sxs-lookup"><span data-stu-id="6f06c-199">control.exe netconnections</span></span> | <span data-ttu-id="6f06c-200">Consente di visualizzare la cartella **connessioni di rete** .</span><span class="sxs-lookup"><span data-stu-id="6f06c-200">Displays the **Network Connections** folder.</span></span>             |
| <span data-ttu-id="6f06c-201">control.exe infrarossi</span><span class="sxs-lookup"><span data-stu-id="6f06c-201">control.exe infrared</span></span>       | <span data-ttu-id="6f06c-202">Avvia la finestra di **monitoraggio a infrarossi** (se installata).</span><span class="sxs-lookup"><span data-stu-id="6f06c-202">Launches the **Infrared Monitor** window (if installed).</span></span> |
| <span data-ttu-id="6f06c-203">control.exe userpasswords</span><span class="sxs-lookup"><span data-stu-id="6f06c-203">control.exe userpasswords</span></span>  | <span data-ttu-id="6f06c-204">Avvia la finestra **account utente** .</span><span class="sxs-lookup"><span data-stu-id="6f06c-204">Launches the **User Accounts** window.</span></span>                   |



 

## <a name="related-topics"></a><span data-ttu-id="6f06c-205">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6f06c-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f06c-206">Elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="6f06c-206">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="6f06c-207">Linee guida sull'esperienza utente</span><span class="sxs-lookup"><span data-stu-id="6f06c-207">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="6f06c-208">Registrazione degli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="6f06c-208">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="6f06c-209">Uso di CPLApplet</span><span class="sxs-lookup"><span data-stu-id="6f06c-209">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="6f06c-210">Elaborazione del messaggio del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="6f06c-210">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="6f06c-211">Estensione degli elementi del pannello di controllo di sistema</span><span class="sxs-lookup"><span data-stu-id="6f06c-211">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="6f06c-212">Assegnazione delle categorie del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="6f06c-212">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="6f06c-213">Creazione di collegamenti alle attività ricercabili per un elemento del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="6f06c-213">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="6f06c-214">Accesso al pannello di controllo in modalità provvisoria in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f06c-214">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
