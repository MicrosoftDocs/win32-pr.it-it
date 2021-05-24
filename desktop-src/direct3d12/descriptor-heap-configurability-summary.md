---
title: Riepilogo della configurazione dell'heap dei descrittori
description: La tabella seguente riepiloga le informazioni sul supporto degli heap visibili agli shader e non shader.
ms.assetid: DF266915-6224-4FFB-BE3E-34A44F7318DD
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cfef479e88e5c77df0732113597a4742ecb909c
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335571"
---
# <a name="descriptor-heap-configurability-summary"></a><span data-ttu-id="9513c-103">Riepilogo della configurazione dell'heap dei descrittori</span><span class="sxs-lookup"><span data-stu-id="9513c-103">Descriptor Heap Configurability Summary</span></span>

<span data-ttu-id="9513c-104">La tabella seguente riepiloga le informazioni sul supporto degli heap visibili agli shader e non shader.</span><span class="sxs-lookup"><span data-stu-id="9513c-104">The following table summarizes information about Shader and non-Shader visible heap support.</span></span>



|                               | <span data-ttu-id="9513c-105">Heap descrittore visibile shader</span><span class="sxs-lookup"><span data-stu-id="9513c-105">Shader Visible Descriptor Heap</span></span>                                                 | <span data-ttu-id="9513c-106">Heap del descrittore non visibile allo shader</span><span class="sxs-lookup"><span data-stu-id="9513c-106">Non Shader Visible Descriptor Heap</span></span>                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9513c-107">**Tipi di heap supportati**</span><span class="sxs-lookup"><span data-stu-id="9513c-107">**Heap Types Supported**</span></span>          | <span data-ttu-id="9513c-108">CBV \_ SRV \_ UAV, Sampler</span><span class="sxs-lookup"><span data-stu-id="9513c-108">CBV\_SRV\_UAV, Sampler</span></span>                                                         | <span data-ttu-id="9513c-109">Tutti</span><span class="sxs-lookup"><span data-stu-id="9513c-109">All</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9513c-110">**Proprietà della pagina CPU supportate**</span><span class="sxs-lookup"><span data-stu-id="9513c-110">**CPU Page Properties Supported**</span></span> | <span data-ttu-id="9513c-111">NON \_ DISPONIBILE, COMBINAZIONE DI \_ SCRITTURA</span><span class="sxs-lookup"><span data-stu-id="9513c-111">NOT\_AVAILABLE, WRITE\_COMBINE</span></span>                                                 | <span data-ttu-id="9513c-112">WRITE \_ BACK</span><span class="sxs-lookup"><span data-stu-id="9513c-112">WRITE\_BACK</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="9513c-113">**Gestione della residenza per app**</span><span class="sxs-lookup"><span data-stu-id="9513c-113">**Residency Management By App**</span></span>   | <span data-ttu-id="9513c-114">Sì, responsabile dell'app</span><span class="sxs-lookup"><span data-stu-id="9513c-114">Yes, app responsible</span></span>                                                           | <span data-ttu-id="9513c-115">Non applicabile (non visibile alla GPU).</span><span class="sxs-lookup"><span data-stu-id="9513c-115">Not applicable (not GPU visible).</span></span>                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="9513c-116">**Supporto per la modifica del descrittore**</span><span class="sxs-lookup"><span data-stu-id="9513c-116">**Descriptor Edit Support**</span></span>       | <span data-ttu-id="9513c-117">Copiare solo la destinazione, tramite l'aggiornamento dell'elenco dei comandi e/o la copia della CPU se la CPU è visibile.</span><span class="sxs-lookup"><span data-stu-id="9513c-117">Copy destination only, via command list update and/or CPU copy if CPU visible.</span></span> | <span data-ttu-id="9513c-118">Solo lettura e scrittura della CPU.</span><span class="sxs-lookup"><span data-stu-id="9513c-118">CPU read and write only.</span></span> <span data-ttu-id="9513c-119">Nessun accesso diretto alla GPU.</span><span class="sxs-lookup"><span data-stu-id="9513c-119">No direct GPU access.</span></span> <span data-ttu-id="9513c-120">Può essere usato per la copia immediata della CPU (come origine e destinazione).</span><span class="sxs-lookup"><span data-stu-id="9513c-120">Can be used for immediate CPU copying (as a source and destination).</span></span> <span data-ttu-id="9513c-121">Può essere usato come origine di aggiornamento in un elenco di comandi. I descrittori verranno copiati nell'archivio dell'elenco dei comandi durante il record dell'elenco dei comandi.</span><span class="sxs-lookup"><span data-stu-id="9513c-121">Can be used as an update source on a command list – this will copy the descriptors into command list storage during command list record.</span></span> <span data-ttu-id="9513c-122">Durante l'esecuzione, la copia archiviata verrà copiata nella destinazione, che deve essere un heap visibile allo shader.</span><span class="sxs-lookup"><span data-stu-id="9513c-122">On execution, the stored copy will get copied to the destination, which must be a shader visible heap.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9513c-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9513c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9513c-124">Heap dei descrittori</span><span class="sxs-lookup"><span data-stu-id="9513c-124">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




