---
description: Wilogutl.exe facilita l'analisi dei file di log da un'installazione di Windows Installer e visualizza le soluzioni suggerite agli errori rilevati in un file di log.
ms.assetid: 09aa03ba-992f-47ab-999b-ebdfe85c1ea7
title: Wilogutl.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec81c3c82299a08fd947fbbecc7afd8a373252b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319951"
---
# <a name="wilogutlexe"></a><span data-ttu-id="1885c-103">Wilogutl.exe</span><span class="sxs-lookup"><span data-stu-id="1885c-103">Wilogutl.exe</span></span>

<span data-ttu-id="1885c-104">Wilogutl.exe facilita l'analisi dei file di log da un'installazione di Windows Installer e visualizza le soluzioni suggerite agli errori rilevati in un file di log.</span><span class="sxs-lookup"><span data-stu-id="1885c-104">Wilogutl.exe assists the analysis of log files from a Windows Installer installation, and it displays suggested solutions to errors that are found in a log file.</span></span>

<span data-ttu-id="1885c-105">Gli errori non critici non vengono visualizzati.</span><span class="sxs-lookup"><span data-stu-id="1885c-105">Non-critical errors are not displayed.</span></span> <span data-ttu-id="1885c-106">Wilogutl.exe possono essere eseguiti in modalità non interattiva o con un'interfaccia utente (UI).</span><span class="sxs-lookup"><span data-stu-id="1885c-106">Wilogutl.exe can be run in quiet mode or with a user interface (UI).</span></span> <span data-ttu-id="1885c-107">Lo strumento genera report come file di testo sia nell'interfaccia utente che nelle modalità non interattiva.</span><span class="sxs-lookup"><span data-stu-id="1885c-107">The tool generates reports as text files in both the UI and quiet modes.</span></span> <span data-ttu-id="1885c-108">Funziona meglio con i file di log dettagliati Windows Installer, ma funziona anche con log non dettagliati.</span><span class="sxs-lookup"><span data-stu-id="1885c-108">It works best with verbose Windows Installer log files, but also works with non-verbose logs.</span></span> <span data-ttu-id="1885c-109">Per altre informazioni, vedere [Registrazione](logging.md).</span><span class="sxs-lookup"><span data-stu-id="1885c-109">For more information, see [Logging](logging.md).</span></span>

<span data-ttu-id="1885c-110">Questo strumento è disponibile solo nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="1885c-110">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1885c-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1885c-111">Syntax</span></span>

<span data-ttu-id="1885c-112">\**wilogutl.exe\*\*\*\[<options>\]\[<source file>\]\[<options>\]\[<report file directory>\]*</span><span class="sxs-lookup"><span data-stu-id="1885c-112">**wilogutl.exe** *\[<options>\]\[<source file>\]\[<options>\]\[<report file directory>\]*</span></span>

<span data-ttu-id="1885c-113">È possibile utilizzare le seguenti righe di comando per eseguire in modalità non interattiva.</span><span class="sxs-lookup"><span data-stu-id="1885c-113">You can use the following command lines to run in quiet mode.</span></span>

<span data-ttu-id="1885c-114">**Wilogutl/q/l** *c: \\ mymsilog. log* **/o** *c \\ OutputDir \\*</span><span class="sxs-lookup"><span data-stu-id="1885c-114">**wilogutl /q /l** *c:\\mymsilog.log* **/o** *c\\outputdir\\*</span></span>

<span data-ttu-id="1885c-115">**Wilogutl/q/l** *c: \\ mymsilog. log*</span><span class="sxs-lookup"><span data-stu-id="1885c-115">**wilogutl /q /l** *c:\\mymsilog.log*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="1885c-116">Opzioni della riga di comando</span><span class="sxs-lookup"><span data-stu-id="1885c-116">Command-Line Options</span></span>

<span data-ttu-id="1885c-117">Wilogutl.exe usa le seguenti opzioni della riga di comando senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="1885c-117">Wilogutl.exe uses the following case insensitive command-line options.</span></span> <span data-ttu-id="1885c-118">È possibile usare un delimitatore di trattino al posto di una barra.</span><span class="sxs-lookup"><span data-stu-id="1885c-118">A dash delimiter can be used in place of a slash.</span></span>



