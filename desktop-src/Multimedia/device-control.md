---
title: Controllo dispositivo (Windows multimediali)
description: Controllo dei dispositivi
ms.assetid: b4479803-f1da-4646-909e-c4ef412ebdcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6878e5e759f3eddb5e98d241d9a8d081005e3545dc2f0054b46630619eaa06fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497241"
---
# <a name="device-control-windows-multimedia"></a>Controllo dispositivo (Windows multimediali)

Per controllare un dispositivo MCI, aprire il dispositivo, inviare i comandi necessari e quindi chiudere il dispositivo. I comandi possono essere molto simili, anche per dispositivi MCI completamente diversi. Ad esempio, la serie seguente di comandi MCI riproduce la sesta traccia di un CD audio usando la [**funzione mciSendString:**](/previous-versions//dd757161(v=vs.85))


```C++
mciSendString("open cdaudio", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("set cdaudio time format tmsf", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("play cdaudio from 6 to 7", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close cdaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



L'esempio seguente mostra una serie simile di comandi MCI che riproduce i primi 10.000 campioni di un file audio waveform:


```C++
mciSendString(
    "open c:\mmdata\purplefi.wav type waveaudio alias finch", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
mciSendString("set finch time format samples", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("play finch from 1 to 10000", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close finch", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



Questi esempi illustrano alcuni fatti interessanti sui comandi MCI:

-   Gli stessi comandi di base ([**open**](open.md), [**set**](set.md), [**play**](play.md)e [**close)**](close.md)vengono usati con i dispositivi audio CD e audio waveform. Gli stessi comandi MCI vengono usati con tutti i dispositivi MCI.
-   Il comando open per il dispositivo audio waveform include una specifica del nome file. Il dispositivo audio waveform è un dispositivo composto *(associato* a un file di dati), mentre il dispositivo audio CD è un dispositivo semplice *(uno* senza un file di dati associato).
-   Il set comando specifica i formati di ora in ogni caso, ma il flag di formato ora per il dispositivo audio CD specifica tracce/minuti/secondi/frame (TMSF), mentre il formato dell'ora usato con il dispositivo audio waveform specifica "samples".
-   Le variabili usate con i flag "from" e "to" sono appropriate per il rispettivo formato di ora. Ad esempio, per il dispositivo audio CD, le variabili specificano un intervallo di tracce, ma per il dispositivo audio waveform, le variabili specificano un intervallo di campioni.

 

 
