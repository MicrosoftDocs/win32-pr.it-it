---
description: Preparazione di un file di configurazione delle risorse
ms.assetid: 292b57ea-1c7e-49b6-876c-4ad307a2ec43
title: Preparazione di un file di configurazione delle risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac162ad7f6d20148e0ef60cb9dc15da41cc27186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128926"
---
# <a name="preparing-a-resource-configuration-file"></a><span data-ttu-id="9eee5-103">Preparazione di un file di configurazione delle risorse</span><span class="sxs-lookup"><span data-stu-id="9eee5-103">Preparing a Resource Configuration File</span></span>

<span data-ttu-id="9eee5-104">Entrambe le utilità del compilatore MUIRCT e RC descritte in [Utilità risorse](resource-utilities.md) forniscono un'opzione della riga di comando che consente di specificare un file di configurazione delle risorse per le risorse della lingua di base.</span><span class="sxs-lookup"><span data-stu-id="9eee5-104">Both the MUIRCT and the RC Compiler utilities described in [Resource Utilities](resource-utilities.md) provide a command line option that allows you to specify a resource configuration file for the base language resources.</span></span> <span data-ttu-id="9eee5-105">L'uso di questo file XML pubblico leggibile consente un maggiore controllo sulla suddivisione delle risorse rispetto a quelle che è possibile ottenere usando le normali opzioni della riga di comando delle utilità.</span><span class="sxs-lookup"><span data-stu-id="9eee5-105">Use of this public, human-readable XML file allows more control over the splitting of resources than can be obtained using the regular command line switches of the utilities.</span></span> <span data-ttu-id="9eee5-106">Tuttavia, anche se non si fornisce un file di configurazione delle risorse come input, i file di risorse LN e Language-specific conterranno i dati di configurazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="9eee5-106">However, even if you do not provide a resource configuration file as an input, the LN and language-specific resource files will contain resource configuration data.</span></span>

<span data-ttu-id="9eee5-107">Tutti i file di configurazione delle risorse per le applicazioni Win32 iniziano e terminano in modo identico:</span><span class="sxs-lookup"><span data-stu-id="9eee5-107">All resource configuration files for Win32 applications begin and end identically:</span></span>


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>

<resources>
        
        <!-- a single win32Resources element goes here -->

