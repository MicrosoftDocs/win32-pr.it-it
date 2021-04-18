---
description: In questa sezione viene illustrato come creare un dizionario personalizzato per il riconoscimento della grafia.
ms.assetid: 83abf534-740c-44a3-bbd4-babb54f2930e
title: Creazione di dizionari personalizzati per il riconoscimento della grafia in Windows 7 e Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80b9b7b5a1d9dfadddd83825aea7d6f676439999
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305683"
---
# <a name="creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="40251-103">Creazione di dizionari personalizzati per il riconoscimento della grafia in Windows 7 e Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="40251-103">Creating Custom Dictionaries for Handwriting Recognition in Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="40251-104">In questa sezione viene illustrato come creare un dizionario personalizzato per il riconoscimento della grafia.</span><span class="sxs-lookup"><span data-stu-id="40251-104">This section explains how to create a custom dictionary for handwriting recognition.</span></span>

<span data-ttu-id="40251-105">Nel sistema operativo Windows 7 e nel sistema operativo Windows Server 2008 R2, l'accuratezza del riconoscimento della grafia può essere significativamente migliorata tramite l'uso di dizionari personalizzati.</span><span class="sxs-lookup"><span data-stu-id="40251-105">In the Windows 7 operating system and the Windows Server 2008 R2 operating system, the accuracy of handwriting recognition can be significantly improved through the use of custom dictionaries.</span></span> <span data-ttu-id="40251-106">Questi dizionari integrano o sostituiscono i dizionari di sistema usati per la grafia.</span><span class="sxs-lookup"><span data-stu-id="40251-106">These dictionaries supplement or replace system dictionaries used for handwriting.</span></span> <span data-ttu-id="40251-107">Il supporto per il riconoscimento della grafia viene fornito tramite la funzionalità Servizi di riconoscimento della grafia che deve essere abilitata tramite Server Manager.</span><span class="sxs-lookup"><span data-stu-id="40251-107">Support for handwriting recognition is provided through the Ink and Handwriting Services feature that needs to be enabled through Server Manager.</span></span>

> [!Note]  
> <span data-ttu-id="40251-108">I dizionari personalizzati possono essere installati per un linguaggio solo se il riconoscimento della grafia per tale lingua è installato.</span><span class="sxs-lookup"><span data-stu-id="40251-108">Custom dictionaries can be installed for a language only if the handwriting recognizer for that language is installed.</span></span>

 

<span data-ttu-id="40251-109">Per configurare un dizionario personalizzato per la grafia sono necessari due passaggi di base:</span><span class="sxs-lookup"><span data-stu-id="40251-109">There are two basic steps to setting up a custom dictionary for handwriting:</span></span>

-   <span data-ttu-id="40251-110">Compila un elenco di parole.</span><span class="sxs-lookup"><span data-stu-id="40251-110">Compile a word list.</span></span> <span data-ttu-id="40251-111">La compilazione crea un file di dizionario personalizzato compilato (con estensione hwrdict).</span><span class="sxs-lookup"><span data-stu-id="40251-111">The compilation creates a compiled custom dictionary (.hwrdict) file.</span></span>
-   <span data-ttu-id="40251-112">Installare il dizionario personalizzato compilato.</span><span class="sxs-lookup"><span data-stu-id="40251-112">Install the compiled custom dictionary.</span></span>

## <a name="compiling-a-word-list"></a><span data-ttu-id="40251-113">Compilazione di un elenco di parole</span><span class="sxs-lookup"><span data-stu-id="40251-113">Compiling a Word List</span></span>

<span data-ttu-id="40251-114">L'elenco di parole da compilare deve essere in formato testo normale e deve essere salvato utilizzando una codifica Unicode.</span><span class="sxs-lookup"><span data-stu-id="40251-114">The word list to be compiled must be in plain-text format and should be saved using a Unicode encoding.</span></span> <span data-ttu-id="40251-115">Altre codifiche non funzioneranno.</span><span class="sxs-lookup"><span data-stu-id="40251-115">Other encodings will not work.</span></span> <span data-ttu-id="40251-116">Ogni riga del file di testo viene considerata come una singola voce nel dizionario.</span><span class="sxs-lookup"><span data-stu-id="40251-116">Each line of the text file is taken as a single entry in the dictionary.</span></span> <span data-ttu-id="40251-117">Sono consentite le voci di unità multiword contenenti uno o più spazi.</span><span class="sxs-lookup"><span data-stu-id="40251-117">Multiword units entries containing one or more spaces are allowed.</span></span> <span data-ttu-id="40251-118">Gli spazi all'inizio o alla fine di una riga vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="40251-118">Spaces at the beginning or end of a line are ignored.</span></span>

