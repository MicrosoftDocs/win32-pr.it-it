---
title: Riproduzione di cicli per MCIWnd
description: Riproduzione di cicli (MCIWnd)
ms.assetid: 59e27271-332a-4c62-bfcd-5377cdbf0848
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2d6a22e917cf764b37444bcaf4afb0393e1c1b
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334385"
---
# <a name="looping-playback-for-mciwnd"></a><span data-ttu-id="e3e5d-103">Riproduzione di cicli per MCIWnd</span><span class="sxs-lookup"><span data-stu-id="e3e5d-103">Looping Playback for MCIWnd</span></span>

<span data-ttu-id="e3e5d-104">MCIWnd supporta la riproduzione come ciclo continuo.</span><span class="sxs-lookup"><span data-stu-id="e3e5d-104">MCIWnd supports playback as a continuous loop.</span></span> <span data-ttu-id="e3e5d-105">È possibile riprodurre ripetutamente il contenuto di un file o di un dispositivo come ciclo utilizzando la macro [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) in combinazione con il pulsante **Riproduci** sulla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="e3e5d-105">You can play the content of a file or device repeatedly as a loop by using the [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) macro in combination with the **Play** button on the toolbar.</span></span> <span data-ttu-id="e3e5d-106">Il dispositivo di riproduzione video, MCIAVI, supporta i cicli di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="e3e5d-106">The video playback device, MCIAVI, supports playback loops.</span></span> <span data-ttu-id="e3e5d-107">Per determinare se la riproduzione continua è stata attivata, usare la macro [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) .</span><span class="sxs-lookup"><span data-stu-id="e3e5d-107">To determine if continuous playback has been activated, use the [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) macro.</span></span>

 

 