| <span data-ttu-id="1885c-119">Opzione</span><span class="sxs-lookup"><span data-stu-id="1885c-119">Option</span></span> | <span data-ttu-id="1885c-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1885c-120">Description</span></span>                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1885c-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1885c-121">none</span></span>   | <span data-ttu-id="1885c-122">Viene eseguito in modalità interfaccia utente, senza opzioni della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="1885c-122">Runs in UI mode—without command-line options.</span></span>                                                                                                                                                   |
| <span data-ttu-id="1885c-123">/q</span><span class="sxs-lookup"><span data-stu-id="1885c-123">/q</span></span>     | <span data-ttu-id="1885c-124">Specifica la modalità non interattiva.</span><span class="sxs-lookup"><span data-stu-id="1885c-124">Specifies the quiet mode.</span></span> <span data-ttu-id="1885c-125">Wilogutl.exe genera file di report e non visualizza un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="1885c-125">Wilogutl.exe generates report files and does not display a user interface.</span></span>                                                                                            |
| <span data-ttu-id="1885c-126">/l</span><span class="sxs-lookup"><span data-stu-id="1885c-126">/l</span></span>     | <span data-ttu-id="1885c-127">Specifica il nome del file di log da analizzare.</span><span class="sxs-lookup"><span data-stu-id="1885c-127">Specifies the name of the log file to be analyzed.</span></span> <span data-ttu-id="1885c-128">Questa opzione è obbligatoria quando si usa la modalità non interattiva.</span><span class="sxs-lookup"><span data-stu-id="1885c-128">This option is required when using the quiet mode.</span></span>                                                                                           |
| <span data-ttu-id="1885c-129">/o</span><span class="sxs-lookup"><span data-stu-id="1885c-129">/o</span></span>     | <span data-ttu-id="1885c-130">Specifica la directory di output per i file di report.</span><span class="sxs-lookup"><span data-stu-id="1885c-130">Specifies the output directory for report files.</span></span> <span data-ttu-id="1885c-131">Questo percorso di output viene usato solo quando è in esecuzione in modalità non interattiva.</span><span class="sxs-lookup"><span data-stu-id="1885c-131">This output path is used only when running in quiet mode.</span></span> <span data-ttu-id="1885c-132">Se l'opzione non è presente, i report vengono inseriti nella directory C: \\ WiLogResults</span><span class="sxs-lookup"><span data-stu-id="1885c-132">If the option is not present, the reports are put in the C:\\WiLogResults directory.</span></span> |



 

