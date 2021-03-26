---
description: Una matrice di associazioni è un elenco ordinato di percorsi del registro di sistema usati per archiviare le informazioni su un tipo di elemento, inclusi gestori, verbi e altri attributi, come l'icona e il nome visualizzato del tipo.
title: Matrici di associazione
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9ECD19CA-833E-4565-A0EF-FB16BF7B3F44
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 75d42a8758e5c6380414c7b93979b4f93cafd013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128887"
---
# <a name="association-arrays"></a><span data-ttu-id="c44f0-103">Matrici di associazione</span><span class="sxs-lookup"><span data-stu-id="c44f0-103">Association Arrays</span></span>

<span data-ttu-id="c44f0-104">Una matrice di associazioni è un elenco ordinato di percorsi del registro di sistema usati per archiviare le informazioni su un tipo di elemento, inclusi gestori, verbi e altri attributi, come l'icona e il nome visualizzato del tipo.</span><span class="sxs-lookup"><span data-stu-id="c44f0-104">An association array is an ordered list of registry locations used to store information about an item type, including handlers, verbs, and other attributes like the icon and display name of the type.</span></span> <span data-ttu-id="c44f0-105">La shell USA matrici di associazione per eseguire una query su un set predefinito di percorsi del registro di sistema che potrebbero contenere informazioni su un elemento della shell.</span><span class="sxs-lookup"><span data-stu-id="c44f0-105">The Shell uses association arrays to query a predefined set of registry locations that might contain information about a Shell item.</span></span>

