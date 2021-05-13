---
description: Rappresenta un oggetto nella shell.
title: Oggetto IShellDispatch (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9B429C03-7F80-45db-B8CD-58D19FAD2E61
ms.openlocfilehash: 02fbead4b2d40a91ec6dab70f536d1ea3241ee84
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840892"
---
# <a name="ishelldispatch-object"></a><span data-ttu-id="3285e-103">Oggetto IShellDispatch</span><span class="sxs-lookup"><span data-stu-id="3285e-103">IShellDispatch object</span></span>

<span data-ttu-id="3285e-104">Rappresenta un oggetto nella shell.</span><span class="sxs-lookup"><span data-stu-id="3285e-104">Represents an object in the Shell.</span></span> <span data-ttu-id="3285e-105">Vengono forniti metodi per controllare la shell ed eseguire comandi all'interno della shell.</span><span class="sxs-lookup"><span data-stu-id="3285e-105">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="3285e-106">Sono disponibili anche metodi per ottenere altri oggetti correlati alla shell.</span><span class="sxs-lookup"><span data-stu-id="3285e-106">There are also methods to obtain other Shell-related objects.</span></span>

> [!Note]  
> <span data-ttu-id="3285e-107">**IShellDispatch viene** implementato e accessibile tramite [**l'oggetto Shell.**](shell.md)</span><span class="sxs-lookup"><span data-stu-id="3285e-107">**IShellDispatch** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="3285e-108">Membri</span><span class="sxs-lookup"><span data-stu-id="3285e-108">Members</span></span>

<span data-ttu-id="3285e-109">**L'oggetto IShellDispatch** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3285e-109">The **IShellDispatch** object has these types of members:</span></span>

-   [<span data-ttu-id="3285e-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="3285e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="3285e-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3285e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3285e-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="3285e-112">Methods</span></span>

<span data-ttu-id="3285e-113">**L'oggetto IShellDispatch** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="3285e-113">The **IShellDispatch** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="3285e-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="3285e-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="3285e-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3285e-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3285e-116"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="3285e-116"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3285e-117">Crea una finestra di dialogo che consente all'utente di selezionare una cartella e quindi restituisce l'oggetto <a href="folder.md"><strong>Folder della</strong></a> cartella selezionata.</span><span class="sxs-lookup"><span data-stu-id="3285e-117">Creates a dialog box that enables the user to select a folder and then returns the selected folder's <a href="folder.md"><strong>Folder</strong></a> object.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3285e-118"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="3285e-118"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3285e-119">Sovrapporre tutte le finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="3285e-119">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="3285e-120">Questo metodo ha lo stesso effetto del clic con il pulsante destro del mouse sulla barra delle applicazioni e della <strong>selezione di Sovrapponi finestre.</strong></span><span class="sxs-lookup"><span data-stu-id="3285e-120">This method has the same effect as right-clicking the taskbar and selecting <strong>Cascade windows</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3285e-121"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="3285e-121"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3285e-122">Esegue l'applicazione Pannello di controllo specificata.</span><span class="sxs-lookup"><span data-stu-id="3285e-122">Runs the specified Control Panel application.</span></span> <span data-ttu-id="3285e-123">Se l'applicazione è già aperta, attiverà l'istanza in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3285e-123">If the application is already open, it will activate the running instance.</span></span> <br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="3285e-124">A data di Windows Vista, la maggior Pannello di controllo applicazioni sono elementi della shell e non possono essere aperte con questa funzione.</span><span class="sxs-lookup"><span data-stu-id="3285e-124">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="3285e-125">Per aprire tali Pannello di controllo applicazioni, passare il nome canonico a control.exe.</span><span class="sxs-lookup"><span data-stu-id="3285e-125">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="3285e-126">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="3285e-126">For example:</span></span></p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3285e-127"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></span><span class="sxs-lookup"><span data-stu-id="3285e-127"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3285e-128">Espulse il computer dall'alloggiamento di espansione.</span><span class="sxs-lookup"><span data-stu-id="3285e-128">Ejects the computer from its docking station.</span></span> <span data-ttu-id="3285e-129">Questo è lo stesso che si fa clic sul menu <strong>Start</strong> e si <strong>seleziona Espulsa PC</strong>, se il computer supporta questo comando.</span><span class="sxs-lookup"><span data-stu-id="3285e-129">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Eject PC</strong>, if your computer supports this command.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3285e-130"><a href="ishelldispatch-explore.md"><strong>Esplorare</strong></a></span><span class="sxs-lookup"><span data-stu-id="3285e-130"><a href="ishelldispatch-explore.md"><strong>Explore</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3285e-131">Apre una cartella specificata in una finestra Esplora risorse dati.</span><span class="sxs-lookup"><span data-stu-id="3285e-131">Opens a specified folder in a Windows Explorer window.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3285e-132"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></span><span class="sxs-lookup"><span data-stu-id="3285e-132"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3285e-133">Visualizza la <strong>finestra di</strong> dialogo Esegui per l'utente.</span><span class="sxs-lookup"><span data-stu-id="3285e-133">Displays the <strong>Run</strong> dialog to the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3285e-134"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></span><span class="sxs-lookup"><span data-stu-id="3285e-134"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3285e-135">Visualizza la <strong>finestra di dialogo Risultati ricerca:</strong> Computer.</span><span class="sxs-lookup"><span data-stu-id="3285e-135">Displays the <strong>Search Results: Computers</strong> dialog box.</span></span> <span data-ttu-id="3285e-136">La finestra di dialogo mostra il risultato della ricerca di un computer specificato.</span><span class="sxs-lookup"><span data-stu-id="3285e-136">The dialog box shows the result of the search for a specified computer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3285e-137"><a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a></span><span class="sxs-lookup"><span data-stu-id="3285e-137"><a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3285e-138">Visualizza la <strong>finestra di dialogo Trova:</strong> Tutti i file.</span><span class="sxs-lookup"><span data-stu-id="3285e-138">Displays the <strong>Find: All Files</strong> dialog box.</span></span> <span data-ttu-id="3285e-139">Questo è lo stesso che si fa clic sul menu <strong>Start</strong> e quindi si seleziona <strong>Cerca</strong>.</span><span class="sxs-lookup"><span data-stu-id="3285e-139">This is the same as clicking the <strong>Start</strong> menu and then selecting <strong>Search</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3285e-140"><a href="ishelldispatch-help.md"><strong>Guida</strong></a></span><span class="sxs-lookup"><span data-stu-id="3285e-140"><a href="ishelldispatch-help.md"><strong>Help</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3285e-141">Visualizza la finestra Guida e supporto tecnico di Windows.</span><span class="sxs-lookup"><span data-stu-id="3285e-141">Displays the Windows Help and Support window.</span></span> <span data-ttu-id="3285e-142">Questo metodo ha lo stesso effetto di fare clic sul menu <strong>Start</strong> e selezionare <strong>Guida e supporto tecnico</strong>.</span><span class="sxs-lookup"><span data-stu-id="3285e-142">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Help and Support</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3285e-143"><a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a></span><span class="sxs-lookup"><span data-stu-id="3285e-143"><a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3285e-144">Riduce a icona tutte le finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="3285e-144">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="3285e-145">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliere Riduci a icona Tutte le <strong>finestre</strong> nei sistemi meno recenti o facendo clic sull'icona <strong>Mostra desktop</strong> sulla barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="3285e-145">This method has the same effect as right-clicking the taskbar and selecting <strong>Minimize All Windows</strong> on older systems or clicking the <strong>Show Desktop</strong> icon on the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3285e-146"><a href="ishelldispatch-namespace.md"><strong>Namespace</strong></a></span><span class="sxs-lookup"><span data-stu-id="3285e-146"><a href="ishelldispatch-namespace.md"><strong>NameSpace</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3285e-147">Crea e restituisce un <a href="folder.md"><strong>oggetto Folder</strong></a> per la cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="3285e-147">Creates and returns a <a href="folder.md"><strong>Folder</strong></a> object for the specified folder.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3285e-148"><a href="ishelldispatch-open.md"><strong>Apri</strong></a></span><span class="sxs-lookup"><span data-stu-id="3285e-148"><a href="ishelldispatch-open.md"><strong>Open</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3285e-149">Apre la cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="3285e-149">Opens the specified folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3285e-150"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></span><span class="sxs-lookup"><span data-stu-id="3285e-150"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3285e-151">Aggiorna il contenuto del menu <strong>Start.</strong></span><span class="sxs-lookup"><span data-stu-id="3285e-151">Refreshes the contents of the <strong>Start</strong> menu.</span></span> <span data-ttu-id="3285e-152">Utilizzato solo con sistemi che precedono Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3285e-152">Used only with systems preceding Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3285e-153"><a href="ishelldispatch-settime.md"><strong>Settime</strong></a></span><span class="sxs-lookup"><span data-stu-id="3285e-153"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3285e-154">Consente di visualizzare <strong>la finestra di dialogo Data e</strong> ora .</span><span class="sxs-lookup"><span data-stu-id="3285e-154">Displays the <strong>Date and Time</strong> dialog box.</span></span> <span data-ttu-id="3285e-155">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sull'orologio nell'area di stato della barra delle applicazioni e <strong>scegliere Regola data/ora.</strong></span><span class="sxs-lookup"><span data-stu-id="3285e-155">This method has the same effect as right-clicking the clock in the taskbar status area and selecting <strong>Adjust date/time</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3285e-156"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="3285e-156"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3285e-157">Consente di visualizzare <strong>la finestra di dialogo Arresta</strong> Windows .</span><span class="sxs-lookup"><span data-stu-id="3285e-157">Displays the <strong>Shut Down Windows</strong> dialog box.</span></span> <span data-ttu-id="3285e-158">Si tratta di un'operazione identica a quando si fa clic sul menu <strong>Start</strong> e si <strong>sceglie Arresta</strong>.</span><span class="sxs-lookup"><span data-stu-id="3285e-158">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Shut Down</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3285e-159"><a href="ishelldispatch-suspend.md"><strong>Sospendi</strong></a></span><span class="sxs-lookup"><span data-stu-id="3285e-159"><a href="ishelldispatch-suspend.md"><strong>Suspend</strong></a></span></span></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3285e-160"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></span><span class="sxs-lookup"><span data-stu-id="3285e-160"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3285e-161">Affianca orizzontalmente tutte le finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="3285e-161">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="3285e-162">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e <strong>scegliere Mostra finestre in pila.</strong></span><span class="sxs-lookup"><span data-stu-id="3285e-162">This method has the same effect as right-clicking the taskbar and selecting <strong>Show windows stacked</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3285e-163"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></span><span class="sxs-lookup"><span data-stu-id="3285e-163"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3285e-164">Affianca verticalmente tutte le finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="3285e-164">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="3285e-165">Questo metodo ha lo stesso effetto del clic con il pulsante destro del mouse sulla barra delle applicazioni e della selezione <strong>di Mostra finestre affiancate.</strong></span><span class="sxs-lookup"><span data-stu-id="3285e-165">This method has the same effect as right-clicking the taskbar and selecting <strong>Show windows side by side</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3285e-166"><a href="ishelldispatch-trayproperties.md"><strong>Proprietà della barra delle applicazioni</strong></a></span><span class="sxs-lookup"><span data-stu-id="3285e-166"><a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3285e-167">Visualizza la finestra <strong>di dialogo Proprietà barra delle</strong> applicazioni e menu Start .</span><span class="sxs-lookup"><span data-stu-id="3285e-167">Displays the <strong>Taskbar and Start Menu Properties</strong> dialog box.</span></span> <span data-ttu-id="3285e-168">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e <strong>scegliere Proprietà.</strong></span><span class="sxs-lookup"><span data-stu-id="3285e-168">This method has the same effect as right-clicking the taskbar and selecting <strong>Properties</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="3285e-169"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span><span class="sxs-lookup"><span data-stu-id="3285e-169"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3285e-170">Ripristina tutte le finestre del desktop nello stato in cui si trovavano prima dell'ultimo <a href="shell-minimizeall.md"><strong>comando MinimizeAll.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3285e-170">Restores all desktop windows to the state they were in before the last <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> command.</span></span> <span data-ttu-id="3285e-171">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliere Annulla Riduci a icona tutte le finestre <strong>(nei</strong> sistemi precedenti) o un secondo clic sull'icona Mostra <strong>desktop</strong> nella barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="3285e-171">This method has the same effect as right-clicking the taskbar and selecting <strong>Undo Minimize All Windows</strong> (on older systems) or a second clicking of the <strong>Show Desktop</strong> icon in the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="3285e-172"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></span><span class="sxs-lookup"><span data-stu-id="3285e-172"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="3285e-173">Crea e restituisce un <a href="shellwindows.md"><strong>oggetto ShellWindows.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3285e-173">Creates and returns a <a href="shellwindows.md"><strong>ShellWindows</strong></a> object.</span></span> <span data-ttu-id="3285e-174">Questo oggetto rappresenta una raccolta di tutte le finestre aperte che appartengono alla shell.</span><span class="sxs-lookup"><span data-stu-id="3285e-174">This object represents a collection of all of the open windows that belong to the Shell.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="3285e-175">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3285e-175">Properties</span></span>

<span data-ttu-id="3285e-176">**L'oggetto IShellDispatch** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3285e-176">The **IShellDispatch** object has these properties.</span></span>



| <span data-ttu-id="3285e-177">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3285e-177">Property</span></span>                                                     | <span data-ttu-id="3285e-178">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="3285e-178">Access type</span></span>          | <span data-ttu-id="3285e-179">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3285e-179">Description</span></span>                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="3285e-180">**Applicazione**</span><span class="sxs-lookup"><span data-stu-id="3285e-180">**Application**</span></span>](ishelldispatch-application.md)<br/> | <span data-ttu-id="3285e-181">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3285e-181">Read-only</span></span><br/> | <span data-ttu-id="3285e-182">Contiene un oggetto che rappresenta un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3285e-182">Contains an object that represents an application.</span></span><br/>                    |
| [<span data-ttu-id="3285e-183">**Padre**</span><span class="sxs-lookup"><span data-stu-id="3285e-183">**Parent**</span></span>](ishelldispatch-parent.md)<br/>           | <span data-ttu-id="3285e-184">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3285e-184">Read-only</span></span><br/> | <span data-ttu-id="3285e-185">Recupera un oggetto che rappresenta l'elemento padre dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="3285e-185">Retrieves an object that represents the parent of the current object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3285e-186">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3285e-186">Requirements</span></span>



| <span data-ttu-id="3285e-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="3285e-187">Requirement</span></span> | <span data-ttu-id="3285e-188">Valore</span><span class="sxs-lookup"><span data-stu-id="3285e-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3285e-189">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3285e-189">Minimum supported client</span></span><br/> | <span data-ttu-id="3285e-190">Solo app desktop di Windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3285e-190">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3285e-191">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3285e-191">Minimum supported server</span></span><br/> | <span data-ttu-id="3285e-192">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3285e-192">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3285e-193">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3285e-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="3285e-194"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="3285e-194"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="3285e-195">Idl</span><span class="sxs-lookup"><span data-stu-id="3285e-195">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3285e-196"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="3285e-196"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="3285e-197">DLL</span><span class="sxs-lookup"><span data-stu-id="3285e-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3285e-198"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="3285e-198"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3285e-199">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3285e-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3285e-200">**Idispatch**</span><span class="sxs-lookup"><span data-stu-id="3285e-200">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="3285e-201">**Oggetto Shell**</span><span class="sxs-lookup"><span data-stu-id="3285e-201">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 
