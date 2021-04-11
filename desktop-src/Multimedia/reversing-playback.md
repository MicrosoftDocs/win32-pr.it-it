---
title: Inversione della riproduzione
description: Inversione della riproduzione
ms.assetid: cb7c1293-42d7-4c74-b9e6-cc8899ca7c54
keywords:
- MCIWndPlayReverse (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a708915679f75bfe478c160d71d35b0bcfa48a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395914"
---
# <a name="reversing-playback"></a><span data-ttu-id="70930-104">Inversione della riproduzione</span><span class="sxs-lookup"><span data-stu-id="70930-104">Reversing Playback</span></span>

<span data-ttu-id="70930-105">Alcuni dispositivi supportano la riproduzione in direzione inversa.</span><span class="sxs-lookup"><span data-stu-id="70930-105">Some devices support playback in the reverse direction.</span></span> <span data-ttu-id="70930-106">È possibile riprodurre il contenuto di un dispositivo di questo tipo in direzione inversa usando la macro [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) .</span><span class="sxs-lookup"><span data-stu-id="70930-106">You can play the content of such a device in the reverse direction by using the [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) macro.</span></span> <span data-ttu-id="70930-107">Questa macro definisce l'ambito di riproduzione dalla posizione corrente fino all'inizio del contenuto.</span><span class="sxs-lookup"><span data-stu-id="70930-107">This macro defines the playback scope from the current playback position to the beginning of the content.</span></span> <span data-ttu-id="70930-108">Il dispositivo Digital-video, MCIAVI. DRV, può riprodurre le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="70930-108">The digital-video device, MCIAVI.DRV, can play backward.</span></span> <span data-ttu-id="70930-109">Quando viene richiamato **MCIWndPlayReverse** , i dispositivi che non possono riprodurre versioni precedenti, ad esempio audio CD, possono generare un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="70930-109">Devices that cannot play backward, such as CD audio, can issue an error message when **MCIWndPlayReverse** is invoked.</span></span>

 

 




