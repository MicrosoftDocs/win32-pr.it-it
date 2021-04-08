---
title: Recupero degli attributi dei metadati
description: Recupero degli attributi dei metadati
ms.assetid: d1d2c8e0-7445-4ee1-94d9-4c1ed74f8fe2
keywords:
- Windows Media Format SDK, recupero degli attributi dei metadati
- Formato di sistemi avanzati (ASF), recupero degli attributi dei metadati
- ASF (Advanced Systems Format), recupero degli attributi dei metadati
- metadati, recupero di attributi
- flussi, recupero di attributi di metadati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c918cb47e77c3fd69c64de586b84b7f6244e4c9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046272"
---
# <a name="retrieving-metadata-attributes"></a><span data-ttu-id="8e9d5-108">Recupero degli attributi dei metadati</span><span class="sxs-lookup"><span data-stu-id="8e9d5-108">Retrieving Metadata Attributes</span></span>

<span data-ttu-id="8e9d5-109">Per recuperare un attributo da un'intestazione di file, è necessario conoscerne il numero di flusso e l'indice.</span><span class="sxs-lookup"><span data-stu-id="8e9d5-109">To retrieve an attribute from a file header, you must know the stream number and index of the attribute.</span></span> <span data-ttu-id="8e9d5-110">È possibile usare il metodo [**IWMHeaderInfo3:: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) per ottenere gli indici per tutti gli attributi con lo stesso nome o tutti gli indici nella stessa lingua.</span><span class="sxs-lookup"><span data-stu-id="8e9d5-110">You can use the [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) method to get the indexes for all attributes with the same name or all indexes in the same language.</span></span> <span data-ttu-id="8e9d5-111">Analogamente agli altri metodi di [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), **GetAttributeIndices** gestisce un singolo flusso o con tutti gli attributi a livello di file che usano il flusso 0.</span><span class="sxs-lookup"><span data-stu-id="8e9d5-111">Like the other methods of [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), **GetAttributeIndices** deals with a single stream, or with all file-level attributes using stream 0.</span></span> <span data-ttu-id="8e9d5-112">È possibile usare 0xFFFF per il numero di flusso per ottenere gli indici globali che corrispondono ai criteri nell'intero file, indipendentemente dal numero di flusso.</span><span class="sxs-lookup"><span data-stu-id="8e9d5-112">You can use 0xFFFF for the stream number to get global indexes matching your criteria throughout the entire file, regardless of stream number.</span></span>

<span data-ttu-id="8e9d5-113">Quando si conosce l'indice dell'attributo che si desidera recuperare, chiamare [**IWMHeaderInfo3:: GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) per ottenere l'attributo.</span><span class="sxs-lookup"><span data-stu-id="8e9d5-113">When you know the index of the attribute you want to retrieve, call [**IWMHeaderInfo3::GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) to get the attribute.</span></span> <span data-ttu-id="8e9d5-114">È necessario effettuare due chiamate a **GetAttributeByIndexEx** per ogni attributo recuperato.</span><span class="sxs-lookup"><span data-stu-id="8e9d5-114">You need to make two calls to **GetAttributeByIndexEx** for each attribute retrieved.</span></span> <span data-ttu-id="8e9d5-115">Alla prima chiamata, passare **null** per i puntatori al nome e al buffer dei dati per ottenere le dimensioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="8e9d5-115">On the first call, pass **NULL** for the name and data buffer pointers to get the size needed.</span></span> <span data-ttu-id="8e9d5-116">Allocare quindi i buffer delle dimensioni indicate ed effettuare la seconda chiamata per recuperare il nome e i dati.</span><span class="sxs-lookup"><span data-stu-id="8e9d5-116">Then allocate buffers of the size indicated and make the second call to retrieve the name and data.</span></span>

<span data-ttu-id="8e9d5-117">Per un esempio di codice che illustra come recuperare gli attributi di metadati, vedere [per recuperare tutti i metadati in un file](to-retrieve-all-metadata-in-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="8e9d5-117">For example code showing how to retrieve metadata attributes, see [To Retrieve All Metadata in a File](to-retrieve-all-metadata-in-a-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e9d5-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8e9d5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e9d5-119">**Utilizzo dei metadati**</span><span class="sxs-lookup"><span data-stu-id="8e9d5-119">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




