---
description: La classe del dispositivo wave/in è costituita da dispositivi audio per l'input audio Wave di basso livello.
ms.assetid: b2f32019-088f-4805-af7e-559a8179b1e6
title: Wave/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3465a575937538c6a4113ec544b1d246fec3a598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233254"
---
# <a name="wavein"></a>Wave/in

La classe del dispositivo wave/in è costituita da dispositivi audio per l'input audio Wave di basso livello. Per accedere a questi dispositivi, è possibile usare le funzioni Wave descritte nel Software Development Kit (SDK) della piattaforma. I dispositivi in questa classe sono associati a dispositivi line che supportano il \_ tipo di supporto AUTOMATEDVOICE LINEMEDIAMODE, specificato nel membro **dwMediaModes** della struttura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) per il dispositivo linea.

Le funzioni [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) compilano una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando il membro **dwStringFormat** sul \_ valore binario STRINGFORMAT e aggiungendo il membro aggiuntivo seguente:

``` syntax
DWORD DeviceId;  // identifier of audio device
```

Il membro **DeviceID** è l'identificatore di un dispositivo audio chiuso. Questo identificatore viene usato in una chiamata alla funzione [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) per aprire il dispositivo per l'input. È possibile usare l'handle del dispositivo risultante per registrare i dati audio digitati dalla linea o dal dispositivo telefonico.

Sebbene esista anche una classe di dispositivo "Wave" per i dispositivi audio Wave di basso livello, è consigliabile usare sempre la classe del dispositivo wave/in per l'input wave di basso livello.

Per altre informazioni sulle funzioni Wave, vedere [**funzioni multimediali**](../multimedia/multimedia-functions.md).

 

 
