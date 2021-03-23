---
title: Riepilogo di configurabilità heap descrittore
description: Nella tabella seguente sono riepilogate le informazioni sullo shader e sul supporto dell'heap visibile non shader.
ms.assetid: DF266915-6224-4FFB-BE3E-34A44F7318DD
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ce6718e95b774f83d25a84476616643c77c119
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104409"
---
# <a name="descriptor-heap-configurability-summary"></a><span data-ttu-id="a1d7f-103">Riepilogo di configurabilità heap descrittore</span><span class="sxs-lookup"><span data-stu-id="a1d7f-103">Descriptor Heap Configurability Summary</span></span>

<span data-ttu-id="a1d7f-104">Nella tabella seguente sono riepilogate le informazioni sullo shader e sul supporto dell'heap visibile non shader.</span><span class="sxs-lookup"><span data-stu-id="a1d7f-104">The following table summarizes information about Shader and non-Shader visible heap support.</span></span>



|                               | <span data-ttu-id="a1d7f-105">Heap descrittore visibile dello shader</span><span class="sxs-lookup"><span data-stu-id="a1d7f-105">Shader Visible Descriptor Heap</span></span>                                                 | <span data-ttu-id="a1d7f-106">Heap descrittore non visibile per shader</span><span class="sxs-lookup"><span data-stu-id="a1d7f-106">Non Shader Visible Descriptor Heap</span></span>                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1d7f-107">Tipi di heap supportati</span><span class="sxs-lookup"><span data-stu-id="a1d7f-107">Heap Types Supported</span></span>          | <span data-ttu-id="a1d7f-108">CBV \_ SRV \_ UAV, campionatore</span><span class="sxs-lookup"><span data-stu-id="a1d7f-108">CBV\_SRV\_UAV, Sampler</span></span>                                                         | <span data-ttu-id="a1d7f-109">Tutti</span><span class="sxs-lookup"><span data-stu-id="a1d7f-109">All</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a1d7f-110">Proprietà della pagina CPU supportate</span><span class="sxs-lookup"><span data-stu-id="a1d7f-110">CPU Page Properties Supported</span></span> | <span data-ttu-id="a1d7f-111">NON \_ disponibile, scrittura \_ combinata</span><span class="sxs-lookup"><span data-stu-id="a1d7f-111">NOT\_AVAILABLE, WRITE\_COMBINE</span></span>                                                 | <span data-ttu-id="a1d7f-112">Scrivi \_ indietro</span><span class="sxs-lookup"><span data-stu-id="a1d7f-112">WRITE\_BACK</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="a1d7f-113">Gestione della residenza per app</span><span class="sxs-lookup"><span data-stu-id="a1d7f-113">Residency Management By App</span></span>   | <span data-ttu-id="a1d7f-114">Sì, app responsabile</span><span class="sxs-lookup"><span data-stu-id="a1d7f-114">Yes, app responsible</span></span>                                                           | <span data-ttu-id="a1d7f-115">Non applicabile (non visibile GPU).</span><span class="sxs-lookup"><span data-stu-id="a1d7f-115">Not applicable (not GPU visible).</span></span>                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="a1d7f-116">Supporto per la modifica del descrittore</span><span class="sxs-lookup"><span data-stu-id="a1d7f-116">Descriptor Edit Support</span></span>       | <span data-ttu-id="a1d7f-117">Solo destinazione di copia, tramite l'aggiornamento dell'elenco dei comandi e/o la copia della CPU se la CPU è visibile.</span><span class="sxs-lookup"><span data-stu-id="a1d7f-117">Copy destination only, via command list update and/or CPU copy if CPU visible.</span></span> | <span data-ttu-id="a1d7f-118">CPU di sola lettura e scrittura.</span><span class="sxs-lookup"><span data-stu-id="a1d7f-118">CPU read and write only.</span></span> <span data-ttu-id="a1d7f-119">Nessun accesso diretto alla GPU.</span><span class="sxs-lookup"><span data-stu-id="a1d7f-119">No direct GPU access.</span></span> <span data-ttu-id="a1d7f-120">Può essere usato per la copia immediata della CPU (come origine e destinazione).</span><span class="sxs-lookup"><span data-stu-id="a1d7f-120">Can be used for immediate CPU copying (as a source and destination).</span></span> <span data-ttu-id="a1d7f-121">Può essere usato come origine di aggiornamento in un elenco di comandi. in questo modo, i descrittori verranno copiati nell'archiviazione dell'elenco dei comandi durante il record dell'elenco dei comandi.</span><span class="sxs-lookup"><span data-stu-id="a1d7f-121">Can be used as an update source on a command list – this will copy the descriptors into command list storage during command list record.</span></span> <span data-ttu-id="a1d7f-122">Durante l'esecuzione, la copia archiviata verrà copiata nella destinazione, che deve essere un heap visibile dello shader.</span><span class="sxs-lookup"><span data-stu-id="a1d7f-122">On execution, the stored copy will get copied to the destination, which must be a shader visible heap.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a1d7f-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a1d7f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1d7f-124">Heap descrittore</span><span class="sxs-lookup"><span data-stu-id="a1d7f-124">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