<span data-ttu-id="c44f0-106">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="c44f0-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="c44f0-107">Informazioni sulle matrici di associazione</span><span class="sxs-lookup"><span data-stu-id="c44f0-107">About Association Arrays</span></span>](#about-association-arrays)
-   [<span data-ttu-id="c44f0-108">Esecuzione di query su matrici di associazione</span><span class="sxs-lookup"><span data-stu-id="c44f0-108">Querying Association Arrays</span></span>](#querying-association-arrays)
-   [<span data-ttu-id="c44f0-109">Utilizzo di matrici di associazione per una determinata origine dati della shell</span><span class="sxs-lookup"><span data-stu-id="c44f0-109">Working with Association Arrays for a Particular Shell Data Source</span></span>](#working-with-association-arrays-for-a-particular-shell-data-source)
    -   [<span data-ttu-id="c44f0-110">Matrici di associazioni di origini dati della shell</span><span class="sxs-lookup"><span data-stu-id="c44f0-110">Shell Data Source Association Arrays</span></span>](#shell-data-source-association-arrays)
-   [<span data-ttu-id="c44f0-111">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="c44f0-111">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="c44f0-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c44f0-112">Related topics</span></span>](#related-topics)

## <a name="about-association-arrays"></a><span data-ttu-id="c44f0-113">Informazioni sulle matrici di associazione</span><span class="sxs-lookup"><span data-stu-id="c44f0-113">About Association Arrays</span></span>

<span data-ttu-id="c44f0-114">Una matrice di associazioni è un elenco ordinato di percorsi del registro di sistema che contengono informazioni su un tipo di elemento, inclusi gestori, verbi e altri attributi, ad esempio l'icona e il nome visualizzato del tipo.</span><span class="sxs-lookup"><span data-stu-id="c44f0-114">An association array is an ordered list of registry locations that contain information about an item type, including handlers, verbs, and other attributes such as the icon and display name of the type.</span></span> <span data-ttu-id="c44f0-115">Queste informazioni sul tipo di elemento possono essere registrate a diversi livelli di specificità.</span><span class="sxs-lookup"><span data-stu-id="c44f0-115">This information about the item type can be registered at varying levels of specificity.</span></span> <span data-ttu-id="c44f0-116">È ad esempio possibile registrare un verbo che sarà visualizzato solo per un tipo di file specifico, ad esempio. jpg, oppure per tutti gli elementi con lo stesso sistema. Kind (ad esempio, System. Kind = immagine) o per tutti gli elementi.</span><span class="sxs-lookup"><span data-stu-id="c44f0-116">For example, you can register a verb that will show up only for a specific file type (such as .jpg), or for all items with the same System.Kind (for example, System.kind = picture), or for all items.</span></span>

<span data-ttu-id="c44f0-117">La shell USA matrici di associazione per eseguire una query su un set predefinito di percorsi del registro di sistema che potrebbero potenzialmente contenere informazioni sull'elemento.</span><span class="sxs-lookup"><span data-stu-id="c44f0-117">The Shell uses association arrays to query a predefined set of registry locations that might potentially contain information about the item.</span></span> <span data-ttu-id="c44f0-118">Le API di Association array possono essere usate per recuperare dalla sottochiave del registro di sistema un singolo valore che contiene le informazioni richieste, con tale valore proveniente dalla prima voce della matrice che lo fornisce.</span><span class="sxs-lookup"><span data-stu-id="c44f0-118">The association array APIs can be used to retrieve from the registry subkey a single value that contains the requested information, with that value coming from the first entry in the array that provides it.</span></span> <span data-ttu-id="c44f0-119">Il valore predefinito dell'icona, ad esempio, viene recuperato in questo modo.</span><span class="sxs-lookup"><span data-stu-id="c44f0-119">For example, the default icon value is retrieved this way.</span></span> <span data-ttu-id="c44f0-120">La matrice di associazioni può essere utilizzata anche per recuperare un set di valori archiviati nelle sottochiavi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c44f0-120">The association array can also be used to retrieve a set of values that are stored in the registry subkeys.</span></span> <span data-ttu-id="c44f0-121">Ad esempio, l'elenco dei verbi viene compilato da quei verbi registrati in tutte le sottochiavi.</span><span class="sxs-lookup"><span data-stu-id="c44f0-121">For example, the list of verbs is built from those verbs that are registered under all the subkeys.</span></span>

<span data-ttu-id="c44f0-122">Quando la shell esegue una query su un set predefinito di percorsi del registro di sistema per ottenere informazioni su un elemento della shell, inserisce i percorsi del registro di sistema in una matrice in ordine dalla posizione più specifica alla più generale.</span><span class="sxs-lookup"><span data-stu-id="c44f0-122">After the Shell queries a predefined set of registry locations for information about a Shell item, it puts the registry locations into an array in order from the most specific location to the most general.</span></span>

<span data-ttu-id="c44f0-123">Poiché le matrici di associazione sono elenchi ordinati, forniscono agli sviluppatori di applicazioni un meccanismo per l'aggiunta di informazioni al registro di sistema che verranno restituite per un tipo specifico di elemento.</span><span class="sxs-lookup"><span data-stu-id="c44f0-123">Because association arrays are ordered lists, they provide application developers with a mechanism for adding information to the registry that will be returned for a specific type of item.</span></span> <span data-ttu-id="c44f0-124">Analogamente, gli array di associazioni consentono agli sviluppatori di applicazioni di aggiungere informazioni al registro di sistema per un gruppo specifico di elementi quando tali elementi sono registrati in una posizione più generale.</span><span class="sxs-lookup"><span data-stu-id="c44f0-124">Likewise, association arrays permit application developers to add information to the registry for a specific group of items when those items are registered at a more general location.</span></span> <span data-ttu-id="c44f0-125">Questa logica informa la decisione sulla posizione più appropriata nel registro di sistema per archiviare le informazioni sugli elementi della shell.</span><span class="sxs-lookup"><span data-stu-id="c44f0-125">This logic informs your decision about the most appropriate location in the registry to store information about Shell items.</span></span>

<span data-ttu-id="c44f0-126">In un sistema Windows predefinito, un file con estensione jpg presenta la seguente matrice di associazioni:</span><span class="sxs-lookup"><span data-stu-id="c44f0-126">On a default Windows system a .jpg file has the following association array:</span></span>

-   <span data-ttu-id="c44f0-127">**HKEY \_ Jpgfile \_ radice classi** \\ </span><span class="sxs-lookup"><span data-stu-id="c44f0-127">**HKEY\_CLASSES\_ROOT**\\**jpgfile**</span></span>
-   <span data-ttu-id="c44f0-128">**HKEY \_ Classi \_ radice** \\ **SystemFileAssociations** \\ **. jpg**</span><span class="sxs-lookup"><span data-stu-id="c44f0-128">**HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations**\\ **.jpg**</span></span>
-   <span data-ttu-id="c44f0-129">**HKEY \_ Immagine \_ radice classi** \\ </span><span class="sxs-lookup"><span data-stu-id="c44f0-129">**HKEY\_CLASSES\_ROOT**\\**image**</span></span>
-   <span data-ttu-id="c44f0-130">**HKEY \_ \_radice classi** \\ \* *\** _</span><span class="sxs-lookup"><span data-stu-id="c44f0-130">**HKEY\_CLASSES\_ROOT**\\**\** _</span></span>
-   <span data-ttu-id="c44f0-131">_ *HKEY \_ classi \_ radice **\\** AllFilesystemObjects*\*</span><span class="sxs-lookup"><span data-stu-id="c44f0-131">_ *HKEY\_CLASSES\_ROOT **\\** AllFilesystemObjects*\*</span></span>

<span data-ttu-id="c44f0-132">Per informazioni sulla registrazione di matrici di associazione, vedere [registrazione dell'applicazione](app-registration.md).</span><span class="sxs-lookup"><span data-stu-id="c44f0-132">For information on registering association arrays, see [Application Registration](app-registration.md).</span></span>

## <a name="querying-association-arrays"></a><span data-ttu-id="c44f0-133">Esecuzione di query su matrici di associazione</span><span class="sxs-lookup"><span data-stu-id="c44f0-133">Querying Association Arrays</span></span>

<span data-ttu-id="c44f0-134">Sono disponibili API shell per recuperare informazioni da un intervallo di sottochiavi del registro di sistema, dalla sottochiave del registro di sistema più specifica a un superset delle informazioni in tutte le sottochiavi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c44f0-134">There are Shell APIs to retrieve information from a range of registry subkeys, from the most specific registry subkey to a superset of the information across all registry subkeys.</span></span>

<span data-ttu-id="c44f0-135">L'uso più comune di una matrice di associazioni consiste nell'eseguire una query per ottenere un singolo valore restituito dalla Shell dall'elemento più specifico della matrice con le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="c44f0-135">The most common use of an association array is to query for a single value that the Shell returns from the most specific element in the array that has the requested information.</span></span> <span data-ttu-id="c44f0-136">Nell'esempio di codice riportato di seguito viene illustrato come eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="c44f0-136">The following code example shows how to do that.</span></span>


```
IQueryAssociations *pqa;

// pShellItem is assumed to be an existing IShellItem object.
hr = pShellItem->BindToHandler(NULL, BHID_AssociationArray, IID_PPV_ARGS(&pqa));
if (SUCCEEDED(hr))
{
    wchar_t szValue[256];
    DWORD cbValue = sizeof(szValue);      // Count of bytes in the array

    hr = pqa->GetData(0, ASSOCDATA_VALUE, L"InfoTip", szValue, &cbValue);
    if (SUCCEEDED(hr))
    {
        // The "InfoTip" value is used to compute the infotip string from
        // properties of an item.
    }
    pqa->Release();
}
```



<span data-ttu-id="c44f0-137">Le API seguenti possono essere utilizzate per eseguire una query su una matrice di associazioni o per costruire un oggetto [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) della matrice di associazione su cui è possibile eseguire una query:</span><span class="sxs-lookup"><span data-stu-id="c44f0-137">The following APIs can be used to query an association array or to construct an association array [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) object that can be queried:</span></span>

-   <span data-ttu-id="c44f0-138">[**AssocCreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate) (prima di Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="c44f0-138">[**AssocCreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate) (prior to Windows Vista)</span></span>
-   [<span data-ttu-id="c44f0-139">**AssocCreateForClasses**</span><span class="sxs-lookup"><span data-stu-id="c44f0-139">**AssocCreateForClasses**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses)
-   [<span data-ttu-id="c44f0-140">**AssocQueryString**</span><span class="sxs-lookup"><span data-stu-id="c44f0-140">**AssocQueryString**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringa)

## <a name="working-with-association-arrays-for-a-particular-shell-data-source"></a><span data-ttu-id="c44f0-141">Utilizzo di matrici di associazione per una determinata origine dati della shell</span><span class="sxs-lookup"><span data-stu-id="c44f0-141">Working with Association Arrays for a Particular Shell Data Source</span></span>

<span data-ttu-id="c44f0-142">Ogni origine dati della shell definisce la matrice di associazioni per i relativi elementi.</span><span class="sxs-lookup"><span data-stu-id="c44f0-142">Each Shell data source defines the association array for its items.</span></span> <span data-ttu-id="c44f0-143">La definizione di una matrice di associazioni è in genere una funzione del tipo di elemento.</span><span class="sxs-lookup"><span data-stu-id="c44f0-143">Defining an association array is usually a function of the type of item.</span></span> <span data-ttu-id="c44f0-144">Gli implementatori di origini dati della shell devono definire e documentare le matrici di associazione per consentire alle applicazioni di estendere il comportamento di tali tipi, ad esempio per la registrazione di verbi o altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="c44f0-144">Shell data source implementers should define and document the association arrays to enable applications to extend the behavior of those types, such as for registering verbs or other information.</span></span> <span data-ttu-id="c44f0-145">Le applicazioni possono estendere il comportamento degli elementi in base all'aggiunta di dati alle sottochiavi di matrice di associazione, ad esempio l'aggiunta di verbi per gli elementi.</span><span class="sxs-lookup"><span data-stu-id="c44f0-145">Applications can extend the behavior of items based on adding data to the association array subkeys, such as adding verbs for items.</span></span>

<span data-ttu-id="c44f0-146">L'origine dati file system compila una matrice di associazioni per i file in base alle sottochiavi del registro di sistema e ai ProgID speciali seguenti:</span><span class="sxs-lookup"><span data-stu-id="c44f0-146">The file system data source builds an association array for files based on the following registry subkeys and special ProgIDs:</span></span>

-   <span data-ttu-id="c44f0-147">Se il file ha un ProgID registrato, viene usato il ProgID **\_ \_ radice delle classi HKEY** \\  .</span><span class="sxs-lookup"><span data-stu-id="c44f0-147">If the file has a registered ProgID, **HKEY\_CLASSES\_ROOT**\\*ProgID* is used.</span></span> <span data-ttu-id="c44f0-148">In caso contrario, vengono usate **\_ le classi HKEY \_ radice** \\ **sconosciuta** .</span><span class="sxs-lookup"><span data-stu-id="c44f0-148">Otherwise **HKEY\_CLASSES\_ROOT**\\**Unknown** is used.</span></span>
-   <span data-ttu-id="c44f0-149">L'estensione del nome file è registrata in **HKEY \_ classi \_ radice** \\ **SystemFileAssociations** \\ *. FileExtension* sottochiave.</span><span class="sxs-lookup"><span data-stu-id="c44f0-149">The file name extension is registered under **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations**\\ *.fileExtension* subkey.</span></span>
-   <span data-ttu-id="c44f0-150">Nella tabella seguente sono riportati i ProgID speciali.</span><span class="sxs-lookup"><span data-stu-id="c44f0-150">Special ProgIDs are shown in the following table.</span></span> 

    | <span data-ttu-id="c44f0-151">ProgID speciale</span><span class="sxs-lookup"><span data-stu-id="c44f0-151">Special progID</span></span>                                    | <span data-ttu-id="c44f0-152">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c44f0-152">Description</span></span>                   |
    |---------------------------------------------------|-------------------------------|
    | <span data-ttu-id="c44f0-153">**HKEY \_ \_radice classi** \\ \* *\** _</span><span class="sxs-lookup"><span data-stu-id="c44f0-153">**HKEY\_CLASSES\_ROOT**\\**\** _</span></span>                   | <span data-ttu-id="c44f0-154">Tutti i file (non cartelle)</span><span class="sxs-lookup"><span data-stu-id="c44f0-154">All files (non-folders)</span></span>       |
    | <span data-ttu-id="c44f0-155">_ *HKEY \_ classi \_ radice **\\** AllFilesystemObjects*\*</span><span class="sxs-lookup"><span data-stu-id="c44f0-155">_ *HKEY\_CLASSES\_ROOT **\\** AllFilesystemObjects*\*</span></span> | <span data-ttu-id="c44f0-156">File e cartelle di file system</span><span class="sxs-lookup"><span data-stu-id="c44f0-156">Files and file system folders</span></span> |
    | <span data-ttu-id="c44f0-157">**HKEY \_ Directory \_ radice classi** \\ </span><span class="sxs-lookup"><span data-stu-id="c44f0-157">**HKEY\_CLASSES\_ROOT**\\**Directory**</span></span>            | <span data-ttu-id="c44f0-158">Cartelle del file System</span><span class="sxs-lookup"><span data-stu-id="c44f0-158">File system folders</span></span>           |
    | <span data-ttu-id="c44f0-159">**HKEY \_ Cartella \_ radice classi** \\ </span><span class="sxs-lookup"><span data-stu-id="c44f0-159">**HKEY\_CLASSES\_ROOT**\\**Folder**</span></span>               | <span data-ttu-id="c44f0-160">Contenitori della shell</span><span class="sxs-lookup"><span data-stu-id="c44f0-160">Shell containers</span></span>              |

    

     

### <a name="shell-data-source-association-arrays"></a><span data-ttu-id="c44f0-161">Matrici di associazioni di origini dati della shell</span><span class="sxs-lookup"><span data-stu-id="c44f0-161">Shell Data Source Association Arrays</span></span>

<span data-ttu-id="c44f0-162">Nell'elenco seguente sono riportate alcune delle matrici di associazioni dell'archivio dati della shell che possono essere utilizzate per gli scopi descritti in questo argomento:</span><span class="sxs-lookup"><span data-stu-id="c44f0-162">The following list represents some of the Shell data store association arrays that can be used for the purposes described in this topic:</span></span>

-   <span data-ttu-id="c44f0-163">**HKEY \_ \_radice classi** \\ \* *\** _</span><span class="sxs-lookup"><span data-stu-id="c44f0-163">**HKEY\_CLASSES\_ROOT**\\**\** _</span></span>
-   <span data-ttu-id="c44f0-164">_ *HKEY \_ classi \_ radice **\\** AllFilesystemObjects*\*</span><span class="sxs-lookup"><span data-stu-id="c44f0-164">_ *HKEY\_CLASSES\_ROOT **\\** AllFilesystemObjects*\*</span></span>
-   <span data-ttu-id="c44f0-165">**HKEY \_ \_Radice delle classi** \\ **Kind.Document**</span><span class="sxs-lookup"><span data-stu-id="c44f0-165">**HKEY\_CLASSES\_ROOT**\\**Kind.Document**</span></span>
-   <span data-ttu-id="c44f0-166">**HKEY \_ Risultati \_ radice classi** \\ </span><span class="sxs-lookup"><span data-stu-id="c44f0-166">**HKEY\_CLASSES\_ROOT**\\**Results**</span></span>
-   <span data-ttu-id="c44f0-167">**HKEY \_ Classi \_ radice** \\ **SystemFileAssociations** \\ **. docx**</span><span class="sxs-lookup"><span data-stu-id="c44f0-167">**HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations**\\ **.docx**</span></span>
-   <span data-ttu-id="c44f0-168">**HKEY \_ \_Radice delle classi** \\ **Word.Document. 12**</span><span class="sxs-lookup"><span data-stu-id="c44f0-168">**HKEY\_CLASSES\_ROOT**\\**Word.Document.12**</span></span>

<span data-ttu-id="c44f0-169">Le matrici di associazioni delle origini dati della shell che possono essere usate per DBFolder (un archivio dati della shell che rappresenta gli elementi nei risultati della ricerca e nelle viste basate su query) sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="c44f0-169">Shell data source association arrays that can be used for DBFolder (a Shell data store that represents items in search results and query-based views) are as follows:</span></span>

-   <span data-ttu-id="c44f0-170">Unità</span><span class="sxs-lookup"><span data-stu-id="c44f0-170">Drives</span></span>
-   <span data-ttu-id="c44f0-171">Rete</span><span class="sxs-lookup"><span data-stu-id="c44f0-171">Network</span></span>
-   <span data-ttu-id="c44f0-172">RegItems</span><span class="sxs-lookup"><span data-stu-id="c44f0-172">RegItems</span></span>
-   <span data-ttu-id="c44f0-173">Esempi:</span><span class="sxs-lookup"><span data-stu-id="c44f0-173">Examples:</span></span>
    -   <span data-ttu-id="c44f0-174">ContentView</span><span class="sxs-lookup"><span data-stu-id="c44f0-174">ContentView</span></span>
    -   <span data-ttu-id="c44f0-175">Verbi</span><span class="sxs-lookup"><span data-stu-id="c44f0-175">Verbs</span></span>

<span data-ttu-id="c44f0-176">Altre matrici di associazioni comuni includono cartella e stampanti.</span><span class="sxs-lookup"><span data-stu-id="c44f0-176">Other common association arrays include Folder and Printers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c44f0-177">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="c44f0-177">Additional Resources</span></span>

-   <span data-ttu-id="c44f0-178">Per creare un archivio dati della shell, vedere [Implementing the Basic Folder Object Interfaces](nse-implement.md).</span><span class="sxs-lookup"><span data-stu-id="c44f0-178">To create a Shell data store, see [Implementing the Basic Folder Object Interfaces](nse-implement.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c44f0-179">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c44f0-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c44f0-180">Registrazione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="c44f0-180">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="c44f0-181">Tipi di file</span><span class="sxs-lookup"><span data-stu-id="c44f0-181">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="c44f0-182">Funzionamento delle associazioni di file</span><span class="sxs-lookup"><span data-stu-id="c44f0-182">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="c44f0-183">Visualizzazione contenuto per tipo di file o tipo</span><span class="sxs-lookup"><span data-stu-id="c44f0-183">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="c44f0-184">Tipo di file Verifier</span><span class="sxs-lookup"><span data-stu-id="c44f0-184">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="c44f0-185">Gestori di tipi di file</span><span class="sxs-lookup"><span data-stu-id="c44f0-185">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="c44f0-186">Identificatori a livello di codice</span><span class="sxs-lookup"><span data-stu-id="c44f0-186">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="c44f0-187">Tipi percepiti</span><span class="sxs-lookup"><span data-stu-id="c44f0-187">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> </dl>

 

 