<span data-ttu-id="1885c-133">Quando viene eseguito in modalità interfaccia utente, Wilogutl.exe Visualizza le seguenti finestre di dialogo.</span><span class="sxs-lookup"><span data-stu-id="1885c-133">When run in UI mode, Wilogutl.exe displays the following dialog boxes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1885c-134">Nome</span><span class="sxs-lookup"><span data-stu-id="1885c-134">Name</span></span></th>
<th><span data-ttu-id="1885c-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1885c-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1885c-136">Analizzatore log dettagliato Windows Installer</span><span class="sxs-lookup"><span data-stu-id="1885c-136">Windows Installer Verbose Log Analyzer</span></span></td>
<td><span data-ttu-id="1885c-137">La finestra di dialogo analizzatore log dettagliato di Windows Installer consente agli utenti di selezionare un file di log per l'analisi:</span><span class="sxs-lookup"><span data-stu-id="1885c-137">The Windows Installer Verbose Log Analyzer dialog box enables users to select a log file for analysis:</span></span>
<ul>
<li><span data-ttu-id="1885c-138">Il pulsante <strong>Apri</strong> apre il file nel blocco note.</span><span class="sxs-lookup"><span data-stu-id="1885c-138">The <strong>Open</strong> button opens the file in Notepad.</span></span> <span data-ttu-id="1885c-139">È possibile utilizzare l'area di anteprima per verificare che sia stato selezionato il file di log corretto.</span><span class="sxs-lookup"><span data-stu-id="1885c-139">The preview area can be used to verify that the correct log file has been selected.</span></span></li>
<li><span data-ttu-id="1885c-140">Il pulsante <strong>analizza</strong> avvia l'analisi dei file di log e visualizza la finestra di dialogo visualizzazione file di log dettagliata.</span><span class="sxs-lookup"><span data-stu-id="1885c-140">The <strong>Analyze</strong> button begins log file analysis and displays the Detailed Log File View dialog box.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1885c-141">Visualizzazione dettagliata del file di log</span><span class="sxs-lookup"><span data-stu-id="1885c-141">Detailed Log File View</span></span></td>
<td><span data-ttu-id="1885c-142">Nella finestra di dialogo visualizzazione file di log dettagliata vengono visualizzate le informazioni sull'errore registrate.</span><span class="sxs-lookup"><span data-stu-id="1885c-142">The Detailed Log File View dialog box displays logged error information.</span></span> <span data-ttu-id="1885c-143">Usare i pulsanti <strong>indietro</strong> e <strong>Avanti</strong> per spostarsi tra più errori.</span><span class="sxs-lookup"><span data-stu-id="1885c-143">Use the <strong>Back</strong> and <strong>Next</strong> buttons to navigate through multiple errors.</span></span> <span data-ttu-id="1885c-144">Per visualizzare gli errori non critici, selezionare la casella di controllo <strong>Mostra errori di debug ignorati</strong> .</span><span class="sxs-lookup"><span data-stu-id="1885c-144">To display non-critical errors select the <strong>Show Ignored Debug Errors</strong> check box.</span></span> <span data-ttu-id="1885c-145">Viene visualizzata la versione del programma di installazione nel computer utilizzato per eseguire l'installazione registrata.</span><span class="sxs-lookup"><span data-stu-id="1885c-145">The installer version on the computer used to run the logged installation is displayed.</span></span> <span data-ttu-id="1885c-146">Se l'installazione registrata è stata eseguita con autorizzazioni elevate, la casella di controllo <strong>installazione con privilegi elevati</strong> è selezionata e le informazioni vengono fornite nelle caselle di testo Dettagli <strong>privilegi lato client</strong> e <strong>privilegi lato server</strong> .</span><span class="sxs-lookup"><span data-stu-id="1885c-146">If the logged installation was run with elevated permissions, the <strong>Elevated install</strong> check box is selected and information is provided in the <strong>Client Side Privilege Details</strong> and <strong>Server Side Privilege Details</strong> text boxes.</span></span> <span data-ttu-id="1885c-147">Nella finestra di dialogo visualizzazione file di log dettagliata sono disponibili i pulsanti seguenti:</span><span class="sxs-lookup"><span data-stu-id="1885c-147">The Detailed Log File View dialog box contains the following buttons:</span></span><br/>
<ul>
<li><span data-ttu-id="1885c-148"><strong>Stati</strong> - di Consente di visualizzare la finestra di dialogo stati componenti e funzionalità.</span><span class="sxs-lookup"><span data-stu-id="1885c-148"><strong>States</strong> - Show the Feature and Component States dialog box.</span></span></li>
<li><span data-ttu-id="1885c-149"><strong>Proprietà</strong> - di Visualizza la finestra di dialogo Proprietà.</span><span class="sxs-lookup"><span data-stu-id="1885c-149"><strong>Properties</strong> - Show the Properties dialog box.</span></span></li>
<li><span data-ttu-id="1885c-150"><strong>Criteri</strong> - di Mostra la finestra di dialogo criteri.</span><span class="sxs-lookup"><span data-stu-id="1885c-150"><strong>Policies</strong> - Show the Policies dialog box.</span></span></li>
<li><span data-ttu-id="1885c-151">Log con annotazioni <strong>HTML</strong> - Mostra log come file HTML con annotazioni.</span><span class="sxs-lookup"><span data-stu-id="1885c-151"><strong>HTML Annotated Log</strong> - Show log as annotated HTML file.</span></span></li>
<li><span data-ttu-id="1885c-152"><strong>Salva risultati</strong> - Consente di salvare i file di report nella directory specificata.</span><span class="sxs-lookup"><span data-stu-id="1885c-152"><strong>Save Results</strong> - Save report files to specified directory.</span></span></li>
<li><span data-ttu-id="1885c-153">Guida del messaggio di <strong>errore</strong> - Mostra la guida del messaggio di errore del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="1885c-153"><strong>Error Message Help</strong> - Show installer error message help.</span></span></li>
<li><span data-ttu-id="1885c-154"><strong>Guida</strong> - di Mostra la guida per Windows Installer Setup Log Analyzer.</span><span class="sxs-lookup"><span data-stu-id="1885c-154"><strong>Help</strong> - Show help for Windows Installer Setup Log Analyzer.</span></span></li>
<li><span data-ttu-id="1885c-155"><strong>Come leggere un file</strong> - di log Visualizzare il documento della guida del file di log.</span><span class="sxs-lookup"><span data-stu-id="1885c-155"><strong>How to Read a Log File</strong> - Show the log file help document.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1885c-156">Stati di funzionalità e componenti</span><span class="sxs-lookup"><span data-stu-id="1885c-156">Feature and Component States</span></span></td>
<td><span data-ttu-id="1885c-157">Nella finestra di dialogo <strong>stati funzionalità e</strong> componenti vengono visualizzati gli Stati delle funzionalità e dei componenti di:</span><span class="sxs-lookup"><span data-stu-id="1885c-157">The <strong>Feature and Component States</strong> dialog box displays the states of features and components:</span></span>
<ul>
<li><span data-ttu-id="1885c-158">Nella colonna <strong>funzionalità</strong> viene visualizzato il nome della funzionalità nel pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="1885c-158">The <strong>Feature</strong> column shows the name for the feature in the installation package.</span></span></li>
<li><span data-ttu-id="1885c-159">Nella colonna <strong>componente</strong> viene visualizzato il nome del componente nel pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="1885c-159">The <strong>Component</strong> column shows the name of the component in the installation package.</span></span></li>
<li><span data-ttu-id="1885c-160">Nella colonna <strong>installato</strong> viene visualizzato lo stato della funzionalità o del componente alla fine dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="1885c-160">The <strong>Installed</strong> column shows the feature or component's state at the end of the installation.</span></span></li>
<li><span data-ttu-id="1885c-161">Nella colonna <strong>richiesta</strong> viene visualizzata la selezione dell'utente durante l'installazione per lo stato della funzionalità o del componente.</span><span class="sxs-lookup"><span data-stu-id="1885c-161">The <strong>Request</strong> column shows the user's selection during the installation for the feature or component's state.</span></span></li>
<li><span data-ttu-id="1885c-162">Nella colonna <strong>azione</strong> viene visualizzata l'azione eseguita dal programma di installazione per la funzionalità o il componente.</span><span class="sxs-lookup"><span data-stu-id="1885c-162">The <strong>Action</strong> column shows the action taken by the installer for the feature or component.</span></span></li>
</ul>
<span data-ttu-id="1885c-163">Per ulteriori informazioni, vedere <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>MsiGetComponentState</strong></a> e <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>MsiGetFeatureState</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1885c-163">For more information, see <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>MsiGetComponentState</strong></a> and <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>MsiGetFeatureState</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1885c-164">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1885c-164">Properties</span></span></td>
<td><span data-ttu-id="1885c-165">Nella finestra di dialogo proprietà vengono visualizzate Windows Installer <a href="properties.md">Proprietà</a> e i relativi valori alla fine dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="1885c-165">The Properties dialog box shows Windows Installer <a href="properties.md">Properties</a> and their values at the end of the installation.</span></span> <span data-ttu-id="1885c-166">È possibile ordinare le proprietà in base al nome o al valore:</span><span class="sxs-lookup"><span data-stu-id="1885c-166">You can sort the properties by name or by value:</span></span>
<ul>
<li><span data-ttu-id="1885c-167">La scheda <strong>client</strong> Mostra le proprietà e i valori durante la parte lato client dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="1885c-167">The <strong>Client</strong> tab shows properties and values during the client side portion of the installation.</span></span></li>
<li><span data-ttu-id="1885c-168">La scheda <strong>Server</strong> Mostra le proprietà e i valori durante la parte relativa al server dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="1885c-168">The <strong>Server</strong> tab shows properties and values during the server portion of the installation.</span></span></li>
<li><span data-ttu-id="1885c-169">La scheda <strong>nidificata</strong> Mostra le proprietà e i valori di tutte le <a href="concurrent-installations.md">installazioni simultanee</a>.</span><span class="sxs-lookup"><span data-stu-id="1885c-169">The <strong>Nested</strong> tab shows the properties and values of any <a href="concurrent-installations.md">Concurrent Installations</a>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1885c-170">Criteri</span><span class="sxs-lookup"><span data-stu-id="1885c-170">Policies</span></span></td>
<td><span data-ttu-id="1885c-171">Nella finestra di dialogo criteri viene visualizzato il set di <a href="system-policy.md">criteri di sistema</a> dopo l'installazione:</span><span class="sxs-lookup"><span data-stu-id="1885c-171">The Policies dialog box displays the <a href="system-policy.md">System Policy</a> set after the installation:</span></span>
<ul>
<li><span data-ttu-id="1885c-172">Il valore 0 (zero) impostato per il criterio indica che i criteri non sono abilitati.</span><span class="sxs-lookup"><span data-stu-id="1885c-172">A value of 0 (zero) set for the policy means the policy is not enabled.</span></span></li>
<li><span data-ttu-id="1885c-173">Il valore 1 (uno) indica che i criteri sono abilitati.</span><span class="sxs-lookup"><span data-stu-id="1885c-173">A value of 1 (one) means the policy is enabled.</span></span></li>
<li><span data-ttu-id="1885c-174">Valore?</span><span class="sxs-lookup"><span data-stu-id="1885c-174">A value of ?</span></span> <span data-ttu-id="1885c-175">(punto interrogativo) indica che il valore dei criteri non è registrato nel log.</span><span class="sxs-lookup"><span data-stu-id="1885c-175">(question mark) means the policy value is not recorded in the log.</span></span></li>
</ul>
<span data-ttu-id="1885c-176">Se è necessario un valore dei criteri non presente nel log, provare a usare Regedit.exe per verificare se le chiavi del registro di sistema nel computer non sono presenti nell'installazione.</span><span class="sxs-lookup"><span data-stu-id="1885c-176">If you need a policy value that is not in the log, try using Regedit.exe to check the registry keys on the computer failing the installation.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="report-files"></a><span data-ttu-id="1885c-177">File di report</span><span class="sxs-lookup"><span data-stu-id="1885c-177">Report Files</span></span>

