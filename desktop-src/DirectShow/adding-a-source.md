---
description: Aggiunta di un'origine
ms.assetid: 8c5d1050-a696-4a5d-be68-806420d0cd78
title: Aggiunta di un'origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee583cd8971c183f2e03b92f68e2d6ba555c41db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304270"
---
# <a name="adding-a-source"></a><span data-ttu-id="a9855-103">Aggiunta di un'origine</span><span class="sxs-lookup"><span data-stu-id="a9855-103">Adding a Source</span></span>

<span data-ttu-id="a9855-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="a9855-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="a9855-105">Creare un oggetto di origine nello stesso modo in cui si creano altri oggetti della sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="a9855-105">Create a source object the same way you create other timeline objects.</span></span> <span data-ttu-id="a9855-106">Prima di inserirlo nella sequenza temporale, tuttavia, è necessario specificare almeno le proprietà seguenti nell'origine.</span><span class="sxs-lookup"><span data-stu-id="a9855-106">Before inserting it into the timeline, however, you must specify at least the following properties on the source.</span></span>

-   <span data-ttu-id="a9855-107">Ora di inizio e di fine rispetto alla sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="a9855-107">The start and stop times, relative to the timeline.</span></span> <span data-ttu-id="a9855-108">Chiamare il metodo [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md) .</span><span class="sxs-lookup"><span data-stu-id="a9855-108">Call the [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md) method.</span></span>
-   <span data-ttu-id="a9855-109">File multimediale da utilizzare come origine.</span><span class="sxs-lookup"><span data-stu-id="a9855-109">The media file to use as a source.</span></span> <span data-ttu-id="a9855-110">Chiamare il metodo [**IAMTimelineSrc:: Semedianame**](iamtimelinesrc-setmedianame.md) con una stringa di caratteri wide che rappresenta il nome del file.</span><span class="sxs-lookup"><span data-stu-id="a9855-110">Call the [**IAMTimelineSrc::SetMediaName**](iamtimelinesrc-setmedianame.md) method with a wide-character string representing the name of the file.</span></span>
-   <span data-ttu-id="a9855-111">L'ora di inizio e di fine del supporto, che sono relative al file originale.</span><span class="sxs-lookup"><span data-stu-id="a9855-111">The media start and stop times, which are relative to the original file.</span></span> <span data-ttu-id="a9855-112">Chiamare il metodo [**IAMTimelineSrc:: SetMediaTimes**](iamtimelinesrc-setmediatimes.md) .</span><span class="sxs-lookup"><span data-stu-id="a9855-112">Call the [**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md) method.</span></span> <span data-ttu-id="a9855-113">Per altre informazioni sui tempi dei supporti, vedere [Time in DirectShow editing Services](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="a9855-113">For more information about media times, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="a9855-114">Nell'esempio seguente il clip di origine inizia quattro secondi nel file.</span><span class="sxs-lookup"><span data-stu-id="a9855-114">In the following example, the source clip starts four seconds into the file.</span></span> <span data-ttu-id="a9855-115">La durata del supporto è di 10 secondi, il doppio della durata della sequenza temporale, che indica che l'origine verrà riprodotto alla velocità di due volte normale.</span><span class="sxs-lookup"><span data-stu-id="a9855-115">The media duration is 10 seconds, twice the length of the timeline duration, meaning the source will play at twice normal speed.</span></span> <span data-ttu-id="a9855-116">Le unità di costante sono definite come 10 milioni (10 ^ 7) ed è uguale a un secondo.</span><span class="sxs-lookup"><span data-stu-id="a9855-116">The constant UNITS is defined as 10000000 (10^7) and equals one second.</span></span>


```C++
pSourceObj->SetStartStop(0, 50000000)
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.avi"), 15);
pSource->SetMediaName(bstrFile); 
SysFreeString(bstrFile);
pSource->SetMediaTimes(40000000, 140000000);
```



> [!Note]  
> <span data-ttu-id="a9855-117">Attualmente, DES non può eseguire contemporaneamente il rendering di più di 75 origini compresse con codec di Gestione compressione video (VCM).</span><span class="sxs-lookup"><span data-stu-id="a9855-117">Currently, DES cannot simultaneously render more than 75 sources that were compressed with Video Compression Manager (VCM) codecs.</span></span> <span data-ttu-id="a9855-118">Inoltre, se il progetto contiene più di 75 origini di questo tipo, è necessario utilizzare la riconnessione dinamica oppure il programma DES non può visualizzare in anteprima il progetto.</span><span class="sxs-lookup"><span data-stu-id="a9855-118">Also, if the project as a whole contains more than 75 such sources, you must use dynamic reconnection or DES cannot preview the project.</span></span> <span data-ttu-id="a9855-119">Per ulteriori informazioni, vedere [**IRenderEngine:: SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span><span class="sxs-lookup"><span data-stu-id="a9855-119">For more information, see [**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span></span>

 

<span data-ttu-id="a9855-120">Per ulteriori informazioni sulle origini, vedere [utilizzo delle origini](working-with-sources.md).</span><span class="sxs-lookup"><span data-stu-id="a9855-120">For more information about sources, see [Working with Sources](working-with-sources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9855-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a9855-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9855-122">Creazione di una sequenza temporale</span><span class="sxs-lookup"><span data-stu-id="a9855-122">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



