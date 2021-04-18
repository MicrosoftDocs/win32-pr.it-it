---
title: Acquisizione diretta da un dispositivo a un file ASF (QASF)
description: Acquisizione diretta da un dispositivo a un file ASF (QASF)
ms.assetid: 684a11e3-d507-4219-bc0b-6dfe5e85dad1
keywords:
- Windows Media Format SDK, acquisizione da dispositivi a file ASF (QASF)
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), acquisizione da dispositivi (QASF)
- ASF (formato avanzato dei sistemi), acquisizione da dispositivi (QASF)
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, acquisizione da dispositivi a file ASF (QASF)
- Windows Media Format SDK, QASF
- Formato Advanced Systems (ASF), QASF
- ASF (formato avanzato dei sistemi), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faaf5ba8df3cffbb2121451d3bd1b456fc994078
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298561"
---
# <a name="capturing-directly-from-a-device-to-an-asf-file-qasf"></a><span data-ttu-id="72f42-114">Acquisizione diretta da un dispositivo a un file ASF (QASF)</span><span class="sxs-lookup"><span data-stu-id="72f42-114">Capturing Directly from a Device to an ASF File (QASF)</span></span>

<span data-ttu-id="72f42-115">Quando si acquisisce audio o video direttamente in un file ASF, il grafo del filtro è simile al diagramma seguente, a seconda del tipo di dispositivo di acquisizione usato.</span><span class="sxs-lookup"><span data-stu-id="72f42-115">When capturing audio or video directly to an ASF file, the filter graph looks something like the following diagram, depending on the type of capture device being used.</span></span>

![grafico di acquisizione da webcam a WMV](images/asf-webcam.png)

<span data-ttu-id="72f42-117">Nella documentazione di DirectShow SDK viene descritto in dettaglio come creare grafici di acquisizione, ma è importante ricordare quando si creano grafici di acquisizione usando il writer ASF WM: il writer ASF WM non verrà eseguito a meno che tutti i relativi pin non siano connessi.</span><span class="sxs-lookup"><span data-stu-id="72f42-117">The DirectShow SDK documentation describes in detail how to create capture graphs, but there is one important point to remember when creating capture graphs using the WM ASF Writer: the WM ASF Writer will not run unless all of its pins are connected.</span></span> <span data-ttu-id="72f42-118">Se si configura il writer ASF WM con il profilo di sistema predefinito (scelta non consigliata) o qualsiasi profilo con flussi audio e video, verrà creato un pin di input per ogni flusso e ognuno di questi pin deve essere connesso.</span><span class="sxs-lookup"><span data-stu-id="72f42-118">If you configure the WM ASF Writer with the default system profile (not recommended), or any profile with audio and video streams, then it will create an input pin for each stream and each of those pins must be connected.</span></span> <span data-ttu-id="72f42-119">Se non si intende acquisire audio, ad esempio, assicurarsi di configurare il filtro con un profilo di solo video in modo che non venga creato alcun pin audio.</span><span class="sxs-lookup"><span data-stu-id="72f42-119">If you do not intend to capture audio, for example, then be sure to configure the filter with a video-only profile so that no audio pin is created.</span></span>

 

 




