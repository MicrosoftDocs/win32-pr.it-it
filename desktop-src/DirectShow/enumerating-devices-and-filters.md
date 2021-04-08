---
description: Enumerazione dei dispositivi e dei filtri
ms.assetid: 334bba2a-7477-4115-9ce0-d4495c1fc290
title: Enumerazione dei dispositivi e dei filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69997a4af4f3160f0b338bc9c595adea83a5354
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876829"
---
# <a name="enumerating-devices-and-filters"></a><span data-ttu-id="91b1f-103">Enumerazione dei dispositivi e dei filtri</span><span class="sxs-lookup"><span data-stu-id="91b1f-103">Enumerating Devices and Filters</span></span>

<span data-ttu-id="91b1f-104">A volte un'applicazione deve individuare un filtro particolare nel sistema dell'utente.</span><span class="sxs-lookup"><span data-stu-id="91b1f-104">Sometimes an application needs to locate a particular filter on the user's system.</span></span> <span data-ttu-id="91b1f-105">Ad esempio, un'applicazione di acquisizione video potrebbe visualizzare un elenco di dispositivi di acquisizione disponibili.</span><span class="sxs-lookup"><span data-stu-id="91b1f-105">For example, a video capture application might display a list of available capture devices.</span></span> <span data-ttu-id="91b1f-106">Poiché DirectShow usa un'architettura basata su componenti, non è possibile stabilire in fase di progettazione quali filtri sono installati nel sistema dell'utente.</span><span class="sxs-lookup"><span data-stu-id="91b1f-106">Because DirectShow uses a component-based architecture, you cannot know at design time which filters are installed on the user's system.</span></span> <span data-ttu-id="91b1f-107">Questa operazione è particolarmente valida per i filtri che rappresentano i dispositivi hardware.</span><span class="sxs-lookup"><span data-stu-id="91b1f-107">This is particularly true for filters that represent hardware devices.</span></span> <span data-ttu-id="91b1f-108">DirectShow fornisce due componenti che individuano i filtri registrati:</span><span class="sxs-lookup"><span data-stu-id="91b1f-108">DirectShow provides two components that locate registered filters:</span></span>

-   <span data-ttu-id="91b1f-109">L' [enumeratore di dispositivo di sistema](system-device-enumerator.md) trova i filtri in base alla relativa categoria.</span><span class="sxs-lookup"><span data-stu-id="91b1f-109">The [System Device Enumerator](system-device-enumerator.md) finds filters by their category.</span></span>
-   <span data-ttu-id="91b1f-110">Il [mapper del filtro](filter-mapper.md) trova i filtri in base ai criteri di ricerca forniti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="91b1f-110">The [Filter Mapper](filter-mapper.md) finds filters according to search criteria supplied by the application.</span></span>

<span data-ttu-id="91b1f-111">Gli enumeratori descritti in questa sezione seguono il formato standard usato dalle interfacce di enumerazione COM.</span><span class="sxs-lookup"><span data-stu-id="91b1f-111">The enumerators discussed in this section follow the standard form used by COM enumeration interfaces.</span></span> <span data-ttu-id="91b1f-112">Per ulteriori informazioni, vedere l'argomento "IEnumXXXX" in Microsoft Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="91b1f-112">For more information, see the "IEnumXXXX" topic in the Microsoft Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="91b1f-113">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="91b1f-113">This section contains the following topics:</span></span>

-   [<span data-ttu-id="91b1f-114">Uso di System Device Enumerator</span><span class="sxs-lookup"><span data-stu-id="91b1f-114">Using the System Device Enumerator</span></span>](using-the-system-device-enumerator.md)
-   [<span data-ttu-id="91b1f-115">Uso del mapper dei filtri</span><span class="sxs-lookup"><span data-stu-id="91b1f-115">Using the Filter Mapper</span></span>](using-the-filter-mapper.md)

## <a name="related-topics"></a><span data-ttu-id="91b1f-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="91b1f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91b1f-117">Attività DirectShow di base</span><span class="sxs-lookup"><span data-stu-id="91b1f-117">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 



