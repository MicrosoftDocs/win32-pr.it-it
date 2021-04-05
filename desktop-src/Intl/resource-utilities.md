---
description: In questo argomento vengono descritte due utilità utilizzate per compilare applicazioni MUI.
ms.assetid: 8ba94001-fc46-41e0-a071-0dc500a20753
title: Utilità per le risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550cf283779a57bc5ca35f88d336646b061c3f1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968106"
---
# <a name="resource-utilities"></a><span data-ttu-id="5540e-103">Utilità per le risorse</span><span class="sxs-lookup"><span data-stu-id="5540e-103">Resource Utilities</span></span>

<span data-ttu-id="5540e-104">In questo argomento vengono descritte due utilità utilizzate per compilare applicazioni MUI.</span><span class="sxs-lookup"><span data-stu-id="5540e-104">This topic describes two utilities used to build MUI applications.</span></span> <span data-ttu-id="5540e-105">Mentre MUIRCT è uno strumento specifico di MUI, MUI usa anche l'utilità del compilatore Windows RC standard.</span><span class="sxs-lookup"><span data-stu-id="5540e-105">While MUIRCT is a MUI-specific tool, MUI also makes use of the standard Windows RC Compiler utility.</span></span> <span data-ttu-id="5540e-106">Le istruzioni per l'uso di queste utilità sono fornite in [localizzazione delle risorse e compilazione dell'applicazione](localizing-resources-and-building-the-application.md).</span><span class="sxs-lookup"><span data-stu-id="5540e-106">Instructions for using these utilities are provided in [Localizing Resources and Building the Application](localizing-resources-and-building-the-application.md).</span></span>

## <a name="muirct-utility"></a><span data-ttu-id="5540e-107">Utilità MUIRCT</span><span class="sxs-lookup"><span data-stu-id="5540e-107">MUIRCT Utility</span></span>

<span data-ttu-id="5540e-108">MUIRCT (Muirct.exe) è un'utilità della riga di comando per suddividere un file eseguibile standard in un file di risorse e file di risorse specifici della lingua, ovvero localizzabili.</span><span class="sxs-lookup"><span data-stu-id="5540e-108">MUIRCT (Muirct.exe) is a command line utility for splitting a standard executable file into an LN file and language-specific (that is, localizable) resource files.</span></span> <span data-ttu-id="5540e-109">Ognuno dei file risultanti contiene i dati di configurazione delle risorse per l'associazione di file.</span><span class="sxs-lookup"><span data-stu-id="5540e-109">Each of the resulting files contains resource configuration data for file association.</span></span> <span data-ttu-id="5540e-110">MUIRCT è incluso nel Microsoft Windows SDK per Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5540e-110">MUIRCT is included in the Microsoft Windows SDK for Windows Vista.</span></span>

> [!Note]  
> <span data-ttu-id="5540e-111">A partire da Windows Vista, il caricatore di risorse Win32 viene aggiornato per caricare le risorse da file specifici della lingua, oltre che da un file.</span><span class="sxs-lookup"><span data-stu-id="5540e-111">Starting with Windows Vista, the Win32 resource loader is updated to load resources from language-specific files as well as from LN files.</span></span>

 

### <a name="muirct-usages"></a><span data-ttu-id="5540e-112">Utilizzi MUIRCT</span><span class="sxs-lookup"><span data-stu-id="5540e-112">MUIRCT Usages</span></span>

1.  <span data-ttu-id="5540e-113">Suddividere il binario in un file binario e MUI principale basato sul \_ file di configurazione RC.</span><span class="sxs-lookup"><span data-stu-id="5540e-113">Split binary into main binary and mui file based on rc\_config file.</span></span>

    `Muirct -q rc_config [-c checksum_file [-b LangID]] [-x LangID] [-g LangId]     [-f] [-m] [-v level] source_file [output_LN_file] [output_MUI_file]`

2.  <span data-ttu-id="5540e-114">Estrarre checksum dal file di checksum \_ e inserirlo nel file di output \_ .</span><span class="sxs-lookup"><span data-stu-id="5540e-114">Extract checksum from checksum\_file and insert it in output\_file.</span></span>

    `Muirct -c checksum_file [-b LangID] -e output_file`

3.  <span data-ttu-id="5540e-115">Calcolare il checksum in base al \_ file di checksum e inserirlo nel file di output \_ .</span><span class="sxs-lookup"><span data-stu-id="5540e-115">Calculate checksum based on checksum\_file and insert it in output\_file.</span></span>

    `Muirct  -c checksum_file [-b LangID] -q rc_config  -z output_file`

4.  <span data-ttu-id="5540e-116">Dump del contenuto dei dati di configurazione delle risorse dal file di input \_ .</span><span class="sxs-lookup"><span data-stu-id="5540e-116">Dump resource configuration data contents from input\_file.</span></span>

    `Muirct -d input_file`

### <a name="muirct-syntax"></a><span data-ttu-id="5540e-117">Sintassi di MUIRCT</span><span class="sxs-lookup"><span data-stu-id="5540e-117">MUIRCT Syntax</span></span>

<span data-ttu-id="5540e-118">MUIRCT può assumere la direzione dalle opzioni della riga di comando e/o da un file di configurazione delle risorse, specificato con l'opzione-q.</span><span class="sxs-lookup"><span data-stu-id="5540e-118">MUIRCT can take direction from command line switches and/or from a resource configuration file, specified using the -q switch.</span></span>


```C++
muirct [-h|-?] [ -c checksum_file] [-b langid]  ]
     [-g langid] [-q resource configuration file<RCF>] [-v level] [-x langid]
     [-e output_file]  [-z output_file] [-f] [-d MUI'ized file] [-m file_version]

source_filename [language_neutral_filename] [mui_filename]
```



<span data-ttu-id="5540e-119">**Opzioni e argomenti**</span><span class="sxs-lookup"><span data-stu-id="5540e-119">**Switches and Arguments**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5540e-120">-h |-?</span><span class="sxs-lookup"><span data-stu-id="5540e-120">-h|-?</span></span></td>
<td><span data-ttu-id="5540e-121">Mostra la schermata della guida.</span><span class="sxs-lookup"><span data-stu-id="5540e-121">Shows help screen.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5540e-122">-c</span><span class="sxs-lookup"><span data-stu-id="5540e-122">-c</span></span></td>
<td><span data-ttu-id="5540e-123">Specifica il checksum_file di input da cui estrarre o calcolare il checksum della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5540e-123">Specifies the input checksum_file from which to extract or calculate the resource checksum.</span></span> <span data-ttu-id="5540e-124">Checksum_file deve essere un file binario Win32 contenente le risorse localizzabili.</span><span class="sxs-lookup"><span data-stu-id="5540e-124">Checksum_file must be a Win32 binary file containing localizable resources.</span></span> <span data-ttu-id="5540e-125">Se checksum_file contiene risorse per più di un linguaggio, è necessario usare l'opzione-b per specificare quali di queste devono essere usate in caso contrario MUIRCT ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="5540e-125">If checksum_file contains resources for more than one language, the -b switch must be used to specify which of these should be used otherwise MUIRCT fails.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5540e-126">-b</span><span class="sxs-lookup"><span data-stu-id="5540e-126">-b</span></span></td>
<td><span data-ttu-id="5540e-127">Specifica la lingua da utilizzare quando il checksum_file specificato con-c contiene risorse in più lingue.</span><span class="sxs-lookup"><span data-stu-id="5540e-127">Specifies the language to be used when the checksum_file specified with -c contains resources in multiple languages.</span></span> <span data-ttu-id="5540e-128">Questa opzione può essere usata solo in combinazione con l'opzione-c.</span><span class="sxs-lookup"><span data-stu-id="5540e-128">This switch can only be used in conjunction with the -c switch.</span></span> <span data-ttu-id="5540e-129">L'identificatore della lingua può essere in formato decimale o esadecimale.</span><span class="sxs-lookup"><span data-stu-id="5540e-129">The language identifier can be in decimal or hexadecimal format.</span></span> <span data-ttu-id="5540e-130">MUIRCT ha esito negativo se il checksum_file contiene risorse in più lingue e il parametro-b non è specificato o se la lingua specificata dall'opzione-b non è stata trovata nel checksum_file.</span><span class="sxs-lookup"><span data-stu-id="5540e-130">MUIRCT fails if the checksum_file contains resources in multiple language and the -b is not specified or if the language specified by the -b switch cannot be found in the checksum_file.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5540e-131">-g</span><span class="sxs-lookup"><span data-stu-id="5540e-131">-g</span></span></td>
<td><span data-ttu-id="5540e-132">Specifica l'ID lingua da includere come lingua di fallback finale nella sezione dati di configurazione delle risorse del file LN.</span><span class="sxs-lookup"><span data-stu-id="5540e-132">Specifies the language ID to be included as the ultimate fallback language in the resource configuration data section of the LN file.</span></span> <span data-ttu-id="5540e-133">Se il caricatore di risorse non riesce a caricare un file con estensione MUI richiesto dalle lingue dell'interfaccia utente preferita dal thread, usa la lingua di fallback finale come ultimo tentativo.</span><span class="sxs-lookup"><span data-stu-id="5540e-133">If the resource loader fails to load a requested .mui file from the thread preferred UI languages, it uses the ultimate fallback language as its last attempt.</span></span> <span data-ttu-id="5540e-134">Il valore LangID può essere specificato in formato decimale o esadecimale.</span><span class="sxs-lookup"><span data-stu-id="5540e-134">The LangID value can be specified in decimal or hexadecimal format.</span></span> <span data-ttu-id="5540e-135">Ad esempio, la lingua inglese (Stati Uniti) può essere specificata da-g 0x409 o-g 1033.</span><span class="sxs-lookup"><span data-stu-id="5540e-135">For example English (United States) can be specified by -g 0x409 or -g 1033.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5540e-136">-Q</span><span class="sxs-lookup"><span data-stu-id="5540e-136">-q</span></span></td>
<td><span data-ttu-id="5540e-137">Specifica che il source_file deve essere suddiviso nel output_LN_file e output_MUI_file in base al layout del file rc_config.</span><span class="sxs-lookup"><span data-stu-id="5540e-137">Specifies that the source_file is to be split into the output_LN_file and the output_MUI_file according to the rc_config file layout.</span></span> <span data-ttu-id="5540e-138">Il file di rc_config è un file in formato XML che specifica le risorse che verranno estratte nel file con estensione MUI e che verranno lasciate nel file in.</span><span class="sxs-lookup"><span data-stu-id="5540e-138">The rc_config file is an XML formatted file that specifies which resources will be extracted to the .mui file and which will be left in the LN file.</span></span> <span data-ttu-id="5540e-139">Il rc_config può specificare la distribuzione dei tipi di risorse e dei singoli elementi denominati tra i output_LN_file e output_MUI_file.</span><span class="sxs-lookup"><span data-stu-id="5540e-139">The rc_config can specify the distribution of resource types and individual named items between the output_LN_file and output_MUI_file.</span></span> <span data-ttu-id="5540e-140">Il source_file deve essere un file binario Win32 che contiene risorse in una sola lingua. in caso contrario MUIRCT avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="5540e-140">The source_file must be a Win32 binary that contains resources in a single language otherwise MUIRCT fails.</span></span> <span data-ttu-id="5540e-141">MUIRCT non suddivide il file se è indipendente dalla lingua, a indicare che nel file è presente solo l'ID lingua valore 0.</span><span class="sxs-lookup"><span data-stu-id="5540e-141">MUIRCT does not split the file if it is language neutral which is indicated by having only language ID value 0 in the file.</span></span> <span data-ttu-id="5540e-142">I output_LN_file e output_mui_file sono i nomi del file con estensione MUI e indipendente dalla lingua in cui è suddiviso il source_file.</span><span class="sxs-lookup"><span data-stu-id="5540e-142">The output_LN_file and output_mui_file are the names of the language neutral and .mui file into which the source_file is split.</span></span> <span data-ttu-id="5540e-143">Questi nomi di file sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="5540e-143">These file names are optional.</span></span> <span data-ttu-id="5540e-144">Se non vengono specificati, MUIRCT aggiunge le estensioni. LN e. mui a source_file.</span><span class="sxs-lookup"><span data-stu-id="5540e-144">If they are not specified, MUIRCT appends the extensions .ln and .mui to source_file.</span></span> <span data-ttu-id="5540e-145">In genere è consigliabile rimuovere l' &quot; estensione. LN &quot; prima di distribuire il file.</span><span class="sxs-lookup"><span data-stu-id="5540e-145">Typically you should remove the &quot;.ln&quot; extension before deploying the file.</span></span> <span data-ttu-id="5540e-146">MUIRCT associa il output_LN_file e output_MUI_file calcolando un checksum basato sul nome source_file e la versione del file e inserendo il risultato nella sezione di configurazione della risorsa di ogni file di output.</span><span class="sxs-lookup"><span data-stu-id="5540e-146">MUIRCT associates the output_LN_file and output_MUI_file by calculating a checksum based on the source_file name and file version and inserting the result into the resource configuration section of each output file.</span></span> <span data-ttu-id="5540e-147">Se usato in combinazione con l'opzione-c, l'opzione-q avrà la precedenza.</span><span class="sxs-lookup"><span data-stu-id="5540e-147">When used in conjunction with the -c switch, the -q switch takes precedence.</span></span> <span data-ttu-id="5540e-148">Se il file rc_config fornito con l'opzione-q contiene un checksum MUIRCT ignora l'opzione-c e inserisce il valore di checksum dal valore, rc_config file nei file LN e. mui.</span><span class="sxs-lookup"><span data-stu-id="5540e-148">If the rc_config file supplied with the -q switch contains a checksum MUIRCT ignores the -c switch and inserts the checksum value from the value, rc_config file into the LN and.mui files.</span></span> <span data-ttu-id="5540e-149">Se non viene trovato alcun valore di checksum nella rc_config, MUIRCT calcola il checksum della risorsa in base al comportamento dell'opzione-c.</span><span class="sxs-lookup"><span data-stu-id="5540e-149">If no checksum value is found in the rc_config, MUIRCT calculates the resource checksum based on the behavior of the -c switch.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5540e-150">-v</span><span class="sxs-lookup"><span data-stu-id="5540e-150">-v</span></span></td>
<td><span data-ttu-id="5540e-151">Specifica il livello di maggiori per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="5540e-151">Specifies the level of verboseness for logging.</span></span> <span data-ttu-id="5540e-152">Specificare 1 per stampare tutti i messaggi di errore di base e i risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5540e-152">Specify 1 to print all basic error messages and operation results.</span></span> <span data-ttu-id="5540e-153">Specificare 2 per includere anche le informazioni sulle risorse (tipo, nome, identificatore della lingua) incluse nel file con estensione MUI e nel file.</span><span class="sxs-lookup"><span data-stu-id="5540e-153">Specify 2 to also include the resource information (type, name, language identifier) included in the .mui file and LN file.</span></span> <span data-ttu-id="5540e-154">Il valore predefinito è-v 1</span><span class="sxs-lookup"><span data-stu-id="5540e-154">The default is -v 1</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5540e-155">-X</span><span class="sxs-lookup"><span data-stu-id="5540e-155">-x</span></span></td>
<td><span data-ttu-id="5540e-156">Specifica l'ID lingua con cui MUIRCT contrassegna tutti i tipi di risorsa aggiunti alla sezione delle risorse del file con estensione MUI.</span><span class="sxs-lookup"><span data-stu-id="5540e-156">Specifies the language ID with which MUIRCT marks all resource types added to the resource section of the .mui file.</span></span> <span data-ttu-id="5540e-157">Il valore LangID può essere specificato in formato decimale o esadecimale.</span><span class="sxs-lookup"><span data-stu-id="5540e-157">The LangID value can be specified in decimal or hexadecimal format.</span></span> <span data-ttu-id="5540e-158">Ad esempio, la lingua inglese (Stati Uniti) può essere specificata da-x 0x409 o-x 1033.</span><span class="sxs-lookup"><span data-stu-id="5540e-158">For example English (United States) can be specified by -x 0x409 or -x 1033.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5540e-159">-E</span><span class="sxs-lookup"><span data-stu-id="5540e-159">-e</span></span></td>
<td><span data-ttu-id="5540e-160">Estrae il checksum della risorsa contenuto nell'checksum_file fornito con l'opzione-c e lo inserisce nella output_file specificata.</span><span class="sxs-lookup"><span data-stu-id="5540e-160">Extracts the resource checksum contained in the checksum_file provided with the -c switch and inserts it in the specified output_file.</span></span> <span data-ttu-id="5540e-161">Quando si specifica-e, MUIRCT ignora tutte le opzioni diverse dall'opzione-c.</span><span class="sxs-lookup"><span data-stu-id="5540e-161">When -e is specified, MUIRCT ignores all switches other than the -c switch.</span></span> <span data-ttu-id="5540e-162">In questo caso il checksum_file deve essere un file binario Win32 che contiene una sezione di dati di configurazione delle risorse con un valore di checksum.</span><span class="sxs-lookup"><span data-stu-id="5540e-162">In this case the checksum_file must be a Win32 binary file that contains a resource configuration data section with a checksum value.</span></span> <span data-ttu-id="5540e-163">Il output_file deve essere un file esistente o MUI.</span><span class="sxs-lookup"><span data-stu-id="5540e-163">The output_file must be an existing LN file or .mui file.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5540e-164">-Z</span><span class="sxs-lookup"><span data-stu-id="5540e-164">-z</span></span></td>
<td><span data-ttu-id="5540e-165">Calcola e inserisce i dati di checksum delle risorse nel file di output specificato.</span><span class="sxs-lookup"><span data-stu-id="5540e-165">Calculates and inserts resource checksum data in the specified output file.</span></span> <span data-ttu-id="5540e-166">MUIRCT basa il calcolo del checksum sull'input fornito con l'opzione-c e l'opzione facoltativa-b.</span><span class="sxs-lookup"><span data-stu-id="5540e-166">MUIRCT bases checksum calculation on the input provided with the -c switch, and the optional -b switch.</span></span> <span data-ttu-id="5540e-167">Se si specifica un file di output per l'opzione-z che non esiste, MUIRCT si chiude con un errore.</span><span class="sxs-lookup"><span data-stu-id="5540e-167">If you specify an output file for the -z switch that does not exist, MUIRCT exits with a failure.</span></span><br/> <span data-ttu-id="5540e-168">Esempio: calcola il checksum basato sulle risorse localizzabili in Notepad.exe e inserisce il checksum nel file di output Notepad2.exe.</span><span class="sxs-lookup"><span data-stu-id="5540e-168">Example: Calculates the checksum based on localizable resources in Notepad.exe and inserts the checksum into the output file Notepad2.exe.</span></span><br/> <code>muirct -c notepad.exe -q myprog.rcconfig -z notepad2.exe</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5540e-169">-f</span><span class="sxs-lookup"><span data-stu-id="5540e-169">-f</span></span></td>
<td><span data-ttu-id="5540e-170">Consente la creazione di un file con estensione MUI con la risorsa di versione come unica risorsa localizzabile.</span><span class="sxs-lookup"><span data-stu-id="5540e-170">Enables creating a .mui file with the version resource being the only localizable resource.</span></span> <span data-ttu-id="5540e-171">Per impostazione predefinita, MUIRCT non consente questa operazione.</span><span class="sxs-lookup"><span data-stu-id="5540e-171">By default, MUIRCT does not allow this.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5540e-172">-d</span><span class="sxs-lookup"><span data-stu-id="5540e-172">-d</span></span></td>
<td><span data-ttu-id="5540e-173">Individua e Visualizza i dati di configurazione delle risorse incorporati nel file di origine.</span><span class="sxs-lookup"><span data-stu-id="5540e-173">Locates and displays embedded resource configuration data in the source file.</span></span> <span data-ttu-id="5540e-174">Quando si specifica questa opzione, MUIRCT ignora tutte le altre opzioni della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="5540e-174">When you specify this switch, MUIRCT ignores all other command line options.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5540e-175">-M</span><span class="sxs-lookup"><span data-stu-id="5540e-175">-m</span></span></td>
<td><span data-ttu-id="5540e-176">Specifica il numero di versione da usare per il calcolo del checksum per l'associazione dei output_LN_file e output_MUI_file.</span><span class="sxs-lookup"><span data-stu-id="5540e-176">Specifies the version number to use when calculating the checksum for associating the output_LN_file and output_MUI_file.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5540e-177">source_filename</span><span class="sxs-lookup"><span data-stu-id="5540e-177">source_filename</span></span></td>
<td><span data-ttu-id="5540e-178">Nome del file di origine binario localizzato; non è possibile usare i caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="5540e-178">Name of the localized binary source file; wildcards cannot be used.</span></span> <span data-ttu-id="5540e-179">Questo file può contenere solo risorse in una lingua.</span><span class="sxs-lookup"><span data-stu-id="5540e-179">This file can only contain resources in one language.</span></span> <span data-ttu-id="5540e-180">Se nel file sono presenti risorse in più lingue, MUIRCT ha esito negativo, a meno che non venga utilizzata l'opzione-b.</span><span class="sxs-lookup"><span data-stu-id="5540e-180">If there are resources in multiple languages in the file, MUIRCT fails, unless the -b switch is used.</span></span> <span data-ttu-id="5540e-181">Se il file contiene risorse con identificatori di lingua con solo valore 0, MUIRCT non suddivide il file perché un identificatore di lingua 0 indica una lingua neutra.</span><span class="sxs-lookup"><span data-stu-id="5540e-181">If the file contains resources with language identifiers having value 0 only, MUIRCT does not split the file because a language identifier of 0 indicates a neutral language.</span></span><br/> <span data-ttu-id="5540e-182">Per l'opzione-d, source_filename è un file in o un file di risorse specifico della lingua per il quale MUIRCT deve visualizzare i dati di configurazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="5540e-182">For the -d switch, source_filename is either an LN file or a language-specific resource file for which MUIRCT is to display resource configuration data.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5540e-183">language_neutral_filename</span><span class="sxs-lookup"><span data-stu-id="5540e-183">language_neutral_filename</span></span></td>
<td><span data-ttu-id="5540e-184">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5540e-184">Optional.</span></span> <span data-ttu-id="5540e-185">Nome del file LN.</span><span class="sxs-lookup"><span data-stu-id="5540e-185">Name of LN file.</span></span> <span data-ttu-id="5540e-186">Se non si specifica il nome del file, MUIRCT aggiunge una seconda estensione &quot; . LN &quot; al nome del file di origine da utilizzare come nome file indipendente dalla lingua.</span><span class="sxs-lookup"><span data-stu-id="5540e-186">If you do not specify the name of this file, MUIRCT appends a second extension &quot;.ln&quot; to the source file name to use as the language-neutral file name.</span></span> <span data-ttu-id="5540e-187">In genere è consigliabile rimuovere l' &quot; estensione. LN &quot; prima di distribuire il file.</span><span class="sxs-lookup"><span data-stu-id="5540e-187">Typically you should remove the &quot;.ln&quot; extension before deploying the file.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="5540e-188">Il file LN non deve contenere stringhe o menu.</span><span class="sxs-lookup"><span data-stu-id="5540e-188">The LN file should not contain strings or menus.</span></span> <span data-ttu-id="5540e-189">È necessario rimuoverli manualmente.</span><span class="sxs-lookup"><span data-stu-id="5540e-189">You should remove them manually.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5540e-190">mui_filename</span><span class="sxs-lookup"><span data-stu-id="5540e-190">mui_filename</span></span></td>
<td><span data-ttu-id="5540e-191">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5540e-191">Optional.</span></span> <span data-ttu-id="5540e-192">Nome del file di risorse specifico della lingua.</span><span class="sxs-lookup"><span data-stu-id="5540e-192">Name of language-specific resource file.</span></span> <span data-ttu-id="5540e-193">Se non si specifica un nome, MUIRCT aggiunge una seconda estensione &quot; MUI &quot; al nome del file di origine da utilizzare come nome file. In genere, MUIRCT crea un file di risorse specifico per la lingua.</span><span class="sxs-lookup"><span data-stu-id="5540e-193">If you do not specify a name, MUIRCT appends a second extension &quot;.mui&quot; to the source file name to use as the file name.Normally, MUIRCT creates a language-specific resource file.</span></span> <span data-ttu-id="5540e-194">Tuttavia, non crea un file di risorse se sussistono le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5540e-194">However, it does not create a resource file if any of the following conditions exist:</span></span><br/>
<ul>
<li><span data-ttu-id="5540e-195">Nessuna risorsa localizzabile si trova nel file binario originale.</span><span class="sxs-lookup"><span data-stu-id="5540e-195">No localizable resources are in the original binary file.</span></span></li>
<li><span data-ttu-id="5540e-196">L'unica lingua della risorsa trovata nel file binario originale è la lingua neutra.</span><span class="sxs-lookup"><span data-stu-id="5540e-196">The only resource language found in the original binary file is the neutral language.</span></span></li>
<li><span data-ttu-id="5540e-197">Il file binario originale contiene risorse per più di una lingua, senza contare la lingua neutra.</span><span class="sxs-lookup"><span data-stu-id="5540e-197">The original binary file has resources for more than one language, not counting the neutral language.</span></span> <span data-ttu-id="5540e-198">Se il file binario contiene risorse per due lingue e una di esse è la lingua neutra, l'utilità considera il file come monolingua e crea un file di risorse specifico della lingua se sono presenti risorse localizzabili.</span><span class="sxs-lookup"><span data-stu-id="5540e-198">If the binary file contains resources for two languages, and one of them is the neutral language, the utility considers the file to be monolingual and creates a language-specific resource file if there are localizable resources.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="muirct-language-output"></a><span data-ttu-id="5540e-199">Output della lingua MUIRCT</span><span class="sxs-lookup"><span data-stu-id="5540e-199">MUIRCT Language Output</span></span>

<span data-ttu-id="5540e-200">MUIRCT sceglie il valore dell'attributo "UltimateFallbackLanguage" da inserire nei dati di configurazione della risorsa nel file in base all'ordine seguente, dalla priorità più alta a quella più bassa:</span><span class="sxs-lookup"><span data-stu-id="5540e-200">MUIRCT chooses the "UltimateFallbackLanguage" attribute value to insert in the LN file resource configuration data based on the following order, from highest priority to lowest:</span></span>

1.  <span data-ttu-id="5540e-201">Attributo "UltimateFallbackLanguage" nel file di configurazione della risorsa di origine, se ne viene passato uno come input.</span><span class="sxs-lookup"><span data-stu-id="5540e-201">"UltimateFallbackLanguage" attribute in the source resource configuration file, if one is passed in as input.</span></span>
2.  <span data-ttu-id="5540e-202">Lingua specificata con l'opzione-g.</span><span class="sxs-lookup"><span data-stu-id="5540e-202">The language specified with the -g switch.</span></span>
3.  <span data-ttu-id="5540e-203">Lingua del file di input.</span><span class="sxs-lookup"><span data-stu-id="5540e-203">Input file language.</span></span>

<span data-ttu-id="5540e-204">MUIRCT sceglie il valore dell'attributo "Language" da inserire nei dati di configurazione delle risorse del file con estensione MUI in base all'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="5540e-204">MUIRCT picks the "language" attribute value to insert in the .mui file resource configuration data based on the following order:</span></span>

1.  <span data-ttu-id="5540e-205">attributo "Language" nel file di configurazione della risorsa di origine, se ne viene passato uno come input.</span><span class="sxs-lookup"><span data-stu-id="5540e-205">"language" attribute in the source resource configuration file, if one is passed in as input.</span></span>
2.  <span data-ttu-id="5540e-206">Lingua specificata dall'opzione-x (Force Language).</span><span class="sxs-lookup"><span data-stu-id="5540e-206">The language specified by the -x switch (force language).</span></span>
3.  <span data-ttu-id="5540e-207">Lingua del file di input.</span><span class="sxs-lookup"><span data-stu-id="5540e-207">Input file language.</span></span>

### <a name="muirct-checksum-handling"></a><span data-ttu-id="5540e-208">Gestione checksum MUIRCT</span><span class="sxs-lookup"><span data-stu-id="5540e-208">MUIRCT Checksum Handling</span></span>

<span data-ttu-id="5540e-209">Il sistema operativo normalmente calcola il checksum sulle risorse specifiche della lingua in un file, a meno che non si specifichi il checksum tramite un file di configurazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="5540e-209">The operating system normally calculates the checksum over the language-specific resources in a file unless you specify the checksum through a resource configuration file.</span></span> <span data-ttu-id="5540e-210">Se il checksum è lo stesso per il file in e per tutti i file di risorse specifici della lingua associati e l'attributo Language nella configurazione della risorsa in e la corrispondenza dipendente dalla lingua, il caricatore di risorse è in grado di caricare correttamente le risorse.</span><span class="sxs-lookup"><span data-stu-id="5540e-210">As long as the checksum is the same for the LN file and all associated language-specific resource files, and the language attribute in the resource configuration in the LN and language dependent match, the resource loader can successfully load resources.</span></span>

<span data-ttu-id="5540e-211">MUIRCT supporta diversi metodi per inserire i checksum appropriati nei dati di configurazione delle risorse:</span><span class="sxs-lookup"><span data-stu-id="5540e-211">MUIRCT supports several methods for placing appropriate checksums in the resource configuration data:</span></span>

1.  <span data-ttu-id="5540e-212">Compilare un eseguibile per ogni lingua, che contiene sia il codice che le risorse.</span><span class="sxs-lookup"><span data-stu-id="5540e-212">Build an executable for each language, containing both code and resources.</span></span> <span data-ttu-id="5540e-213">Successivamente, usare MUIRCT per suddividere ognuno di questi file in un file in e in un file di risorse specifico della lingua.</span><span class="sxs-lookup"><span data-stu-id="5540e-213">After this, use MUIRCT to split each of these files into an LN file and a language-specific resource file.</span></span> <span data-ttu-id="5540e-214">MUIRCT viene eseguito più volte, una volta per generare un file di risorse per ciascuna lingua.</span><span class="sxs-lookup"><span data-stu-id="5540e-214">MUIRCT runs multiple times, once to generate a resource file for each language.</span></span> <span data-ttu-id="5540e-215">È possibile eseguire la compilazione nei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="5540e-215">You can perform the build in the following ways:</span></span>
    1.  <span data-ttu-id="5540e-216">Usare l'opzione-q per specificare un valore di checksum nel file di configurazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="5540e-216">Use the -q switch to specify a checksum value in the resource configuration file.</span></span> <span data-ttu-id="5540e-217">MUIRCT inserisce questo valore in tutti i file di risorse e specifici della lingua prodotti.</span><span class="sxs-lookup"><span data-stu-id="5540e-217">MUIRCT places this value in all the LN files and language-specific resource files produced.</span></span> <span data-ttu-id="5540e-218">È necessario adottare una strategia per scegliere questo valore, come descritto più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="5540e-218">You need to adopt a strategy for choosing this value, as described later in this topic.</span></span>
    2.  <span data-ttu-id="5540e-219">Usare l'opzione-c (e, facoltativamente, l'opzione-b) per scegliere una singola lingua con risorse da cui MUIRCT estrae il checksum.</span><span class="sxs-lookup"><span data-stu-id="5540e-219">Use the -c switch (and, optionally, the -b switch) to choose a single language having resources from which MUIRCT extracts the checksum.</span></span>
    3.  <span data-ttu-id="5540e-220">Usare l'opzione-z per scegliere una singola lingua con risorse da cui MUIRCT estrae sempre il checksum.</span><span class="sxs-lookup"><span data-stu-id="5540e-220">Use the -z switch to choose a single language having resources from which MUIRCT always extracts the checksum.</span></span> <span data-ttu-id="5540e-221">Applicare questo checksum dopo che i file sono stati compilati con altri metodi.</span><span class="sxs-lookup"><span data-stu-id="5540e-221">Apply this checksum after the files have been built using other methods.</span></span>
