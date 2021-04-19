---
description: Sequenza temporale
ms.assetid: a3b8bff2-8593-483c-af49-a975ab2dc330
title: Sequenza temporale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6ac73b84409629f63ad4be469edf6b943f9e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319555"
---
# <a name="the-timeline"></a><span data-ttu-id="9a65a-103">Sequenza temporale</span><span class="sxs-lookup"><span data-stu-id="9a65a-103">The Timeline</span></span>

<span data-ttu-id="9a65a-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="9a65a-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="9a65a-105">La sequenza temporale espone l'interfaccia [**IAMTimeline**](iamtimeline.md) .</span><span class="sxs-lookup"><span data-stu-id="9a65a-105">The timeline exposes the [**IAMTimeline**](iamtimeline.md) interface.</span></span> <span data-ttu-id="9a65a-106">Questa interfaccia contiene i metodi per l'impostazione delle proprietà nella sequenza temporale; per aggiungere gruppi alla sequenza temporale; e per la creazione di oggetti della sequenza temporale, ad esempio gruppi, tracce e origini.</span><span class="sxs-lookup"><span data-stu-id="9a65a-106">This interface contains methods for setting properties on the timeline; for adding groups to the timeline; and for creating timeline objects, such as groups, tracks, and sources.</span></span> <span data-ttu-id="9a65a-107">Per creare una nuova sequenza temporale, chiamare la funzione standard **CoCreateInstance** come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="9a65a-107">To create a new timeline, call the standard **CoCreateInstance** function as follows:</span></span>


```C++
IAMTimeline *pTL = NULL;
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
        IID_IAMTimeline, (void**)&pTL);
```



<span data-ttu-id="9a65a-108">La nuova sequenza temporale è vuota.</span><span class="sxs-lookup"><span data-stu-id="9a65a-108">The new timeline is empty.</span></span> <span data-ttu-id="9a65a-109">A questo punto è possibile caricare un file di progetto esistente (vedere [caricamento e visualizzazione in anteprima di un progetto](loading-and-previewing-a-project.md)) o creare la sequenza temporale creando e inserendo nuovi oggetti (vedere costruzione di [una sequenza temporale](constructing-a-timeline.md)).</span><span class="sxs-lookup"><span data-stu-id="9a65a-109">At this point you can either load an existing project file (see [Loading and Previewing a Project](loading-and-previewing-a-project.md)), or build up the timeline by creating and inserting new objects (see [Constructing a Timeline](constructing-a-timeline.md)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a65a-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9a65a-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a65a-111">Panoramica dei componenti della sequenza temporale</span><span class="sxs-lookup"><span data-stu-id="9a65a-111">Overview of the Timeline Components</span></span>](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



