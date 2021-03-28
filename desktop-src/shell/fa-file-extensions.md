---
description: La registrazione di un tipo di file è il primo passaggio per la creazione di un'associazione di file, che rende il tipo di file &\# 0034, noto&\# 0034; alla Shell. Tuttavia, senza gestori di tipi di file, la shell non è in grado di esporre le informazioni all'utente da e sul file.
ms.assetid: c0c5c3ef-35ff-4ab6-bb8a-1f0640109d50
title: Gestori di tipi di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cba365b6eb704def7644002b8a87c3842b62aa77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879010"
---
# <a name="file-type-handlers"></a><span data-ttu-id="17c88-104">Gestori di tipi di file</span><span class="sxs-lookup"><span data-stu-id="17c88-104">File Type Handlers</span></span>

<span data-ttu-id="17c88-105">La [registrazione di un tipo di file](fa-how-work.md) è il primo passaggio nella creazione di un'associazione di file che rende il tipo di file "noto" alla Shell.</span><span class="sxs-lookup"><span data-stu-id="17c88-105">[Registering a file type](fa-how-work.md) is the first step in creating a file association, which makes that file type "known" to the Shell.</span></span> <span data-ttu-id="17c88-106">Tuttavia, senza gestori di tipi di file, la shell non è in grado di esporre le informazioni all'utente da e sul file.</span><span class="sxs-lookup"><span data-stu-id="17c88-106">However, without file type handlers, the Shell is unable to expose information to the user from and about the file.</span></span>