2.  <span data-ttu-id="5540e-222">Compilare un eseguibile contenente codice e risorse per un singolo linguaggio.</span><span class="sxs-lookup"><span data-stu-id="5540e-222">Build an executable containing both code and resources for a single language.</span></span> <span data-ttu-id="5540e-223">Successivamente, usare MUIRCT per suddividere le risorse tra il file LN e il file di risorse specifico della lingua.</span><span class="sxs-lookup"><span data-stu-id="5540e-223">After this, use MUIRCT to split the resources between the LN file and the language-specific resource file.</span></span> <span data-ttu-id="5540e-224">Infine, usare uno strumento di localizzazione binaria per modificare il file di risorse risultante per ogni lingua.</span><span class="sxs-lookup"><span data-stu-id="5540e-224">Finally, use a binary localization tool to modify the resulting resource file for each language.</span></span>

<span data-ttu-id="5540e-225">La convenzione più comune per la gestione dei checksum consiste nel basare il checksum sulle risorse in lingua inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="5540e-225">The most common convention for checksum handling is to base the checksum on the English (United States) resources.</span></span> <span data-ttu-id="5540e-226">È possibile adottare una convenzione diversa, purché sia coerente per ogni file in.</span><span class="sxs-lookup"><span data-stu-id="5540e-226">You are free to adopt a different convention, as long as it is consistent for each LN file.</span></span> <span data-ttu-id="5540e-227">Ad esempio, è perfettamente accettabile per un'azienda di sviluppo software basare i relativi checksum nel software che si basa su risorse francesi (Francia) invece che in inglese (Stati Uniti), purché tutte le applicazioni dispongano di risorse francesi (Francia) su cui basare i checksum.</span><span class="sxs-lookup"><span data-stu-id="5540e-227">For example, it is perfectly acceptable for a software development enterprise to base its checksums in the software it builds on French (France) resources instead of English (United States) resources, as long as all the applications have French (France) resources on which to base the checksums.</span></span> <span data-ttu-id="5540e-228">È inoltre accettabile usare il file di configurazione delle risorse per assegnare un valore esadecimale arbitrario di un massimo di 16 cifre esadecimali come checksum.</span><span class="sxs-lookup"><span data-stu-id="5540e-228">It is also acceptable to use the resource configuration file to assign an arbitrary hexadecimal value of up to 16 hexadecimal digits as a checksum.</span></span> <span data-ttu-id="5540e-229">Questa ultima strategia impedisce l'uso effettivo delle opzioni-z,-c e-b di MUIRCT.</span><span class="sxs-lookup"><span data-stu-id="5540e-229">This last strategy precludes the effective use of the -z, -c, and -b switches of MUIRCT.</span></span> <span data-ttu-id="5540e-230">Richiede l'adozione di un metodo utilizzando [**GuidGen**](/previous-versions/windows/embedded/ms924300(v=msdn.10)) o un altro strumento per generare valori di checksum.</span><span class="sxs-lookup"><span data-stu-id="5540e-230">It requires adoption of a method using either [**GuidGen**](/previous-versions/windows/embedded/ms924300(v=msdn.10)) or some other tool to generate checksum values.</span></span> <span data-ttu-id="5540e-231">Questa strategia richiede anche la configurazione di un criterio per determinare quando modificare il valore quando si aggiungono nuove risorse localizzabili.</span><span class="sxs-lookup"><span data-stu-id="5540e-231">This strategy also requires you to set up a policy for determining when to modify the value when adding new localizable resources.</span></span>

