---
description: Oggetti secondari
ms.assetid: 03cbd590-b573-4a98-9ab7-fe548800cfcb
title: Oggetti secondari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8b427a315231577f1608a168629bc8b77d2cc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883726"
---
# <a name="subobjects"></a><span data-ttu-id="46ae0-103">Oggetti secondari</span><span class="sxs-lookup"><span data-stu-id="46ae0-103">Subobjects</span></span>

<span data-ttu-id="46ae0-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="46ae0-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="46ae0-105">Origini, effetti e transizioni hanno puntatori interni ad altri oggetti COM, detti *sottooggetti*.</span><span class="sxs-lookup"><span data-stu-id="46ae0-105">Sources, effects, and transitions have internal pointers to other COM objects, called *subobjects*.</span></span> <span data-ttu-id="46ae0-106">Il sottooggetto esegue il lavoro effettivo dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="46ae0-106">The subobject performs the actual work of the object.</span></span> <span data-ttu-id="46ae0-107">Il sottooggetto di un'origine è il componente che crea il video o i dati audio.</span><span class="sxs-lookup"><span data-stu-id="46ae0-107">The subobject of a source is the component that creates the video or audio data.</span></span> <span data-ttu-id="46ae0-108">Il sottooggetto di un effetto o di una transizione è il componente che trasforma i dati. ad esempio, in un effetto video, viene creato l'effetto visivo nel flusso video.</span><span class="sxs-lookup"><span data-stu-id="46ae0-108">The subobject of an effect or transition is the component that transforms the data; for example, in a video effect, it creates the visual effect in the video stream.</span></span>

<span data-ttu-id="46ae0-109">Il tipo di oggetto SubObject dipende dal tipo di oggetto:</span><span class="sxs-lookup"><span data-stu-id="46ae0-109">The type of subobject depends on the type of object:</span></span>

-   <span data-ttu-id="46ae0-110">Origine: qualsiasi filtro di origine o filtro del parser DirectShow che supporta la ricerca e produce un formato supportato da DES.</span><span class="sxs-lookup"><span data-stu-id="46ae0-110">Source: Any DirectShow source filter or parser filter that supports seeking and produces a format that DES supports.</span></span> <span data-ttu-id="46ae0-111">Può trattarsi di un formato compresso se esistono filtri DirectShow per decodificarlo.</span><span class="sxs-lookup"><span data-stu-id="46ae0-111">It can be a compressed format if DirectShow filters exist to decode it.</span></span>
-   <span data-ttu-id="46ae0-112">Effetto: per i video, qualsiasi oggetto 2D® DirectX® Transform a input singolo.</span><span class="sxs-lookup"><span data-stu-id="46ae0-112">Effect: For video, any 2-D one-input Microsoft® DirectX® Transform object.</span></span> <span data-ttu-id="46ae0-113">Per audio, qualsiasi filtro effetto audio DirectShow.</span><span class="sxs-lookup"><span data-stu-id="46ae0-113">For audio, any DirectShow audio effect filter.</span></span>
-   <span data-ttu-id="46ae0-114">Transizione: per video, qualsiasi oggetto di trasformazione DirectX a due input 2D.</span><span class="sxs-lookup"><span data-stu-id="46ae0-114">Transition: For video, any 2-D two-input DirectX Transform object.</span></span> <span data-ttu-id="46ae0-115">L'audio non supporta le transizioni.</span><span class="sxs-lookup"><span data-stu-id="46ae0-115">Audio does not support transitions.</span></span>

<span data-ttu-id="46ae0-116">Gruppi, composizioni e tracce non dispongono di sottooggetti.</span><span class="sxs-lookup"><span data-stu-id="46ae0-116">Groups, compositions, and tracks do not have subobjects.</span></span>

<span data-ttu-id="46ae0-117">L'applicazione non imposta direttamente il puntatore del sottooggetto.</span><span class="sxs-lookup"><span data-stu-id="46ae0-117">The application does not directly set the subobject pointer.</span></span> <span data-ttu-id="46ae0-118">Per gli effetti e le transizioni, l'applicazione chiama il metodo [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) per specificare il GUID dell'oggetto SubObject.</span><span class="sxs-lookup"><span data-stu-id="46ae0-118">For effects and transitions, the application calls the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method to specify the GUID of the subobject.</span></span> <span data-ttu-id="46ae0-119">Per gli oggetti di origine, un'applicazione chiama in genere [**IAMTimelineSrc:: Semedianame**](iamtimelinesrc-setmedianame.md) per specificare il nome di un file di origine.</span><span class="sxs-lookup"><span data-stu-id="46ae0-119">For source objects, an application typically calls the [**IAMTimelineSrc::SetMediaName**](iamtimelinesrc-setmedianame.md) to specify the name of a source file.</span></span> <span data-ttu-id="46ae0-120">Tuttavia, il metodo **SetSubObjectGUID** può essere usato anche per gli oggetti di origine, per specificare l'identificatore di classe (CLSID) di un filtro.</span><span class="sxs-lookup"><span data-stu-id="46ae0-120">However, the **SetSubObjectGUID** method can also be used for source objects, to specify the class identifier (CLSID) of a filter.</span></span>

<span data-ttu-id="46ae0-121">Per ulteriori informazioni, vedere [utilizzo di origini](working-with-sources.md) e [utilizzo di effetti e transizioni](working-with-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="46ae0-121">For more information, see [Working with Sources](working-with-sources.md) and [Working with Effects and Transitions](working-with-effects-and-transitions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="46ae0-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="46ae0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46ae0-123">Panoramica dei componenti della sequenza temporale</span><span class="sxs-lookup"><span data-stu-id="46ae0-123">Overview of the Timeline Components</span></span>](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



