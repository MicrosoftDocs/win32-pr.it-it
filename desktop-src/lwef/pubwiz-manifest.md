---
title: Utilizzo del manifesto di trasferimento
description: La pubblicazione guidata sul Web e l'ordinamento guidato stampa online utilizzano il manifesto di trasferimento per comunicare i dettagli del trasferimento dei dati tra il computer client e il sito del server.
ms.assetid: b7bb541c-3bf4-4aab-ac70-c006517e772e
keywords:
- Pubblicazione guidata sul Web, trasferimento manifesto
- Procedura guidata per l'ordine di stampa online, trasferimento manifesto
- trasferire il manifesto
- manifest
- finestra. External, trasferimento manifesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20fa7b3a35a6f06e2939b6c25f82d12c2b98a7f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872502"
---
# <a name="using-the-transfer-manifest"></a><span data-ttu-id="bef2e-108">Utilizzo del manifesto di trasferimento</span><span class="sxs-lookup"><span data-stu-id="bef2e-108">Using the Transfer Manifest</span></span>

<span data-ttu-id="bef2e-109">La pubblicazione guidata sul Web e l'ordinamento guidato stampa online utilizzano il manifesto di trasferimento per comunicare i dettagli del trasferimento dei dati tra il computer client e il sito del server.</span><span class="sxs-lookup"><span data-stu-id="bef2e-109">The Web Publishing Wizard and Online Print Ordering Wizard use the transfer manifest to communicate details of data transfer between the client computer and the server site.</span></span>

## <a name="the-purpose-of-the-transfer-manifest"></a><span data-ttu-id="bef2e-110">Scopo del manifesto di trasferimento</span><span class="sxs-lookup"><span data-stu-id="bef2e-110">The Purpose of the Transfer Manifest</span></span>

<span data-ttu-id="bef2e-111">Il manifesto di trasferimento descrive i file che coinvolgono il trasferimento, inclusi i dettagli, ad esempio la gerarchia di destinazione e i metadati del file.</span><span class="sxs-lookup"><span data-stu-id="bef2e-111">The transfer manifest describes files involved in the transfer, including details such as the destination hierarchy and the file's metadata.</span></span> <span data-ttu-id="bef2e-112">Lo script lato server può modificare il manifesto rimuovendo i file non appropriati dall'elenco e aggiungendo le informazioni su come e dove trasferire i file.</span><span class="sxs-lookup"><span data-stu-id="bef2e-112">Server-side script can modify the manifest by removing inappropriate files from the list and adding information about how and where the files should be transferred.</span></span>

<span data-ttu-id="bef2e-113">Il manifesto viene esposto come finestra proprietà **. External. Property ("TransferManifest")**, un documento XML Document Object Model (Dom).</span><span class="sxs-lookup"><span data-stu-id="bef2e-113">The manifest is exposed as the property **window.external.Property("TransferManifest")**, an XML Document Object Model (DOM) document.</span></span> <span data-ttu-id="bef2e-114">Per ulteriori informazioni sul modello DOM XML, vedere la documentazione MSDN relativa a [IXMLDOMDocument/DOMDocument](/previous-versions/windows/desktop/ms756987(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bef2e-114">For more information on the XML DOM, see the MSDN documentation for [IXMLDOMDocument/DOMDocument](/previous-versions/windows/desktop/ms756987(v=vs.85)).</span></span>

<span data-ttu-id="bef2e-115">L'organizzazione di primo livello del manifesto di trasferimento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="bef2e-115">The top-level organization of the transfer manifest is as follows:</span></span>


```
<transfermanifest>
    <filelist/>
    <folderlist/>
    <uploadinfo/>
</transfermanifest>
```



<span data-ttu-id="bef2e-116">La pagina HTML sul lato server può utilizzare i nodi del manifesto per ottenere determinate informazioni sui file da copiare e quindi modificare di conseguenza l'interfaccia utente del servizio.</span><span class="sxs-lookup"><span data-stu-id="bef2e-116">The server-side HTML page can use the nodes in the manifest to obtain certain information about the files to be copied and then modify the service's UI accordingly.</span></span> <span data-ttu-id="bef2e-117">Ad esempio, un sito di stampa di foto può utilizzare le informazioni per visualizzare le anteprime delle immagini scelte, mentre un sito di archiviazione può utilizzare le informazioni per assicurarsi che sia disponibile spazio di archiviazione sufficiente per tale utente.</span><span class="sxs-lookup"><span data-stu-id="bef2e-117">For instance, a photo printing site might use the information to display thumbnails of the chosen images, while a storage site might use the information to ensure that sufficient storage space is available for that user.</span></span> <span data-ttu-id="bef2e-118">Per informazioni complete sugli attributi e sui nodi del manifesto di trasferimento, vedere [Transfer manifest schema](/windows/desktop/shell/interfaces).</span><span class="sxs-lookup"><span data-stu-id="bef2e-118">For complete information on the transfer manifest nodes and attributes, see [Transfer Manifest Schema](/windows/desktop/shell/interfaces).</span></span>

<span data-ttu-id="bef2e-119">Lo schema del manifesto di trasferimento viene scritto come modello aperto in modo che gli elementi non definiti specificamente nello schema siano visualizzati nel manifesto di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="bef2e-119">The transfer manifest schema is written as an open model so that elements not specifically defined in the schema may appear in the transfer manifest.</span></span> <span data-ttu-id="bef2e-120">Pertanto, un sito del provider può aggiungere elementi proprietari per il proprio utilizzo senza compromettere la validità del manifesto.</span><span class="sxs-lookup"><span data-stu-id="bef2e-120">Therefore, a provider site might add proprietary elements for its own use without disturbing the validity of the manifest.</span></span> <span data-ttu-id="bef2e-121">Lo schema viene definito anche in modo che l'ordine degli elementi non sia limitato.</span><span class="sxs-lookup"><span data-stu-id="bef2e-121">The schema is also defined so that the order of elements is not restricted.</span></span>

> [!Note]  
> <span data-ttu-id="bef2e-122">Il manifesto viene ricreato ogni volta che viene scelto un nuovo provider, in modo che il provider abbia la possibilità di archiviare le informazioni sul sito nel manifesto.</span><span class="sxs-lookup"><span data-stu-id="bef2e-122">The manifest is re-created each time a new provider is chosen so that the provider has a chance to store site information in the manifest.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bef2e-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bef2e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bef2e-124">Trasferimento dello schema del manifesto</span><span class="sxs-lookup"><span data-stu-id="bef2e-124">Transfer Manifest Schema</span></span>](/windows/desktop/shell/interfaces)
</dt> </dl>

 

 