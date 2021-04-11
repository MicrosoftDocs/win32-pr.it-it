---
description: In questo argomento vengono elencate le procedure consigliate per la creazione di un archivio dati basato sul Web in cui è possibile eseguire ricerche mediante la ricerca federata di Windows e l'integrazione delle origini dati remote con Esplora risorse senza dover scrivere o distribuire codice sul lato client di Windows.
ms.assetid: d9b62cf5-7236-4252-b88d-18120f50c62c
title: Procedure consigliate seguenti in ricerca federata di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed94f42b4470694209e37f5ede8a05d87a290d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128575"
---
# <a name="following-best-practices-in-windows-federated-search"></a><span data-ttu-id="7ae51-103">Procedure consigliate seguenti in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="7ae51-103">Following Best Practices in Windows Federated Search</span></span>

<span data-ttu-id="7ae51-104">In questo argomento vengono elencate le procedure consigliate per la creazione di un archivio dati basato sul Web in cui è possibile eseguire ricerche mediante la ricerca federata di Windows e l'integrazione delle origini dati remote con Esplora risorse senza dover scrivere o distribuire codice sul lato client di Windows.</span><span class="sxs-lookup"><span data-stu-id="7ae51-104">This topic lists the best practices through which you can build a web-based data store that can be searched using Windows federated search, and integrates your remote data sources with Windows Explorer without having to write or deploy any Windows client-side code.</span></span>