<span data-ttu-id="1885c-178">Quando si esegue un'analisi in modalità non interattiva o si fa clic sul pulsante **Salva risultati** nella finestra di dialogo **visualizzazione file di log dettagliata** , il Windows Installer strumento Analizzatore configurazione genera tre file di testo e un file di log con annotazioni HTML.</span><span class="sxs-lookup"><span data-stu-id="1885c-178">When performing a quiet mode analysis or clicking the **Save Results** button on the **Detailed Log File View** dialog, the Windows Installer Setup Analyzer tool generates three text files and an HTML annotated log file.</span></span>

<span data-ttu-id="1885c-179">Nella tabella seguente vengono identificati i nomi e il contenuto dei file di report.</span><span class="sxs-lookup"><span data-stu-id="1885c-179">The following table identifies the names and contents in the report files.</span></span>



| <span data-ttu-id="1885c-180">Nome</span><span class="sxs-lookup"><span data-stu-id="1885c-180">Name</span></span>                      | <span data-ttu-id="1885c-181">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1885c-181">Description</span></span>                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1885c-182">LogFileName \_summary.txt</span><span class="sxs-lookup"><span data-stu-id="1885c-182">logfilename\_summary.txt</span></span>  | <span data-ttu-id="1885c-183">Riepiloga il file di log.</span><span class="sxs-lookup"><span data-stu-id="1885c-183">Summarizes the log file.</span></span> <span data-ttu-id="1885c-184">Elenca le informazioni visualizzate nella finestra di dialogo visualizzazione file di log dettagliata e il primo errore.</span><span class="sxs-lookup"><span data-stu-id="1885c-184">Lists the information displayed by the Detailed Log File View dialog box and the first error.</span></span>         |
| <span data-ttu-id="1885c-185">LogFileName \_errors.txt</span><span class="sxs-lookup"><span data-stu-id="1885c-185">logfilename\_errors.txt</span></span>   | <span data-ttu-id="1885c-186">Identifica il numero di errori, gli errori e le soluzioni consigliate.</span><span class="sxs-lookup"><span data-stu-id="1885c-186">Identifies the number of errors, the errors, and recommended solutions.</span></span> <span data-ttu-id="1885c-187">In questo file vengono elencati errori critici e non critici.</span><span class="sxs-lookup"><span data-stu-id="1885c-187">This file lists both critical and non-critical errors.</span></span> |
| <span data-ttu-id="1885c-188">LogFileName \_policies.txt</span><span class="sxs-lookup"><span data-stu-id="1885c-188">logfilename\_policies.txt</span></span> | <span data-ttu-id="1885c-189">Identifica i nomi dei criteri e i valori impostati alla fine dell'installazione come nella finestra di dialogo criteri.</span><span class="sxs-lookup"><span data-stu-id="1885c-189">Identifies the policy names and values set at the end of the installation as in the Policies dialog box.</span></span>                       |
| <span data-ttu-id="1885c-190">Dettagli \_logfilename.htm</span><span class="sxs-lookup"><span data-stu-id="1885c-190">details\_logfilename.htm</span></span>  | <span data-ttu-id="1885c-191">Log con annotazioni HTML con una legenda per la codifica a colori.</span><span class="sxs-lookup"><span data-stu-id="1885c-191">An HTML annotated log with a legend for the color coding.</span></span>                                                                      |



 