<span data-ttu-id="5540e-232">Per applicare il checksum in lingua inglese (Stati Uniti) a tutti i file, è possibile usare uno dei metodi di gestione del checksum descritti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="5540e-232">To apply the English (United States) checksum to all files, you can use any of the checksum handling methods described above.</span></span> <span data-ttu-id="5540e-233">Ad esempio, è possibile generare il file di risorse nel file e nella lingua per l'inglese (Stati Uniti), quindi usare l'opzione MUIRCT-d per ottenere il checksum risultante.</span><span class="sxs-lookup"><span data-stu-id="5540e-233">For example, you can generate the LN file and language-specific resource file for English (United States), then use the MUIRCT -d switch to obtain the resulting checksum.</span></span> <span data-ttu-id="5540e-234">È possibile copiare questo checksum nel file di configurazione delle risorse e usare l'opzione-q con MUIRCT per applicare il checksum a tutti gli altri file.</span><span class="sxs-lookup"><span data-stu-id="5540e-234">You can copy this checksum into your resource configuration file and use the -q switch with MUIRCT to apply the checksum to all other files.</span></span>

### <a name="use-of-a-resource-configuration-file-with-muirct"></a><span data-ttu-id="5540e-235">Uso di un file di configurazione delle risorse con MUIRCT</span><span class="sxs-lookup"><span data-stu-id="5540e-235">Use of a Resource Configuration File with MUIRCT</span></span>