<span data-ttu-id="7ae51-105">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="7ae51-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="7ae51-106">Procedure consigliate per la ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="7ae51-106">Best Practices for Windows Federated Search</span></span>](#best-practices-for-windows-federated-search)
-   [<span data-ttu-id="7ae51-107">Procedure consigliate per la creazione di output RSS</span><span class="sxs-lookup"><span data-stu-id="7ae51-107">Best Practices for Creating RSS Output</span></span>](#best-practices-for-creating-rss-output)
-   [<span data-ttu-id="7ae51-108">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="7ae51-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="7ae51-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ae51-109">Related topics</span></span>](#related-topics)

## <a name="best-practices-for-windows-federated-search"></a><span data-ttu-id="7ae51-110">Procedure consigliate per la ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="7ae51-110">Best Practices for Windows Federated Search</span></span>

<span data-ttu-id="7ae51-111">Le procedure consigliate per l'utilizzo di [OpenSearch](https://github.com/dewitt/opensearch) in Windows 7 sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ae51-111">Best practices for working with [OpenSearch](https://github.com/dewitt/opensearch) in Windows 7 are as follows:</span></span>

-   <span data-ttu-id="7ae51-112">Supporta i parametri *{startIndex}* e *{count}* e assicurati di restituire sempre il numero di elementi richiesti a meno che non venga restituito l'ultimo risultato.</span><span class="sxs-lookup"><span data-stu-id="7ae51-112">Support the *{startIndex}* and *{count}* parameters, and be sure to always return the number of items requested unless you are returning the last of the results.</span></span>
-   <span data-ttu-id="7ae51-113">Se si conosce l'estensione del nome file, eseguirne il mapping alla proprietà della shell di Windows [System. FileExtension](../properties/props-system-fileextension.md) .</span><span class="sxs-lookup"><span data-stu-id="7ae51-113">If you know the file name extension, map it to the [System.FileExtension](../properties/props-system-fileextension.md) Windows Shell property.</span></span> <span data-ttu-id="7ae51-114">L'utilizzo delle estensioni di file è un modo migliore per identificare un tipo di file rispetto al tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="7ae51-114">Using file name extensions is a better way to identify a file type than MIME type.</span></span>
-   <span data-ttu-id="7ae51-115">Verificare che il tipo MIME o l'estensione di file specificata nel RSS corrisponda al nome file e al tipo MIME restituiti nell'intestazione HTTP dal server Web che ospita l'elemento quando viene richiesto il contenuto dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="7ae51-115">Ensure that the MIME type or file name extension that you specify in the RSS matches the file name and MIME type returned in the HTTP header by the web server that hosts the item when the item content is requested.</span></span>
-   <span data-ttu-id="7ae51-116">Se si restituiscono elementi di file, quando possibile, restituire una dimensione del file.</span><span class="sxs-lookup"><span data-stu-id="7ae51-116">If you are returning file items, return a file size whenever possible.</span></span> <span data-ttu-id="7ae51-117">In questo modo si garantisce che la finestra di dialogo stato del download sia accurata.</span><span class="sxs-lookup"><span data-stu-id="7ae51-117">This ensures that the download progress dialog box is accurate.</span></span>
-   <span data-ttu-id="7ae51-118">Verificare che le richieste di elementi oltre la fine del set di risultati non restituiscano risultati.</span><span class="sxs-lookup"><span data-stu-id="7ae51-118">Verify that requests for items beyond the end of the results set return no results.</span></span>
    > [!Note]  
    > <span data-ttu-id="7ae51-119">Non ripetere i risultati.</span><span class="sxs-lookup"><span data-stu-id="7ae51-119">Do not repeat results.</span></span>

     

-   <span data-ttu-id="7ae51-120">Non inserire tag HTML dove non appartengono.</span><span class="sxs-lookup"><span data-stu-id="7ae51-120">Do not put HTML tags where they don't belong.</span></span> <span data-ttu-id="7ae51-121">In base alla specifica RSS, sono validi nel campo Description, ma non nel campo title.</span><span class="sxs-lookup"><span data-stu-id="7ae51-121">Per the RSS specification, they are valid in the description field, but not in the title field.</span></span>
-   <span data-ttu-id="7ae51-122">Non creare enclosure per gli elementi della pagina Web.</span><span class="sxs-lookup"><span data-stu-id="7ae51-122">Do not create enclosures for webpage items.</span></span> <span data-ttu-id="7ae51-123">Se, ad esempio, si crea un'enclosure e si esegue il mapping di un'estensione di file con estensione aspx, il file viene scaricato da Esplora risorse nella cache Internet ed eseguito da tale finestra.</span><span class="sxs-lookup"><span data-stu-id="7ae51-123">For example, if you create an enclosure and map a file name extension of .aspx, the file is downloaded by Windows Explorer to the Internet cache and executed from there.</span></span> <span data-ttu-id="7ae51-124">I Web browser non gestiscono il tipo di file aspx.</span><span class="sxs-lookup"><span data-stu-id="7ae51-124">Web browsers do not handle the .aspx file type.</span></span> <span data-ttu-id="7ae51-125">L'utente otterrebbe una finestra di dialogo **Apri con** oppure il file potrebbe essere aperto da un'applicazione come Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7ae51-125">The user would get an **Open with** dialog box, or the file might be opened by an application like Microsoft Visual Studio.</span></span> <span data-ttu-id="7ae51-126">Per evitare questo problema, restituire un elemento link solo per le pagine Web.</span><span class="sxs-lookup"><span data-stu-id="7ae51-126">Avoid this by returning a link element only for webpages.</span></span>
-   <span data-ttu-id="7ae51-127">Fornire un URL di rollup Web nel file con estensione osdx usando un modello di URL con `format="text\html"` .</span><span class="sxs-lookup"><span data-stu-id="7ae51-127">Provide a web roll-over URL in the .osdx file using a URL template with `format="text\html"`.</span></span>
-   <span data-ttu-id="7ae51-128">Specificare un URL per la cartella padre, il contenitore o la pagina Web eseguendo il mapping di un valore di URL di elemento personalizzato alla proprietà della shell di Windows [System. ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) .</span><span class="sxs-lookup"><span data-stu-id="7ae51-128">Provide a URL to the parent folder, container, or webpage by mapping a custom element URL value to the [System.ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) Windows Shell property.</span></span>

## <a name="best-practices-for-creating-rss-output"></a><span data-ttu-id="7ae51-129">Procedure consigliate per la creazione di output RSS</span><span class="sxs-lookup"><span data-stu-id="7ae51-129">Best Practices for Creating RSS Output</span></span>

<span data-ttu-id="7ae51-130">Le procedure consigliate per la creazione dell'output RSS sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ae51-130">Best practices for creating RSS output are as follows:</span></span>

-   <span data-ttu-id="7ae51-131">Ogni elemento deve restituire un URL `link` o un `enclosure` valore (o equivalente, ad esempio `media:content` )</span><span class="sxs-lookup"><span data-stu-id="7ae51-131">Each item MUST return a URL `link` or `enclosure` value (or equivalent, such as `media:content`)</span></span>
-   <span data-ttu-id="7ae51-132">Non includere tag di formattazione HTML nell'attributo **title** oppure tali tag verranno visualizzati nel titolo e visualizzati in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="7ae51-132">Do not include any HTML formatting tags in the **title** attribute, or those tags will appear in the title and be displayed in Windows Explorer.</span></span>
-   <span data-ttu-id="7ae51-133">Per l'elemento **Description** :</span><span class="sxs-lookup"><span data-stu-id="7ae51-133">For the **description** element:</span></span>
    -   <span data-ttu-id="7ae51-134">Mostra informazioni sufficienti in modo che l'utente sappia perché il risultato potrebbe essere pertinente.</span><span class="sxs-lookup"><span data-stu-id="7ae51-134">Show enough information so that the user knows why this result might be relevant.</span></span>
    -   <span data-ttu-id="7ae51-135">Non includere la formattazione HTML.</span><span class="sxs-lookup"><span data-stu-id="7ae51-135">Do not include HTML formatting.</span></span> <span data-ttu-id="7ae51-136">Il provider [OpenSearch](https://github.com/dewitt/opensearch) rimuove la formattazione, il che potrebbe comportare risultati minori di quelli auspicabili per la descrizione.</span><span class="sxs-lookup"><span data-stu-id="7ae51-136">The [OpenSearch](https://github.com/dewitt/opensearch) provider removes the formatting, which might result in less than desirable results for your description.</span></span>
    -   <span data-ttu-id="7ae51-137">Non includere metadati già disponibili in altri elementi, ad esempio il nome del file dell'enclosure, le dimensioni, la data di modifica e così via, perché Esplora risorse Visualizza già i metadati.</span><span class="sxs-lookup"><span data-stu-id="7ae51-137">Do not include metadata that is already provided in other elements, such as enclosure file name, size, modified date, and so forth, because Windows Explorer already displays the metadata.</span></span> <span data-ttu-id="7ae51-138">La visualizzazione nell'elemento **Description** è ridondante.</span><span class="sxs-lookup"><span data-stu-id="7ae51-138">Displaying it in the **description** element would be redundant.</span></span>
-   <span data-ttu-id="7ae51-139">Per gli URL del contenuto o dell'enclosure:</span><span class="sxs-lookup"><span data-stu-id="7ae51-139">For enclosure or content URLs:</span></span>
    -   <span data-ttu-id="7ae51-140">Specificare l'attributo Type come tipo MIME valido.</span><span class="sxs-lookup"><span data-stu-id="7ae51-140">Specify the type attribute as a valid MIME type.</span></span>
    -   <span data-ttu-id="7ae51-141">Specificare le dimensioni del file in byte.</span><span class="sxs-lookup"><span data-stu-id="7ae51-141">Specify the file size in bytes.</span></span>
-   <span data-ttu-id="7ae51-142">Se si implementa l'output RSS in .NET utilizzando `DateTime` , testare il feed in Microsoft Internet Explorer per verificare se è valido prima della distribuzione in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="7ae51-142">If you are implementing RSS output in .NET using `DateTime`, test your feed in Microsoft Internet Explorer to see if it is valid before deploying it to Windows Explorer.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7ae51-143">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="7ae51-143">Additional Resources</span></span>

<span data-ttu-id="7ae51-144">Per ulteriori informazioni sull'implementazione della Federazione di ricerca negli archivi dati remoti tramite le tecnologie OpenSearch in Windows 7 e versioni successive, vedere l'argomento relativo alle risorse aggiuntive in [ricerca federata in Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7ae51-144">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ae51-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ae51-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ae51-146">Ricerca federata in Windows</span><span class="sxs-lookup"><span data-stu-id="7ae51-146">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="7ae51-147">Introduzione con ricerca federata in Windows</span><span class="sxs-lookup"><span data-stu-id="7ae51-147">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="7ae51-148">Connessione del servizio Web in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="7ae51-148">Connecting Your Web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="7ae51-149">Abilitazione dell'archivio dati in ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="7ae51-149">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="7ae51-150">Creazione di un file di descrizione OpenSearch nella ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="7ae51-150">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="7ae51-151">Distribuzione di connettori di ricerca nella ricerca federata di Windows</span><span class="sxs-lookup"><span data-stu-id="7ae51-151">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> <dt>

[<span data-ttu-id="7ae51-152">Estensione dell'indice</span><span class="sxs-lookup"><span data-stu-id="7ae51-152">Extending the Index</span></span>](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
