---
title: Comportamento predefinito dei driver
description: Comportamento predefinito dei driver
ms.assetid: ed6905eb-67ad-421d-be00-4a5585dff7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61312010759ddd1bf152f0e51f7605bda1954329096913b61dac14a671908f0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144524"
---
# <a name="default-behavior-of-drivers"></a>Comportamento predefinito dei driver

In molte situazioni, le specifiche del comando MCI definiscono i valori predefiniti e il comportamento per i driver di un particolare tipo di dispositivo. Poiché i dispositivi multimediali possono avere un'ampia gamma di funzionalità (e limitazioni), possono esserci aree di comportamento non definite. Inoltre, i driver possono gestire le eccezioni in modo diverso, in base alle funzionalità del dispositivo.

Si considerino ad esempio i comandi seguenti inviati a un driver waveform-audio usando la [**funzione mciSendString:**](/previous-versions//dd757161(v=vs.85))


```C++
mciSendString("open sound.wav alias sound", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("play sound notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("record sound from 0 notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



Il [**comando record**](record.md) restituisce un valore "Parametro non compreso nell'intervallo" e arresta la riproduzione avviata dal comando di [**riproduzione**](play.md) precedente. Si potrebbe prevedere che il driver convalidi il comando di registrazione prima di arrestare la riproduzione, ma il driver arresta prima la riproduzione.

 

 