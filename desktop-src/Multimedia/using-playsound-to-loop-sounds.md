---
title: Uso di PlaySound per riprodurre in ciclo i suoni
description: Uso di PlaySound per riprodurre in ciclo i suoni
ms.assetid: 747b9a76-5ff3-488e-ba85-c4d926e1e723
keywords:
- audio waveform, funzione PlaySound
- audio waveform, suoni a ciclo continuo
- waveform audio,fdwSound parameter
- Funzione PlaySound, riproduzione a ciclo continuo di suoni
- Funzione PlaySound, parametro fdwSound
- looping waveform-audio sounds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf97321a72ab566bf622e725700dbf336ddba6d92b9b8e6df9150357492656f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136119"
---
# <a name="using-playsound-to-loop-sounds"></a>Uso di PlaySound per riprodurre in ciclo i suoni

Se si specificano i flag SND LOOP e SND ASYNC per il parametro \_ \_ *fdwSound* della funzione [**PlaySound,**](/previous-versions//dd743680(v=vs.85)) il suono continuerà a essere riprodotto ripetutamente come illustrato nell'esempio seguente:


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_LOOP | SND_ASYNC); 
```



Se si vuole riprodurre un suono a ciclo continuo, è necessario riprodurlo in modo asincrono. non è possibile usare il flag SND \_ SYNC con il flag LOOP SND. \_ Un suono a ciclo continuo continuerà a essere riprodotto fino a quando non si chiama **PlaySound** per riprodurre un altro suono. Per interrompere la riproduzione di un suono (a ciclo continuo o asincrono) senza riprodurre un altro suono, usare l'istruzione seguente:


```C++
PlaySound(NULL, NULL, 0); 
```



 

 