<span data-ttu-id="5540e-236">Quando si usa MUIRCT, è possibile specificare i dati di configurazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="5540e-236">You can specify resource configuration data when using MUIRCT.</span></span> <span data-ttu-id="5540e-237">Indipendentemente dal fatto che venga specificato in modo esplicito un file di configurazione delle risorse, ogni file di risorse specifico della lingua presenta dati di configurazione delle risorse, così come tutti i file con un file di risorse associato.</span><span class="sxs-lookup"><span data-stu-id="5540e-237">Whether or not you explicitly supply a resource configuration file, every language-specific resource file has resource configuration data, as does any LN file with an associated resource file.</span></span> <span data-ttu-id="5540e-238">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="5540e-238">For example:</span></span>

-   <span data-ttu-id="5540e-239">Se si usa l'opzione-q per specificare un file di configurazione delle risorse, ma non sono presenti risorse localizzabili nel file di origine di input, non viene generato alcun file di risorse specifico della lingua e il file in risultante non contiene dati di configurazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="5540e-239">If you use the -q switch to specify a resource configuration file, but there are no localizable resources in your input source file, no language-specific resource file is generated and the resulting LN file does not contain resource configuration data.</span></span> <span data-ttu-id="5540e-240">Inoltre, se il file di origine di input dispone di risorse multilingue, MUIRCT non suddividerà il file.</span><span class="sxs-lookup"><span data-stu-id="5540e-240">Also, if the input source file has multilingual resources, then MUIRCT won't split the file.</span></span>