<span data-ttu-id="40251-119">Un dizionario personalizzato viene compilato da una riga di comando.</span><span class="sxs-lookup"><span data-stu-id="40251-119">A custom dictionary is compiled from a command line.</span></span> <span data-ttu-id="40251-120">Per compilare un dizionario, aprire una finestra di comando, passare alla cartella contenente l'elenco di parole, quindi eseguire HwrComp.exe con le opzioni della riga di comando che si desidera utilizzare.</span><span class="sxs-lookup"><span data-stu-id="40251-120">To compile a dictionary, open a command window, navigate to the folder containing the word list, and then run HwrComp.exe with the command-line options you want to use.</span></span>

<span data-ttu-id="40251-121">Nell'esempio seguente viene illustrata la sintassi di utilizzo per le opzioni della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="40251-121">The following example shows the usage syntax for the command-line options.</span></span>

``` syntax
Usage: hwrcomp       [-lang <localename>] [-type <type>]
    [-comment <comment>]
    [-o <dictfile.hwrdict>]
    <inputfile>
     
```

### <a name="explanation-of-options"></a><span data-ttu-id="40251-122">Spiegazione delle opzioni</span><span class="sxs-lookup"><span data-stu-id="40251-122">Explanation of Options</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="40251-123">Parametro</span><span class="sxs-lookup"><span data-stu-id="40251-123">Parameter</span></span></th>
<th><span data-ttu-id="40251-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40251-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="40251-125">-lang <localename></span><span class="sxs-lookup"><span data-stu-id="40251-125">-lang <localename></span></span></td>
<td><span data-ttu-id="40251-126">Nome delle impostazioni locali specificato assegnato al file del dizionario personalizzato compilato.</span><span class="sxs-lookup"><span data-stu-id="40251-126">The specified locale name assigned to the compiled custom dictionary file.</span></span> <span data-ttu-id="40251-127">L'argomento <localename> ha il formato Language-Region.</span><span class="sxs-lookup"><span data-stu-id="40251-127">The argument <localename> has the form language-REGION.</span></span> <span data-ttu-id="40251-128">Un esempio è en-US, che indica la lingua inglese nell'area Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="40251-128">An example of this is en-US, which signifies the English language in the United States region.</span></span> <span data-ttu-id="40251-129">Per esempi di questo formato, vedere [costanti e stringhe degli identificatori di lingua](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="40251-129">For examples of this form, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span> <span data-ttu-id="40251-130">Le lingue seguenti sono supportate per Windows 7 e Windows Server 2008 R2 da questa funzionalità: en-US, en-GB, en-CA, en-AU, de-DE, de-CH, fr-FR, es-ES, es-MX, es-AR, it-IT, nl-NL, NL-BE, PT-BR, PT-PT, da-DK, sv-SE, nb-NO, nn-NO, fi-FI, pl-PL, CS-CZ, ur-RU, RO-RO, Sr-Latn-CS, Sr-Cyrl-CS, ca-ES e HR-HR.</span><span class="sxs-lookup"><span data-stu-id="40251-130">The following languages are supported for Windows 7 and Windows Server 2008 R2 by this feature: en-US, en-GB, en-CA, en-AU, de-DE, de-CH, fr-FR, es-ES, es-MX, es-AR, it-IT, nl-NL, nl-BE, pt-BR, pt-PT, da-DK, sv-SE, nb-NO, nn-NO, fi-FI, pl-PL, cs-CZ, ru-RU, ro-RO, sr-Latn-CS, sr-Cyrl-CS, ca-ES and hr-HR.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40251-131">-tipo <type></span><span class="sxs-lookup"><span data-stu-id="40251-131">-type <type></span></span></td>
<td><span data-ttu-id="40251-132">L'argomento option <type> è una concatenazione a singola stringa dell'uso della risorsa come elenco di parole principale (primario) o come supplemento all'elenco di parole principale (secondario) seguito dal nome effettivo dell'elenco di parole a cui viene applicata la risorsa (ad esempio dizionario o cognome).</span><span class="sxs-lookup"><span data-stu-id="40251-132">The option argument <type> is a single-string concatenation of the resource's use as either the main word list (PRIMARY) or as a supplement to the main word list (SECONDARY) followed by the actual word list name to which the resource is applied (such as DICTIONARY or SURNAME).</span></span> <span data-ttu-id="40251-133">Di seguito sono indicati i valori possibili:</span><span class="sxs-lookup"><span data-stu-id="40251-133">The following are possible values:</span></span>
<ul>
<li><span data-ttu-id="40251-134">PRIMARY-CITYNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="40251-134">PRIMARY-CITYNAME-LIST</span></span></li>
<li><span data-ttu-id="40251-135">PRIMARY-COUNTRYNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="40251-135">PRIMARY-COUNTRYNAME-LIST</span></span></li>
<li><span data-ttu-id="40251-136">PRIMARY-COUNTRYSHORTNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="40251-136">PRIMARY-COUNTRYSHORTNAME-LIST</span></span></li>
<li><span data-ttu-id="40251-137">PRIMARY-DICTIONARY</span><span class="sxs-lookup"><span data-stu-id="40251-137">PRIMARY-DICTIONARY</span></span></li>
<li><span data-ttu-id="40251-138">PRIMARY-DATENAME-LIST</span><span class="sxs-lookup"><span data-stu-id="40251-138">PRIMARY-GIVENNAME-LIST</span></span></li>
<li><span data-ttu-id="40251-139">PRIMARY-STATEORPROVINCE-LIST</span><span class="sxs-lookup"><span data-stu-id="40251-139">PRIMARY-STATEORPROVINCE-LIST</span></span></li>
<li><span data-ttu-id="40251-140">PRIMARY-STREETNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="40251-140">PRIMARY-STREETNAME-LIST</span></span></li>
<li><span data-ttu-id="40251-141">PRIMARY-COGNOME-ELENCO</span><span class="sxs-lookup"><span data-stu-id="40251-141">PRIMARY-SURNAME-LIST</span></span></li>
<li><span data-ttu-id="40251-142">SECONDARY-CITYNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="40251-142">SECONDARY-CITYNAME-LIST</span></span></li>
<li><span data-ttu-id="40251-143">SECONDARY-COUNTRYNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="40251-143">SECONDARY-COUNTRYNAME-LIST</span></span></li>
<li><span data-ttu-id="40251-144">SECONDARY-COUNTRYSHORTNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="40251-144">SECONDARY-COUNTRYSHORTNAME-LIST</span></span></li>
<li><span data-ttu-id="40251-145">DIZIONARIO SECONDARIO</span><span class="sxs-lookup"><span data-stu-id="40251-145">SECONDARY-DICTIONARY</span></span></li>
<li><span data-ttu-id="40251-146">SECONDARY-EMAILSMTP-LIST</span><span class="sxs-lookup"><span data-stu-id="40251-146">SECONDARY-EMAILSMTP-LIST</span></span></li>
<li><span data-ttu-id="40251-147">SECONDARY-EMAILUSERNAME-LIST</span><span class="sxs-lookup"><span data-stu-id="40251-147">SECONDARY-EMAILUSERNAME-LIST</span></span></li>
<li><span data-ttu-id="40251-148">ELENCO SECONDARIO-SPECIFICATO</span><span class="sxs-lookup"><span data-stu-id="40251-148">SECONDARY-GIVENNAME-LIST</span></span></li>
<li><span data-ttu-id="40251-149">SECONDARY-STATEORPROVINCE-LIST</span><span class="sxs-lookup"><span data-stu-id="40251-149">SECONDARY-STATEORPROVINCE-LIST</span></span></li>
<li><span data-ttu-id="40251-150">SECONDARY-VIA-ELENCO</span><span class="sxs-lookup"><span data-stu-id="40251-150">SECONDARY-STREETNAME-LIST</span></span></li>
<li><span data-ttu-id="40251-151">SECONDARY-COGNOME-ELENCO</span><span class="sxs-lookup"><span data-stu-id="40251-151">SECONDARY-SURNAME-LIST</span></span></li>
<li><span data-ttu-id="40251-152">ELENCO SECONDARIO-URL</span><span class="sxs-lookup"><span data-stu-id="40251-152">SECONDARY-URL-LIST</span></span></li>
</ul>
<span data-ttu-id="40251-153">Se un valore di tipo inizia con il prefisso primario, il dizionario compilato, dopo l'installazione, sostituirà il dizionario di sistema per tale lingua.</span><span class="sxs-lookup"><span data-stu-id="40251-153">If a type value starts with the prefix PRIMARY, the compiled dictionary, after it is installed, will replace the system dictionary for that language.</span></span> <span data-ttu-id="40251-154">Il valore PRIMARY-DICTIONARY rappresenta il dizionario principale di sistema per una lingua.</span><span class="sxs-lookup"><span data-stu-id="40251-154">The value PRIMARY-DICTIONARY represents the main system dictionary for a language.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="40251-155">La sostituzione di un dizionario di sistema non esegue alcuna operazione sul contenuto del dizionario di sistema originale, perché la sostituzione è attiva solo fino a quando il dizionario personalizzato non è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="40251-155">Replacing a system dictionary does nothing to the original system dictionary content, as the replacement is in effect only until the custom dictionary has been removed.</span></span>
</blockquote>
<br/> <span data-ttu-id="40251-156">Se un valore di tipo inizia con il prefisso SECONDARY, il dizionario compilato completerà il dizionario di sistema senza sostituirlo.</span><span class="sxs-lookup"><span data-stu-id="40251-156">If a type value starts with the prefix SECONDARY, the compiled dictionary will supplement the system dictionary without replacing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40251-157">-Commento</span><span class="sxs-lookup"><span data-stu-id="40251-157">-comment</span></span> <comment></td>
<td><span data-ttu-id="40251-158">Il commento specificato viene compilato nel file del dizionario.</span><span class="sxs-lookup"><span data-stu-id="40251-158">The specified comment is compiled into the dictionary file.</span></span> <span data-ttu-id="40251-159">Il commento deve essere una singola stringa e non più di 64 caratteri.</span><span class="sxs-lookup"><span data-stu-id="40251-159">The comment must be a single string and no longer than 64 characters.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40251-160">-o <dictfile.hwrdict></span><span class="sxs-lookup"><span data-stu-id="40251-160">-o <dictfile.hwrdict></span></span></td>
<td><span data-ttu-id="40251-161">L'output viene scritto nel nome file specificato da <dictfile.hwrdict> .</span><span class="sxs-lookup"><span data-stu-id="40251-161">Output is written to the file name specified by <dictfile.hwrdict>.</span></span><br/> <span data-ttu-id="40251-162">Se questa opzione è mancante, il nome del file di output viene derivato dal nome del file di input originale, con l'estensione del file di input sostituita da. hwrdict.</span><span class="sxs-lookup"><span data-stu-id="40251-162">If this option is missing, the output file name is derived from the original input file name, with the input file extension replaced by .hwrdict.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="defaults"></a><span data-ttu-id="40251-163">Valori predefiniti</span><span class="sxs-lookup"><span data-stu-id="40251-163">Defaults</span></span>

<span data-ttu-id="40251-164">Se non viene specificato alcun parametro, i valori predefiniti dell'opzione sono</span><span class="sxs-lookup"><span data-stu-id="40251-164">If no parameters are specified, the default option values are</span></span>

<span data-ttu-id="40251-165">-lang <current input language> -Type-dizionario secondario</span><span class="sxs-lookup"><span data-stu-id="40251-165">-lang <current input language> -type SECONDARY-DICTIONARY</span></span>

### <a name="examples"></a><span data-ttu-id="40251-166">Esempio</span><span class="sxs-lookup"><span data-stu-id="40251-166">Examples</span></span>

<span data-ttu-id="40251-167">Il codice seguente compila il file di input mylist1.txt, applica i valori di opzione predefiniti e crea il file di output mylist1. hwrdict.</span><span class="sxs-lookup"><span data-stu-id="40251-167">The following compiles the input file mylist1.txt, applies the default option values, and creates the output file mylist1.hwrdict.</span></span>

``` syntax
hwrcomp mylist1.txt
```

<span data-ttu-id="40251-168">Il codice seguente, invece, compila mylist1.txt in myrsrc1. hwrdict, ma assegna "English (US)" (en-US) come Language e SECONDARY-DICTIONARY come tipo.</span><span class="sxs-lookup"><span data-stu-id="40251-168">In contrast, the following compiles mylist1.txt into myrsrc1.hwrdict, but assigns "English (US)" (en-US) as the language and SECONDARY-DICTIONARY as the type.</span></span>

``` syntax
hwrcomp -lang en-US -type SECONDARY-DICTIONARY -o myrsrc1 mylist1.txt 
```

## <a name="installing-a-compiled-custom-dictionary"></a><span data-ttu-id="40251-169">Installazione di un dizionario personalizzato compilato</span><span class="sxs-lookup"><span data-stu-id="40251-169">Installing a Compiled Custom Dictionary</span></span>

<span data-ttu-id="40251-170">HwrComp.exe crea un file con estensione hwrdict, che è in un formato binario utilizzabile da un riconoscimento della grafia.</span><span class="sxs-lookup"><span data-stu-id="40251-170">HwrComp.exe creates a .hwrdict file, which is in a binary format usable by a handwriting recognizer.</span></span> <span data-ttu-id="40251-171">Questo file può essere installato in qualsiasi computer che esegue Windows 7 o Windows Server 2008 R2 che supporta il riconoscimento della grafia.</span><span class="sxs-lookup"><span data-stu-id="40251-171">This file can be installed on any computer running Windows 7 or Windows Server 2008 R2 that supports handwriting recognition.</span></span> <span data-ttu-id="40251-172">Un dizionario viene installato solo per l'utente corrente o per tutti gli utenti di un computer.</span><span class="sxs-lookup"><span data-stu-id="40251-172">A dictionary is installed either for just the current user or for all users on a machine.</span></span>

<span data-ttu-id="40251-173">Un file di dizionario personalizzato compilato può essere installato dalla riga di comando utilizzando lo strumento HwrReg.exe.</span><span class="sxs-lookup"><span data-stu-id="40251-173">A compiled custom dictionary file can be installed from the command line using the tool HwrReg.exe.</span></span> <span data-ttu-id="40251-174">Questo strumento è utile se si desidera eseguire l'override di alcuni valori di configurazione che vengono compilati nel file o sono i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="40251-174">This tool is useful if you wish to override some of the configuration values that either are compiled into the file or are the default values.</span></span> <span data-ttu-id="40251-175">Esistono due modi per eseguire HwrReg.exe: in modalità di controllo/installazione e in modalità elenco/rimozione.</span><span class="sxs-lookup"><span data-stu-id="40251-175">There are two ways to run HwrReg.exe: in check/install mode and in list/remove mode.</span></span>

### <a name="running-hwrregexe-in-checkinstall-mode"></a><span data-ttu-id="40251-176">Esecuzione di HwrReg.exe in modalità di controllo/installazione</span><span class="sxs-lookup"><span data-stu-id="40251-176">Running HwrReg.exe in Check/Install Mode</span></span>

<span data-ttu-id="40251-177">Questa modalità è per i file di dizionario personalizzati che non sono stati ancora installati.</span><span class="sxs-lookup"><span data-stu-id="40251-177">This mode is for custom dictionary files that have not yet been installed.</span></span> <span data-ttu-id="40251-178">Di seguito viene illustrata la sintassi di utilizzo per le opzioni della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="40251-178">The following shows the usage syntax for the command-line options.</span></span>

``` syntax
Usage: hwrreg        [-check]
    [-lang <localename>] 
    [-scope {all|me}]
    [-noprompt] 
    <dictfile.hwrdict>
```

### <a name="explanation-of-options"></a><span data-ttu-id="40251-179">Spiegazione delle opzioni</span><span class="sxs-lookup"><span data-stu-id="40251-179">Explanation of Options</span></span>



| <span data-ttu-id="40251-180">Parametro</span><span class="sxs-lookup"><span data-stu-id="40251-180">Parameter</span></span>                | <span data-ttu-id="40251-181">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40251-181">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40251-182">-controllo</span><span class="sxs-lookup"><span data-stu-id="40251-182">-check</span></span>                   | <span data-ttu-id="40251-183">Il file del dizionario viene verificato senza essere installato.</span><span class="sxs-lookup"><span data-stu-id="40251-183">The dictionary file is verified without being installed.</span></span> <span data-ttu-id="40251-184">L'opzione check Visualizza il commento del file, più le informazioni di registrazione che verrebbero usate per installare il file.</span><span class="sxs-lookup"><span data-stu-id="40251-184">The  check option displays the file's comment, plus the registration information that would be used to install the file.</span></span> <span data-ttu-id="40251-185">Questa opzione è utile per verificare le informazioni di registrazione prima di eseguire l'installazione.</span><span class="sxs-lookup"><span data-stu-id="40251-185">This option is useful for verifying registration information before the installation is performed.</span></span> <br/> <span data-ttu-id="40251-186">Se questa opzione è mancante, HwrReg.exe installa il dizionario personalizzato.</span><span class="sxs-lookup"><span data-stu-id="40251-186">If this option is missing, HwrReg.exe installs the custom dictionary.</span></span><br/>  |
|  <span data-ttu-id="40251-187">lang <localename></span><span class="sxs-lookup"><span data-stu-id="40251-187">lang <localename></span></span> | <span data-ttu-id="40251-188">Il file del dizionario viene verificato senza essere installato.</span><span class="sxs-lookup"><span data-stu-id="40251-188">The dictionary file is verified without being installed.</span></span> <span data-ttu-id="40251-189">L'opzione check Visualizza il commento del file, più le informazioni di registrazione che verrebbero usate per installare il file.</span><span class="sxs-lookup"><span data-stu-id="40251-189">The  check option displays the file's comment, plus the registration information that would be used to install the file.</span></span> <span data-ttu-id="40251-190">Questa opzione è utile per verificare le informazioni di registrazione prima di eseguire l'installazione.</span><span class="sxs-lookup"><span data-stu-id="40251-190">This option is useful for verifying registration information before the installation is performed.</span></span> <br/> <span data-ttu-id="40251-191">Se questa opzione è mancante, HwrReg.exe installa il dizionario personalizzato.</span><span class="sxs-lookup"><span data-stu-id="40251-191">If this option is missing, HwrReg.exe installs the custom dictionary.</span></span> <br/> |
|  <span data-ttu-id="40251-192">ambito {All \| me}</span><span class="sxs-lookup"><span data-stu-id="40251-192">scope {all\|me}</span></span>         | <span data-ttu-id="40251-193">Il dizionario personalizzato è installato per tutti gli utenti (ambito tutti) o solo per l'utente corrente (ambito me).</span><span class="sxs-lookup"><span data-stu-id="40251-193">The custom dictionary is installed either for all users ( scope all) or for just the current user ( scope me).</span></span> <span data-ttu-id="40251-194">Per l'installazione di con ambito, è necessario che il comando venga eseguito in un prompt dei comandi con privilegi elevati. in caso contrario, verrà restituito un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="40251-194">Installing with  scope all requires the command to be run in an elevated command prompt; otherwise, an error code will be returned.</span></span> <br/> <span data-ttu-id="40251-195">Se questa opzione non è presente, l'ambito dell'installazione è solo l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="40251-195">If this option is missing, the installation is scoped to just the current user.</span></span><br/>                          |
|  <span data-ttu-id="40251-196">noprompt</span><span class="sxs-lookup"><span data-stu-id="40251-196">noprompt</span></span>                | <span data-ttu-id="40251-197">HwrReg.exe non richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="40251-197">HwrReg.exe does not prompt for confirmation.</span></span> <span data-ttu-id="40251-198">Questa operazione può essere utile quando si esegue hwrReg.exe da uno script.</span><span class="sxs-lookup"><span data-stu-id="40251-198">This can be useful when running hwrReg.exe from a script.</span></span> <br/>                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="40251-199">Nell'esempio seguente viene installato il dizionario personalizzato myrsrc1. hwrdict per la lingua "danese (Danimarca)" (da DK), con l'ambito predefinito solo dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="40251-199">The following example installs the custom dictionary myrsrc1.hwrdict for language "Danish (Denmark)" (da DK), with the default scope of just the current user.</span></span>

``` syntax
hwrreg -lang da-DK myrsrc1.hwrdict 
```

### <a name="running-hwrregexe-in-listremove-mode"></a><span data-ttu-id="40251-200">Esecuzione di HwrReg.exe in modalità elenco/rimozione</span><span class="sxs-lookup"><span data-stu-id="40251-200">Running HwrReg.exe in List/Remove Mode</span></span>

<span data-ttu-id="40251-201">In questa modalità è possibile elencare o rimuovere i dizionari personalizzati installati.</span><span class="sxs-lookup"><span data-stu-id="40251-201">This mode either lists or removes installed custom dictionaries.</span></span> <span data-ttu-id="40251-202">Di seguito viene illustrata la sintassi di utilizzo per le opzioni della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="40251-202">The following shows the usage syntax for the command-line options.</span></span>

``` syntax
Usage: hwrreg        [-lang <localename>] 
    [-scope {all|me}] 
    [-type <type>]
    -list | -remove
```

### <a name="explanation-of-options"></a><span data-ttu-id="40251-203">Spiegazione delle opzioni</span><span class="sxs-lookup"><span data-stu-id="40251-203">Explanation of Options</span></span>



| <span data-ttu-id="40251-204">Parametro</span><span class="sxs-lookup"><span data-stu-id="40251-204">Parameter</span></span>                | <span data-ttu-id="40251-205">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40251-205">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <span data-ttu-id="40251-206">lang <localename></span><span class="sxs-lookup"><span data-stu-id="40251-206">lang <localename></span></span> | <span data-ttu-id="40251-207">I dizionari registrati solo per questo nome delle impostazioni locali vengono elencati o rimossi.</span><span class="sxs-lookup"><span data-stu-id="40251-207">The dictionaries registered for only this locale name are listed or removed.</span></span> <span data-ttu-id="40251-208">L'argomento <localename> ha l'area della lingua del modulo.</span><span class="sxs-lookup"><span data-stu-id="40251-208">The argument <localename> has the form language REGION.</span></span> <span data-ttu-id="40251-209">Per esempi di questo formato, vedere [costanti e stringhe degli identificatori di lingua](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="40251-209">For examples of this form, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span> <br/> <span data-ttu-id="40251-210">Se questa opzione è mancante, i dizionari per tutte le lingue vengono elencati o rimossi.</span><span class="sxs-lookup"><span data-stu-id="40251-210">If this option is missing, dictionaries for all languages are listed or removed.</span></span><br/> |
|  <span data-ttu-id="40251-211">ambito {All \| me}</span><span class="sxs-lookup"><span data-stu-id="40251-211">scope {all\|me}</span></span>         | <span data-ttu-id="40251-212">Il dizionario personalizzato è installato per tutti gli utenti (ambito tutti) o solo per l'utente corrente (ambito me).</span><span class="sxs-lookup"><span data-stu-id="40251-212">The custom dictionary is installed either for all users ( scope all) or for just the current user ( scope me).</span></span> <span data-ttu-id="40251-213">Per l'installazione di con ambito, è necessario che il comando venga eseguito in un prompt dei comandi con privilegi elevati. in caso contrario, verrà restituito un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="40251-213">Installing with  scope all requires the command to be run in an elevated command prompt; otherwise, an error code will be returned.</span></span> <br/> <span data-ttu-id="40251-214">Se questa opzione non è presente, l'ambito dell'installazione è solo l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="40251-214">If this option is missing, the installation is scoped to just the current user.</span></span><br/>                      |
|  <span data-ttu-id="40251-215">tipo <type></span><span class="sxs-lookup"><span data-stu-id="40251-215">type <type></span></span>       | <span data-ttu-id="40251-216">Elenca o rimuove solo i dizionari registrati con il tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="40251-216">Lists or removes only dictionaries that are registered with the specified type.</span></span><br/> <span data-ttu-id="40251-217">Se questa opzione è mancante, tutti i tipi di dizionario vengono elencati o rimossi.</span><span class="sxs-lookup"><span data-stu-id="40251-217">If this option is missing, all dictionary types are listed or removed.</span></span> <span data-ttu-id="40251-218">L'installazione o la rimozione di un dizionario personalizzato di un altro tipo, ad esempio PRIMARY-COUNTRYname-LIST, può influire sul riconoscimento della grafia in altri contesti.</span><span class="sxs-lookup"><span data-stu-id="40251-218">Installing or removing a custom dictionary of another type (such as PRIMARY-COUNTRYNAME-LIST) may affect handwriting recognition in other contexts.</span></span> <br/>                                              |
|  <span data-ttu-id="40251-219">list</span><span class="sxs-lookup"><span data-stu-id="40251-219">list</span></span>                    | <span data-ttu-id="40251-220">Elenca tutti i dizionari installati che corrispondono alle altre opzioni.</span><span class="sxs-lookup"><span data-stu-id="40251-220">Lists all installed dictionaries that match the other options.</span></span><br/> <span data-ttu-id="40251-221">Se questa opzione è mancante, è necessario specificare l'opzione Remove.</span><span class="sxs-lookup"><span data-stu-id="40251-221">If this option is missing, the option  remove must be specified.</span></span><br/>                                                                                                                                                                                                                          |
|  <span data-ttu-id="40251-222">remove</span><span class="sxs-lookup"><span data-stu-id="40251-222">remove</span></span>                  | <span data-ttu-id="40251-223">Richiede la rimozione di qualsiasi dizionario corrispondente alle altre opzioni.</span><span class="sxs-lookup"><span data-stu-id="40251-223">Prompts for removal of any dictionary that matches the other options.</span></span><br/> <span data-ttu-id="40251-224">Se questa opzione è mancante, è necessario specificare l'elenco di opzioni.</span><span class="sxs-lookup"><span data-stu-id="40251-224">If this option is missing, the option  list must be specified.</span></span><br/>                                                                                                                                                                                                                     |



 

### <a name="examples"></a><span data-ttu-id="40251-225">Esempio</span><span class="sxs-lookup"><span data-stu-id="40251-225">Examples</span></span>

<span data-ttu-id="40251-226">Di seguito sono elencati i dizionari con lingua "inglese (Stati Uniti)" (en US) e tipo dizionario primario e installati solo per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="40251-226">The following lists dictionaries that have language "English (US)" (en US) and type PRIMARY DICTIONARY and that are installed for just the current user.</span></span>

``` syntax
hwrreg -list -lang en-US -type PRIMARY-DICTIONARY
                  
```

<span data-ttu-id="40251-227">Analogamente, di seguito vengono rimossi i dizionari che corrispondono agli stessi criteri.</span><span class="sxs-lookup"><span data-stu-id="40251-227">Similarly, the following removes dictionaries that match the same criteria.</span></span>

``` syntax
hwrreg -remove -lang en-US -type PRIMARY-DICTIONARY
                  
```

## <a name="general-notes-on-custom-dictionaries"></a><span data-ttu-id="40251-228">Note generali sui dizionari personalizzati</span><span class="sxs-lookup"><span data-stu-id="40251-228">General Notes on Custom Dictionaries</span></span>

-   <span data-ttu-id="40251-229">Se si installano due dizionari personalizzati con lo stesso tipo, lingua e ambito, la seconda operazione sovrascriverà la prima.</span><span class="sxs-lookup"><span data-stu-id="40251-229">If you install two custom dictionaries that have the same type, language, and scope, the second installation will overwrite the first.</span></span>
-   <span data-ttu-id="40251-230">Se si installano due dizionari personalizzati con lo stesso tipo e la stessa lingua, ma con ambiti diversi (uno per tutti gli utenti e uno per l'utente corrente), il dizionario installato per l'utente corrente ha la precedenza e il dizionario installato per tutti gli utenti viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="40251-230">If you install two custom dictionaries with the same type and language, but with different scopes (one for all users, and one for the current user), the dictionary installed for the current user takes precedence, and the dictionary installed for all users is ignored.</span></span>

 

