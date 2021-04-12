---
title: Ottenere informazioni sui compressori e i decompressori
description: Ottenere informazioni sui compressori e i decompressori
ms.assetid: 2f1edfd0-dd30-42ea-a5ae-24265d3f8af3
keywords:
- Gestione compressione video (VCM), recupero di informazioni sui commediatori
- VCM (Video Compression Manager), recupero di informazioni sui commediatori
- ICGetInfo (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 874793233ef0aec4de5b372573fb8dcd79f5d875
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395546"
---
# <a name="obtaining-information-about-compressors-and-decompressors"></a><span data-ttu-id="0f698-106">Ottenere informazioni sui compressori e i decompressori</span><span class="sxs-lookup"><span data-stu-id="0f698-106">Obtaining Information About Compressors and Decompressors</span></span>

<span data-ttu-id="0f698-107">Nell'esempio seguente viene usata la funzione [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) per ottenere informazioni su un compressore o un decompressore.</span><span class="sxs-lookup"><span data-stu-id="0f698-107">The following example uses the [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) function to obtain information about a compressor or decompressor.</span></span>


```C++
ICINFO ICInfo; 
ICGetInfo(hIC, &ICInfo, sizeof(ICInfo)); 
 
```



<span data-ttu-id="0f698-108">Nell'esempio seguente vengono usate le macro [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) e [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) per ottenere i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="0f698-108">The following example uses the [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) and [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) macros to obtain the default values.</span></span>


```C++
DWORD dwKeyFrameRate, dwQuality; 
dwKeyFrameRate = ICGetDefaultKeyFrameRate(hIC); 
dwQuality = ICGetDefaultQuality(hIC); 
 
```



<span data-ttu-id="0f698-109">Nell'esempio seguente vengono utilizzate le macro [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) e [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) per visualizzare una finestra di dialogo informazioni su per il compressore o il decompressore, se la finestra di dialogo è presente.</span><span class="sxs-lookup"><span data-stu-id="0f698-109">The following example uses the [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) and [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) macros to display an About dialog box for the compressor or decompressor, if the dialog box exists.</span></span>


```C++
// If the compressor has an About dialog box, display it.

if ( ICQueryAbout(hIC)) ICAbout(hIC, hwndApp); 
 
```



 

 