## <a name="return-values"></a><span data-ttu-id="1885c-192">Valori restituiti</span><span class="sxs-lookup"><span data-stu-id="1885c-192">Return Values</span></span>

<span data-ttu-id="1885c-193">Se vengono passati argomenti della riga di comando non validi per le operazioni in modalità non interattiva, Wilogutl.exe non esegue alcuna operazione e il processo restituisce uno dei valori indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="1885c-193">If invalid command-line arguments are passed for quiet mode operations, Wilogutl.exe does nothing, and the process returns one of the values in the following table.</span></span>



| <span data-ttu-id="1885c-194">Valore</span><span class="sxs-lookup"><span data-stu-id="1885c-194">Value</span></span> | <span data-ttu-id="1885c-195">Significato</span><span class="sxs-lookup"><span data-stu-id="1885c-195">Meaning</span></span>                                                                 |
|-------|-------------------------------------------------------------------------|
| <span data-ttu-id="1885c-196">1</span><span class="sxs-lookup"><span data-stu-id="1885c-196">1</span></span>     | <span data-ttu-id="1885c-197">È stata specificata una directory di output non valida.</span><span class="sxs-lookup"><span data-stu-id="1885c-197">Bad output directory is specified.</span></span>                                      |
| <span data-ttu-id="1885c-198">2</span><span class="sxs-lookup"><span data-stu-id="1885c-198">2</span></span>     | <span data-ttu-id="1885c-199">Il nome del file di log specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="1885c-199">Bad log file name is specified.</span></span>                                         |
| <span data-ttu-id="1885c-200">3</span><span class="sxs-lookup"><span data-stu-id="1885c-200">3</span></span>     | <span data-ttu-id="1885c-201">Passato/q, ma non è presente l'opzione richiesta/l per il nome del file di log.</span><span class="sxs-lookup"><span data-stu-id="1885c-201">Passed /q, but is missing the required switch /l for the log file name.</span></span> |
| <span data-ttu-id="1885c-202">4</span><span class="sxs-lookup"><span data-stu-id="1885c-202">4</span></span>     | <span data-ttu-id="1885c-203">È stato passato/l, ma manca l'opzione obbligatoria/q per la modalità non interattiva.</span><span class="sxs-lookup"><span data-stu-id="1885c-203">Passed /l, but is missing the required switch /q for quiet mode.</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1885c-204">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1885c-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1885c-205">Versioni rilasciate, strumenti e ridistribuibili</span><span class="sxs-lookup"><span data-stu-id="1885c-205">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> <dt>

[<span data-ttu-id="1885c-206">Strumenti di sviluppo Windows Installer</span><span class="sxs-lookup"><span data-stu-id="1885c-206">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> </dl>

 

 




