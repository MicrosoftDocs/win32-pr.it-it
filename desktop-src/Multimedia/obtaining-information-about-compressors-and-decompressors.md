---
title: Recupero di informazioni sui compressori e sui decompressori
description: Recupero di informazioni sui compressori e sui decompressori
ms.assetid: 2f1edfd0-dd30-42ea-a5ae-24265d3f8af3
keywords:
- gestione compressione video(VCM), recupero di informazioni sui compressi
- VCM (gestione compressione video), recupero di informazioni sui compressi
- Funzione ICGetInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b023a8f82fa92aa78a2a2dcf47a8f6c9447f943ac0f68440c6d7aff3123fc84e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038441"
---
# <a name="obtaining-information-about-compressors-and-decompressors"></a>Recupero di informazioni sui compressori e sui decompressori

Nell'esempio seguente viene utilizzata [**la funzione ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) per ottenere informazioni su un compressore o un decompressore.


```C++
ICINFO ICInfo; 
ICGetInfo(hIC, &ICInfo, sizeof(ICInfo)); 
 
```



Nell'esempio seguente vengono utilizzate le macro [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) e [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) per ottenere i valori predefiniti.


```C++
DWORD dwKeyFrameRate, dwQuality; 
dwKeyFrameRate = ICGetDefaultKeyFrameRate(hIC); 
dwQuality = ICGetDefaultQuality(hIC); 
 
```



Nell'esempio seguente vengono utilizzate le macro [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) e [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) per visualizzare una finestra di dialogo Informazioni su per il compressore o il decompressore, se presente.


```C++
// If the compressor has an About dialog box, display it.

if ( ICQueryAbout(hIC)) ICAbout(hIC, hwndApp); 
 
```



 

 




