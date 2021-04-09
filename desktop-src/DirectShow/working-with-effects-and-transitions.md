---
description: Utilizzo degli effetti e delle transizioni
ms.assetid: 00e97d02-ff43-4e1f-9806-abaeb9288058
title: Utilizzo degli effetti e delle transizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99029269ac86e17246fd641341b071654582bc4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968688"
---
# <a name="working-with-effects-and-transitions"></a><span data-ttu-id="03e5f-103">Utilizzo degli effetti e delle transizioni</span><span class="sxs-lookup"><span data-stu-id="03e5f-103">Working with Effects and Transitions</span></span>

<span data-ttu-id="03e5f-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="03e5f-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="03e5f-105">Gli effetti modificano un singolo clip, traccia o composizione.</span><span class="sxs-lookup"><span data-stu-id="03e5f-105">Effects modify a single clip, track, or composition.</span></span> <span data-ttu-id="03e5f-106">Le transizioni creano un seques da una traccia o compositionsto un altro.</span><span class="sxs-lookup"><span data-stu-id="03e5f-106">Transitions create seques from one track or compositionsto another.</span></span>

<span data-ttu-id="03e5f-107">I [servizi di modifica DirectShow](directshow-editing-services.md) usano oggetti di trasformazione DirectX per le transizioni video e gli effetti video.</span><span class="sxs-lookup"><span data-stu-id="03e5f-107">[DirectShow Editing Services](directshow-editing-services.md) uses DirectX Transform objects for its video transitions and video effects.</span></span> <span data-ttu-id="03e5f-108">Per le transizioni video, usare qualsiasi oggetto di trasformazione DirectX a due input 2D.</span><span class="sxs-lookup"><span data-stu-id="03e5f-108">For video transitions, use any 2-D two-input DirectX Transform object.</span></span> <span data-ttu-id="03e5f-109">Per gli effetti video, usare qualsiasi oggetto trasformazione DirectX a input singolo 2D.</span><span class="sxs-lookup"><span data-stu-id="03e5f-109">For video effects, use any 2-D one-input DirectX Transform object.</span></span> <span data-ttu-id="03e5f-110">Microsoft non supporta più lo sviluppo di oggetti di trasformazione DirectX di terze parti.</span><span class="sxs-lookup"><span data-stu-id="03e5f-110">Microsoft no longer supports the development of third-party DirectX Transform objects.</span></span> <span data-ttu-id="03e5f-111">Tuttavia, diverse sono fornite con DirectShow e altre sono fornite con Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="03e5f-111">However, several are provided with DirectShow and others are provided with Microsoft Internet Explorer.</span></span> <span data-ttu-id="03e5f-112">Per ulteriori informazioni sulle transizioni fornite con Internet Explorer, vedere [riferimenti a filtri visivi e transizioni](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms532853(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="03e5f-112">For more information about the transitions provided with Internet Explorer, see [Visual Filters and Transitions Reference](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms532853(v=vs.85)).</span></span>

<span data-ttu-id="03e5f-113">Per gli effetti audio, è possibile usare qualsiasi filtro effetto audio DirectShow.</span><span class="sxs-lookup"><span data-stu-id="03e5f-113">For audio effects, you can use any DirectShow audio effect filter.</span></span> <span data-ttu-id="03e5f-114">DES fornisce anche un [effetto busta volume](volume-envelope-effect.md) per l'impostazione del volume su una traccia o un clip.</span><span class="sxs-lookup"><span data-stu-id="03e5f-114">DES also provides a [Volume Envelope Effect](volume-envelope-effect.md) for setting the volume on a track or clip.</span></span> <span data-ttu-id="03e5f-115">DES non supporta le transizioni audio.</span><span class="sxs-lookup"><span data-stu-id="03e5f-115">DES does not support audio transitions.</span></span>

<span data-ttu-id="03e5f-116">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="03e5f-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="03e5f-117">Aggiunta di oggetti Effect e Transition</span><span class="sxs-lookup"><span data-stu-id="03e5f-117">Adding Effect and Transition Objects</span></span>](adding-effect-and-transition-objects.md)
-   [<span data-ttu-id="03e5f-118">Anteprima degli effetti e delle transizioni</span><span class="sxs-lookup"><span data-stu-id="03e5f-118">Previewing Effects and Transitions</span></span>](previewing-effects-and-transitions.md)
-   [<span data-ttu-id="03e5f-119">Enumerazione degli effetti e delle transizioni</span><span class="sxs-lookup"><span data-stu-id="03e5f-119">Enumerating Effects and Transitions</span></span>](enumerating-effects-and-transitions.md)
-   [<span data-ttu-id="03e5f-120">Impostazione delle proprietà per effetti e transizioni</span><span class="sxs-lookup"><span data-stu-id="03e5f-120">Setting Properties on Effects and Transitions</span></span>](setting-properties-on-effects-and-transitions.md)
-   [<span data-ttu-id="03e5f-121">Direzione della transizione</span><span class="sxs-lookup"><span data-stu-id="03e5f-121">Transition Direction</span></span>](transition-direction.md)

## <a name="related-topics"></a><span data-ttu-id="03e5f-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="03e5f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03e5f-123">Uso dei servizi di modifica DirectShow</span><span class="sxs-lookup"><span data-stu-id="03e5f-123">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 
