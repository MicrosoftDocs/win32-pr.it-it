---
title: Uso di HTMLView con i negozi online
description: Uso di HTMLView con i negozi online
ms.assetid: 78de7ef3-400c-4411-8ade-35c421805df8
keywords:
- Windows Media Player Online Stores, HTMLView
- negozi online, HTMLView
- digitare 1 Store online, HTMLView
- digitare 2 archivi online, HTMLView
- HTMLView, archivi online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d136be4f7866b6911b8b007de7e784d6133c217
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298912"
---
# <a name="using-htmlview-with-online-stores"></a><span data-ttu-id="10a7d-108">Uso di HTMLView con i negozi online</span><span class="sxs-lookup"><span data-stu-id="10a7d-108">Using HTMLView with Online Stores</span></span>

<span data-ttu-id="10a7d-109">Windows Media Player richiede agli utenti l'autorizzazione per visualizzare il contenuto di HTMLView in **Now Playing**.</span><span class="sxs-lookup"><span data-stu-id="10a7d-109">Windows Media Player prompts users for permission to display HTMLView content in **Now Playing**.</span></span> <span data-ttu-id="10a7d-110">Gli archivi online possono disabilitare questa richiesta specificando un valore di URL di base nell'elemento **HtmlView** del documento ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="10a7d-110">Online stores can disable this prompt by specifying a base URL value in the **HTMLView** element of the ServiceInfo document.</span></span> <span data-ttu-id="10a7d-111">Quando Windows Media Player apre una playlist che specifica il contenuto di HTMLView da visualizzare, il lettore confronta l'URL di base del documento ServiceInfo dell'archivio online attivo corrente con l'URL di base del contenuto di HTMLView.</span><span class="sxs-lookup"><span data-stu-id="10a7d-111">When Windows Media Player opens a playlist that specifies HTMLView content to display, the Player compares the base URL from the ServiceInfo document of the current active online store to the base URL of the HTMLView content.</span></span> <span data-ttu-id="10a7d-112">Se corrispondono, Windows Media Player Visualizza il contenuto di HTMLView senza richiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="10a7d-112">If they match, Windows Media Player displays the HTMLView content without prompting the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10a7d-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="10a7d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10a7d-114">**Visualizzazione di pagine Web in Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="10a7d-114">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="10a7d-115">**Elemento HTMLView**</span><span class="sxs-lookup"><span data-stu-id="10a7d-115">**HTMLView Element**</span></span>](htmlview-element.md)
</dt> <dt>

[<span data-ttu-id="10a7d-116">**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="10a7d-116">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




