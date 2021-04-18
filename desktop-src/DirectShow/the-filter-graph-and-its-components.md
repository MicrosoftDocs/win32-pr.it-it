---
description: Il grafico del filtro e i relativi componenti
ms.assetid: 3747bfcd-1e4a-404c-a493-26d3c20bab21
title: Il grafico del filtro e i relativi componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473fb3dfe327eb43bb2065417c7be80f7537d06a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316292"
---
# <a name="the-filter-graph-and-its-components"></a><span data-ttu-id="e87a4-103">Il grafico del filtro e i relativi componenti</span><span class="sxs-lookup"><span data-stu-id="e87a4-103">The Filter Graph and Its Components</span></span>

<span data-ttu-id="e87a4-104">Questo articolo descrive i principali componenti di DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e87a4-104">This article describes the major components of DirectShow.</span></span> <span data-ttu-id="e87a4-105">È concepita come introduzione per gli sviluppatori di applicazioni e per gli sviluppatori che scrivono filtri DirectShow personalizzati.</span><span class="sxs-lookup"><span data-stu-id="e87a4-105">It is intended as an introduction for application developers and for developers writing custom DirectShow filters.</span></span> <span data-ttu-id="e87a4-106">Gli sviluppatori di applicazioni possono in genere ignorare molti dei dettagli di basso livello di DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e87a4-106">Application developers can usually ignore many of the low-level details of DirectShow.</span></span> <span data-ttu-id="e87a4-107">Tuttavia, è comunque consigliabile leggere questa sezione per avere una conoscenza generale dell'architettura DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e87a4-107">However, it is still a good idea to read this section, to have a general understanding of the DirectShow architecture.</span></span>

<span data-ttu-id="e87a4-108">In questo articolo sono contenute le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e87a4-108">This article contains the following sections:</span></span>

-   [<span data-ttu-id="e87a4-109">Informazioni sui filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="e87a4-109">About DirectShow Filters</span></span>](about-directshow-filters.md)
-   [<span data-ttu-id="e87a4-110">Informazioni su Filter Graph Manager</span><span class="sxs-lookup"><span data-stu-id="e87a4-110">About the Filter Graph Manager</span></span>](about-the-filter-graph-manager.md)
-   [<span data-ttu-id="e87a4-111">Informazioni sui tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="e87a4-111">About Media Types</span></span>](about-media-types.md)
-   [<span data-ttu-id="e87a4-112">Informazioni su esempi e allocatori multimediali</span><span class="sxs-lookup"><span data-stu-id="e87a4-112">About Media Samples and Allocators</span></span>](about-media-samples-and-allocators.md)
-   [<span data-ttu-id="e87a4-113">Come i dispositivi hardware partecipano al grafico di filtro</span><span class="sxs-lookup"><span data-stu-id="e87a4-113">How Hardware Devices Participate in the Filter Graph</span></span>](how-hardware-devices-participate-in-the-filter-graph.md)

 

 



