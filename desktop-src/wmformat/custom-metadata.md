---
title: Metadati personalizzati
description: Metadati personalizzati
ms.assetid: 86132163-da56-416a-9539-874d18972932
keywords:
- Windows Media Format SDK, metadati personalizzati
- ASF (Advanced Systems Format), metadati personalizzati
- ASF (Advanced Systems Format), metadati personalizzati
- Windows Media Format SDK, interfaccia IWMHeaderInfo3
- Advanced Systems Format (ASF), interfaccia IWMHeaderInfo3
- ASF (formato avanzato dei sistemi), interfaccia IWMHeaderInfo3
- metadati, personalizzazione
- IWMHeaderInfo3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a795ab184e5bd6120278f61c0d3654679fd79c28
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "103724028"
---
# <a name="custom-metadata"></a><span data-ttu-id="44da2-111">Metadati personalizzati</span><span class="sxs-lookup"><span data-stu-id="44da2-111">Custom Metadata</span></span>

<span data-ttu-id="44da2-112">Oltre ai molti attributi supportati forniti con Windows Media Format SDK, è possibile creare attributi di metadati per le specifiche.</span><span class="sxs-lookup"><span data-stu-id="44da2-112">In addition to the many supported attributes provided with the Windows Media Format SDK, you can create metadata attributes to your own specifications.</span></span> <span data-ttu-id="44da2-113">Quando si creano attributi di metadati personalizzati, è consigliabile utilizzare una convenzione di denominazione facilmente identificabile per evitare possibili conflitti con gli attributi creati da altri.</span><span class="sxs-lookup"><span data-stu-id="44da2-113">When creating custom metadata attributes, you should use an easily identifiable naming convention to avoid possible conflict with attributes created by others.</span></span>

<span data-ttu-id="44da2-114">Si consiglia di usare i metodi di [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) per creare i metadati a causa della flessibilità aggiunta fornita dai metodi di [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).</span><span class="sxs-lookup"><span data-stu-id="44da2-114">It is recommended that you use the methods of [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) to create your metadata because of the added flexibility they provide over the methods of [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).</span></span>

## <a name="related-topics"></a><span data-ttu-id="44da2-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="44da2-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44da2-116">**Attributi**</span><span class="sxs-lookup"><span data-stu-id="44da2-116">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="44da2-117">**Funzionalità dei metadati**</span><span class="sxs-lookup"><span data-stu-id="44da2-117">**Metadata Features**</span></span>](metadata-features.md)
</dt> <dt>

[<span data-ttu-id="44da2-118">**Utilizzo dei metadati**</span><span class="sxs-lookup"><span data-stu-id="44da2-118">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




