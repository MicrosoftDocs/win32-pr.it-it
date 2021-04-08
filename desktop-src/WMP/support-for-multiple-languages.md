---
title: Supporto per più lingue
description: Supporto per più lingue
ms.assetid: f46efb7f-73d1-4f64-aa44-cb50170a2245
keywords:
- Playlist Windows Media Metafile, supporto per più lingue
- playlist di metafile, supporto per più lingue
- playlist, supporto per più lingue
- Playlist Windows Media Metafile, supporto per più lingue
- playlist di metafile, supporto per più linguaggi
- playlist, supporto per più lingue
- Playlist Windows Media Metafile, supporto linguistico
- playlist di metafile, supporto del linguaggio
- playlist, supporto linguistico
- supporto per più lingue
- supporto multilingue
- supporto delle lingue
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d8855aeb798e4243182a6f82479289ccccbd97d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045195"
---
# <a name="support-for-multiple-languages"></a><span data-ttu-id="fef0d-115">Supporto per più lingue</span><span class="sxs-lookup"><span data-stu-id="fef0d-115">Support for Multiple Languages</span></span>

<span data-ttu-id="fef0d-116">Windows Media Player 9 Series o versioni successive supporta i file multimediali di Windows creati utilizzando il set di caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="fef0d-116">Windows Media Player 9 Series or later supports Windows Media metafiles created using the Unicode character set.</span></span> <span data-ttu-id="fef0d-117">In questo modo è possibile includere metadati multilingue nella playlist del metafile.</span><span class="sxs-lookup"><span data-stu-id="fef0d-117">This allows you to include multilingual metadata in your metafile playlist.</span></span> <span data-ttu-id="fef0d-118">Le regole seguenti regolano l'utilizzo di metadati multilingue nei metafile multimediali di Windows:</span><span class="sxs-lookup"><span data-stu-id="fef0d-118">The following rules govern the use of multilingual metadata in Windows Media metafiles:</span></span>

-   <span data-ttu-id="fef0d-119">I caratteri devono essere codificati con lo schema di codifica UTF-8.</span><span class="sxs-lookup"><span data-stu-id="fef0d-119">Characters must be encoded using the UTF-8 encoding scheme.</span></span>
-   <span data-ttu-id="fef0d-120">La playlist del metafile deve includere il **param** seguente al livello della playlist:</span><span class="sxs-lookup"><span data-stu-id="fef0d-120">The metafile playlist must include the following **PARAM** at the playlist level:</span></span>
    ```XML
    <PARAM  NAME = "Encoding"  VALUE = "utf-8">
    
    ```

    

-   <span data-ttu-id="fef0d-121">Questa funzionalità è supportata solo in Windows Media Player 9 serie o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="fef0d-121">Only Windows Media Player 9 Series or later supports this functionality.</span></span>
-   <span data-ttu-id="fef0d-122">Se la playlist del metafile non viene salvata con la codifica UTF-8 e l'elemento **param** corretto, verrà analizzato utilizzando la tabella codici delle impostazioni locali di sistema predefinita del computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fef0d-122">If the metafile playlist is not saved with UTF-8 encoding and the correct **PARAM** element, it will be parsed using the default system locale code page of the user's computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fef0d-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fef0d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fef0d-124">**PARAM (elemento)**</span><span class="sxs-lookup"><span data-stu-id="fef0d-124">**PARAM Element**</span></span>](param-element.md)
</dt> <dt>

[<span data-ttu-id="fef0d-125">**Cenni preliminari sui file di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="fef0d-125">**Windows Media Metafiles Overview**</span></span>](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