> [!Note]  
> <span data-ttu-id="5540e-241">Attualmente il comportamento di MUIRCT è incoerente quando l'elemento neutralResources del file di configurazione della risorsa non contiene elementi resourceType e l'elemento localizedResources contiene stringhe e menu, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="5540e-241">Currently the behavior of MUIRCT is inconsistent when the neutralResources element of the resource configuration file contains no resourceType elements and the localizedResources element contains strings and menus, for example.</span></span> <span data-ttu-id="5540e-242">In tal caso, MUIRCT suddivide le risorse nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="5540e-242">In such a case, MUIRCT splits the resources as follows:</span></span>
>
> -   <span data-ttu-id="5540e-243">Tutte le risorse nel file binario originale (incluse le stringhe e i menu), oltre alle risorse MUI, vengono inserite nel file LN.</span><span class="sxs-lookup"><span data-stu-id="5540e-243">All resources in the original binary (including strings and menus), plus the MUI resources, are placed in the LN file.</span></span>
> -   <span data-ttu-id="5540e-244">Le stringhe, i menu e le risorse MUI vengono inseriti nel file di risorse specifico della lingua appropriato.</span><span class="sxs-lookup"><span data-stu-id="5540e-244">Strings, menus, and MUI resources are placed in the appropriate language-specific resource file.</span></span>

 

