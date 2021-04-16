---
description: Creazione di una sequenza temporale
ms.assetid: 4909f797-d296-4c9f-83fb-543e48bbe75d
title: Creazione di una sequenza temporale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c16b1134eb92b3e3ac5a0f1919d7c4a2736b206
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401260"
---
# <a name="constructing-a-timeline"></a><span data-ttu-id="f41e6-103">Creazione di una sequenza temporale</span><span class="sxs-lookup"><span data-stu-id="f41e6-103">Constructing a Timeline</span></span>

<span data-ttu-id="f41e6-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="f41e6-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="f41e6-105">Questo articolo descrive come costruire una sequenza temporale nei [servizi di modifica DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="f41e6-105">This article describes how to construct a timeline in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="f41e6-106">Viene presentata un'applicazione console di esempio che crea una sequenza temporale e ne esegue il rendering.</span><span class="sxs-lookup"><span data-stu-id="f41e6-106">It presents an example console application that creates a timeline and renders it.</span></span> <span data-ttu-id="f41e6-107">La sequenza temporale è minima, costituita da un singolo gruppo video con una clip di origine, ma illustra la maggior parte dei concetti necessari per creare sequenze temporali più complesse.</span><span class="sxs-lookup"><span data-stu-id="f41e6-107">The timeline is minimal, consisting of a single video group with one source clip, but it demonstrates most of the concepts needed to create more complex timelines.</span></span>

<span data-ttu-id="f41e6-108">Questo articolo contiene gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="f41e6-108">This article contains the following topics.</span></span>

-   [<span data-ttu-id="f41e6-109">Creazione di oggetti Timeline</span><span class="sxs-lookup"><span data-stu-id="f41e6-109">Creating Timeline Objects</span></span>](creating-timeline-objects.md)
-   [<span data-ttu-id="f41e6-110">Creazione di gruppi, composizioni e tracce</span><span class="sxs-lookup"><span data-stu-id="f41e6-110">Creating Groups, Compositions, and Tracks</span></span>](creating-groups-compositions-and-tracks.md)
-   [<span data-ttu-id="f41e6-111">Impostazione del tipo di supporto di gruppo</span><span class="sxs-lookup"><span data-stu-id="f41e6-111">Setting the Group Media Type</span></span>](setting-the-group-media-type.md)
-   [<span data-ttu-id="f41e6-112">Aggiunta di un'origine</span><span class="sxs-lookup"><span data-stu-id="f41e6-112">Adding a Source</span></span>](adding-a-source.md)
-   [<span data-ttu-id="f41e6-113">Creazione di una sequenza temporale: codice di esempio</span><span class="sxs-lookup"><span data-stu-id="f41e6-113">Creating a Timeline: Example Code</span></span>](creating-a-timeline--example-code.md)

## <a name="related-topics"></a><span data-ttu-id="f41e6-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f41e6-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f41e6-115">Uso dei servizi di modifica DirectShow</span><span class="sxs-lookup"><span data-stu-id="f41e6-115">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



