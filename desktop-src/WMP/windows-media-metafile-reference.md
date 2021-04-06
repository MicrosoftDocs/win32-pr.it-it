---
title: Informazioni di riferimento sui metafile di Windows Media
description: Informazioni di riferimento sui metafile di Windows Media
ms.assetid: 03dadba3-0143-46f0-990a-108196eb58ab
keywords:
- Metafile di Windows Media, informazioni di riferimento
- Metafile, riferimento
- informazioni di riferimento sui metafile di Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d2c8d20d64e9a363fb37594519253206d30483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044678"
---
# <a name="windows-media-metafile-reference"></a><span data-ttu-id="49f58-106">Informazioni di riferimento sui metafile di Windows Media</span><span class="sxs-lookup"><span data-stu-id="49f58-106">Windows Media Metafile Reference</span></span>

<span data-ttu-id="49f58-107">Questa documentazione di riferimento illustra gli elementi e le estensioni di file per i file di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="49f58-107">This reference documents elements and file name extensions for Windows Media metafiles.</span></span> <span data-ttu-id="49f58-108">Il riferimento è suddiviso nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="49f58-108">The reference is divided into the following sections.</span></span>



| <span data-ttu-id="49f58-109">Sezione</span><span class="sxs-lookup"><span data-stu-id="49f58-109">Section</span></span>                                                                                    | <span data-ttu-id="49f58-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49f58-110">Description</span></span>                                                                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49f58-111">Riferimento agli elementi metafile di Windows Media</span><span class="sxs-lookup"><span data-stu-id="49f58-111">Windows Media Metafile Elements Reference</span></span>](windows-media-metafile-elements-reference.md) | <span data-ttu-id="49f58-112">Documenta gli elementi metafile, incluse le definizioni, gli attributi e i relativi valori, nonché le condizioni speciali correlate a ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="49f58-112">Documents metafile elements, including definitions, attributes and their values, and special conditions related to each element.</span></span> |
| [<span data-ttu-id="49f58-113">Estensioni di file</span><span class="sxs-lookup"><span data-stu-id="49f58-113">File Name Extensions</span></span>](file-name-extensions.md)                                           | <span data-ttu-id="49f58-114">Documenta le estensioni dei nomi di file di metafile con regole e linee guida per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="49f58-114">Documents metafile file name extensions with rules and guidelines on their use.</span></span>                                                  |



 

<span data-ttu-id="49f58-115">I metafile di Windows Media sono file di testo che forniscono informazioni su un flusso di file e la relativa presentazione.</span><span class="sxs-lookup"><span data-stu-id="49f58-115">Windows Media metafiles are text files that provide information about a file stream and its presentation.</span></span> <span data-ttu-id="49f58-116">I metafile sono basati sulla sintassi Extensible Markup Language (XML) e sono costituiti da vari elementi di tipo XML con i relativi tag e attributi.</span><span class="sxs-lookup"><span data-stu-id="49f58-116">The metafiles are based on the Extensible Markup Language (XML) syntax, and are made up of various XML-like elements with their tags and attributes.</span></span> <span data-ttu-id="49f58-117">Ogni elemento definisce un'impostazione o un'azione per i flussi multimediali.</span><span class="sxs-lookup"><span data-stu-id="49f58-117">Each element defines a setting or action for streaming media.</span></span>

<span data-ttu-id="49f58-118">Sono disponibili due set di tag di elemento per i metafile.</span><span class="sxs-lookup"><span data-stu-id="49f58-118">There are two sets of element tags available for metafiles.</span></span> <span data-ttu-id="49f58-119">I metafile lato client hanno un set di elementi e i metafile del lato server hanno un altro set di elementi.</span><span class="sxs-lookup"><span data-stu-id="49f58-119">Client-side metafiles have one set of elements, and server-side metafiles have another set of elements.</span></span>

<span data-ttu-id="49f58-120">Se un tag di elemento non ha elementi figlio (quelli che modificano o sono contenuti all'interno di un altro elemento), è possibile usare una singola barra (/) alla fine del tag di apertura al posto di un tag di chiusura.</span><span class="sxs-lookup"><span data-stu-id="49f58-120">If an element tag does not have any child elements (those that modify or are contained within another element), a single slash character (/) can be used at the end of the opening tag in place of a closing tag.</span></span> <span data-ttu-id="49f58-121">Se gli elementi figlio non vengono visualizzati tra il tag di apertura e di chiusura per un elemento, non sono elementi figlio per quell'elemento e vengono ignorati o generano un errore nella sintassi del metafile.</span><span class="sxs-lookup"><span data-stu-id="49f58-121">If child elements do not appear between the opening and closing tag for an element, they are not child elements for that element, and are ignored or cause an error in the syntax of the metafile.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49f58-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="49f58-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49f58-123">**Informazioni sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="49f58-123">**About Windows Media Metafiles**</span></span>](about-windows-media-metafiles.md)
</dt> <dt>

[<span data-ttu-id="49f58-124">**Guida ai metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="49f58-124">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> <dt>

[<span data-ttu-id="49f58-125">**Metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="49f58-125">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 