### <a name="examples-for-using-muirct"></a><span data-ttu-id="5540e-245">Esempi per l'uso di MUIRCT</span><span class="sxs-lookup"><span data-stu-id="5540e-245">Examples for Using MUIRCT</span></span>

<span data-ttu-id="5540e-246">**Esempi di utilizzo standard**</span><span class="sxs-lookup"><span data-stu-id="5540e-246">**Examples of Standard Usage**</span></span>


```C++
muirct -q mui.MMF bar.exe barnew.exe barnew.exe.mui

muirct -d myprog.exe.mui
```



<span data-ttu-id="5540e-247">**Esempio di file di output con l'opzione-d**</span><span class="sxs-lookup"><span data-stu-id="5540e-247">**Example of LN File Output Using -d Switch**</span></span>

<span data-ttu-id="5540e-248">Di seguito è riportato un esempio di output dei dati di configurazione delle risorse da un file LN, Shell32.dll, usando l'opzione-d con MUIRCT:</span><span class="sxs-lookup"><span data-stu-id="5540e-248">Here is an example of the resource configuration data output from an LN file, Shell32.dll, using the -d switch with MUIRCT:</span></span>


```C++
Signature          -    fecdfecd
Length             -    148
RC Config Version  -    10000
FileType           -    11
SystemAttributes   -    100
UltimateFallback location    -  external
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    AVI FTR ORDERSTREAM TYPELIB UIFILE XML MUI
MainIDTypes        -    1 2 3 12 14 16 24
MuiNameTypes       -    MUI
MuiIDTypes         -    2 3 4 5 6 9 14 16
UltimateFallbackLanguage   -   en-US
```



<span data-ttu-id="5540e-249">**Esempio di Language-Specific output del file di risorse con l'opzione-d**</span><span class="sxs-lookup"><span data-stu-id="5540e-249">**Example of Language-Specific Resource File Output Using -d Switch**</span></span>

<span data-ttu-id="5540e-250">Di seguito è riportato un esempio di output dei dati di configurazione delle risorse da un file con estensione MUI, Shell32.dll. mui, usando l'opzione-d per MUIRCT:</span><span class="sxs-lookup"><span data-stu-id="5540e-250">Here is an example of the resource configuration data output from a .mui file, Shell32.dll.mui, using the -d switch for MUIRCT:</span></span>


```C++
Signature          -    fecdfecd
Length             -     c8
RC Config Version  -    10000
FileType           -    12
SystemAttributes   -    100
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    MUI
MainIDTypes        -    2 3 4 5 6 9 14 16
Language           -    en-US
```



## <a name="rc-compiler-utility"></a><span data-ttu-id="5540e-251">RC (utilità del compilatore)</span><span class="sxs-lookup"><span data-stu-id="5540e-251">RC Compiler Utility</span></span>

<span data-ttu-id="5540e-252">Il compilatore RC (Rc.exe) è un'utilità della riga di comando per la compilazione di un file di script di definizione di risorsa (estensione RC) in file di risorse (estensione res).</span><span class="sxs-lookup"><span data-stu-id="5540e-252">RC Compiler (Rc.exe) is a command line utility for compiling a resource definition script file (.rc extension) into resource files (.res extension).</span></span> <span data-ttu-id="5540e-253">Il compilatore RC è incluso nella Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="5540e-253">RC Compiler is included in the Windows SDK.</span></span> <span data-ttu-id="5540e-254">Questo documento illustra solo l'uso del compilatore RC con le funzionalità relative a MUI del caricatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="5540e-254">This document only explains the use of RC Compiler with MUI-related capabilities of the resource loader.</span></span> <span data-ttu-id="5540e-255">Per informazioni complete sul compilatore, vedere [informazioni sui file di risorse](../menurc/about-resource-files.md).</span><span class="sxs-lookup"><span data-stu-id="5540e-255">For complete information about the compiler, see [About Resource Files](../menurc/about-resource-files.md).</span></span>

<span data-ttu-id="5540e-256">Il compilatore RC consente di compilare, da un singolo set di origini, un file LN e un file di risorse distinto specifico per la lingua.</span><span class="sxs-lookup"><span data-stu-id="5540e-256">RC Compiler allows you to build, from a single set of sources, an LN file and a separate language-specific resource file.</span></span> <span data-ttu-id="5540e-257">Per quanto riguarda MUIRCT, i file sono associati ai dati di configurazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="5540e-257">As for MUIRCT, the files are associated by resource configuration data.</span></span>

### <a name="rc-compiler-syntax-as-used-for-mui-resources"></a><span data-ttu-id="5540e-258">Sintassi del compilatore RC usata per le risorse MUI</span><span class="sxs-lookup"><span data-stu-id="5540e-258">RC Compiler Syntax as Used for MUI Resources</span></span>

