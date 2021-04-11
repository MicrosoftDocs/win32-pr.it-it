---
title: Per creare una configurazione di ridistribuzione
description: Per creare una configurazione di ridistribuzione
ms.assetid: cf2c8fa1-cfd6-47cc-b572-ba1b95d59105
keywords:
- Windows Media Format SDK, ridistribuzione software
- ASF (Advanced Systems Format), ridistribuzione del software
- ASF (formato avanzato dei sistemi), ridistribuzione del software
- Windows Media Format SDK, ridistribuzione
- ASF (Advanced Systems Format), ridistribuzione
- ASF (formato avanzato dei sistemi), ridistribuzione
- ridistribuzione del software, creazione
- ridistribuzione del software, WMFDist.exe
- ridistribuzione, creazione
- ridistribuzione, WMFDist.exe
- WMFDist.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0c2f241d8c1ad164bc14608103f423a7aba78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221360"
---
# <a name="to-create-a-redistribution-setup"></a><span data-ttu-id="48916-114">Per creare una configurazione di ridistribuzione</span><span class="sxs-lookup"><span data-stu-id="48916-114">To Create a Redistribution Setup</span></span>

1.  <span data-ttu-id="48916-115">Chiedere alla routine di installazione di installare i file dell'applicazione e apportare le impostazioni necessarie prima di richiamare il pacchetto di ridistribuzione.</span><span class="sxs-lookup"><span data-stu-id="48916-115">Have your setup routine install your application files and make required settings before invoking the redistribution package.</span></span>
2.  <span data-ttu-id="48916-116">Installare WMFDist.exe.</span><span class="sxs-lookup"><span data-stu-id="48916-116">Install WMFDist.exe.</span></span> <span data-ttu-id="48916-117">È possibile utilizzare il flag/Q: a per eseguire un'installazione automatica e non interattiva ed escludere l'interfaccia utente della configurazione di ridistribuzione durante l'installazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="48916-117">You can use the /Q:A flag to do a quiet, unattended installation and suppress the user interface of the redistribution setup during the installation of your application.</span></span> <span data-ttu-id="48916-118">La routine deve quindi rilevare se il riavvio è necessario alla fine.</span><span class="sxs-lookup"><span data-stu-id="48916-118">Your routine must then detect whether restarting is needed at the end.</span></span>

    <span data-ttu-id="48916-119">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="48916-119">For example:</span></span>

    ```C++
    WMFDist.exe /Q:A
    ```

    

## <a name="related-topics"></a><span data-ttu-id="48916-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="48916-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48916-121">**Ridistribuzione del software**</span><span class="sxs-lookup"><span data-stu-id="48916-121">**Software Redistribution**</span></span>](software-redistribution.md)
</dt> </dl>

 

 




