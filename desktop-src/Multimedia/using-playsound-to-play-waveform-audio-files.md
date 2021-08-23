---
title: Uso di PlaySound per riprodurre Waveform-Audio file
description: Uso di PlaySound per riprodurre Waveform-Audio file
ms.assetid: 8b7d191b-6b0c-4dff-84de-cb3a5c314b80
keywords:
- audio waveform, funzione PlaySound
- audio waveform, riproduzione di file
- audio waveform, estensione di file WAV
- Funzione PlaySound, riproduzione di file audio waveform
- riproduzione di file audio waveform,funzione PlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa83125665e2a99cc0f47da0893cbc113c0be7a251d62eb66a91e7a1218dac5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687851"
---
# <a name="using-playsound-to-play-waveform-audio-files"></a>Uso di PlaySound per riprodurre Waveform-Audio file

La maggior parte dei file audio waveform usa . Estensione del nome file WAV.

L'istruzione seguente riproduce C: \\ SOUNDS \\ BELLS. File WAV:


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC); 
```



Se il file specificato non esiste o se il file non rientra nella memoria disponibile, [**PlaySound**](/previous-versions//dd743680(v=vs.85)) riproduce il suono di sistema predefinito. Se non è stato definito alcun suono di sistema predefinito, **PlaySound** ha esito negativo senza produrre alcun suono. Se non si vuole riprodurre il suono di sistema predefinito, specificare il flag SND \_ NODEFAULT, come illustrato nell'esempio seguente:


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC | SND_NODEFAULT); 
```



 

 