---
description: Rappresenta gli oggetti nella shell. Vengono forniti metodi per controllare la shell ed eseguire comandi all'interno della shell. Sono disponibili anche metodi per ottenere altri oggetti correlati alla shell.
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
ms.openlocfilehash: 55f8062b71e553ec5ceefa413b45f439874744b8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841762"
---
# <a name="shell-object"></a><span data-ttu-id="4b017-105">Oggetto shell</span><span class="sxs-lookup"><span data-stu-id="4b017-105">Shell object</span></span>

<span data-ttu-id="4b017-106">Rappresenta gli oggetti nella shell.</span><span class="sxs-lookup"><span data-stu-id="4b017-106">Represents the objects in the Shell.</span></span> <span data-ttu-id="4b017-107">Vengono forniti metodi per controllare la shell ed eseguire comandi all'interno della shell.</span><span class="sxs-lookup"><span data-stu-id="4b017-107">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="4b017-108">Sono disponibili anche metodi per ottenere altri oggetti correlati alla shell.</span><span class="sxs-lookup"><span data-stu-id="4b017-108">There are also methods to obtain other Shell-related objects.</span></span>

## <a name="members"></a><span data-ttu-id="4b017-109">Membri</span><span class="sxs-lookup"><span data-stu-id="4b017-109">Members</span></span>

<span data-ttu-id="4b017-110">**L'oggetto Shell** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4b017-110">The **Shell** object has these types of members:</span></span>

