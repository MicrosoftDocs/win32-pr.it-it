---
description: Rappresenta gli oggetti nella shell. Vengono forniti metodi per controllare la shell e per eseguire comandi all'interno della shell. Sono inoltre disponibili metodi per ottenere altri oggetti correlati alla Shell.
title: 'Oggetto di shell (Shldisp.h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 75fc151e-5b9e-476b-b4e5-b848917357a8
ms.openlocfilehash: 3e891278d98ca2eb51fca11054cba01947e03c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884389"
---
# <a name="shell-object"></a><span data-ttu-id="02e0b-105">Oggetto Shell</span><span class="sxs-lookup"><span data-stu-id="02e0b-105">Shell object</span></span>

<span data-ttu-id="02e0b-106">Rappresenta gli oggetti nella shell.</span><span class="sxs-lookup"><span data-stu-id="02e0b-106">Represents the objects in the Shell.</span></span> <span data-ttu-id="02e0b-107">Vengono forniti metodi per controllare la shell e per eseguire comandi all'interno della shell.</span><span class="sxs-lookup"><span data-stu-id="02e0b-107">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="02e0b-108">Sono inoltre disponibili metodi per ottenere altri oggetti correlati alla Shell.</span><span class="sxs-lookup"><span data-stu-id="02e0b-108">There are also methods to obtain other Shell-related objects.</span></span>

## <a name="members"></a><span data-ttu-id="02e0b-109">Membri</span><span class="sxs-lookup"><span data-stu-id="02e0b-109">Members</span></span>

<span data-ttu-id="02e0b-110">L'oggetto **Shell** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="02e0b-110">The **Shell** object has these types of members:</span></span>

