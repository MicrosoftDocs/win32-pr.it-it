---
description: Vengono illustrati i metodi di apertura di un Pannello di controllo per Windows Vista e sistemi successivi e vengono illustrati i comandi Pannello di controllo legacy.
ms.assetid: c17167ab-e9a0-4290-955c-484d038b82af
title: Esecuzione di Pannello di controllo elementi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cb6ae2fa08231d3876e1a5a636e404f519f4a6
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581759"
---
# <a name="executing-control-panel-items"></a><span data-ttu-id="4ccf5-103">Esecuzione di Pannello di controllo elementi</span><span class="sxs-lookup"><span data-stu-id="4ccf5-103">Executing Control Panel Items</span></span>

> [!Note]  
> <span data-ttu-id="4ccf5-104">Se si sta cercando l'elenco dei nomi canonici e dei moduli per Pannello di controllo elementi, vedere [Nomi canonici Pannello di controllo elementi](controlpanel-canonical-names.md).</span><span class="sxs-lookup"><span data-stu-id="4ccf5-104">If you are looking for the list of canonical and module names for Control Panel items, see [Canonical Names of Control Panel Items](controlpanel-canonical-names.md).</span></span>

 

<span data-ttu-id="4ccf5-105">È possibile aprire un elemento Pannello di controllo due modi:</span><span class="sxs-lookup"><span data-stu-id="4ccf5-105">There are two ways to open a Control Panel item:</span></span>

-   <span data-ttu-id="4ccf5-106">L'utente può aprire Pannello di controllo e quindi aprire un elemento facendo clic o facendo doppio clic sull'icona dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-106">The user can open Control Panel and then open an item by clicking or double-clicking the item's icon.</span></span>
-   <span data-ttu-id="4ccf5-107">L'utente o un'applicazione può avviare Pannello di controllo elemento eseguendolo direttamente dal prompt della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-107">The user or an application can start a Control Panel item by executing it directly from the command line prompt.</span></span>

<span data-ttu-id="4ccf5-108">Un'applicazione può aprire il Pannello di controllo a livello di codice usando la [**funzione WinExec.**](/windows/win32/api/winbase/nf-winbase-winexec)</span><span class="sxs-lookup"><span data-stu-id="4ccf5-108">An application can open the Control Panel programmatically by using the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function.</span></span>


```
WinExec("c:\windows\system32\control.exe", SW_NORMAL);
```



<span data-ttu-id="4ccf5-109">L'esempio seguente illustra come un'applicazione può avviare Pannello di controllo elemento denominato **MyCpl.cpl** usando la [**funzione WinExec.**](/windows/win32/api/winbase/nf-winbase-winexec)</span><span class="sxs-lookup"><span data-stu-id="4ccf5-109">The following example shows how an application can start the Control Panel item named **MyCpl.cpl** by using the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function.</span></span>


```
WinExec("c:\windows\system32\control.exe MyCpl.cpl", SW_NORMAL);
```



<span data-ttu-id="4ccf5-110">Quando un Pannello di controllo elemento viene aperto tramite una riga di comando, è possibile indicarvi di aprirlo in una scheda specifica dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-110">When a Control Panel item is opened through a command line, you can instruct it to open to a particular tab in the item.</span></span> <span data-ttu-id="4ccf5-111">A causa dell'aggiunta e della rimozione di determinate schede in alcuni elementi Windows Vista Pannello di controllo, la numerazione delle schede potrebbe essere stata modificata rispetto a quella in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-111">Due to the addition and removal of certain tabs in some Windows Vista Control Panel items, the numbering of the tabs might have changed from that in Windows XP.</span></span> <span data-ttu-id="4ccf5-112">Ad esempio, nell'esempio seguente viene avviata la quarta scheda nell'elemento System Windows XP e la terza scheda in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-112">For instance, the following example launches the fourth tab in the System item on Windows XP and the third tab on Windows Vista.</span></span>


```
control.exe sysdm.cpl,,3
```