-   [<span data-ttu-id="4b017-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="4b017-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="4b017-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4b017-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4b017-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="4b017-113">Methods</span></span>

<span data-ttu-id="4b017-114">**L'oggetto Shell** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4b017-114">The **Shell** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="4b017-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="4b017-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="4b017-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b017-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4b017-117"><a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-117"><a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-118">Aggiunge un file all'elenco degli elementi usati più di recente.</span><span class="sxs-lookup"><span data-stu-id="4b017-118">Adds a file to the most recently used (MRU) list.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4b017-119"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-119"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-120">Crea una finestra di dialogo che consente all'utente di selezionare una cartella e quindi restituisce l'oggetto <a href="folder.md"><strong>Folder della</strong></a> cartella selezionata.</span><span class="sxs-lookup"><span data-stu-id="4b017-120">Creates a dialog box that enables the user to select a folder and then returns the selected folder's <a href="folder.md"><strong>Folder</strong></a> object.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4b017-121"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-121"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-122">Determina se l'utente corrente può avviare e arrestare il servizio denominato.</span><span class="sxs-lookup"><span data-stu-id="4b017-122">Determines if the current user can start and stop the named service.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4b017-123"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-123"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-124">Sovrapporre tutte le finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="4b017-124">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="4b017-125">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliere <strong>Sovrapponi finestre.</strong></span><span class="sxs-lookup"><span data-stu-id="4b017-125">This method has the same effect as right-clicking the taskbar and selecting <strong>Cascade Windows</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4b017-126"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-126"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-127">Esegue l'Pannello di controllo specificata (\*.cpl).</span><span class="sxs-lookup"><span data-stu-id="4b017-127">Runs the specified Control Panel (\*.cpl) application.</span></span> <span data-ttu-id="4b017-128">Se l'applicazione è già aperta, attiverà l'istanza in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4b017-128">If the application is already open, it will activate the running instance.</span></span> <br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="4b017-129">A causa di Windows Vista, la maggior Pannello di controllo applicazioni sono elementi della shell e non possono essere aperte con questa funzione.</span><span class="sxs-lookup"><span data-stu-id="4b017-129">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="4b017-130">Per aprire queste Pannello di controllo applicazioni, passare il nome canonico a control.exe.</span><span class="sxs-lookup"><span data-stu-id="4b017-130">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="4b017-131">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="4b017-131">For example:</span></span></p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4b017-132"><a href="shell-ejectpc.md"><strong>EjectPC</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-132"><a href="shell-ejectpc.md"><strong>EjectPC</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-133">Espulse il computer dall'alloggiamento di espansione.</span><span class="sxs-lookup"><span data-stu-id="4b017-133">Ejects the computer from its docking station.</span></span> <span data-ttu-id="4b017-134">Questo è lo stesso che si fa clic sul menu <strong>Start</strong> e si <strong>seleziona Espulsa PC</strong>, se il computer supporta questo comando.</span><span class="sxs-lookup"><span data-stu-id="4b017-134">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Eject PC</strong>, if your computer supports this command.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4b017-135"><a href="shell-explore.md"><strong>Esplorare</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-135"><a href="shell-explore.md"><strong>Explore</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-136">Apre una cartella specificata in una finestra Esplora risorse dati.</span><span class="sxs-lookup"><span data-stu-id="4b017-136">Opens a specified folder in a Windows Explorer window.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4b017-137"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-137"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-138">Ottiene il valore per un criterio di Internet Explorer specificati.</span><span class="sxs-lookup"><span data-stu-id="4b017-138">Gets the value for a specified Internet Explorer policy.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4b017-139"><a href="shell-filerun.md"><strong>FileRun</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-139"><a href="shell-filerun.md"><strong>FileRun</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-140">Visualizza la <strong>finestra di</strong> dialogo Esegui per l'utente.</span><span class="sxs-lookup"><span data-stu-id="4b017-140">Displays the <strong>Run</strong> dialog to the user.</span></span> <span data-ttu-id="4b017-141">Questo metodo ha lo stesso effetto di fare clic sul menu <strong>Start</strong> e selezionare <strong>Esegui</strong>.</span><span class="sxs-lookup"><span data-stu-id="4b017-141">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Run</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4b017-142"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-142"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-143">Visualizza la <strong>finestra di dialogo Risultati ricerca:</strong> Computer.</span><span class="sxs-lookup"><span data-stu-id="4b017-143">Displays the <strong>Search Results: Computers</strong> dialog box.</span></span> <span data-ttu-id="4b017-144">La finestra di dialogo mostra il risultato della ricerca di un computer specificato.</span><span class="sxs-lookup"><span data-stu-id="4b017-144">The dialog box shows the result of the search for a specified computer.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4b017-145"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-145"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-146">Visualizza la <strong>finestra di dialogo Trova:</strong> Tutti i file.</span><span class="sxs-lookup"><span data-stu-id="4b017-146">Displays the <strong>Find: All Files</strong> dialog box.</span></span> <span data-ttu-id="4b017-147">Equivale a fare clic sul menu <strong>Start</strong> e quindi selezionare <strong>Cerca</strong> (o il relativo equivalente in sistemi precedenti a Windows XP).</span><span class="sxs-lookup"><span data-stu-id="4b017-147">This is the same as clicking the <strong>Start</strong> menu and then selecting <strong>Search</strong> (or its equivalent under systems earlier than Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4b017-148"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-148"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-149">Consente di visualizzare <strong>la finestra di dialogo</strong> Trova stampante .</span><span class="sxs-lookup"><span data-stu-id="4b017-149">Displays the <strong>Find Printer</strong> dialog box.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4b017-150"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-150"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-151">Recupera un'impostazione globale della shell.</span><span class="sxs-lookup"><span data-stu-id="4b017-151">Retrieves a global Shell setting.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4b017-152"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-152"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-153">Recupera le informazioni di sistema.</span><span class="sxs-lookup"><span data-stu-id="4b017-153">Retrieves system information.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4b017-154"><a href="shell-help.md"><strong>Guida</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-154"><a href="shell-help.md"><strong>Help</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-155">Visualizza la finestra di Guida e supporto tecnico.</span><span class="sxs-lookup"><span data-stu-id="4b017-155">Displays the Windows Help and Support Center.</span></span> <span data-ttu-id="4b017-156">Questo metodo ha lo stesso effetto di fare clic sul menu <strong>Start</strong> e scegliere <strong>Guida e supporto tecnico.</strong></span><span class="sxs-lookup"><span data-stu-id="4b017-156">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Help and Support</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4b017-157"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-157"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-158">Recupera l'impostazione di restrizione di un gruppo dal Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4b017-158">Retrieves a group's restriction setting from the registry.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4b017-159"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>Esecuzione di IsServiceRunning</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-159"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-160">Restituisce un valore che indica se un determinato servizio è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4b017-160">Returns a value that indicates whether a particular service is running.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4b017-161"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-161"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-162">Riduce a icona tutte le finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="4b017-162">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="4b017-163">Questo metodo ha lo stesso effetto di <strong></strong> fare clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliere Riduci a icona tutte le finestre nei sistemi meno recenti oppure fare clic sull'icona Mostra <strong>desktop</strong> nell'area Avvio veloce della barra delle applicazioni in Windows 2000 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4b017-163">This method has the same effect as right-clicking the taskbar and selecting <strong>Minimize All Windows</strong> on older systems or clicking the <strong>Show Desktop</strong> icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4b017-164"><a href="shell-namespace.md"><strong>Namespace</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-164"><a href="shell-namespace.md"><strong>NameSpace</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-165">Crea e restituisce un <a href="folder.md"><strong>oggetto Folder</strong></a> per la cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="4b017-165">Creates and returns a <a href="folder.md"><strong>Folder</strong></a> object for the specified folder.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4b017-166"><a href="shell-open.md"><strong>Apri</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-166"><a href="shell-open.md"><strong>Open</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-167">Apre la cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="4b017-167">Opens the specified folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4b017-168"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-168"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-169">Aggiorna il contenuto del menu <strong>Start.</strong></span><span class="sxs-lookup"><span data-stu-id="4b017-169">Refreshes the contents of the <strong>Start</strong> menu.</span></span> <span data-ttu-id="4b017-170">Utilizzato solo con sistemi che precedono Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4b017-170">Used only with systems preceding Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4b017-171"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-171"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-172">Visualizza il riquadro Ricerca app.</span><span class="sxs-lookup"><span data-stu-id="4b017-172">Displays the Apps Search pane.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4b017-173"><a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-173"><a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-174">Avvia un servizio denominato.</span><span class="sxs-lookup"><span data-stu-id="4b017-174">Starts a named service.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4b017-175"><a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-175"><a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-176">Arresta un servizio denominato.</span><span class="sxs-lookup"><span data-stu-id="4b017-176">Stops a named service.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4b017-177"><a href="shell-settime.md"><strong>Settime</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-177"><a href="shell-settime.md"><strong>SetTime</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-178">Consente di visualizzare <strong>la finestra di dialogo Proprietà data</strong> e ora .</span><span class="sxs-lookup"><span data-stu-id="4b017-178">Displays the <strong>Date and Time Properties</strong> dialog box.</span></span> <span data-ttu-id="4b017-179">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sull'orologio nell'area di stato della barra delle applicazioni e scegliere <strong>Regola data/ora</strong>.</span><span class="sxs-lookup"><span data-stu-id="4b017-179">This method has the same effect as right-clicking the clock in the taskbar status area and selecting <strong>Adjust Date/Time</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4b017-180"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-180"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-181">Esegue un'operazione specificata su un file specificato.</span><span class="sxs-lookup"><span data-stu-id="4b017-181">Performs a specified operation on a specified file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4b017-182"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-182"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-183">Visualizza una barra del browser.</span><span class="sxs-lookup"><span data-stu-id="4b017-183">Displays a browser bar.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4b017-184"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-184"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-185">Visualizza la <strong>finestra di dialogo Arresta</strong> Windows.</span><span class="sxs-lookup"><span data-stu-id="4b017-185">Displays the <strong>Shut Down Windows</strong> dialog box.</span></span> <span data-ttu-id="4b017-186">Questa operazione è identica a quando si fa clic sul menu <strong>Start</strong> e si <strong>sceglie Arresta</strong>.</span><span class="sxs-lookup"><span data-stu-id="4b017-186">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Shut Down</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4b017-187"><a href="shell-suspend.md"><strong>Sospendi</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-187"><a href="shell-suspend.md"><strong>Suspend</strong></a></span></span></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4b017-188"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-188"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-189">Affianca tutte le finestre del desktop orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="4b017-189">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="4b017-190">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliere <strong>Affianca finestre orizzontalmente.</strong></span><span class="sxs-lookup"><span data-stu-id="4b017-190">This method has the same effect as right-clicking the taskbar and selecting <strong>Tile Windows Horizontally</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4b017-191"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-191"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-192">Affianca verticalmente tutte le finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="4b017-192">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="4b017-193">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e <strong>scegliere Affianca finestre verticalmente.</strong></span><span class="sxs-lookup"><span data-stu-id="4b017-193">This method has the same effect as right-clicking the taskbar and selecting <strong>Tile Windows Vertically</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4b017-194"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-194"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-195">Visualizza o nasconde il desktop.</span><span class="sxs-lookup"><span data-stu-id="4b017-195">Displays or hides the desktop.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4b017-196"><a href="shell-trayproperties.md"><strong>Proprietà della barra delle applicazioni</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-196"><a href="shell-trayproperties.md"><strong>TrayProperties</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-197">Visualizza la finestra <strong>di dialogo Proprietà barra delle</strong> applicazioni e menu Start .</span><span class="sxs-lookup"><span data-stu-id="4b017-197">Displays the <strong>Taskbar and Start Menu Properties</strong> dialog box.</span></span> <span data-ttu-id="4b017-198">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e <strong>scegliere Proprietà.</strong></span><span class="sxs-lookup"><span data-stu-id="4b017-198">This method has the same effect as right-clicking the taskbar and selecting <strong>Properties</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4b017-199"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-199"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-200">Ripristina tutte le finestre desktop allo stesso stato in cui si trovavano prima dell'ultimo <a href="shell-minimizeall.md"><strong>comando MinimizeAll.</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-200">Restores all desktop windows to the same state they were in before the last <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> command.</span></span> <span data-ttu-id="4b017-201">Questo metodo ha lo stesso effetto di <strong></strong> fare clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliere Annulla Riduci a icona tutte le finestre nei sistemi precedenti o un secondo clic sull'icona Mostra <strong>desktop</strong> nell'area Avvio veloce della barra delle applicazioni in Windows 2000 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4b017-201">This method has the same effect as right-clicking the taskbar and selecting <strong>Undo Minimize All Windows</strong> on older systems or a second clicking of the <strong>Show Desktop</strong> icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4b017-202"><a href="shell-windows.md"><strong>Windows</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-202"><a href="shell-windows.md"><strong>Windows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-203">Crea e restituisce un <a href="shellwindows.md"><strong>oggetto ShellWindows.</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-203">Creates and returns a <a href="shellwindows.md"><strong>ShellWindows</strong></a> object.</span></span> <span data-ttu-id="4b017-204">Questo oggetto rappresenta una raccolta di tutte le finestre aperte che appartengono alla shell.</span><span class="sxs-lookup"><span data-stu-id="4b017-204">This object represents a collection of all of the open windows that belong to the Shell.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4b017-205"><a href="shell-windowssecurity.md"><strong>WindowsSicurezza</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-205"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-206">Consente di visualizzare <strong>Sicurezza di Windows</strong> finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="4b017-206">Displays the <strong>Windows Security</strong> dialog box.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4b017-207"><a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b017-207"><a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4b017-208">Visualizza le finestre aperte in uno stack 3D che è possibile scorrere.</span><span class="sxs-lookup"><span data-stu-id="4b017-208">Displays your open windows in a 3D stack that you can flip through.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="4b017-209">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4b017-209">Properties</span></span>

<span data-ttu-id="4b017-210">**L'oggetto Shell** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4b017-210">The **Shell** object has these properties.</span></span>



| <span data-ttu-id="4b017-211">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4b017-211">Property</span></span>                                            | <span data-ttu-id="4b017-212">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="4b017-212">Access type</span></span>          | <span data-ttu-id="4b017-213">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b017-213">Description</span></span>                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="4b017-214">**Applicazione**</span><span class="sxs-lookup"><span data-stu-id="4b017-214">**Application**</span></span>](shell-application.md)<br/> | <span data-ttu-id="4b017-215">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b017-215">Read-only</span></span><br/> | <span data-ttu-id="4b017-216">Contiene l'oggetto Application dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4b017-216">Contains the object's Application object.</span></span><br/>                        |
| [<span data-ttu-id="4b017-217">**Padre**</span><span class="sxs-lookup"><span data-stu-id="4b017-217">**Parent**</span></span>](shell-parent.md)<br/>           | <span data-ttu-id="4b017-218">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b017-218">Read-only</span></span><br/> | <span data-ttu-id="4b017-219">Ottiene un oggetto che rappresenta l'elemento padre dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="4b017-219">Gets an object that represents the parent of the current object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4b017-220">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b017-220">Requirements</span></span>



| <span data-ttu-id="4b017-221">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b017-221">Requirement</span></span> | <span data-ttu-id="4b017-222">Valore</span><span class="sxs-lookup"><span data-stu-id="4b017-222">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b017-223">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b017-223">Minimum supported client</span></span><br/> | <span data-ttu-id="4b017-224">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="4b017-224">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4b017-225">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b017-225">Minimum supported server</span></span><br/> | <span data-ttu-id="4b017-226">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4b017-226">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4b017-227">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4b017-227">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b017-228"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="4b017-228"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="4b017-229">Idl</span><span class="sxs-lookup"><span data-stu-id="4b017-229">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4b017-230"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="4b017-230"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="4b017-231">DLL</span><span class="sxs-lookup"><span data-stu-id="4b017-231">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b017-232"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="4b017-232"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