-   [<span data-ttu-id="02e0b-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="02e0b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="02e0b-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="02e0b-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="02e0b-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="02e0b-113">Methods</span></span>

<span data-ttu-id="02e0b-114">Questi metodi sono disponibili nell'oggetto **Shell** .</span><span class="sxs-lookup"><span data-stu-id="02e0b-114">The **Shell** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="02e0b-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="02e0b-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="02e0b-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02e0b-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="02e0b-117"><a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-117"><a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-118">Aggiunge un file all'elenco degli ultimi elementi usati (MRU).</span><span class="sxs-lookup"><span data-stu-id="02e0b-118">Adds a file to the most recently used (MRU) list.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="02e0b-119"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-119"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-120">Crea una finestra di dialogo che consente all'utente di selezionare una cartella e quindi restituisce l'oggetto <a href="folder.md"><strong>cartella</strong></a> della cartella selezionata.</span><span class="sxs-lookup"><span data-stu-id="02e0b-120">Creates a dialog box that enables the user to select a folder and then returns the selected folder's <a href="folder.md"><strong>Folder</strong></a> object.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="02e0b-121"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-121"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-122">Determina se l'utente corrente può avviare e arrestare il servizio denominato.</span><span class="sxs-lookup"><span data-stu-id="02e0b-122">Determines if the current user can start and stop the named service.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="02e0b-123"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-123"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-124">Si sovrappone a tutte le finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="02e0b-124">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="02e0b-125">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e selezionare <strong>Cascade Windows</strong>.</span><span class="sxs-lookup"><span data-stu-id="02e0b-125">This method has the same effect as right-clicking the taskbar and selecting <strong>Cascade Windows</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="02e0b-126"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-126"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-127">Esegue l'applicazione del pannello di controllo (\*. cpl) specificata.</span><span class="sxs-lookup"><span data-stu-id="02e0b-127">Runs the specified Control Panel (\*.cpl) application.</span></span> <span data-ttu-id="02e0b-128">Se l'applicazione è già aperta, attiverà l'istanza in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="02e0b-128">If the application is already open, it will activate the running instance.</span></span> <br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="02e0b-129">A partire da Windows Vista, la maggior parte delle applicazioni del pannello di controllo sono elementi della shell e non possono essere aperti con questa funzione.</span><span class="sxs-lookup"><span data-stu-id="02e0b-129">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="02e0b-130">Per aprire le applicazioni del pannello di controllo, passare il nome canonico a control.exe.</span><span class="sxs-lookup"><span data-stu-id="02e0b-130">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="02e0b-131">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="02e0b-131">For example:</span></span></p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="02e0b-132"><a href="shell-ejectpc.md"><strong>EjectPC</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-132"><a href="shell-ejectpc.md"><strong>EjectPC</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-133">Espelle il computer dalla relativa stazione di ancoraggio.</span><span class="sxs-lookup"><span data-stu-id="02e0b-133">Ejects the computer from its docking station.</span></span> <span data-ttu-id="02e0b-134">Questa operazione equivale a fare clic sul menu <strong>Start</strong> e selezionare <strong>eject PC (Rimuovi PC</strong>) se il computer supporta questo comando.</span><span class="sxs-lookup"><span data-stu-id="02e0b-134">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Eject PC</strong>, if your computer supports this command.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="02e0b-135"><a href="shell-explore.md"><strong>Esplora</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-135"><a href="shell-explore.md"><strong>Explore</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-136">Apre una cartella specificata in una finestra di Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="02e0b-136">Opens a specified folder in a Windows Explorer window.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="02e0b-137"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-137"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-138">Ottiene il valore per i criteri di Internet Explorer specificati.</span><span class="sxs-lookup"><span data-stu-id="02e0b-138">Gets the value for a specified Internet Explorer policy.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="02e0b-139"><a href="shell-filerun.md"><strong>FileRun</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-139"><a href="shell-filerun.md"><strong>FileRun</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-140">Consente di visualizzare la finestra di dialogo <strong>Esegui</strong> all'utente.</span><span class="sxs-lookup"><span data-stu-id="02e0b-140">Displays the <strong>Run</strong> dialog to the user.</span></span> <span data-ttu-id="02e0b-141">Questo metodo ha lo stesso effetto di quando si fa clic sul menu <strong>Start</strong> e si seleziona <strong>Esegui</strong>.</span><span class="sxs-lookup"><span data-stu-id="02e0b-141">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Run</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="02e0b-142"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-142"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-143">Consente di visualizzare la finestra di dialogo <strong>Risultati ricerca: computer</strong> .</span><span class="sxs-lookup"><span data-stu-id="02e0b-143">Displays the <strong>Search Results: Computers</strong> dialog box.</span></span> <span data-ttu-id="02e0b-144">Nella finestra di dialogo viene visualizzato il risultato della ricerca di un computer specifico.</span><span class="sxs-lookup"><span data-stu-id="02e0b-144">The dialog box shows the result of the search for a specified computer.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="02e0b-145"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-145"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-146">Consente di visualizzare la finestra di dialogo <strong>trova: tutti i file</strong> .</span><span class="sxs-lookup"><span data-stu-id="02e0b-146">Displays the <strong>Find: All Files</strong> dialog box.</span></span> <span data-ttu-id="02e0b-147">Questa operazione equivale a fare clic sul menu <strong>Start</strong> e quindi selezionare <strong>Cerca</strong> (o l'equivalente in sistemi precedenti a Windows XP).</span><span class="sxs-lookup"><span data-stu-id="02e0b-147">This is the same as clicking the <strong>Start</strong> menu and then selecting <strong>Search</strong> (or its equivalent under systems earlier than Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="02e0b-148"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-148"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-149">Consente di visualizzare la finestra di dialogo <strong>Trova stampante</strong> .</span><span class="sxs-lookup"><span data-stu-id="02e0b-149">Displays the <strong>Find Printer</strong> dialog box.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="02e0b-150"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-150"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-151">Recupera un'impostazione della shell globale.</span><span class="sxs-lookup"><span data-stu-id="02e0b-151">Retrieves a global Shell setting.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="02e0b-152"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-152"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-153">Recupera le informazioni di sistema.</span><span class="sxs-lookup"><span data-stu-id="02e0b-153">Retrieves system information.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="02e0b-154"><a href="shell-help.md"><strong>Help</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-154"><a href="shell-help.md"><strong>Help</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-155">Visualizza la guida e il supporto tecnico di Windows.</span><span class="sxs-lookup"><span data-stu-id="02e0b-155">Displays the Windows Help and Support Center.</span></span> <span data-ttu-id="02e0b-156">Questo metodo ha lo stesso effetto di quando si fa clic sul menu <strong>Start</strong> e si seleziona <strong>Guida e supporto</strong>.</span><span class="sxs-lookup"><span data-stu-id="02e0b-156">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Help and Support</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="02e0b-157"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-157"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-158">Recupera l'impostazione di restrizione di un gruppo dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="02e0b-158">Retrieves a group's restriction setting from the registry.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="02e0b-159"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-159"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-160">Restituisce un valore che indica se un particolare servizio è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="02e0b-160">Returns a value that indicates whether a particular service is running.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="02e0b-161"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-161"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-162">Riduce al minimo tutte le finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="02e0b-162">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="02e0b-163">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e selezionare <strong>Riduci a icona tutte le finestre</strong> nei sistemi meno recenti oppure fare clic sull'icona <strong>Mostra desktop</strong> nell'area avvio veloce della barra delle applicazioni in Windows 2000 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="02e0b-163">This method has the same effect as right-clicking the taskbar and selecting <strong>Minimize All Windows</strong> on older systems or clicking the <strong>Show Desktop</strong> icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="02e0b-164"><a href="shell-namespace.md"><strong>NameSpace</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-164"><a href="shell-namespace.md"><strong>NameSpace</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-165">Crea e restituisce un oggetto <a href="folder.md"><strong>Folder</strong></a> per la cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="02e0b-165">Creates and returns a <a href="folder.md"><strong>Folder</strong></a> object for the specified folder.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="02e0b-166"><a href="shell-open.md"><strong>Aprire</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-166"><a href="shell-open.md"><strong>Open</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-167">Apre la cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="02e0b-167">Opens the specified folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="02e0b-168"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-168"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-169">Aggiorna il contenuto del menu <strong>Start</strong> .</span><span class="sxs-lookup"><span data-stu-id="02e0b-169">Refreshes the contents of the <strong>Start</strong> menu.</span></span> <span data-ttu-id="02e0b-170">Utilizzato solo con i sistemi precedenti a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="02e0b-170">Used only with systems preceding Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="02e0b-171"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-171"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-172">Consente di visualizzare il riquadro di ricerca delle app.</span><span class="sxs-lookup"><span data-stu-id="02e0b-172">Displays the Apps Search pane.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="02e0b-173"><a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-173"><a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-174">Avvia un servizio denominato.</span><span class="sxs-lookup"><span data-stu-id="02e0b-174">Starts a named service.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="02e0b-175"><a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-175"><a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-176">Arresta un servizio denominato.</span><span class="sxs-lookup"><span data-stu-id="02e0b-176">Stops a named service.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="02e0b-177"><a href="shell-settime.md"><strong>SetTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-177"><a href="shell-settime.md"><strong>SetTime</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-178">Consente di visualizzare la finestra di dialogo <strong>Proprietà data e ora</strong> .</span><span class="sxs-lookup"><span data-stu-id="02e0b-178">Displays the <strong>Date and Time Properties</strong> dialog box.</span></span> <span data-ttu-id="02e0b-179">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sull'orologio nell'area stato della barra delle applicazioni e scegliere <strong>regola Data/ora</strong>.</span><span class="sxs-lookup"><span data-stu-id="02e0b-179">This method has the same effect as right-clicking the clock in the taskbar status area and selecting <strong>Adjust Date/Time</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="02e0b-180"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-180"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-181">Esegue un'operazione specificata su un file specificato.</span><span class="sxs-lookup"><span data-stu-id="02e0b-181">Performs a specified operation on a specified file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="02e0b-182"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-182"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-183">Visualizza una barra del browser.</span><span class="sxs-lookup"><span data-stu-id="02e0b-183">Displays a browser bar.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="02e0b-184"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-184"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-185">Consente di visualizzare la finestra di dialogo <strong>arresta Windows</strong> .</span><span class="sxs-lookup"><span data-stu-id="02e0b-185">Displays the <strong>Shut Down Windows</strong> dialog box.</span></span> <span data-ttu-id="02e0b-186">Equivale a fare clic sul menu <strong>Start</strong> e selezionare <strong>Arresta</strong>.</span><span class="sxs-lookup"><span data-stu-id="02e0b-186">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Shut Down</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="02e0b-187"><a href="shell-suspend.md"><strong>Sospendere</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-187"><a href="shell-suspend.md"><strong>Suspend</strong></a></span></span></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="02e0b-188"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-188"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-189">Riquadri orizzontalmente tutte le finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="02e0b-189">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="02e0b-190">Questo metodo ha lo stesso effetto che si fa clic con il pulsante destro del mouse sulla barra delle applicazioni e si seleziona <strong>finestre affiancate orizzontalmente</strong></span><span class="sxs-lookup"><span data-stu-id="02e0b-190">This method has the same effect as right-clicking the taskbar and selecting <strong>Tile Windows Horizontally</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="02e0b-191"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-191"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-192">Riquadri verticalmente tutte le finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="02e0b-192">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="02e0b-193">Questo metodo ha lo stesso effetto che si fa clic con il pulsante destro del mouse sulla barra delle applicazioni e si seleziona <strong>finestre affiancate verticalmente</strong></span><span class="sxs-lookup"><span data-stu-id="02e0b-193">This method has the same effect as right-clicking the taskbar and selecting <strong>Tile Windows Vertically</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="02e0b-194"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-194"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-195">Consente di visualizzare o nascondere il desktop.</span><span class="sxs-lookup"><span data-stu-id="02e0b-195">Displays or hides the desktop.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="02e0b-196"><a href="shell-trayproperties.md"><strong>TrayProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-196"><a href="shell-trayproperties.md"><strong>TrayProperties</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-197">Consente di visualizzare la <strong>barra delle applicazioni e la finestra di dialogo Proprietà menu Start</strong> .</span><span class="sxs-lookup"><span data-stu-id="02e0b-197">Displays the <strong>Taskbar and Start Menu Properties</strong> dialog box.</span></span> <span data-ttu-id="02e0b-198">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliere <strong>Proprietà</strong>.</span><span class="sxs-lookup"><span data-stu-id="02e0b-198">This method has the same effect as right-clicking the taskbar and selecting <strong>Properties</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="02e0b-199"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-199"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-200">Ripristina tutte le finestre desktop nello stesso stato in cui si trovavano prima dell'ultimo comando <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="02e0b-200">Restores all desktop windows to the same state they were in before the last <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> command.</span></span> <span data-ttu-id="02e0b-201">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e selezionare <strong>Annulla Riduci</strong> a icona tutte le finestre nei sistemi meno recenti o un secondo clic sull'icona <strong>Mostra desktop</strong> nell'area avvio veloce della barra delle applicazioni in Windows 2000 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="02e0b-201">This method has the same effect as right-clicking the taskbar and selecting <strong>Undo Minimize All Windows</strong> on older systems or a second clicking of the <strong>Show Desktop</strong> icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="02e0b-202"><a href="shell-windows.md"><strong>Windows</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-202"><a href="shell-windows.md"><strong>Windows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-203">Crea e restituisce un oggetto <a href="shellwindows.md"><strong>ShellWindows</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="02e0b-203">Creates and returns a <a href="shellwindows.md"><strong>ShellWindows</strong></a> object.</span></span> <span data-ttu-id="02e0b-204">Questo oggetto rappresenta una raccolta di tutte le finestre aperte che appartengono alla Shell.</span><span class="sxs-lookup"><span data-stu-id="02e0b-204">This object represents a collection of all of the open windows that belong to the Shell.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="02e0b-205"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-205"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-206">Consente di visualizzare la finestra di dialogo <strong>sicurezza di Windows</strong> .</span><span class="sxs-lookup"><span data-stu-id="02e0b-206">Displays the <strong>Windows Security</strong> dialog box.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="02e0b-207"><a href="shell-windowswitcher.md"><strong>Aperto WindowSwitcher</strong></a></span><span class="sxs-lookup"><span data-stu-id="02e0b-207"><a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="02e0b-208">Consente di visualizzare le finestre aperte in uno stack 3D che è possibile scorrere.</span><span class="sxs-lookup"><span data-stu-id="02e0b-208">Displays your open windows in a 3D stack that you can flip through.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="02e0b-209">Proprietà</span><span class="sxs-lookup"><span data-stu-id="02e0b-209">Properties</span></span>

<span data-ttu-id="02e0b-210">L'oggetto **Shell** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="02e0b-210">The **Shell** object has these properties.</span></span>



| <span data-ttu-id="02e0b-211">Proprietà</span><span class="sxs-lookup"><span data-stu-id="02e0b-211">Property</span></span>                                            | <span data-ttu-id="02e0b-212">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="02e0b-212">Access type</span></span>          | <span data-ttu-id="02e0b-213">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02e0b-213">Description</span></span>                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="02e0b-214">**Applicazione**</span><span class="sxs-lookup"><span data-stu-id="02e0b-214">**Application**</span></span>](shell-application.md)<br/> | <span data-ttu-id="02e0b-215">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="02e0b-215">Read-only</span></span><br/> | <span data-ttu-id="02e0b-216">Contiene l'oggetto applicazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="02e0b-216">Contains the object's Application object.</span></span><br/>                        |
| [<span data-ttu-id="02e0b-217">**Padre**</span><span class="sxs-lookup"><span data-stu-id="02e0b-217">**Parent**</span></span>](shell-parent.md)<br/>           | <span data-ttu-id="02e0b-218">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="02e0b-218">Read-only</span></span><br/> | <span data-ttu-id="02e0b-219">Ottiene un oggetto che rappresenta l'elemento padre dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="02e0b-219">Gets an object that represents the parent of the current object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="02e0b-220">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02e0b-220">Requirements</span></span>



| <span data-ttu-id="02e0b-221">Requisito</span><span class="sxs-lookup"><span data-stu-id="02e0b-221">Requirement</span></span> | <span data-ttu-id="02e0b-222">Valore</span><span class="sxs-lookup"><span data-stu-id="02e0b-222">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02e0b-223">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02e0b-223">Minimum supported client</span></span><br/> | <span data-ttu-id="02e0b-224">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="02e0b-224">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="02e0b-225">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02e0b-225">Minimum supported server</span></span><br/> | <span data-ttu-id="02e0b-226">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="02e0b-226">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="02e0b-227">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02e0b-227">Header</span></span><br/>                   | <dl> <span data-ttu-id="02e0b-228"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="02e0b-228"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="02e0b-229">IDL</span><span class="sxs-lookup"><span data-stu-id="02e0b-229">IDL</span></span><br/>                      | <dl> <span data-ttu-id="02e0b-230"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="02e0b-230"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="02e0b-231">DLL</span><span class="sxs-lookup"><span data-stu-id="02e0b-231">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02e0b-232"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="02e0b-232"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