<span data-ttu-id="17c88-107">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="17c88-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="17c88-108">Creare un tipo di file noto a Shell</span><span class="sxs-lookup"><span data-stu-id="17c88-108">Make a File Type Known to Shell</span></span>](#make-a-file-type-known-to-shell)
-   [<span data-ttu-id="17c88-109">Descrizioni del gestore dei tipi di file</span><span class="sxs-lookup"><span data-stu-id="17c88-109">File Type Handler Descriptions</span></span>](#file-type-handler-descriptions)
-   [<span data-ttu-id="17c88-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="17c88-110">Related topics</span></span>](#related-topics)

## <a name="make-a-file-type-known-to-shell"></a><span data-ttu-id="17c88-111">Creare un tipo di file noto a Shell</span><span class="sxs-lookup"><span data-stu-id="17c88-111">Make a File Type Known to Shell</span></span>

<span data-ttu-id="17c88-112">Nello screenshot seguente di Esplora risorse, il file di immagine Desert. known viene visualizzato nella libreria di **Immagini** della shell ed è associato solo all'applicazione Paint.</span><span class="sxs-lookup"><span data-stu-id="17c88-112">In the following screen shot of Windows Explorer, the image file Desert.known appears in the Shell **Pictures** library, and is associated only with the Paint application.</span></span>

![cattura di schermata che Mostra Esplora risorse aprendo un'immagine senza tipo di file](images/file-assoc/fileassoc-filetypehandler.png)

<span data-ttu-id="17c88-114">Il file Desert. known nello screenshot precedente non dispone delle funzionalità seguenti, abilitate da un gestore di tipi di file:</span><span class="sxs-lookup"><span data-stu-id="17c88-114">The Desert.known file in the preceding screen shot lacks the following functionality that is enabled by a file type handler:</span></span>

-   <span data-ttu-id="17c88-115">Anteprima o anteprima</span><span class="sxs-lookup"><span data-stu-id="17c88-115">Thumbnail or preview</span></span>
-   <span data-ttu-id="17c88-116">Verbi specifici dell'immagine nel menu di scelta rapida, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="17c88-116">Image-specific verbs in the shortcut menu, such as:</span></span>
    -   <span data-ttu-id="17c88-117">Ruota anteprima</span><span class="sxs-lookup"><span data-stu-id="17c88-117">Rotate Preview</span></span>
    -   <span data-ttu-id="17c88-118">Imposta come sfondo del desktop</span><span class="sxs-lookup"><span data-stu-id="17c88-118">Set as Desktop Background</span></span>
    -   <span data-ttu-id="17c88-119">Stampa</span><span class="sxs-lookup"><span data-stu-id="17c88-119">Print</span></span>
-   <span data-ttu-id="17c88-120">Proprietà specifiche dell'immagine nel riquadro dei **Dettagli** , ad esempio:</span><span class="sxs-lookup"><span data-stu-id="17c88-120">Image-specific properties in the **Details** pane, such as:</span></span>
    -   <span data-ttu-id="17c88-121">Data di inizio</span><span class="sxs-lookup"><span data-stu-id="17c88-121">Date Taken</span></span>
    -   <span data-ttu-id="17c88-122">Tag</span><span class="sxs-lookup"><span data-stu-id="17c88-122">Tags</span></span>
    -   <span data-ttu-id="17c88-123">Classificazione</span><span class="sxs-lookup"><span data-stu-id="17c88-123">Rating</span></span>
-   <span data-ttu-id="17c88-124">Indicizzazione del testo del file</span><span class="sxs-lookup"><span data-stu-id="17c88-124">Indexing of file text</span></span>

<span data-ttu-id="17c88-125">Nello screenshot seguente, lo stesso file (Desert. known) presenta l'estensione. jpg, ovvero un tipo di file registrato con gestori di tipi di file associati, quindi vengono visualizzate un'immagine di anteprima e altre proprietà.</span><span class="sxs-lookup"><span data-stu-id="17c88-125">In the following screen shot, the same file (Desert.known) has the .jpg extension, which is a registered file type that has associated file type handlers, so a thumbnail image and more properties are shown.</span></span>

![immagine con un tipo di file registrato e gestori di tipi di file associati](images/file-assoc/fileassoc-filetypehandler-2ndex.png)

## <a name="file-type-handler-descriptions"></a><span data-ttu-id="17c88-127">Descrizioni del gestore dei tipi di file</span><span class="sxs-lookup"><span data-stu-id="17c88-127">File Type Handler Descriptions</span></span>

<span data-ttu-id="17c88-128">La funzionalità fornita da ogni gestore dei tipi di file è elencata nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="17c88-128">The functionality provided by each file type handler is listed in the following table:</span></span>



| <span data-ttu-id="17c88-129">Gestore</span><span class="sxs-lookup"><span data-stu-id="17c88-129">Handler</span></span>                                                      | <span data-ttu-id="17c88-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17c88-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17c88-131">Menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="17c88-131">Shortcut menu</span></span>](context-menu-handlers.md)                   | <span data-ttu-id="17c88-132">Un gestore di menu di scelta rapida, talvolta definito gestore di menu di scelta rapida, è un gestore di tipi di file che aggiunge comandi a un menu di scelta rapida esistente.</span><span class="sxs-lookup"><span data-stu-id="17c88-132">A shortcut menu handler, sometimes referred to as a context menu handler, is a file type handler that adds commands to an existing context menu.</span></span> <span data-ttu-id="17c88-133">Questi gestori sono associati a un tipo di file specifico e vengono chiamati ogni volta che viene visualizzato un menu di scelta rapida per un membro del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="17c88-133">These handlers are associated with a particular file type and are called any time a context menu is displayed for a member of the file type.</span></span>                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="17c88-134">Anteprima</span><span class="sxs-lookup"><span data-stu-id="17c88-134">Thumbnail</span></span>](thumbnail-providers.md)                         | <span data-ttu-id="17c88-135">Gestore che fornisce un'immagine per rappresentare un elemento della shell.</span><span class="sxs-lookup"><span data-stu-id="17c88-135">A handler that provides an image to represent a Shell item.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="17c88-136">Proprietà</span><span class="sxs-lookup"><span data-stu-id="17c88-136">Property</span></span>](../properties/building-property-handlers-properties.md) | <span data-ttu-id="17c88-137">Gestore di proprietà che fornisce l'accesso alle proprietà degli elementi per Windows Search, Esplora risorse e altre applicazioni che devono accedere alle proprietà.</span><span class="sxs-lookup"><span data-stu-id="17c88-137">A property handler that provides access to item properties for Windows Search, the Windows Explorer and other applications that need to access properties.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="17c88-138">Anteprima</span><span class="sxs-lookup"><span data-stu-id="17c88-138">Preview</span></span>](preview-handlers.md)                              | <span data-ttu-id="17c88-139">Gestore che produce rapidamente una visualizzazione semplificata e di sola lettura dell'elemento da visualizzare nel riquadro di anteprima di Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="17c88-139">A handler that quickly produces a read-only, simplified view of the item to be displayed in the Windows Explorer preview pane.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="17c88-140">Filtri</span><span class="sxs-lookup"><span data-stu-id="17c88-140">Filters</span></span>](../search/-search-3x-wds-extidx-filters.md)              | <span data-ttu-id="17c88-141">Un filtro, un'implementazione dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , che analizza i documenti per il testo e le proprietà (detti anche attributi).</span><span class="sxs-lookup"><span data-stu-id="17c88-141">A filter, an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface, that scans documents for text and properties (also called attributes).</span></span> <span data-ttu-id="17c88-142">Estrae blocchi di testo da questi documenti, filtrando la formattazione incorporata e mantenendo le informazioni sulla posizione del testo.</span><span class="sxs-lookup"><span data-stu-id="17c88-142">It extracts chunks of text from these documents, filtering out embedded formatting and retaining information about the position of the text.</span></span> <span data-ttu-id="17c88-143">Estrae anche i blocchi di valori, ovvero le proprietà di un intero documento o di parti ben definite di un documento.</span><span class="sxs-lookup"><span data-stu-id="17c88-143">It also extracts chunks of values, which are properties of an entire document or of well defined parts of a document.</span></span> <span data-ttu-id="17c88-144">**IFilter** fornisce le basi per la creazione di applicazioni di livello superiore, ad esempio indicizzatori di documenti e visualizzatori indipendenti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="17c88-144">**IFilter** provides the foundation for building higher-level applications such as document indexers and application-independent viewers.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="17c88-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="17c88-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17c88-146">Registrazione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="17c88-146">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="17c88-147">Tipi di file</span><span class="sxs-lookup"><span data-stu-id="17c88-147">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="17c88-148">Funzionamento delle associazioni di file</span><span class="sxs-lookup"><span data-stu-id="17c88-148">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="17c88-149">Visualizzazione contenuto per tipo di file o tipo</span><span class="sxs-lookup"><span data-stu-id="17c88-149">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="17c88-150">Tipo di file Verifier</span><span class="sxs-lookup"><span data-stu-id="17c88-150">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="17c88-151">Identificatori a livello di codice</span><span class="sxs-lookup"><span data-stu-id="17c88-151">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="17c88-152">Tipi percepiti</span><span class="sxs-lookup"><span data-stu-id="17c88-152">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="17c88-153">Matrici di associazione</span><span class="sxs-lookup"><span data-stu-id="17c88-153">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
