---
description: Requisiti per i decodificatori
ms.assetid: 149aea20-0d37-4b1c-a098-8446c4088ce1
title: Requisiti per i decodificatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461120bec88636e4c015c2e319d855571e8ac1b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481452"
---
# <a name="requirements-for-decoders"></a><span data-ttu-id="64420-103">Requisiti per i decodificatori</span><span class="sxs-lookup"><span data-stu-id="64420-103">Requirements for Decoders</span></span>

<span data-ttu-id="64420-104">I decodificatori che inviano campioni a VMR devono rispettare le regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="64420-104">Decoders that deliver samples to the VMR must observe the following rules:</span></span>

-   <span data-ttu-id="64420-105">Deve essere recapitato un frame di sottoimmagine al VMR per ogni fotogramma video.</span><span class="sxs-lookup"><span data-stu-id="64420-105">There should be one subpicture frame delivered to the VMR for each video frame.</span></span> <span data-ttu-id="64420-106">I due frame dovrebbero avere gli stessi timestamp.</span><span class="sxs-lookup"><span data-stu-id="64420-106">The two frames should have the same time stamps.</span></span>
-   <span data-ttu-id="64420-107">Se l'immagine non è stata modificata, usare il \_ flag AM GBF \_ NOTASYNCPOINT nel metodo [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) per forzare l'allocatore a restituire un buffer contenente l'ultimo frame recapitato a VMR.</span><span class="sxs-lookup"><span data-stu-id="64420-107">If the subpicture has not changed, use the AM\_GBF\_NOTASYNCPOINT flag in the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method to force the allocator to return a buffer containing the last frame delivered to the VMR.</span></span> <span data-ttu-id="64420-108">È sufficiente inserire un nuovo timestamp sull'esempio e recapitarlo a VMR.</span><span class="sxs-lookup"><span data-stu-id="64420-108">Just put a new time stamp on the sample and deliver it to the VMR again.</span></span> <span data-ttu-id="64420-109">Se la notorietà dell'immagine non è vuota, è necessario recapitarla.</span><span class="sxs-lookup"><span data-stu-id="64420-109">If the subpicture fame is blank, you should still deliver it.</span></span> <span data-ttu-id="64420-110">Il VMR rileverà il frame vuoto e non lo mescolerà con il video.</span><span class="sxs-lookup"><span data-stu-id="64420-110">The VMR will detect the empty frame and not blend it with the video.</span></span> <span data-ttu-id="64420-111">Questo test viene eseguito dal chip VGA e non influisce sulle prestazioni di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="64420-111">This test is performed by the VGA chip and does not affect the playback performance.</span></span>
-   <span data-ttu-id="64420-112">Tutti gli esempi, ad eccezione dei flussi live, devono avere un timestamp di inizio e di fine valido collegati.</span><span class="sxs-lookup"><span data-stu-id="64420-112">All samples, except for live streams, must have valid start and stop time stamps attached.</span></span> <span data-ttu-id="64420-113">Il DVD non è un flusso live.</span><span class="sxs-lookup"><span data-stu-id="64420-113">(DVD is not a live stream.)</span></span>
-   <span data-ttu-id="64420-114">I timestamp del campione multimediale devono essere contigui</span><span class="sxs-lookup"><span data-stu-id="64420-114">The media sample time stamps must be contiguous</span></span>
-   <span data-ttu-id="64420-115">Il decodificatore deve identificarsi come VMR per l'uso da parte di generatori di Graph.</span><span class="sxs-lookup"><span data-stu-id="64420-115">The decoder must identify itself as VMR-capable for use by graph builders.</span></span>
-   <span data-ttu-id="64420-116">Il flusso di sottoimmagine dovrebbe ora contenere valori alfa incorporati per pixel.</span><span class="sxs-lookup"><span data-stu-id="64420-116">The subpicture stream should now contain embedded per-pixel alpha values.</span></span> <span data-ttu-id="64420-117">Il tipo di superficie ARGB4444 è ideale per le immagini secondarie.</span><span class="sxs-lookup"><span data-stu-id="64420-117">The ARGB4444 surface type is ideal for subpictures.</span></span>
-   <span data-ttu-id="64420-118">Non presupporre che lo stride della sottoimmagine sia uguale alla larghezza della superficie.</span><span class="sxs-lookup"><span data-stu-id="64420-118">Do not assume that the stride of the subpicture is the same as the surface width.</span></span> <span data-ttu-id="64420-119">Questo non è sempre il caso con VMR.</span><span class="sxs-lookup"><span data-stu-id="64420-119">This is not always the case with the VMR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64420-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="64420-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64420-121">Informazioni sull'accelerazione video DirectX</span><span class="sxs-lookup"><span data-stu-id="64420-121">About DirectX Video Acceleration</span></span>](about-directx-video-acceleration.md)
</dt> </dl>

 

 



