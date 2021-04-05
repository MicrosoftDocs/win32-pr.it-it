---
title: Comportamento predefinito dei driver
description: Comportamento predefinito dei driver
ms.assetid: ed6905eb-67ad-421d-be00-4a5585dff7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e5a4294ffc117041d3aca4273cd1f4b8378814
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726562"
---
# <a name="default-behavior-of-drivers"></a>Comportamento predefinito dei driver

In molte situazioni, le specifiche del comando MCI definiscono i valori predefiniti e il comportamento per i driver di un particolare tipo di dispositivo. Poiché i dispositivi multimediali possono avere un'ampia gamma di funzionalità e limitazioni, è possibile che si verifichino aree di comportamento indefinite. Inoltre, i driver possono gestire le eccezioni in modo diverso, in base alle funzionalità del dispositivo.

Si considerino, ad esempio, i comandi seguenti inviati a un driver audio Waveform usando la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :


```C++
mciSendString("open sound.wav alias sound", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("play sound notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("record sound from 0 notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



Il comando [**record**](record.md) restituisce un valore "Parameter out-of-range" e interrompe la riproduzione avviata dal comando [**Play**](play.md) precedente. Si può prevedere che il driver convalidi il comando record prima di arrestare la riproduzione, ma il driver interrompe prima la riproduzione.

 

 