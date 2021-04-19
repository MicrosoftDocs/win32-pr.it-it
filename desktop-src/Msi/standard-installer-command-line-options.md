---
<span data-ttu-id="59b98-101">Descrizione: il programma eseguibile che interpreta i pacchetti e installa i prodotti è Msiexec.exe. Nota Msiexec imposta anche un livello di errore in return corrispondente ai codici di errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="59b98-101">description: The executable program that interprets packages and installs products is Msiexec.exe.Note  Msiexec also sets an error level on return that corresponds to System Error Codes.</span></span> <span data-ttu-id="59b98-102">Nella tabella seguente vengono identificate le opzioni della riga di comando standard per il programma.</span><span class="sxs-lookup"><span data-stu-id="59b98-102">The following table identifies the standard command-line options for this program.</span></span> <span data-ttu-id="59b98-103">Le opzioni della riga di comando non fanno distinzione tra maiuscole e minuscole. Windows Installer 2,0: le opzioni della riga di comando identificate in questo argomento sono disponibili a partire da Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="59b98-103">Command-line options are case insensitive.Windows Installer 2.0:  The command-line options that are identified in this topic are available beginning with Windows Installer 3.0.</span></span> <span data-ttu-id="59b98-104">Le opzioni Windows Installer Command-Line sono disponibili con Windows Installer&\# 160; 3.0 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="59b98-104">The Windows Installer Command-Line Options are available with Windows Installer&\#160;3.0 and earlier versions.</span></span>
<span data-ttu-id="59b98-105">ms. AssetID: b1707c88-1cca-45AB-BB23-6002bfd5204e title: programma di installazione standard Command-Line opzioni ms. Topic: articolo ms. Date: 05/31/2018</span><span class="sxs-lookup"><span data-stu-id="59b98-105">ms.assetid: b1707c88-1cca-45ab-bb23-6002bfd5204e title: Standard Installer Command-Line Options ms.topic: article ms.date: 05/31/2018</span></span>
---

# <a name="standard-installer-command-line-options"></a><span data-ttu-id="59b98-106">Opzioni di Command-Line del programma di installazione standard</span><span class="sxs-lookup"><span data-stu-id="59b98-106">Standard Installer Command-Line Options</span></span>

<span data-ttu-id="59b98-107">Il programma eseguibile che interpreta i pacchetti e installa i prodotti è Msiexec.exe.</span><span class="sxs-lookup"><span data-stu-id="59b98-107">The executable program that interprets packages and installs products is Msiexec.exe.</span></span>

