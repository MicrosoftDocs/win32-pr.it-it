---
title: Rimozione degli attributi dei metadati
description: Rimozione degli attributi dei metadati
ms.assetid: 44546091-406f-4ae6-914a-942d1b89e0e4
keywords:
- Windows Media Format SDK, rimozione degli attributi dei metadati
- ASF (Advanced Systems Format), rimozione degli attributi dei metadati
- ASF (Advanced Systems Format), rimozione degli attributi dei metadati
- metadati, rimozione di attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b10176452dcc78cc3eca898b61c350a157e568
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104398756"
---
# <a name="removing-metadata-attributes"></a><span data-ttu-id="f4f4d-107">Rimozione degli attributi dei metadati</span><span class="sxs-lookup"><span data-stu-id="f4f4d-107">Removing Metadata Attributes</span></span>

<span data-ttu-id="f4f4d-108">È possibile rimuovere un attributo di metadati passandone l'indice e il numero di flusso al metodo [**IWMHeaderInfo3::D eleteattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute) .</span><span class="sxs-lookup"><span data-stu-id="f4f4d-108">You can remove a metadata attribute by passing its index and stream number to the [**IWMHeaderInfo3::DeleteAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute) method.</span></span> <span data-ttu-id="f4f4d-109">L'ordine in cui gli attributi rimanenti vengono indicizzati dopo la rimozione di un attributo non cambia; tutti gli attributi rimanenti che originariamente avevano un valore di indice maggiore di quello rimosso hanno i valori di indice ridotti di uno.</span><span class="sxs-lookup"><span data-stu-id="f4f4d-109">The order in which the remaining attributes are indexed after removing an attribute does not change; all remaining attributes that originally had an index value greater than the one removed have their index values reduced by one.</span></span> <span data-ttu-id="f4f4d-110">Quando si rimuovono più attributi, eseguire questa operazione in ordine decrescente in base all'indice per evitare di dover calcolare la regolazione nell'indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="f4f4d-110">When removing multiple attributes, do so in descending order by index to avoid having to calculate the adjustment in indexing.</span></span>

<span data-ttu-id="f4f4d-111">Per praticità nella rimozione dei valori, il metodo [**IWMHeaderInfo3:: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) restituisce i valori di indice in ordine decrescente.</span><span class="sxs-lookup"><span data-stu-id="f4f4d-111">For convenience in removing values, the [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) method returns the index values in descending order.</span></span>

> [!Note]  
> <span data-ttu-id="f4f4d-112">I valori di indice ottenuti utilizzando i metodi di [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) non sono compatibili con i valori di indice ottenuti utilizzando i metodi di [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).</span><span class="sxs-lookup"><span data-stu-id="f4f4d-112">Index values obtained by using the methods of [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) are not compatible with index values obtained by using the methods of [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).</span></span> <span data-ttu-id="f4f4d-113">Se si utilizzano i metodi di un'interfaccia per modificare gli attributi in un file, è necessario presupporre che tutti i valori di indice recuperati in precedenza dall'altra interfaccia non siano più validi e che sia necessario ottenerli nuovamente.</span><span class="sxs-lookup"><span data-stu-id="f4f4d-113">If you use the methods of one interface to change attributes in a file, you should assume that any index values previously retrieved from the other interface are no longer valid and must be obtained again.</span></span> <span data-ttu-id="f4f4d-114">Se possibile, è consigliabile evitare di usare i metodi di **IWMHeaderInfo** .</span><span class="sxs-lookup"><span data-stu-id="f4f4d-114">You should avoid using the methods of **IWMHeaderInfo** if possible.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f4f4d-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f4f4d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4f4d-116">**Utilizzo dei metadati**</span><span class="sxs-lookup"><span data-stu-id="f4f4d-116">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




