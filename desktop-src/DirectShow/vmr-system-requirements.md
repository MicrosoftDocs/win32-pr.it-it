---
description: Requisiti di sistema di VMR
ms.assetid: fd50b312-73f0-4c68-a8b1-3497d958bc8f
title: Requisiti di sistema di VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d54d6d1604c3e514f3ceef379eaba4a8fa1ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232279"
---
# <a name="vmr-system-requirements"></a><span data-ttu-id="3a45e-103">Requisiti di sistema di VMR</span><span class="sxs-lookup"><span data-stu-id="3a45e-103">VMR System Requirements</span></span>

<span data-ttu-id="3a45e-104">VMR usa esclusivamente le funzionalità di elaborazione grafica della scheda video del computer; il VMR non esegue alcuna operazione di fusione o rendering dei video usando il processore host, perché a tale scopo potrebbe avere un notevole effetto sulla frequenza dei fotogrammi e sulla qualità del video visualizzato.</span><span class="sxs-lookup"><span data-stu-id="3a45e-104">The VMR uses the graphics-processing capabilities of the computer's display card exclusively; the VMR does not perform any blending or rendering of video using the host processor, because to do so would greatly impact the frame rate and quality of the video being displayed.</span></span> <span data-ttu-id="3a45e-105">Quando si sfruttano le nuove funzionalità offerte da VMR, in particolare la fusione di più flussi video e/o immagini di applicazioni, le prestazioni complessive ottenute dipendono fortemente dalle funzionalità della scheda grafica utilizzata nel computer.</span><span class="sxs-lookup"><span data-stu-id="3a45e-105">When taking advantage of the new features offered by the VMR, particularly blending of multiple video streams and/or application images, the overall performance obtained is highly dependent on the capabilities of the graphics card being used on the computer.</span></span> <span data-ttu-id="3a45e-106">Le schede grafiche che offrono prestazioni ottimali con VMR hanno il seguente supporto hardware integrato:</span><span class="sxs-lookup"><span data-stu-id="3a45e-106">Graphics cards that perform well with the VMR have the following hardware support built into them:</span></span>

-   <span data-ttu-id="3a45e-107">Supporto per le superfici di trama Direct3D e "non di potenza di 2".</span><span class="sxs-lookup"><span data-stu-id="3a45e-107">Support for YUV and "non-power of 2" Direct3D texture surfaces.</span></span>
-   <span data-ttu-id="3a45e-108">Possibilità di StretchBlt da YUV a superfici DirectDraw RGB.</span><span class="sxs-lookup"><span data-stu-id="3a45e-108">The ability to StretchBlt from YUV to RGB DirectDraw surfaces.</span></span>
-   <span data-ttu-id="3a45e-109">Almeno 16 MB di memoria video se è necessario combinare più flussi video.</span><span class="sxs-lookup"><span data-stu-id="3a45e-109">At least 16MB of video memory if multiple video streams are to be blended together.</span></span> <span data-ttu-id="3a45e-110">La quantità effettiva di memoria necessaria dipende dalle dimensioni dell'immagine dei flussi video e dalla risoluzione della modalità di visualizzazione usata.</span><span class="sxs-lookup"><span data-stu-id="3a45e-110">The actual amount of memory required is dependent on the image size of the video streams and resolution of the display mode being used.</span></span>
-   <span data-ttu-id="3a45e-111">Supporto per una sovrapposizione RGB o la possibilità di fondersi a una superficie di sovrimpressione YUV.</span><span class="sxs-lookup"><span data-stu-id="3a45e-111">Support for an RGB overlay or the ability to blend to a YUV overlay surface.</span></span>
-   <span data-ttu-id="3a45e-112">Video con accelerazione hardware (supporto per l'accelerazione video DirectX) con decodifica.</span><span class="sxs-lookup"><span data-stu-id="3a45e-112">Hardware-accelerated video (support for DirectX Video Acceleration) decoding.</span></span>
-   <span data-ttu-id="3a45e-113">Velocità di riempimento in pixel elevate.</span><span class="sxs-lookup"><span data-stu-id="3a45e-113">High pixel fill rates.</span></span>

> [!Note]  
> <span data-ttu-id="3a45e-114">Il VMR richiede che il monitor di sistema sia impostato per una profondità di colore di almeno 16 bit.</span><span class="sxs-lookup"><span data-stu-id="3a45e-114">The VMR requires that the system monitor be set for a color depth of at least 16 bits.</span></span> <span data-ttu-id="3a45e-115">Il VMR non può essere impostato su uno stato di esecuzione se il monitoraggio è impostato per 256 colori.</span><span class="sxs-lookup"><span data-stu-id="3a45e-115">The VMR cannot be put into a run state if the monitor is set for 256 colors.</span></span> <span data-ttu-id="3a45e-116">Inoltre, alcune schede video non possono eseguire operazioni Direct3D quando la visualizzazione è impostata su 24 bit per pixel.</span><span class="sxs-lookup"><span data-stu-id="3a45e-116">Also, some video cards cannot perform Direct3D operations when the display is set to 24 bits per pixel.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3a45e-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3a45e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a45e-118">Informazioni sul rendering del mixaggio video</span><span class="sxs-lookup"><span data-stu-id="3a45e-118">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
</dt> </dl>

 

 