</resources>
</localization>
```



<span data-ttu-id="9eee5-108">In questo argomento vengono illustrati gli aspetti del XML Schema utili per la compilazione di codice non gestito in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="9eee5-108">This topic focuses on the aspects of the XML schema that are useful in building unmanaged code on Windows Vista and later.</span></span> <span data-ttu-id="9eee5-109">In particolare, è interessato solo dal comportamento dell'elemento win32Resources.</span><span class="sxs-lookup"><span data-stu-id="9eee5-109">In particular, it is only concerned with the behavior of the win32Resources element.</span></span>

## <a name="win32resources-element"></a><span data-ttu-id="9eee5-110">Elemento win32Resources</span><span class="sxs-lookup"><span data-stu-id="9eee5-110">win32Resources Element</span></span>

<span data-ttu-id="9eee5-111">L'elemento win32Resources ha gli attributi descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="9eee5-111">The win32Resources element has the attributes described in the following table.</span></span>



| <span data-ttu-id="9eee5-112">Nome attributo</span><span class="sxs-lookup"><span data-stu-id="9eee5-112">Attribute name</span></span>           | <span data-ttu-id="9eee5-113">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="9eee5-113">Mandatory</span></span> | <span data-ttu-id="9eee5-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9eee5-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eee5-115">fileType</span><span class="sxs-lookup"><span data-stu-id="9eee5-115">fileType</span></span>                 | <span data-ttu-id="9eee5-116">No</span><span class="sxs-lookup"><span data-stu-id="9eee5-116">No</span></span>        | <span data-ttu-id="9eee5-117">Tipo di file.</span><span class="sxs-lookup"><span data-stu-id="9eee5-117">Type of file.</span></span> <span data-ttu-id="9eee5-118">Deve sempre essere "Application".</span><span class="sxs-lookup"><span data-stu-id="9eee5-118">Should always be "Application".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="9eee5-119">checksum</span><span class="sxs-lookup"><span data-stu-id="9eee5-119">checksum</span></span>                 | <span data-ttu-id="9eee5-120">No</span><span class="sxs-lookup"><span data-stu-id="9eee5-120">No</span></span>        | <span data-ttu-id="9eee5-121">Valore di checksum da visualizzare nei dati di configurazione delle risorse dei file di risorse nel file e nel linguaggio specifico.</span><span class="sxs-lookup"><span data-stu-id="9eee5-121">Checksum value to appear in the resource configuration data of the LN file and language-specific resource files.</span></span> <span data-ttu-id="9eee5-122">Questo attributo, ad esempio, consente di copiare il checksum da un singolo file di risorse specifico della lingua, per convenzione quello per la lingua inglese (Stati Uniti) e inserire il checksum in un file di risorse specifico della lingua diverso.</span><span class="sxs-lookup"><span data-stu-id="9eee5-122">For example, this attribute allows you to copy the checksum from a single language-specific resource file, by convention the one for English (United States), and place the checksum in a different language-specific resource file.</span></span> <span data-ttu-id="9eee5-123">Il checksum può essere specificato come stringa di numero esadecimale non più lunga di 32 caratteri.</span><span class="sxs-lookup"><span data-stu-id="9eee5-123">The checksum can be specified as a hexadecimal number string that is no longer than 32 characters.</span></span> <span data-ttu-id="9eee5-124">Il valore numerico deve essere contenuto in un numero a 128 bit.</span><span class="sxs-lookup"><span data-stu-id="9eee5-124">The numerical value must be containable in a 128-bit number.</span></span> |
| <span data-ttu-id="9eee5-125">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="9eee5-125">language</span></span>                 | <span data-ttu-id="9eee5-126">No</span><span class="sxs-lookup"><span data-stu-id="9eee5-126">No</span></span>        | <span data-ttu-id="9eee5-127">Lingua specificata utilizzando un formato di nome conforme a RFC 4646 (Windows Vista e versioni successive), ad esempio en-US per la lingua inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="9eee5-127">Language specified using a name format compliant with RFC 4646 (Windows Vista and later), for example, en-US for English (United States).</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="9eee5-128">ultimateFallbackLanguage</span><span class="sxs-lookup"><span data-stu-id="9eee5-128">ultimateFallbackLanguage</span></span> | <span data-ttu-id="9eee5-129">No</span><span class="sxs-lookup"><span data-stu-id="9eee5-129">No</span></span>        | <span data-ttu-id="9eee5-130">Lingua da inserire nei dati di configurazione della risorsa per il file LN, che rappresenta il linguaggio di fallback finale da usare in una ricerca di un file di risorse specifico per la lingua corrispondente.</span><span class="sxs-lookup"><span data-stu-id="9eee5-130">Language to insert into the resource configuration data for the LN file, representing the ultimate fallback language to use in a search for a corresponding language-specific resource file.</span></span> <span data-ttu-id="9eee5-131">Se il caricatore di risorse non riesce a caricare un file di risorse richiesto dalle lingue dell'interfaccia utente preferite del thread, viene usato un linguaggio di fallback finale come ultimo tentativo.</span><span class="sxs-lookup"><span data-stu-id="9eee5-131">If the resource loader fails to load a requested resource file from the thread preferred UI languages, it uses an ultimate fallback language as its last attempt.</span></span> <span data-ttu-id="9eee5-132">Il linguaggio viene specificato utilizzando un formato di nome conforme a RFC 4646 (Windows Vista e versioni successive), ad esempio, en-US per la lingua inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="9eee5-132">The language is specified using a name format compliant with RFC 4646 (Windows Vista and later), for example, en-US for English (United States).</span></span>       |
| <span data-ttu-id="9eee5-133">ultimateFallbackLocation</span><span class="sxs-lookup"><span data-stu-id="9eee5-133">ultimateFallbackLocation</span></span> | <span data-ttu-id="9eee5-134">No</span><span class="sxs-lookup"><span data-stu-id="9eee5-134">No</span></span>        | <span data-ttu-id="9eee5-135">Percorso di fallback.</span><span class="sxs-lookup"><span data-stu-id="9eee5-135">Fallback location.</span></span> <span data-ttu-id="9eee5-136">Specificare "Internal" se le risorse di fallback Ultimate sono compilate nel file LN.</span><span class="sxs-lookup"><span data-stu-id="9eee5-136">Specify "internal" if ultimate fallback resources are compiled into the LN file.</span></span> <span data-ttu-id="9eee5-137">Specificare "External" (impostazione predefinita) se il file LN fa riferimento a un file di risorse specifico della lingua per le risorse di fallback finali.</span><span class="sxs-lookup"><span data-stu-id="9eee5-137">Specify "external" (default) if the LN file is to reference a language-specific resource file for its ultimate fallback resources.</span></span>                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="9eee5-138">Nel file di configurazione delle risorse, l'elemento win32Resources include i sottoelementi descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="9eee5-138">In the resource configuration file, the win32Resources element has the sub-elements described in the next table.</span></span>



| <span data-ttu-id="9eee5-139">Nome dell'elemento</span><span class="sxs-lookup"><span data-stu-id="9eee5-139">Element Name</span></span>       | <span data-ttu-id="9eee5-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9eee5-140">Description</span></span>                                                                                                                              |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eee5-141">localizedResources</span><span class="sxs-lookup"><span data-stu-id="9eee5-141">localizedResources</span></span> | <span data-ttu-id="9eee5-142">Risorse che incapsulano informazioni sui tipi di risorse e le singole risorse contenute in un file di risorse specifico del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="9eee5-142">Resources that encapsulate information about the resource types and individual resources contained in a language-specific resource file.</span></span> |
| <span data-ttu-id="9eee5-143">neutralResources</span><span class="sxs-lookup"><span data-stu-id="9eee5-143">neutralResources</span></span>   | <span data-ttu-id="9eee5-144">Risorse che incapsulano informazioni sui tipi di risorse contenuti in un file LN.</span><span class="sxs-lookup"><span data-stu-id="9eee5-144">Resources that encapsulate information about the resource types contained in an LN file.</span></span>                                                 |



 

## <a name="localizedresources-element"></a><span data-ttu-id="9eee5-145">Elemento localizedResources</span><span class="sxs-lookup"><span data-stu-id="9eee5-145">localizedResources Element</span></span>

<span data-ttu-id="9eee5-146">Elemento resources localizzato.</span><span class="sxs-lookup"><span data-stu-id="9eee5-146">Localized resources element.</span></span> <span data-ttu-id="9eee5-147">Per impostazione predefinita, questo elemento non ha attributi e un solo tipo di sottoelemento.</span><span class="sxs-lookup"><span data-stu-id="9eee5-147">By default, this element has no attributes and only one type of sub-element.</span></span> <span data-ttu-id="9eee5-148">Si tratta semplicemente di un contenitore per gli elementi resourceType.</span><span class="sxs-lookup"><span data-stu-id="9eee5-148">It is just a container for resourceType elements.</span></span>



| <span data-ttu-id="9eee5-149">Nome attributo</span><span class="sxs-lookup"><span data-stu-id="9eee5-149">Attribute Name</span></span> | <span data-ttu-id="9eee5-150">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9eee5-150">Description</span></span>                                                                    |
|----------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="9eee5-151">resourceType</span><span class="sxs-lookup"><span data-stu-id="9eee5-151">resourceType</span></span>   | <span data-ttu-id="9eee5-152">Tipo di una singola risorsa contenuta in un file di risorse specifico del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="9eee5-152">Type of an individual resource contained in a language-specific resource file.</span></span> |



 

## <a name="neutralresources-element"></a><span data-ttu-id="9eee5-153">Elemento neutralResources</span><span class="sxs-lookup"><span data-stu-id="9eee5-153">neutralResources Element</span></span>

<span data-ttu-id="9eee5-154">Elemento resources neutro.</span><span class="sxs-lookup"><span data-stu-id="9eee5-154">Neutral resources element.</span></span> <span data-ttu-id="9eee5-155">Questo elemento è semplicemente un contenitore per gli elementi resourceType.</span><span class="sxs-lookup"><span data-stu-id="9eee5-155">This element is just a container for resourceType elements.</span></span>



| <span data-ttu-id="9eee5-156">Nome attributo</span><span class="sxs-lookup"><span data-stu-id="9eee5-156">Attribute Name</span></span> | <span data-ttu-id="9eee5-157">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9eee5-157">Description</span></span>                                        |
|----------------|----------------------------------------------------|
| <span data-ttu-id="9eee5-158">resourceType</span><span class="sxs-lookup"><span data-stu-id="9eee5-158">resourceType</span></span>   | <span data-ttu-id="9eee5-159">Tipo di una singola risorsa contenuta in un file LN.</span><span class="sxs-lookup"><span data-stu-id="9eee5-159">Type of a single resource contained in an LN file.</span></span> |



 

## <a name="resourcetype-element"></a><span data-ttu-id="9eee5-160">Elemento resourceType</span><span class="sxs-lookup"><span data-stu-id="9eee5-160">resourceType Element</span></span>

<span data-ttu-id="9eee5-161">L'elemento resourceType incapsula le informazioni su un singolo tipo di risorsa o singola risorsa.</span><span class="sxs-lookup"><span data-stu-id="9eee5-161">The resourceType element encapsulates information about a single resource type or individual resource.</span></span> <span data-ttu-id="9eee5-162">Dispone degli attributi elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="9eee5-162">It has the attributes listed below.</span></span>

> [!Caution]  
> <span data-ttu-id="9eee5-163">Alcuni difetti di configurazione delle risorse vengono intercettati solo dal compilatore RC o MUIRCT, a seconda del contenuto del file di risorse di input o del file binario.</span><span class="sxs-lookup"><span data-stu-id="9eee5-163">Some resource configuration defects are caught only by RC Compiler or MUIRCT, depending on the input resource file or binary file content.</span></span> <span data-ttu-id="9eee5-164">Gli errori resourceType nel file di configurazione delle risorse che non esistono nel file di input non vengono rilevati, causando un comportamento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="9eee5-164">The resourceType errors in the resource configuration file that do not exist in the input file are not caught, resulting in unexpected behavior.</span></span> <span data-ttu-id="9eee5-165">Gli utenti possono usare un file di configurazione delle risorse difettoso e non conoscono fino a quando non introducono file binari che usano le parti interrotte del file di configurazione delle risorse, che consente di creare l'aspetto delle interruzioni rispetto ai file binari correnti.</span><span class="sxs-lookup"><span data-stu-id="9eee5-165">Users can be using a defective resource configuration file and do not know until they introduce binaries that use the broken parts of the resource configuration file, which creates the appearance that the breaks are from the current binaries.</span></span>

 



| <span data-ttu-id="9eee5-166">Nome attributo</span><span class="sxs-lookup"><span data-stu-id="9eee5-166">Attribute name</span></span> | <span data-ttu-id="9eee5-167">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="9eee5-167">Mandatory</span></span> | <span data-ttu-id="9eee5-168">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9eee5-168">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eee5-169">typeNameId</span><span class="sxs-lookup"><span data-stu-id="9eee5-169">typeNameId</span></span>     | <span data-ttu-id="9eee5-170">Sì</span><span class="sxs-lookup"><span data-stu-id="9eee5-170">Yes</span></span>       | <span data-ttu-id="9eee5-171">Nome del tipo o identificatore per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="9eee5-171">Type name or identifier for the resource.</span></span> <span data-ttu-id="9eee5-172">Specificare un nome di stringa o un numero.</span><span class="sxs-lookup"><span data-stu-id="9eee5-172">Specify a string name or a number.</span></span> <span data-ttu-id="9eee5-173">Se si usa un numero, anteporre la stringa a " \# " per indicare che rappresenta un numero.</span><span class="sxs-lookup"><span data-stu-id="9eee5-173">If using a number, prepend the string with a "\#" to indicate that it represents a number.</span></span> <span data-ttu-id="9eee5-174">Ogni elemento resourceType deve avere un solo attributo *typeNameId* .</span><span class="sxs-lookup"><span data-stu-id="9eee5-174">Each resourceType element must have only one *typeNameId* attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="9eee5-175">itemName</span><span class="sxs-lookup"><span data-stu-id="9eee5-175">itemName</span></span>       | <span data-ttu-id="9eee5-176">No</span><span class="sxs-lookup"><span data-stu-id="9eee5-176">No</span></span>        | <span data-ttu-id="9eee5-177">Stringa del nome dell'elemento per la risorsa, da inserire nel file di risorse specifico del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="9eee5-177">Item name string for the resource, to be placed in the language-specific resource file.</span></span> <span data-ttu-id="9eee5-178">È possibile specificare più nomi, separati da spazi vuoti, ad esempio, "HTML MOFDATA".</span><span class="sxs-lookup"><span data-stu-id="9eee5-178">You can specify multiple names, separated by white spaces, for example, "HTML MOFDATA".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="9eee5-179">itemId</span><span class="sxs-lookup"><span data-stu-id="9eee5-179">itemId</span></span>         | <span data-ttu-id="9eee5-180">No</span><span class="sxs-lookup"><span data-stu-id="9eee5-180">No</span></span>        | <span data-ttu-id="9eee5-181">Identificatore dell'elemento di risorsa singolo da inserire nel file di risorse specifico della lingua.</span><span class="sxs-lookup"><span data-stu-id="9eee5-181">Identifier of individual resource item, to be placed in the language-specific resource file.</span></span> <span data-ttu-id="9eee5-182">L'elemento può essere specificato come intervallo (ad esempio, "1-12") o da identificatori singoli separati da spazi vuoti (ad esempio, "1 3 4").</span><span class="sxs-lookup"><span data-stu-id="9eee5-182">The item can be specified as a range (for example, "1-12") or by individual identifiers separated by white spaces (for example, "1 3 4").</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="9eee5-183">stringId</span><span class="sxs-lookup"><span data-stu-id="9eee5-183">stringId</span></span>       | <span data-ttu-id="9eee5-184">No</span><span class="sxs-lookup"><span data-stu-id="9eee5-184">No</span></span>        | <span data-ttu-id="9eee5-185">Identificatore di stringa per un singolo elemento di risorsa, da inserire nel file di risorse specifico del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="9eee5-185">String identifier for individual resource item, to be placed in the language-specific resource file.</span></span> <span data-ttu-id="9eee5-186">La stringa può essere specificata come intervallo (ad esempio, "1-12") o da identificatori singoli separati da spazi vuoti (ad esempio, "1 3 4"). Questo attributo consente di specificare le voci della tabella di stringhe localizzabili e non localizzabili.</span><span class="sxs-lookup"><span data-stu-id="9eee5-186">The string can be specified as a range (for example, "1-12") or by individual identifiers separated by white spaces (for example, "1 3 4").This attribute allows the specification of both localizable and nonlocalizable string table entries.</span></span> <span data-ttu-id="9eee5-187">Deve essere usato in combinazione con il valore di *typeNameId* "6", che indica un tipo di risorsa voce della tabella di stringhe.</span><span class="sxs-lookup"><span data-stu-id="9eee5-187">It must be used in conjunction with the *typeNameId* value of "6", denoting a string table entry resource type.</span></span><br/> <span data-ttu-id="9eee5-188">Le stringhe vengono archiviate in blocchi di 16 in una tabella di stringhe.</span><span class="sxs-lookup"><span data-stu-id="9eee5-188">Strings are stored in blocks of 16 in a string table.</span></span> <span data-ttu-id="9eee5-189">Le stringhe da 0 a 15, ad esempio, vengono archiviate in un singolo blocco di elementi di risorsa ed è possibile farvi riferimento nel file di configurazione delle risorse come *ItemId* 1 o come *stringId* "0-15".</span><span class="sxs-lookup"><span data-stu-id="9eee5-189">For example, strings 0 to 15 are stored in a single resource item block and can be referenced in the resource configuration file as *itemId* 1, or as *stringId* "0-15".</span></span> <span data-ttu-id="9eee5-190">Se ad esempio sono presenti cinque stringhe localizzabili e tre stringhe non localizzabili, è necessario assegnare gli identificatori di stringa 0-4 per le stringhe localizzabili e gli identificatori di stringa 16-18 per le stringhe non localizzabili.</span><span class="sxs-lookup"><span data-stu-id="9eee5-190">For example, if there are five localizable strings and three nonlocalizable strings, you should assign string identifiers 0-4 for the localizable strings, and string identifiers 16-18 for the nonlocalizable strings.</span></span> <span data-ttu-id="9eee5-191">Se non si organizzano stringhe in questo modo, i blocchi di stringhe interessati vengono inseriti sia nel file di risorse che nel file di risorse specifico del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="9eee5-191">If you do not organize strings this way, the affected blocks of strings are placed in both the LN file and the language-specific resource file.</span></span><br/> |



 

<span data-ttu-id="9eee5-192">Se si specificano gli attributi *ItemName*, *ItemId* e/o *stringId* per un determinato tipo di risorsa nell'elemento localizedResource, solo gli elementi o le stringhe specificate per il tipo di risorsa designato vengono inseriti nel file di risorse specifico della lingua.</span><span class="sxs-lookup"><span data-stu-id="9eee5-192">If you specify the *itemName*, *itemId*, and/or *stringId* attributes for a particular resource type under the localizedResource element, only these specified items or strings for the designated resource type are placed in the language-specific resource file.</span></span> <span data-ttu-id="9eee5-193">Se viene specificato un elemento resourceType senza un nome di elemento esplicito, un identificatore di elemento o un identificatore di stringa, tutti gli elementi del tipo di risorsa specificato vengono inseriti nel file di risorse specifico del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="9eee5-193">If a resourceType element is specified without any explicit item name, item identifier, or string identifier, all items of the specified resource type are placed in the language-specific resource file.</span></span> <span data-ttu-id="9eee5-194">Gli elementi o i tipi non elencati in nessun elemento localizedResource vengono inseriti nel file LN.</span><span class="sxs-lookup"><span data-stu-id="9eee5-194">Items or types not listed in any localizedResource element are placed in the LN file.</span></span>

<span data-ttu-id="9eee5-195">Di seguito sono riportati i tipi di risorse standard e i relativi identificatori numerici:</span><span class="sxs-lookup"><span data-stu-id="9eee5-195">The following are the standard resource types and their numeric identifiers:</span></span>

-   <span data-ttu-id="9eee5-196">CURSORE (1)</span><span class="sxs-lookup"><span data-stu-id="9eee5-196">CURSOR(1)</span></span>
-   <span data-ttu-id="9eee5-197">BITMAP (2)</span><span class="sxs-lookup"><span data-stu-id="9eee5-197">BITMAP(2)</span></span>
-   <span data-ttu-id="9eee5-198">ICONA (3)</span><span class="sxs-lookup"><span data-stu-id="9eee5-198">ICON(3)</span></span>
-   <span data-ttu-id="9eee5-199">MENU (4)</span><span class="sxs-lookup"><span data-stu-id="9eee5-199">MENU(4)</span></span>
-   <span data-ttu-id="9eee5-200">FINESTRA DI DIALOGO (5)</span><span class="sxs-lookup"><span data-stu-id="9eee5-200">DIALOG(5)</span></span>
-   <span data-ttu-id="9eee5-201">STRINGA (6)</span><span class="sxs-lookup"><span data-stu-id="9eee5-201">STRING(6)</span></span>
-   <span data-ttu-id="9eee5-202">FONTDIR (7)</span><span class="sxs-lookup"><span data-stu-id="9eee5-202">FONTDIR(7)</span></span>
-   <span data-ttu-id="9eee5-203">CARATTERE (8)</span><span class="sxs-lookup"><span data-stu-id="9eee5-203">FONT(8)</span></span>
-   <span data-ttu-id="9eee5-204">ACCELERATORI (9)</span><span class="sxs-lookup"><span data-stu-id="9eee5-204">ACCELERATORS(9)</span></span>
-   <span data-ttu-id="9eee5-205">RCDATA (10)</span><span class="sxs-lookup"><span data-stu-id="9eee5-205">RCDATA(10)</span></span>
-   <span data-ttu-id="9eee5-206">MESSAGETABLE (11)</span><span class="sxs-lookup"><span data-stu-id="9eee5-206">MESSAGETABLE(11)</span></span>
-   <span data-ttu-id="9eee5-207">\_Cursore gruppo (12)</span><span class="sxs-lookup"><span data-stu-id="9eee5-207">GROUP\_CURSOR(12)</span></span>
-   <span data-ttu-id="9eee5-208">Icona di gruppo \_ (14)</span><span class="sxs-lookup"><span data-stu-id="9eee5-208">GROUP\_ICON(14)</span></span>
-   <span data-ttu-id="9eee5-209">VERSIONE (16)</span><span class="sxs-lookup"><span data-stu-id="9eee5-209">VERSION(16)</span></span>
-   <span data-ttu-id="9eee5-210">HTML (23)</span><span class="sxs-lookup"><span data-stu-id="9eee5-210">HTML(23)</span></span>

## <a name="example"></a><span data-ttu-id="9eee5-211">Esempio</span><span class="sxs-lookup"><span data-stu-id="9eee5-211">Example</span></span>


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>
  <resources>
    <win32Resources fileType="Application">
      <neutralResources>
        <resourceType
           typeNameId="#16"
        />
      </neutralResources>
      <localizedResources> 
         <resourceType
                typeNameId="#2"
                itemId="5 6 7 8 9 10 11 12"
                itemName="HTML PRI"
         />
         <resourceType
                typeNameId="#4"
         />
         <resourceType
                typeNameId="#5"
         />
         <resourceType
                typeNameId="#6"
         />
         <resourceType
                typeNameId="#9"
         />
         <resourceType
                typeNameId="#11"
         />
         <resourceType
                typeNameId="#16"
         />
         <resourceType
                typeNameId="HTML"
         />
         <resourceType
                typeNameId="#23"
         />
         <resourceType
                typeNameId="#240"
         />
         <resourceType
                typeNameId="#1024"
         />
         <resourceType
                typeNameId="MY_TYPE"
         />
      </localizedResources> 
    </win32Resources>
  </resources>
</localization>
```



## <a name="remarks"></a><span data-ttu-id="9eee5-212">Commenti</span><span class="sxs-lookup"><span data-stu-id="9eee5-212">Remarks</span></span>

<span data-ttu-id="9eee5-213">Se si include un tipo di risorsa ICON (3), DIALOG (5), STRING (6) o VERSION (16) nell'elemento neutralResources, è necessario duplicare tale voce nell'elemento localizedResources.</span><span class="sxs-lookup"><span data-stu-id="9eee5-213">If you include any ICON(3), DIALOG(5), STRING(6), or VERSION(16) resource type in the neutralResources element, then you have to duplicate that entry in the localizedResources element.</span></span> <span data-ttu-id="9eee5-214">È possibile osservare questo aspetto nell'esempio precedente, in cui il tipo di risorsa 16 viene visualizzato nelle sezioni risorse neutre e localizzate.</span><span class="sxs-lookup"><span data-stu-id="9eee5-214">You can see this illustrated in the example above, where resource type 16 appears in both neutral and localized resources sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9eee5-215">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9eee5-215">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9eee5-216">Preparazione delle risorse</span><span class="sxs-lookup"><span data-stu-id="9eee5-216">Preparing Resources</span></span>](preparing-resources.md)
</dt> </dl>

 

 




