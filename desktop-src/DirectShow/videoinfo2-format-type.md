---
description: Tipo di formato VideoInfo2
ms.assetid: edd2013a-f0c5-4176-ba3a-a3af719ce31d
title: Tipo di formato VideoInfo2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74b0f435e0e2a1b5b1d948c42a881f19300a9c6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308952"
---
# <a name="videoinfo2-format-type"></a><span data-ttu-id="551c8-103">Tipo di formato VideoInfo2</span><span class="sxs-lookup"><span data-stu-id="551c8-103">VideoInfo2 Format Type</span></span>

<span data-ttu-id="551c8-104">Il tipo di supporto preferito del PIN di anteprima potrebbe essere un tipo con formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="551c8-104">A preview pin's preferred media type might be a type with a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format.</span></span> <span data-ttu-id="551c8-105">Questa struttura di formato supporta funzionalità speciali, ad esempio proporzioni di video e immagini interlacciate.</span><span class="sxs-lookup"><span data-stu-id="551c8-105">This format structure supports special features such as interlaced video and picture aspect ratios.</span></span>

<span data-ttu-id="551c8-106">VMR-7 e VMR-9 supportano entrambi [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) direttamente.</span><span class="sxs-lookup"><span data-stu-id="551c8-106">The VMR-7 and the VMR-9 both support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) directly.</span></span> <span data-ttu-id="551c8-107">Quando si connette VMR al decodificatore, il formato migliore sarà negoziato.</span><span class="sxs-lookup"><span data-stu-id="551c8-107">When you connect the VMR to the decoder, they will negotiate the best format.</span></span> <span data-ttu-id="551c8-108">Il filtro renderer video precedente, tuttavia, non supporta **VIDEOINFOHEADER2**.</span><span class="sxs-lookup"><span data-stu-id="551c8-108">The older Video Renderer filter, however, does not support **VIDEOINFOHEADER2**.</span></span> <span data-ttu-id="551c8-109">Per usare i tipi di formato **VIDEOINFOHEADER2** con il filtro renderer video, è necessario inserire il filtro [Overlay Mixer](overlay-mixer-filter.md) nel grafico.</span><span class="sxs-lookup"><span data-stu-id="551c8-109">To use **VIDEOINFOHEADER2** format types with the Video Renderer filter, you must insert the [Overlay Mixer](overlay-mixer-filter.md) filter into the graph.</span></span>

1.  <span data-ttu-id="551c8-110">Enumerare i tipi di supporto preferiti sul pin di output del filtro decodificatore usando il metodo [**Ipin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="551c8-110">Enumerate the preferred media types on the decoder filter's output pin, using the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>
2.  <span data-ttu-id="551c8-111">Controllare il primo tipo di supporto nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="551c8-111">Check the first media type in the enumeration sequence.</span></span>
3.  <span data-ttu-id="551c8-112">Se il formato del tipo **è \_ VideoInfo2**, connettere il pin di output al mixer della sovrimpressione.</span><span class="sxs-lookup"><span data-stu-id="551c8-112">If the format type is **FORMAT\_VideoInfo2**, connect the output pin to the Overlay Mixer.</span></span> <span data-ttu-id="551c8-113">Connettere quindi il mixer della sovrimpressione al renderer video.</span><span class="sxs-lookup"><span data-stu-id="551c8-113">Then connect the Overlay Mixer to the video renderer.</span></span> <span data-ttu-id="551c8-114">(Vedere [pin della porta video](video-port-pins.md)).</span><span class="sxs-lookup"><span data-stu-id="551c8-114">(See [Video Port Pins](video-port-pins.md).)</span></span>

<span data-ttu-id="551c8-115">Se non si è interessati a queste funzionalità, non è necessario usare il mixer overlay.</span><span class="sxs-lookup"><span data-stu-id="551c8-115">If you do not care about these features, you do not have to use the Overlay Mixer.</span></span> <span data-ttu-id="551c8-116">Connettere il decodificatore direttamente al renderer video e si connetterà invece con un formato [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="551c8-116">Connect the decoder directly to the Video Renderer, and it will connect with a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) format instead.</span></span>

## <a name="related-topics"></a><span data-ttu-id="551c8-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="551c8-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="551c8-118">Argomenti sull'acquisizione avanzata</span><span class="sxs-lookup"><span data-stu-id="551c8-118">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="551c8-119">Uso del mixer overlay in acquisizione video</span><span class="sxs-lookup"><span data-stu-id="551c8-119">Using the Overlay Mixer in Video Capture</span></span>](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



