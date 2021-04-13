---
title: Uso di PlaySound per il ciclo di suoni
description: Uso di PlaySound per il ciclo di suoni
ms.assetid: 747b9a76-5ff3-488e-ba85-c4d926e1e723
keywords:
- audio Waveform, funzione PlaySound
- audio della forma d'onda, suoni di loop
- audio Waveform, parametro fdwSound
- Funzione PlaySound, looping Sounds
- Funzione PlaySound, parametro fdwSound
- loop della forma d'onda-suoni audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5373e703c7a02068094e312dee18690a797b330e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398852"
---
# <a name="using-playsound-to-loop-sounds"></a>Uso di PlaySound per il ciclo di suoni

Se si specificano i \_ flag SND loop e snd \_ Async per il parametro *FdwSound* della funzione [**PlaySound**](/previous-versions//dd743680(v=vs.85)) , il suono continuerà a riprodurre ripetutamente, come illustrato nell'esempio seguente:


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_LOOP | SND_ASYNC); 
```



Se si vuole eseguire il loop di un suono, è necessario riprodurlo in modo asincrono. non è possibile usare il \_ flag di sincronizzazione SND con il \_ flag del ciclo SND. Un suono a loop continuerà a essere eseguito fino a quando non si chiama **PlaySound** per riprodurre un altro suono. Per interrompere la riproduzione di un suono (in ciclo o asincrono) senza riprodurre un altro suono, utilizzare l'istruzione seguente:


```C++
PlaySound(NULL, NULL, 0); 
```



 

 