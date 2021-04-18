---
description: Modalità di connessione dei filtri
ms.assetid: 6a126dd5-00fa-4ea6-b00a-09b7e1246874
title: Modalità di connessione dei filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21a72b2540133e84e473e3e82896a6427b923319
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303730"
---
# <a name="how-filters-connect"></a><span data-ttu-id="d1cb4-103">Modalità di connessione dei filtri</span><span class="sxs-lookup"><span data-stu-id="d1cb4-103">How Filters Connect</span></span>

<span data-ttu-id="d1cb4-104">Questo articolo descrive il modo in cui i filtri si connettono in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d1cb4-104">This article describes how filters connect in DirectShow.</span></span> <span data-ttu-id="d1cb4-105">Questo articolo è destinato agli sviluppatori di filtri.</span><span class="sxs-lookup"><span data-stu-id="d1cb4-105">The article is intended for filter developers.</span></span> <span data-ttu-id="d1cb4-106">Se si sta scrivendo un'applicazione DirectShow, probabilmente è possibile ignorare i dettagli presentati qui.</span><span class="sxs-lookup"><span data-stu-id="d1cb4-106">If you are writing a DirectShow application, you can probably ignore the details presented here.</span></span>

<span data-ttu-id="d1cb4-107">Questo articolo contiene gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="d1cb4-107">This article contains the following topics:</span></span>

-   [<span data-ttu-id="d1cb4-108">Connessioni pin</span><span class="sxs-lookup"><span data-stu-id="d1cb4-108">Pin Connections</span></span>](pin-connections.md)
-   [<span data-ttu-id="d1cb4-109">Negoziazione di tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="d1cb4-109">Negotiating Media Types</span></span>](negotiating-media-types.md)
-   [<span data-ttu-id="d1cb4-110">Negozi di allocatori</span><span class="sxs-lookup"><span data-stu-id="d1cb4-110">Negotiating Allocators</span></span>](negotiating-allocators.md)
-   [<span data-ttu-id="d1cb4-111">Fornire un allocatore personalizzato</span><span class="sxs-lookup"><span data-stu-id="d1cb4-111">Providing a Custom Allocator</span></span>](providing-a-custom-allocator.md)
-   [<span data-ttu-id="d1cb4-112">Riconnessione di pin</span><span class="sxs-lookup"><span data-stu-id="d1cb4-112">Reconnecting Pins</span></span>](reconnecting-pins.md)

## <a name="related-topics"></a><span data-ttu-id="d1cb4-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d1cb4-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1cb4-114">Processo di connessione CBasePin</span><span class="sxs-lookup"><span data-stu-id="d1cb4-114">CBasePin Connection Process</span></span>](cbasepin-connection-process.md)
</dt> <dt>

[<span data-ttu-id="d1cb4-115">Scrittura di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="d1cb4-115">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