<span data-ttu-id="5540e-259">Le opzioni del compilatore RC sono definite in dettaglio nell' [uso di RC](../menurc/using-rc-the-rc-command-line-.md).</span><span class="sxs-lookup"><span data-stu-id="5540e-259">RC Compiler switches are defined in detail in [Using RC](../menurc/using-rc-the-rc-command-line-.md).</span></span> <span data-ttu-id="5540e-260">Questa sezione definisce solo le opzioni usate per compilare le risorse MUI.</span><span class="sxs-lookup"><span data-stu-id="5540e-260">This section only defines the switches used to build MUI resources.</span></span> <span data-ttu-id="5540e-261">Tenere presente che ogni opzione non fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="5540e-261">Remember that each switch is case-insensitive.</span></span> <span data-ttu-id="5540e-262">I tipi di risorse sono considerati indipendenti dalla lingua, salvo diversa indicazione.</span><span class="sxs-lookup"><span data-stu-id="5540e-262">Resource types are assumed to be language-neutral unless otherwise indicated.</span></span>


```C++
rc [-h|-?] -fm mui_res_name [-q rc_config_file_name] [-g langid] [-g1 ] [-g2 version]
```



<span data-ttu-id="5540e-263">**Opzioni e argomenti**</span><span class="sxs-lookup"><span data-stu-id="5540e-263">**Switches and Arguments**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5540e-264">-h |-?</span><span class="sxs-lookup"><span data-stu-id="5540e-264">-h|-?</span></span></td>
<td><span data-ttu-id="5540e-265">Mostra la schermata della guida.</span><span class="sxs-lookup"><span data-stu-id="5540e-265">Shows help screen.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5540e-266">-FM</span><span class="sxs-lookup"><span data-stu-id="5540e-266">-fm</span></span></td>
<td><span data-ttu-id="5540e-267">Usa il file di risorse specificato per le risorse specifiche della lingua.</span><span class="sxs-lookup"><span data-stu-id="5540e-267">Uses the specified resource file for language-specific resources.</span></span> <span data-ttu-id="5540e-268">Normalmente il compilatore di risorse crea un file di risorse specifico per la lingua.</span><span class="sxs-lookup"><span data-stu-id="5540e-268">Normally the resource compiler creates a language-specific resource file.</span></span> <span data-ttu-id="5540e-269">Tuttavia, non crea il file se sussistono le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5540e-269">However, it does not create the file if any of the following conditions exist:</span></span><br/>
<ul>
<li><span data-ttu-id="5540e-270">Nel file RC non sono disponibili risorse localizzabili.</span><span class="sxs-lookup"><span data-stu-id="5540e-270">There are no localizable resources in the .rc file.</span></span></li>
<li><span data-ttu-id="5540e-271">L'unica lingua della risorsa trovata nel file RC è la lingua neutra.</span><span class="sxs-lookup"><span data-stu-id="5540e-271">The only resource language found in the .rc file is the neutral language.</span></span></li>
<li><span data-ttu-id="5540e-272">Il file RC contiene risorse per più di un linguaggio, senza contare la lingua neutra.</span><span class="sxs-lookup"><span data-stu-id="5540e-272">The .rc file has resources for more than one language, not counting the neutral language.</span></span> <span data-ttu-id="5540e-273">Se il file RC contiene risorse per due lingue e una di esse è la lingua neutra, il compilatore considera il file come monolinguale.</span><span class="sxs-lookup"><span data-stu-id="5540e-273">If the .rc file contains resources for two languages, and one of them is the neutral language, the compiler considers the file to be monolingual.</span></span> <span data-ttu-id="5540e-274">Se sono presenti risorse localizzabili, il compilatore crea un file di risorse specifico per la lingua.</span><span class="sxs-lookup"><span data-stu-id="5540e-274">If there are any localizable resources, the compiler creates a language-specific resource file.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5540e-275">-Q</span><span class="sxs-lookup"><span data-stu-id="5540e-275">-q</span></span></td>
<td><span data-ttu-id="5540e-276">Usa il file di configurazione della risorsa specificato per ottenere i tipi di risorse da inserire nel file di risorse specifico del linguaggio e nel file LN.</span><span class="sxs-lookup"><span data-stu-id="5540e-276">Uses the specified resource configuration file to obtain the resource types to place in the language-specific resource file and the LN file.</span></span> <span data-ttu-id="5540e-277">Per ulteriori informazioni, vedere <a href="preparing-a-resource-configuration-file.md">preparazione di un file di configurazione delle risorse</a>.</span><span class="sxs-lookup"><span data-stu-id="5540e-277">For more information, see <a href="preparing-a-resource-configuration-file.md">Preparing a Resource Configuration File</a>.</span></span> <span data-ttu-id="5540e-278">In alternativa a questa opzione, è possibile usare le opzioni-j e-k, ma è preferibile usare un file di configurazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="5540e-278">As an alternative to this switch, you can use the -j and -k switches, but it is preferred to use a resource configuration file.</span></span> <br/> <span data-ttu-id="5540e-279">Usando l'opzione-q con un file di configurazione delle risorse, è possibile implementare una divisione basata su elementi e fornire gli attributi che finiranno con la configurazione della risorsa binaria nel file di risorse LN e in quello specifico del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="5540e-279">By using the -q switch with a resource configuration file, you can implement an item-based split and provide attributes that will end up with the binary resource configuration in the LN and language-specific resource file.</span></span> <span data-ttu-id="5540e-280">Questa divisione non è possibile utilizzando le opzioni-j e-k.</span><span class="sxs-lookup"><span data-stu-id="5540e-280">This split is not possible using the -j and -k switches.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="5540e-281">Il processo di suddivisione del compilatore RC non funziona correttamente se si archiviano le risorse e le informazioni sulla versione in file di configurazione delle risorse differenti.</span><span class="sxs-lookup"><span data-stu-id="5540e-281">The RC Compiler split process does not work properly if you store resources and version information in different resource configuration files.</span></span> <span data-ttu-id="5540e-282">In questo caso, il compilatore RC non suddivide le informazioni sulla versione.</span><span class="sxs-lookup"><span data-stu-id="5540e-282">In this case, RC Compiler does not split the version information.</span></span> <span data-ttu-id="5540e-283">Pertanto, si verifica un errore del linker durante il collegamento del file di risorse specifico della lingua perché il file non dispone di risorse di versione.</span><span class="sxs-lookup"><span data-stu-id="5540e-283">Therefore a linker error occurs during linking of the language-specific resource file because the file does not have version resources.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5540e-284">-g</span><span class="sxs-lookup"><span data-stu-id="5540e-284">-g</span></span></td>
<td><span data-ttu-id="5540e-285">Specifica l'identificatore della <a href="language-identifiers.md">lingua di fallback</a> finale in formato esadecimale.</span><span class="sxs-lookup"><span data-stu-id="5540e-285">Specifies the ultimate <a href="language-identifiers.md">fallback language</a> identifier in hexadecimal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5540e-286">-G1</span><span class="sxs-lookup"><span data-stu-id="5540e-286">-g1</span></span></td>
<td><span data-ttu-id="5540e-287">Crea un file MUI. res anche se la risorsa di versione è l'unico contenuto localizzabile.</span><span class="sxs-lookup"><span data-stu-id="5540e-287">Creates a MUI .res file even if the VERSION resource is the only localizable content.</span></span> <span data-ttu-id="5540e-288">Per impostazione predefinita, il compilatore RC non produce un file RES se VERSION è l'unica risorsa localizzabile.</span><span class="sxs-lookup"><span data-stu-id="5540e-288">By default, RC Compiler does not produce a .res file if VERSION is the only localizable resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5540e-289">-g2</span><span class="sxs-lookup"><span data-stu-id="5540e-289">-g2</span></span></td>
<td><span data-ttu-id="5540e-290">Specifica il numero di versione personalizzato da usare per il calcolo del checksum.</span><span class="sxs-lookup"><span data-stu-id="5540e-290">Specifies the custom version number to use when calculating the checksum.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5540e-291">mui_res_name</span><span class="sxs-lookup"><span data-stu-id="5540e-291">mui_res_name</span></span></td>
<td><span data-ttu-id="5540e-292">File di risorse per le risorse specifiche della lingua.</span><span class="sxs-lookup"><span data-stu-id="5540e-292">Resource file for language-specific resources.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5540e-293">rc_config_file_name</span><span class="sxs-lookup"><span data-stu-id="5540e-293">rc_config_file_name</span></span></td>
<td><span data-ttu-id="5540e-294">File di configurazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="5540e-294">Resource configuration file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5540e-295">langid</span><span class="sxs-lookup"><span data-stu-id="5540e-295">langid</span></span></td>
<td><span data-ttu-id="5540e-296">Identificatore della lingua.</span><span class="sxs-lookup"><span data-stu-id="5540e-296">Language identifier.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5540e-297">version</span><span class="sxs-lookup"><span data-stu-id="5540e-297">version</span></span></td>
<td><span data-ttu-id="5540e-298">Numero di versione personalizzato, in un formato, ad esempio &quot; 6.2.0.0 &quot; .</span><span class="sxs-lookup"><span data-stu-id="5540e-298">Custom version number, in a format such as &quot;6.2.0.0&quot;.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="example-for-using-rc-compiler-to-build-mui-resources"></a><span data-ttu-id="5540e-299">Esempio per l'uso del compilatore RC per compilare risorse MUI</span><span class="sxs-lookup"><span data-stu-id="5540e-299">Example for Using RC Compiler to Build MUI Resources</span></span>

