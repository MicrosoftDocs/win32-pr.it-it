---
description: La classe del dispositivo wave/out è costituita da dispositivi audio per l'output audio Wave di basso livello.
ms.assetid: 85894134-e8ad-43e2-8b97-09b80bfd36d5
title: Wave/out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975a3308b6f0b29e130ad07534494e1cb1d991a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885821"
---
# <a name="waveout"></a>Wave/out

La classe del dispositivo wave/out è costituita da dispositivi audio per l'output audio Wave di basso livello. Per accedere a questi dispositivi, è possibile usare le funzioni Wave descritte nel Software Development Kit (SDK) della piattaforma. I dispositivi in questa classe sono associati a dispositivi line che supportano il \_ tipo di supporto AUTOMATEDVOICE LINEMEDIAMODE, specificato nel membro **dwMediaModes** della struttura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) per il dispositivo linea.

Le funzioni [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) compilano una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando il membro **dwStringFormat** sul \_ valore binario STRINGFORMAT e aggiungendo il membro aggiuntivo seguente:

``` syntax
DWORD DeviceId;  // identifier of audio device
```

Il membro **DeviceID** è l'identificatore di un dispositivo audio chiuso. Questo identificatore viene usato in una chiamata alla funzione [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) per aprire il dispositivo per l'output. È possibile usare l'handle del dispositivo risultante per riprodurre dati audio digitalizzati sulla linea o sul dispositivo telefonico.

Sebbene esista anche una classe di dispositivo "Wave" per i dispositivi audio Wave di basso livello, è consigliabile usare sempre la classe del dispositivo wave/out per l'output wave di basso livello.

Per altre informazioni sulle funzioni Wave, vedere [**funzioni multimediali**](../multimedia/multimedia-functions.md).

 

 