> [!Note]  
> <span data-ttu-id="59b98-108">Msiexec imposta anche un livello di errore al ritorno che corrisponde ai [codici di errore di sistema](../debug/system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="59b98-108">Msiexec also sets an error level on return that corresponds to [System Error Codes](../debug/system-error-codes.md).</span></span>

 

<span data-ttu-id="59b98-109">Nella tabella seguente vengono identificate le opzioni della riga di comando standard per il programma.</span><span class="sxs-lookup"><span data-stu-id="59b98-109">The following table identifies the standard command-line options for this program.</span></span> <span data-ttu-id="59b98-110">Le opzioni della riga di comando non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="59b98-110">Command-line options are case insensitive.</span></span>

<span data-ttu-id="59b98-111">**Windows Installer 2,0:** Le opzioni della riga di comando identificate in questo argomento sono disponibili a partire da Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="59b98-111">**Windows Installer 2.0:** The command-line options that are identified in this topic are available beginning with Windows Installer 3.0.</span></span> <span data-ttu-id="59b98-112">Le [Opzioni della riga di comando](command-line-options.md) Windows Installer sono disponibili con Windows Installer 3,0 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="59b98-112">The Windows Installer [Command-Line Options](command-line-options.md) are available with Windows Installer 3.0 and earlier versions.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="59b98-113">Opzione</span><span class="sxs-lookup"><span data-stu-id="59b98-113">Option</span></span></th>
<th><span data-ttu-id="59b98-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="59b98-114">Parameters</span></span></th>
<th><span data-ttu-id="59b98-115">Significato</span><span class="sxs-lookup"><span data-stu-id="59b98-115">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="59b98-116"><strong>/Help</strong></span><span class="sxs-lookup"><span data-stu-id="59b98-116"><strong>/help</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="59b98-117">Guida e opzioni di riferimento rapido.</span><span class="sxs-lookup"><span data-stu-id="59b98-117">Help and quick reference option.</span></span> <span data-ttu-id="59b98-118">Visualizza l'utilizzo corretto del comando di installazione, incluso un elenco di tutte le opzioni e il comportamento.</span><span class="sxs-lookup"><span data-stu-id="59b98-118">Displays the correct usage of the setup command including a list of all switches and behavior.</span></span> <span data-ttu-id="59b98-119">La descrizione dell'utilizzo può essere visualizzata nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="59b98-119">The description of usage can be displayed in the user interface.</span></span> <span data-ttu-id="59b98-120">L'uso errato di qualsiasi opzione richiama questa opzione della guida.</span><span class="sxs-lookup"><span data-stu-id="59b98-120">Incorrect use of any option invokes this help option.</span></span><br/> <span data-ttu-id="59b98-121">Esempio: <strong>msiexec/Help</strong></span><span class="sxs-lookup"><span data-stu-id="59b98-121">Example: <strong>msiexec /help</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="59b98-122">L'opzione della <a href="command-line-options.md">riga di comando</a> Windows Installer equivalente è <strong>/?</strong>.</span><span class="sxs-lookup"><span data-stu-id="59b98-122">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/?</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59b98-123"><strong>/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="59b98-123"><strong>/quiet</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="59b98-124">Opzione di visualizzazione non interattiva.</span><span class="sxs-lookup"><span data-stu-id="59b98-124">Quiet display option.</span></span> <span data-ttu-id="59b98-125">Il programma di installazione esegue un'installazione senza visualizzare un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="59b98-125">The installer runs an installation without displaying a user interface.</span></span> <span data-ttu-id="59b98-126">Non vengono visualizzati messaggi di richiesta, messaggi o finestre di dialogo per l'utente.</span><span class="sxs-lookup"><span data-stu-id="59b98-126">No prompts, messages, or dialog boxes are displayed to the user.</span></span> <span data-ttu-id="59b98-127">L'utente non può annullare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="59b98-127">The user cannot cancel the installation.</span></span> <span data-ttu-id="59b98-128">Usare le opzioni della riga di comando standard <strong>/norestart</strong> o <strong>/forcerestart</strong> per controllare i riavvii.</span><span class="sxs-lookup"><span data-stu-id="59b98-128">Use the <strong>/norestart</strong> or <strong>/forcerestart</strong> standard command-line options to control reboots.</span></span> <span data-ttu-id="59b98-129">Se non vengono specificate opzioni di riavvio, il programma di installazione riavvia il computer ogni volta che è necessario senza visualizzare alcun messaggio di richiesta o avviso per l'utente.</span><span class="sxs-lookup"><span data-stu-id="59b98-129">If no reboot options are specified, the installer restarts the computer whenever necessary without displaying any prompt or warning to the user.</span></span><br/> <span data-ttu-id="59b98-130">Esempi:</span><span class="sxs-lookup"><span data-stu-id="59b98-130">Examples:</span></span> <br/> <span data-ttu-id="59b98-131"><strong>msiexec/package Application.msi/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="59b98-131"><strong>msiexec /package Application.msi /quiet</strong></span></span><br/> <span data-ttu-id="59b98-132"><strong>Msiexec/Uninstall Application.msi/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="59b98-132"><strong>Msiexec /uninstall Application.msi /quiet</strong></span></span><br/> <span data-ttu-id="59b98-133"><strong>Msiexec/Update msipatch. msp/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="59b98-133"><strong>Msiexec /update msipatch.msp /quiet</strong></span></span><br/> <span data-ttu-id="59b98-134"><strong>Msiexec/Uninstall msipatch. msp/Package Application.msi/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="59b98-134"><strong>Msiexec /uninstall msipatch.msp /package Application.msi / quiet</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="59b98-135">L'opzione della <a href="command-line-options.md">riga di comando</a> equivalente Windows Installer è <strong>/qn</strong>.</span><span class="sxs-lookup"><span data-stu-id="59b98-135">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/qn</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59b98-136"><strong>/passive</strong></span><span class="sxs-lookup"><span data-stu-id="59b98-136"><strong>/passive</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="59b98-137">Opzione di visualizzazione passiva.</span><span class="sxs-lookup"><span data-stu-id="59b98-137">Passive display option.</span></span> <span data-ttu-id="59b98-138">Il programma di installazione visualizza all'utente un indicatore di stato che indica che è in corso un'installazione, ma non vengono visualizzati messaggi di richiesta o messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="59b98-138">The installer displays a progress bar to the user that indicates that an installation is in progress but no prompts or error messages are displayed to the user.</span></span> <span data-ttu-id="59b98-139">L'utente non può annullare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="59b98-139">The user cannot cancel the installation.</span></span> <span data-ttu-id="59b98-140">Usare le opzioni della riga di comando standard <strong>/norestart</strong> o <strong>/forcerestart</strong> per controllare i riavvii.</span><span class="sxs-lookup"><span data-stu-id="59b98-140">Use the <strong>/norestart</strong> or <strong>/forcerestart</strong> standard command-line options to control reboots.</span></span> <span data-ttu-id="59b98-141">Se non viene specificata alcuna opzione di riavvio, il programma di installazione riavvia il computer ogni volta che è necessario senza visualizzare alcun messaggio di richiesta o avviso per l'utente.</span><span class="sxs-lookup"><span data-stu-id="59b98-141">If no reboot option is specified, the installer restarts the computer whenever necessary without displaying any prompt or warning to the user.</span></span> <br/> <span data-ttu-id="59b98-142">Esempio: <strong>msiexec/package Application.msi/passive</strong> </span><span class="sxs-lookup"><span data-stu-id="59b98-142">Example: <strong>msiexec /package Application.msi /passive</strong> </span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="59b98-143">L'opzione della <a href="command-line-options.md">riga di comando</a> Windows Installer equivalente è <strong>/qb!-</strong> con <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>= S impostata nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="59b98-143">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/qb!-</strong> with <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>=S set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59b98-144"><strong>/norestart</strong></span><span class="sxs-lookup"><span data-stu-id="59b98-144"><strong>/norestart</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="59b98-145">Non riavviare mai l'opzione.</span><span class="sxs-lookup"><span data-stu-id="59b98-145">Never restart option.</span></span> <span data-ttu-id="59b98-146">Il programma di installazione non riavvia mai il computer dopo l'installazione.</span><span class="sxs-lookup"><span data-stu-id="59b98-146">The installer never restarts the computer after the installation.</span></span><br/> <span data-ttu-id="59b98-147">Esempio: msiexec/package Application.msi <strong>/norestart</strong></span><span class="sxs-lookup"><span data-stu-id="59b98-147">Example: msiexec /package Application.msi <strong>/norestart</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="59b98-148">La riga di comando Windows Installer equivalente è impostata su <a href="reboot.md"><strong>reboot</strong></a>= ReallySuppress nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="59b98-148">The equivalent Windows Installer command line has <a href="reboot.md"><strong>REBOOT</strong></a>=ReallySuppress set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59b98-149"><strong>/forcerestart</strong></span><span class="sxs-lookup"><span data-stu-id="59b98-149"><strong>/forcerestart</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="59b98-150">Sempre l'opzione di riavvio.</span><span class="sxs-lookup"><span data-stu-id="59b98-150">Always restart option.</span></span> <span data-ttu-id="59b98-151">Il programma di installazione riavvia sempre il computer dopo ogni installazione.</span><span class="sxs-lookup"><span data-stu-id="59b98-151">The installer always restarts the computer after every installation.</span></span><br/> <span data-ttu-id="59b98-152">Esempio: msiexec/package Application.msi <strong>/forcerestart</strong></span><span class="sxs-lookup"><span data-stu-id="59b98-152">Example: msiexec /package Application.msi <strong>/forcerestart</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="59b98-153">La riga di comando di Windows Installer equivalente ha <a href="reboot.md"><strong>reboot</strong></a>= Force impostato nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="59b98-153">The equivalent Windows Installer command line has <a href="reboot.md"><strong>REBOOT</strong></a>=Force set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59b98-154"><strong>/promptrestart</strong></span><span class="sxs-lookup"><span data-stu-id="59b98-154"><strong>/promptrestart</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="59b98-155">Richiedi conferma prima di riavviare l'opzione.</span><span class="sxs-lookup"><span data-stu-id="59b98-155">Prompt before restarting option.</span></span> <span data-ttu-id="59b98-156">Visualizza un messaggio che indica che è necessario riavviare il computer per completare l'installazione e chiede all'utente se riavviare il sistema adesso.</span><span class="sxs-lookup"><span data-stu-id="59b98-156">Displays a message that a restart is required to complete the installation and asks the user whether to restart the system now.</span></span> <span data-ttu-id="59b98-157">Questa opzione non può essere usata in combinazione con l'opzione <strong>/quiet</strong> .</span><span class="sxs-lookup"><span data-stu-id="59b98-157">This option cannot be used together with the <strong>/quiet</strong> option.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="59b98-158">La riga di comando equivalente Windows Installer dispone di <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>  =  &quot; &quot; impostato nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="59b98-158">The equivalent Windows Installer command line has <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a> = &quot;&quot; set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59b98-159"><strong>/Uninstall</strong></span><span class="sxs-lookup"><span data-stu-id="59b98-159"><strong>/uninstall</strong></span></span></td>
<td><em><Package.msi|ProductCode></em></td>
<td><span data-ttu-id="59b98-160">Disinstalla il prodotto.</span><span class="sxs-lookup"><span data-stu-id="59b98-160">Uninstall product option.</span></span> <span data-ttu-id="59b98-161">Disinstalla un prodotto.</span><span class="sxs-lookup"><span data-stu-id="59b98-161">Uninstalls a product.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="59b98-162">L'opzione della <a href="command-line-options.md">riga di comando</a> Windows Installer equivalente è <strong>/x</strong>.</span><span class="sxs-lookup"><span data-stu-id="59b98-162">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/x</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59b98-163"><strong>/Uninstall</strong></span><span class="sxs-lookup"><span data-stu-id="59b98-163"><strong>/uninstall</strong></span></span></td>
<td><span data-ttu-id="59b98-164"><em>/Package <Package.msi | ProductCode> /Uninstall <Update1.msp | PatchGUID1> [; Update2. msp | PatchGUID2]</em></span><span class="sxs-lookup"><span data-stu-id="59b98-164"><em>/package <Package.msi | ProductCode> /uninstall <Update1.msp | PatchGUID1>[;Update2.msp | PatchGUID2]</em></span></span></td>
<td><span data-ttu-id="59b98-165">Opzione Disinstalla aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="59b98-165">Uninstall update option.</span></span> <span data-ttu-id="59b98-166">Disinstalla una patch di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="59b98-166">Uninstalls an update patch.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="59b98-167">L'opzione della <a href="command-line-options.md">riga di comando</a> Windows Installer equivalente è <strong>/i</strong> con <a href="msipatchremove.md"><strong>MSIPATCHREMOVE</strong></a>= Update1. msp | PatchGUID1[; Update2. msp | PatchGUID2] impostato nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="59b98-167">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/I</strong> with <a href="msipatchremove.md"><strong>MSIPATCHREMOVE</strong></a>=Update1.msp | PatchGUID1[;Update2.msp | PatchGUID2] set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59b98-168"><strong>/log</strong></span><span class="sxs-lookup"><span data-stu-id="59b98-168"><strong>/log</strong></span></span></td>
<td><em><logfile></em></td>
<td><span data-ttu-id="59b98-169">Opzione log.</span><span class="sxs-lookup"><span data-stu-id="59b98-169">Log option.</span></span> <span data-ttu-id="59b98-170">Scrive le informazioni di registrazione in un file di log nel percorso esistente specificato.</span><span class="sxs-lookup"><span data-stu-id="59b98-170">Writes logging information into a log file at the specified existing path.</span></span> <span data-ttu-id="59b98-171">Il percorso del percorso del file di log deve essere già esistente.</span><span class="sxs-lookup"><span data-stu-id="59b98-171">The path to the log file location must already exist.</span></span> <span data-ttu-id="59b98-172">Il programma di installazione non crea la struttura di directory per il file di log.</span><span class="sxs-lookup"><span data-stu-id="59b98-172">The installer does not create the directory structure for the logfile.</span></span><br/> <span data-ttu-id="59b98-173">Le seguenti informazioni vengono immesse nel log:</span><span class="sxs-lookup"><span data-stu-id="59b98-173">The following information is entered into the log:</span></span><br/>
<ul>
<li><span data-ttu-id="59b98-174">Messaggi di stato</span><span class="sxs-lookup"><span data-stu-id="59b98-174">Status messages</span></span></li>
<li><span data-ttu-id="59b98-175">Avvisi non irreversibili</span><span class="sxs-lookup"><span data-stu-id="59b98-175">Nonfatal warnings</span></span></li>
<li><span data-ttu-id="59b98-176">Tutti i messaggi di errore</span><span class="sxs-lookup"><span data-stu-id="59b98-176">All error messages</span></span></li>
<li><span data-ttu-id="59b98-177">Avvio delle azioni</span><span class="sxs-lookup"><span data-stu-id="59b98-177">Start up of actions</span></span></li>
<li><span data-ttu-id="59b98-178">Record specifici dell'azione</span><span class="sxs-lookup"><span data-stu-id="59b98-178">Action-specific records</span></span></li>
<li><span data-ttu-id="59b98-179">Richieste utente</span><span class="sxs-lookup"><span data-stu-id="59b98-179">User requests</span></span></li>
<li><span data-ttu-id="59b98-180">Parametri iniziali dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="59b98-180">Initial UI parameters</span></span></li>
<li><span data-ttu-id="59b98-181">Informazioni sulla memoria insufficiente o sull'uscita fatale</span><span class="sxs-lookup"><span data-stu-id="59b98-181">Out-of-memory or fatal exit information</span></span></li>
<li><span data-ttu-id="59b98-182">Messaggi spazio su disco esaurito</span><span class="sxs-lookup"><span data-stu-id="59b98-182">Out-of-disk-space messages</span></span></li>
<li><span data-ttu-id="59b98-183">Proprietà Terminal</span><span class="sxs-lookup"><span data-stu-id="59b98-183">Terminal properties</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="59b98-184">L'opzione della <a href="command-line-options.md">riga di comando</a> Windows Installer equivalente è <strong>/l \*</strong>.</span><span class="sxs-lookup"><span data-stu-id="59b98-184">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/L\*</strong>.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="59b98-185">Per ulteriori informazioni su tutti i metodi disponibili per l'impostazione della modalità di registrazione, vedere <a href="normal-logging.md">registrazione normale</a> nella sezione <a href="windows-installer-logging.md">registrazione Windows Installer</a> .</span><span class="sxs-lookup"><span data-stu-id="59b98-185">For more information about all the methods that are available for setting the logging mode, see <a href="normal-logging.md">Normal Logging</a> in the <a href="windows-installer-logging.md">Windows Installer Logging</a> section.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59b98-186"><strong>/Package</strong></span><span class="sxs-lookup"><span data-stu-id="59b98-186"><strong>/package</strong></span></span></td>
<td><em><Package.msi|ProductCode></em></td>
<td><span data-ttu-id="59b98-187">Installare l'opzione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="59b98-187">Install product option.</span></span> <span data-ttu-id="59b98-188">Installa o configura un prodotto.</span><span class="sxs-lookup"><span data-stu-id="59b98-188">Installs or configures a product.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="59b98-189">L'opzione della <a href="command-line-options.md">riga di comando</a> Windows Installer equivalente è <strong>/i</strong>.</span><span class="sxs-lookup"><span data-stu-id="59b98-189">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/I</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59b98-190"><strong>/Update</strong></span><span class="sxs-lookup"><span data-stu-id="59b98-190"><strong>/update</strong></span></span></td>
<td><span data-ttu-id="59b98-191"><em><Update1.msp>[; Update2. msp]</em></span><span class="sxs-lookup"><span data-stu-id="59b98-191"><em><Update1.msp>[;Update2.msp]</em></span></span></td>
<td><span data-ttu-id="59b98-192">Opzione Installa patch.</span><span class="sxs-lookup"><span data-stu-id="59b98-192">Install patches option.</span></span> <span data-ttu-id="59b98-193">Installa una o più patch.</span><span class="sxs-lookup"><span data-stu-id="59b98-193">Installs one or multiple patches.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="59b98-194">La riga di comando equivalente Windows Installer presenta <a href="patch.md"><strong>patch</strong></a> = [msipatch. msp] <; PatchGuid2> impostato nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="59b98-194">The equivalent Windows Installer command line has <a href="patch.md"><strong>PATCH</strong></a> = [msipatch.msp]<;PatchGuid2> set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