<span data-ttu-id="5540e-300">Per illustrare l'operazione del compilatore RC con le risorse MUI, esaminiamo la seguente riga di comando per il file di risorse MyFile. RC:</span><span class="sxs-lookup"><span data-stu-id="5540e-300">To illustrate RC Compiler operation with MUI resources, let's examine the following command line, for the resource file Myfile.rc:</span></span>


```C++
rc -fm myfile_res.res -q myfile.rcconfig myfile.rc
```



<span data-ttu-id="5540e-301">Questa riga di comando fa sì che il compilatore RC esegua le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5540e-301">This command line causes RC Compiler to do the following:</span></span>

-   <span data-ttu-id="5540e-302">Creare il file di risorse specifico per il linguaggio file \_ res. res e un file di risorse indipendente dalla lingua che per impostazione predefinita è MyFile. res, in base al nome del file RC.</span><span class="sxs-lookup"><span data-stu-id="5540e-302">Create the language-specific resource file Myfile\_res.res and a language-neutral resource file that defaults to Myfile.res, based on the name of the .rc file.</span></span>
-   <span data-ttu-id="5540e-303">Aggiungere 2 (elemento 5 6 7 8 9 10 11 12), 4, 5, 6, 9, 11, 16, 23, 240, 1024 \_ tipi di risorse di tipo nel file con estensione res specifico del linguaggio se sono nel file RC.</span><span class="sxs-lookup"><span data-stu-id="5540e-303">Add the 2 (item 5 6 7 8 9 10 11 12), 4, 5, 6, 9, 11, 16, 23, 240, 1024 MY\_TYPE resource types to the language-specific .res file if they are in the .rc file.</span></span>
-   <span data-ttu-id="5540e-304">Aggiungere il tipo di risorsa 16, insieme ad altri tipi di risorse descritti nel file di risorse al file con estensione res indipendente dalla lingua e al file con estensione res specifico della lingua.</span><span class="sxs-lookup"><span data-stu-id="5540e-304">Add resource type 16, along with any other resource types described in the resource file to the language-neutral .res file and to the language-specific .res file.</span></span> <span data-ttu-id="5540e-305">Si noti che, in questo esempio, il tipo di risorsa 16 viene aggiunto in due posizioni.</span><span class="sxs-lookup"><span data-stu-id="5540e-305">Note that, in this example, resource type 16 is being added in two places.</span></span>
-   <span data-ttu-id="5540e-306">Scegliere il valore dell'attributo "UltimateFallbackLanguage" da inserire nei dati di configurazione della risorsa nei file in base ai criteri seguenti, ordinati dalla priorità più alta a quella più bassa:</span><span class="sxs-lookup"><span data-stu-id="5540e-306">Choose the "UltimateFallbackLanguage" attribute value to insert into the LN file resource configuration data based on the following criteria, ordered from highest priority to lowest:</span></span>
    -   <span data-ttu-id="5540e-307">Attributo "UltimateFallbackLanguage" nel file di configurazione della risorsa se ne viene passato uno come input.</span><span class="sxs-lookup"><span data-stu-id="5540e-307">"UltimateFallbackLanguage" attribute in the resource configuration file if one is passed in as input.</span></span>
    -   <span data-ttu-id="5540e-308">Valore dell'attributo Language da inserire nei dati di configurazione delle risorse in base all'ordine del linguaggio del compilatore RC (indipendente dalla lingua e linguaggio del file di risorse specifico della lingua).</span><span class="sxs-lookup"><span data-stu-id="5540e-308">Language attribute value to insert in the resource configuration data based on the RC Compiler language order (language-neutral and language-specific resource file language).</span></span> <span data-ttu-id="5540e-309">Le considerazioni includono il linguaggio nel file RC, il valore della lingua dell'opzione-GL e l'identificatore 0x0409 per l'inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="5540e-309">Considerations include language in the .rc file, language value of the -gl switch, and identifier 0x0409 for English (United States).</span></span>

## <a name="remarks"></a><span data-ttu-id="5540e-310">Commenti</span><span class="sxs-lookup"><span data-stu-id="5540e-310">Remarks</span></span>

<span data-ttu-id="5540e-311">Se si include un tipo di risorsa ICON (3), DIALOG (5), STRING (6) o VERSION (16) nell'elemento neutralResources, è necessario duplicare tale voce nell'elemento localizedResources nel file di configurazione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5540e-311">If you include any ICON(3), DIALOG(5), STRING(6), or VERSION(16) resource type in the neutralResources element, then you have to duplicate that entry in the localizedResources element in the resource configuration file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5540e-312">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5540e-312">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5540e-313">Informazioni di riferimento sull'interfaccia utente multilingue</span><span class="sxs-lookup"><span data-stu-id="5540e-313">Multilingual User Interface Reference</span></span>](multilingual-user-interface-reference.md)
</dt> <dt>

[<span data-ttu-id="5540e-314">Gestione delle risorse MUI</span><span class="sxs-lookup"><span data-stu-id="5540e-314">MUI Resource Management</span></span>](mui-resource-management.md)
</dt> <dt>

[<span data-ttu-id="5540e-315">Localizzazione delle risorse e compilazione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="5540e-315">Localizing Resources and Building the Application</span></span>](localizing-resources-and-building-the-application.md)
</dt> </dl>

 

 
