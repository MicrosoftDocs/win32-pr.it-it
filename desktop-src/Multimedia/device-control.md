---
title: Controllo del dispositivo (Windows Multimedia)
description: Controllo dei dispositivi
ms.assetid: b4479803-f1da-4646-909e-c4ef412ebdcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0e0b59127d160cc44418fd4bce1f9f670d13de
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047741"
---
# <a name="device-control-windows-multimedia"></a>Controllo del dispositivo (Windows Multimedia)

Per controllare un dispositivo MCI, aprire il dispositivo, inviare i comandi necessari e quindi chiudere il dispositivo. I comandi possono essere molto simili, anche per i dispositivi MCI completamente diversi. Ad esempio, la serie seguente di comandi MCI riproduce la sesta traccia di un CD audio usando la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :


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



Nell'esempio riportato di seguito viene illustrata una serie simile di comandi MCI che riproduce i primi 10.000 esempi di un file Waveform-Audio:


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



Questi esempi illustrano alcuni aspetti interessanti sui comandi MCI:

-   Gli stessi comandi di base ([**apertura**](open.md), [**impostazione**](set.md), [**riproduzione**](play.md)e [**chiusura**](close.md)) vengono usati con i dispositivi audio CD e Waveform-Audio. Gli stessi comandi MCI vengono usati con tutti i dispositivi MCI.
-   Il comando Apri per il dispositivo Waveform-Audio include una specifica del nome file. Il dispositivo Waveform-Audio è un *dispositivo composto* (uno associato a un file di dati), mentre il dispositivo audio CD è un *dispositivo semplice* (uno senza un file di dati associato).
-   Il comando set specifica i formati di ora in ogni caso, ma il flag di formato time per il dispositivo audio CD specifica il formato Tracks/minutes/seconds/frames (TMSF), mentre il formato dell'ora usato con il dispositivo Waveform-Audio specifica "Samples".
-   Le variabili utilizzate con i flag "from" e "to" sono appropriate per il rispettivo formato di ora. Per il dispositivo audio CD, ad esempio, le variabili specificano un intervallo di tracce, ma per il dispositivo Waveform-Audio le variabili specificano un intervallo di campioni.

 

 
