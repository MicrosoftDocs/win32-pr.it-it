---
title: Annidamento di metafile
description: Annidamento di metafile
ms.assetid: fa355c98-31e2-4bb9-ad67-fd9a727300c3
keywords:
- Metafile di Windows Media, annidamento
- Metafile di Windows Media, che fanno riferimento ad altri metafile
- annidamento di metafile
- Metafile, annidamento
- Metafile, che fanno riferimento ad altri metafile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3cd5743424858c4bbcd6f66952f4275ea82d947e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328575"
---
# <a name="nesting-metafiles"></a><span data-ttu-id="2b7ae-108">Annidamento di metafile</span><span class="sxs-lookup"><span data-stu-id="2b7ae-108">Nesting Metafiles</span></span>

<span data-ttu-id="2b7ae-109">Un metafile può fare riferimento A un altro metafile.</span><span class="sxs-lookup"><span data-stu-id="2b7ae-109">A metafile can reference another metafile.</span></span> <span data-ttu-id="2b7ae-110">Per fare riferimento a un altro metafile, usare l'elemento **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="2b7ae-110">To reference another metafile, use the **ENTRYREF** element.</span></span> <span data-ttu-id="2b7ae-111">Un elemento **ENTRYREF** nel metafile primario punta a un metafile esterno.</span><span class="sxs-lookup"><span data-stu-id="2b7ae-111">An **ENTRYREF** element in the primary metafile points to an external metafile.</span></span>

<span data-ttu-id="2b7ae-112">Il controllo Windows Media Player elabora gli elementi **entry** del metafile a cui si fa riferimento come se fossero inclusi nel metafile primario nella posizione dell'elemento **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="2b7ae-112">The Windows Media Player control processes the **ENTRY** elements of the referenced metafile as if they were included in the primary metafile at the position of the **ENTRYREF** element.</span></span> <span data-ttu-id="2b7ae-113">Tuttavia, ignora qualsiasi elemento **entry** nel metafile a cui si fa riferimento con l'attributo **SKIPIFREF** impostato su Yes.</span><span class="sxs-lookup"><span data-stu-id="2b7ae-113">However, it skips any **ENTRY** elements in the referenced metafile that have the **SKIPIFREF** attribute set to YES.</span></span>

<span data-ttu-id="2b7ae-114">I controlli Windows Media Player 7,0, 7,1 e Windows Media Player per Windows XP ignorano tutti gli elementi **ENTRYREF** nel metafile a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="2b7ae-114">The Windows Media Player 7.0, 7.1, and Windows Media Player for Windows XP controls ignore any **ENTRYREF** elements in the referenced metafile.</span></span> <span data-ttu-id="2b7ae-115">Di conseguenza, i metafile possono essere annidati un solo livello di profondità usando queste versioni.</span><span class="sxs-lookup"><span data-stu-id="2b7ae-115">Thus, metafiles can only be nested one level deep using these versions.</span></span> <span data-ttu-id="2b7ae-116">Queste versioni ignorano anche l'elemento **ASX** e i relativi attributi nel file a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="2b7ae-116">These versions also ignore the **ASX** element and its attributes in the referenced file.</span></span> <span data-ttu-id="2b7ae-117">Windows Media Player 9 Series o versioni successive supporta la nidificazione di metafile fino a 5 Deep.</span><span class="sxs-lookup"><span data-stu-id="2b7ae-117">Windows Media Player 9 Series or later supports nesting metafiles up to 5 deep.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b7ae-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2b7ae-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b7ae-119">**Creazione di playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="2b7ae-119">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> </dl>

 

 