<span data-ttu-id="4ccf5-113">In questo argomento vengono trattati i seguenti temi:</span><span class="sxs-lookup"><span data-stu-id="4ccf5-113">This topic discusses the following:</span></span>

-   [<span data-ttu-id="4ccf5-114">Windows Nomi canonici di Vista</span><span class="sxs-lookup"><span data-stu-id="4ccf5-114">Windows Vista Canonical Names</span></span>](#windows-vista-canonical-names)
-   [<span data-ttu-id="4ccf5-115">Nuovi comandi per Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ccf5-115">New Commands for Windows Vista</span></span>](#new-commands-for-windows-vista)
-   [<span data-ttu-id="4ccf5-116">Comandi Pannello di controllo legacy</span><span class="sxs-lookup"><span data-stu-id="4ccf5-116">Legacy Control Panel Commands</span></span>](#legacy-control-panel-commands)
-   [<span data-ttu-id="4ccf5-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4ccf5-117">Related topics</span></span>](#related-topics)

## <a name="windows-vista-canonical-names"></a><span data-ttu-id="4ccf5-118">Windows Nomi canonici di Vista</span><span class="sxs-lookup"><span data-stu-id="4ccf5-118">Windows Vista Canonical Names</span></span>

<span data-ttu-id="4ccf5-119">In Windows Vista e versioni successive, il metodo preferito per avviare un elemento Pannello di controllo da una riga di comando è usare il Pannello di controllo canonico dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-119">In Windows Vista and later, the preferred method of launching a Control Panel item from a command line is to use the Control Panel item's canonical name.</span></span> <span data-ttu-id="4ccf5-120">Un nome canonico è una stringa non localizzata dichiarata Pannello di controllo elemento nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-120">A canonical name is a non-localized string that the Control Panel item declares in the registry.</span></span> <span data-ttu-id="4ccf5-121">Il valore dell'uso di un nome canonico è che astrae il nome del modulo Pannello di controllo elemento.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-121">The value of using a canonical name is that it abstracts the module name of the Control Panel item.</span></span> <span data-ttu-id="4ccf5-122">Un elemento può essere implementato in un .dll e successivamente reimplementato come .exe o modificarne il nome del modulo.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-122">An item can be implemented in a .dll and later be reimplemented as a .exe or change its module name.</span></span> <span data-ttu-id="4ccf5-123">Finché il nome canonico rimane invariato, non è necessario aggiornare qualsiasi programma che lo apre usando tale nome canonico.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-123">As long as the canonical name remains the same, then any program that opens it by using that canonical name does not need to be updated.</span></span>

<span data-ttu-id="4ccf5-124">Per convenzione, il nome canonico è formato come "CorporationName.ControlPanelItemName".</span><span class="sxs-lookup"><span data-stu-id="4ccf5-124">By convention, the canonical name is formed as "CorporationName.ControlPanelItemName".</span></span>

<span data-ttu-id="4ccf5-125">L'esempio seguente illustra come un'applicazione può avviare Pannello di controllo'Windows **Update** con [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec).</span><span class="sxs-lookup"><span data-stu-id="4ccf5-125">The following example shows how an application can start the Control Panel item **Windows Update** with [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec).</span></span>


```
WinExec("%systemroot%\system32\control.exe /name Microsoft.WindowsUpdate", SW_NORMAL);
```



<span data-ttu-id="4ccf5-126">Per avviare un Pannello di controllo con il nome canonico, usare: "%systemroot% \\ system32 \\control.exe /name *canonicalName*"</span><span class="sxs-lookup"><span data-stu-id="4ccf5-126">To start a Control Panel item with its canonical name, use: "%systemroot%\\system32\\control.exe /name *canonicalName*"</span></span>

<span data-ttu-id="4ccf5-127">Per aprire una pagina secondaria specifica in un elemento o per aprirla con parametri aggiuntivi, usare: "%systemroot% \\ system32 \\control.exe /name **canonicalName** **/page pageName**"</span><span class="sxs-lookup"><span data-stu-id="4ccf5-127">To open a specific sub-page in an item, or to open it with additional parameters, use: "%systemroot%\\system32\\control.exe /name **canonicalName** /page **pageName**"</span></span>

<span data-ttu-id="4ccf5-128">Un'applicazione può anche implementare il metodo [**IOpenControlPanel::Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) per avviare Pannello di controllo elementi, inclusa la possibilità di aprire una pagina secondaria specifica.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-128">An application can also implement the [**IOpenControlPanel::Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) method to launch Control Panel items, including the ability to open a specific sub-page.</span></span>

<span data-ttu-id="4ccf5-129">Per un elenco completo dei Pannello di controllo canonici degli elementi, vedere [Nomi canonici Pannello di controllo elementi](controlpanel-canonical-names.md).</span><span class="sxs-lookup"><span data-stu-id="4ccf5-129">For a complete list of Control Panel item canonical names, see [Canonical Names of Control Panel Items](controlpanel-canonical-names.md).</span></span>

## <a name="new-commands-for-windows-vista"></a><span data-ttu-id="4ccf5-130">Nuovi comandi per Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ccf5-130">New Commands for Windows Vista</span></span>

<span data-ttu-id="4ccf5-131">In Windows Vista alcune opzioni accessibili da un modulo .cpl in Windows XP vengono ora implementate come .exe file.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-131">On Windows Vista, some options that were accessed by a .cpl module on Windows XP are now implemented as .exe files.</span></span> <span data-ttu-id="4ccf5-132">Ciò garantisce maggiore sicurezza consentendo agli utenti standard di fornire le credenziali di amministratore quando tentano di avviare i file.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-132">This provides added security by allowing standard users to be prompted to provide administrator credentials when trying to launch the files.</span></span> <span data-ttu-id="4ccf5-133">Le stesse righe di comando usate in Windows XP sono accessibili alle opzioni che non richiedono una maggiore sicurezza.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-133">Options that do not require extra security are accessed by the same command lines that were used in Windows XP.</span></span> <span data-ttu-id="4ccf5-134">Di seguito è riportato un elenco di comandi usati in Windows Vista per accedere a schede specifiche Pannello di controllo elementi:</span><span class="sxs-lookup"><span data-stu-id="4ccf5-134">The following is a list of commands used in Windows Vista to access specific tabs of Control Panel items:</span></span>

### <a name="personalization"></a><span data-ttu-id="4ccf5-135">Personalization</span><span class="sxs-lookup"><span data-stu-id="4ccf5-135">Personalization</span></span>

-   <span data-ttu-id="4ccf5-136">Dimensioni del carattere e DPI: %windir% \\ system32 \\DpiScaling.exe</span><span class="sxs-lookup"><span data-stu-id="4ccf5-136">Font size and DPI: %windir%\\system32\\DpiScaling.exe</span></span>
-   <span data-ttu-id="4ccf5-137">Risoluzione dello schermo: %windir% \\ system32 \\control.exe desk.cpl,Impostazioni,@Settings</span><span class="sxs-lookup"><span data-stu-id="4ccf5-137">Screen resolution: %windir%\\system32\\control.exe desk.cpl,Settings,@Settings</span></span>
-   <span data-ttu-id="4ccf5-138">Impostazioni di visualizzazione: %windir% \\ system32 \\control.exe desk.cpl,Impostazioni,@Settings</span><span class="sxs-lookup"><span data-stu-id="4ccf5-138">Display settings: %windir%\\system32\\control.exe desk.cpl,Settings,@Settings</span></span>
-   <span data-ttu-id="4ccf5-139">Temi: %windir% \\ system32 \\control.exe desk.cpl,Temi,@Themes</span><span class="sxs-lookup"><span data-stu-id="4ccf5-139">Themes: %windir%\\system32\\control.exe desk.cpl,Themes,@Themes</span></span>
-   <span data-ttu-id="4ccf5-140">Screensaver: %windir% \\ system32 \\control.exe desk.cpl,screensaver,@screensaver</span><span class="sxs-lookup"><span data-stu-id="4ccf5-140">Screensaver: %windir%\\system32\\control.exe desk.cpl,screensaver,@screensaver</span></span>
-   <span data-ttu-id="4ccf5-141">Multi-monitor: %windir% \\ system32 \\control.exe desk.cpl,Monitor,@Monitor</span><span class="sxs-lookup"><span data-stu-id="4ccf5-141">Multi-monitor: %windir%\\system32\\control.exe desk.cpl,Monitor,@Monitor</span></span>
-   <span data-ttu-id="4ccf5-142">Combinazione colori: %windir% \\ system32 \\control.exe /name Microsoft.Personalization /pageColorization</span><span class="sxs-lookup"><span data-stu-id="4ccf5-142">Color Scheme: %windir%\\system32\\control.exe /name Microsoft.Personalization /page pageColorization</span></span>
-   <span data-ttu-id="4ccf5-143">Sfondo del desktop: %windir% \\ system32 \\control.exe /name Microsoft.Personalization /pageWallpaper</span><span class="sxs-lookup"><span data-stu-id="4ccf5-143">Desktop background: %windir%\\system32\\control.exe /name Microsoft.Personalization /page pageWallpaper</span></span>

> [!Note]  
> <span data-ttu-id="4ccf5-144">Le edizioni Starter e Basic non supportano control.exe comando /name Microsoft.Personalization.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-144">Starter and Basic Editions do not support control.exe /name Microsoft.Personalization command.</span></span>

 

### <a name="system"></a><span data-ttu-id="4ccf5-145">Sistema</span><span class="sxs-lookup"><span data-stu-id="4ccf5-145">System</span></span>

-   <span data-ttu-id="4ccf5-146">Prestazioni: %windir% \\ system32 \\SystemPropertiesPerformance.exe</span><span class="sxs-lookup"><span data-stu-id="4ccf5-146">Performance: %windir%\\system32\\SystemPropertiesPerformance.exe</span></span>
-   <span data-ttu-id="4ccf5-147">Accesso remoto: %windir% \\ system32 \\SystemPropertiesRemote.exe</span><span class="sxs-lookup"><span data-stu-id="4ccf5-147">Remote access: %windir%\\system32\\SystemPropertiesRemote.exe</span></span>
-   <span data-ttu-id="4ccf5-148">Nome computer: %windir% \\ system32 \\SystemPropertiesComputerName.exe</span><span class="sxs-lookup"><span data-stu-id="4ccf5-148">Computer name: %windir%\\system32\\SystemPropertiesComputerName.exe</span></span>
-   <span data-ttu-id="4ccf5-149">Protezione del sistema: %windir% \\ system32 \\SystemPropertiesProtection.exe</span><span class="sxs-lookup"><span data-stu-id="4ccf5-149">System protection: %windir%\\system32\\SystemPropertiesProtection.exe</span></span>
-   <span data-ttu-id="4ccf5-150">Proprietà di sistema avanzate: %windir% \\ system32 \\SystemPropertiesAdvanced.exe</span><span class="sxs-lookup"><span data-stu-id="4ccf5-150">Advanced system properties: %windir%\\system32\\SystemPropertiesAdvanced.exe</span></span>

### <a name="programs-and-features"></a><span data-ttu-id="4ccf5-151">Programmi e funzionalità</span><span class="sxs-lookup"><span data-stu-id="4ccf5-151">Programs and Features</span></span>

-   <span data-ttu-id="4ccf5-152">Aggiungere o rimuovere programmi: %windir% \\ system32 \\control.exe /name Microsoft.ProgramsAndFeatures</span><span class="sxs-lookup"><span data-stu-id="4ccf5-152">Add or remove programs: %windir%\\system32\\control.exe /name Microsoft.ProgramsAndFeatures</span></span>
-   <span data-ttu-id="4ccf5-153">Windows funzionalità: %windir% \\ system32 \\OptionalFeatures.exe</span><span class="sxs-lookup"><span data-stu-id="4ccf5-153">Windows features: %windir%\\system32\\OptionalFeatures.exe</span></span>

### <a name="regional-and-language-options"></a><span data-ttu-id="4ccf5-154">Opzioni internazionali e della lingua</span><span class="sxs-lookup"><span data-stu-id="4ccf5-154">Regional and Language Options</span></span>

-   <span data-ttu-id="4ccf5-155">Tastiera: %systemroot% \\ system32 \\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"keyboard"</span><span class="sxs-lookup"><span data-stu-id="4ccf5-155">Keyboard: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"keyboard"</span></span>
-   <span data-ttu-id="4ccf5-156">Percorso: %systemroot% \\ system32 \\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"location"</span><span class="sxs-lookup"><span data-stu-id="4ccf5-156">Location: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"location"</span></span>
-   <span data-ttu-id="4ccf5-157">Amministrativo: %systemroot% \\ system32 \\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"administrative"</span><span class="sxs-lookup"><span data-stu-id="4ccf5-157">Administrative: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"administrative"</span></span>

### <a name="folder-options"></a><span data-ttu-id="4ccf5-158">Opzioni cartella</span><span class="sxs-lookup"><span data-stu-id="4ccf5-158">Folder Options</span></span>

-   <span data-ttu-id="4ccf5-159">Ricerca di cartelle: %windir% \\ system32 \\rundll32.exe shell32.dll,Opzioni \_ RunDLL 2</span><span class="sxs-lookup"><span data-stu-id="4ccf5-159">Folder searching: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 2</span></span>
-   <span data-ttu-id="4ccf5-160">Associazioni di file: %windir% \\ system32 \\control.exe /name Microsoft.DefaultPrograms /pageFileAssoc</span><span class="sxs-lookup"><span data-stu-id="4ccf5-160">File associations: %windir%\\system32\\control.exe /name Microsoft.DefaultPrograms /page pageFileAssoc</span></span>
-   <span data-ttu-id="4ccf5-161">Visualizzazione: %windir% \\ system32 \\rundll32.exe shell32.dll,Opzioni \_ RunDLL 7</span><span class="sxs-lookup"><span data-stu-id="4ccf5-161">View: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 7</span></span>
-   <span data-ttu-id="4ccf5-162">Generale: %windir% \\ system32 \\rundll32.exe shell32.dll,Opzioni \_ RunDLL 0</span><span class="sxs-lookup"><span data-stu-id="4ccf5-162">General: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 0</span></span>

### <a name="power-options"></a><span data-ttu-id="4ccf5-163">Opzioni risparmio energia</span><span class="sxs-lookup"><span data-stu-id="4ccf5-163">Power Options</span></span>

-   <span data-ttu-id="4ccf5-164">Modificare le impostazioni correnti del piano: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /page pagePlanSettings</span><span class="sxs-lookup"><span data-stu-id="4ccf5-164">Edit current plan settings: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pagePlanSettings</span></span>
-   <span data-ttu-id="4ccf5-165">Impostazioni di sistema: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /pageGlobalSettings</span><span class="sxs-lookup"><span data-stu-id="4ccf5-165">System settings: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pageGlobalSettings</span></span>
-   <span data-ttu-id="4ccf5-166">Creare una combinazione per il risparmio di energia: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /pageCreateNewPlan</span><span class="sxs-lookup"><span data-stu-id="4ccf5-166">Create a power plan: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pageCreateNewPlan</span></span>
-   <span data-ttu-id="4ccf5-167">Non è disponibile alcun comando canonico per la pagina Impostazioni avanzate, a cui si accede nel modo precedente: %windir% \\ system32 \\control.exe powercfg.cpl,3</span><span class="sxs-lookup"><span data-stu-id="4ccf5-167">There is no canonical command for the Advanced Settings page, it is accessed in the older manner: %windir%\\system32\\control.exe powercfg.cpl,,3</span></span>

## <a name="legacy-control-panel-commands"></a><span data-ttu-id="4ccf5-168">Comandi Pannello di controllo legacy</span><span class="sxs-lookup"><span data-stu-id="4ccf5-168">Legacy Control Panel Commands</span></span>

<span data-ttu-id="4ccf5-169">Quando si usa la [**funzione WinExec,**](/windows/win32/api/winbase/nf-winbase-winexec) il sistema può riconoscere comandi Pannello di controllo speciali.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-169">When you use the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function, the system can recognize special Control Panel commands.</span></span> <span data-ttu-id="4ccf5-170">Questi comandi precedono Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-170">These commands predate Windows Vista.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4ccf5-171">control.exe desktop</span><span class="sxs-lookup"><span data-stu-id="4ccf5-171">control.exe desktop</span></span></td>
<td><span data-ttu-id="4ccf5-172">Avvia la finestra <strong>Proprietà dello schermo.</strong></span><span class="sxs-lookup"><span data-stu-id="4ccf5-172">Launches the <strong>Display Properties</strong> window.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="4ccf5-173">Le edizioni Starter e Basic non supportano questo comando.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-173">Starter and Basic Editions do not support this command.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ccf5-174">control.exe colore</span><span class="sxs-lookup"><span data-stu-id="4ccf5-174">control.exe color</span></span></td>
<td><span data-ttu-id="4ccf5-175">Avvia la finestra <strong>Proprietà dello schermo</strong> con la <strong>scheda Aspetto</strong> preselezionata.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-175">Launches the <strong>Display Properties</strong> window with the <strong>Appearance</strong> tab preselected.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ccf5-176">control.exe data/ora</span><span class="sxs-lookup"><span data-stu-id="4ccf5-176">control.exe date/time</span></span></td>
<td><span data-ttu-id="4ccf5-177">Avvia la finestra <strong>Proprietà data e</strong> ora.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-177">Launches the <strong>Date and Time Properties</strong> window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ccf5-178">control.exe internazionale</span><span class="sxs-lookup"><span data-stu-id="4ccf5-178">control.exe international</span></span></td>
<td><span data-ttu-id="4ccf5-179">Avvia la finestra <strong>Opzioni internazionali e della</strong> lingua.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-179">Launches the <strong>Regional and Language Options</strong> window.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ccf5-180">control.exe mouse</span><span class="sxs-lookup"><span data-stu-id="4ccf5-180">control.exe mouse</span></span></td>
<td><span data-ttu-id="4ccf5-181">Avvia la finestra <strong>Proprietà mouse.</strong></span><span class="sxs-lookup"><span data-stu-id="4ccf5-181">Launches the <strong>Mouse Properties</strong> window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ccf5-182">control.exe tastiera</span><span class="sxs-lookup"><span data-stu-id="4ccf5-182">control.exe keyboard</span></span></td>
<td><span data-ttu-id="4ccf5-183">Avvia la finestra <strong>Proprietà tastiera.</strong></span><span class="sxs-lookup"><span data-stu-id="4ccf5-183">Launches the <strong>Keyboard Properties</strong> window.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ccf5-184">control.exe stampanti</span><span class="sxs-lookup"><span data-stu-id="4ccf5-184">control.exe printers</span></span></td>
<td><span data-ttu-id="4ccf5-185">Visualizza la <strong>cartella Stampanti e</strong> fax.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-185">Displays the <strong>Printers and Faxes</strong> folder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ccf5-186">control.exe tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="4ccf5-186">control.exe fonts</span></span></td>
<td><span data-ttu-id="4ccf5-187">Visualizza la <strong>cartella Tipi di</strong> carattere.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-187">Displays the <strong>Fonts</strong> folder.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4ccf5-188">Per Windows 2000 e versioni successive:</span><span class="sxs-lookup"><span data-stu-id="4ccf5-188">For Windows 2000 and later systems:</span></span>



| <span data-ttu-id="4ccf5-189">Comando</span><span class="sxs-lookup"><span data-stu-id="4ccf5-189">Command</span></span>                    | <span data-ttu-id="4ccf5-190">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ccf5-190">Description</span></span>                                              |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="4ccf5-191">control.exe cartelle</span><span class="sxs-lookup"><span data-stu-id="4ccf5-191">control.exe folders</span></span>        | <span data-ttu-id="4ccf5-192">Avvia la **finestra Opzioni** cartella.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-192">Launches the **Folder Options** window.</span></span>                  |
| <span data-ttu-id="4ccf5-193">control.exe netware</span><span class="sxs-lookup"><span data-stu-id="4ccf5-193">control.exe netware</span></span>        | <span data-ttu-id="4ccf5-194">Avvia la finestra **di Novell NetWare** (se installata).</span><span class="sxs-lookup"><span data-stu-id="4ccf5-194">Launches the **Novell NetWare** window (if installed).</span></span>   |
| <span data-ttu-id="4ccf5-195">control.exe telefonia</span><span class="sxs-lookup"><span data-stu-id="4ccf5-195">control.exe telephony</span></span>      | <span data-ttu-id="4ccf5-196">Avvia la finestra **Telefono opzioni modem e** modem.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-196">Launches the **Phone and Modem Options** window.</span></span>         |
| <span data-ttu-id="4ccf5-197">control.exe admintools</span><span class="sxs-lookup"><span data-stu-id="4ccf5-197">control.exe admintools</span></span>     | <span data-ttu-id="4ccf5-198">Visualizza la **cartella Strumenti di** amministrazione.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-198">Displays the **Administrative Tools** folder.</span></span>            |
| <span data-ttu-id="4ccf5-199">control.exe schedtasks</span><span class="sxs-lookup"><span data-stu-id="4ccf5-199">control.exe schedtasks</span></span>     | <span data-ttu-id="4ccf5-200">Visualizza la **cartella Attività** pianificate.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-200">Displays the **Scheduled Tasks** folder.</span></span>                 |
| <span data-ttu-id="4ccf5-201">control.exe netconnections</span><span class="sxs-lookup"><span data-stu-id="4ccf5-201">control.exe netconnections</span></span> | <span data-ttu-id="4ccf5-202">Visualizza la **cartella Connessioni di** rete.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-202">Displays the **Network Connections** folder.</span></span>             |
| <span data-ttu-id="4ccf5-203">control.exe acontrol.exe</span><span class="sxs-lookup"><span data-stu-id="4ccf5-203">control.exe infrared</span></span>       | <span data-ttu-id="4ccf5-204">Avvia la finestra **Monitoraggio a volta a** volta (se installata).</span><span class="sxs-lookup"><span data-stu-id="4ccf5-204">Launches the **Infrared Monitor** window (if installed).</span></span> |
| <span data-ttu-id="4ccf5-205">control.exe userpasswords</span><span class="sxs-lookup"><span data-stu-id="4ccf5-205">control.exe userpasswords</span></span>  | <span data-ttu-id="4ccf5-206">Avvia la **finestra Account** utente.</span><span class="sxs-lookup"><span data-stu-id="4ccf5-206">Launches the **User Accounts** window.</span></span>                   |



 

## <a name="related-topics"></a><span data-ttu-id="4ccf5-207">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4ccf5-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ccf5-208">Pannello di controllo elementi</span><span class="sxs-lookup"><span data-stu-id="4ccf5-208">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="4ccf5-209">Linee guida sull'esperienza utente</span><span class="sxs-lookup"><span data-stu-id="4ccf5-209">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="4ccf5-210">Registrazione di Pannello di controllo elementi</span><span class="sxs-lookup"><span data-stu-id="4ccf5-210">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="4ccf5-211">Uso di CPLApplet</span><span class="sxs-lookup"><span data-stu-id="4ccf5-211">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="4ccf5-212">Pannello di controllo di messaggi</span><span class="sxs-lookup"><span data-stu-id="4ccf5-212">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="4ccf5-213">Estensione di elementi di Pannello di controllo sistema</span><span class="sxs-lookup"><span data-stu-id="4ccf5-213">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="4ccf5-214">Assegnazione di Pannello di controllo categorie</span><span class="sxs-lookup"><span data-stu-id="4ccf5-214">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="4ccf5-215">Creazione di collegamenti di attività ricercabili per un Pannello di controllo ricerca</span><span class="sxs-lookup"><span data-stu-id="4ccf5-215">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="4ccf5-216">Accesso al Pannello di controllo in modalità Cassaforte in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ccf5-216">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
