---
description: La classe del dispositivo MIDI/out è costituita da sequencer MIDI usati per l'output. Per accedere a questi dispositivi, è possibile usare le funzioni MIDI descritte nel Software Development Kit (SDK) della piattaforma.
ms.assetid: 398119ec-2d08-4c37-a993-a9b5ce52bcc8
title: MIDI/out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6ae6a3daba8fa0520fca666e6c43a8b3db86c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225863"
---
# <a name="midiout"></a>MIDI/out

La classe del dispositivo MIDI/out è costituita da sequencer MIDI usati per l'output. Per accedere a questi dispositivi, è possibile usare le funzioni MIDI descritte nel Software Development Kit (SDK) della piattaforma.

Le funzioni [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) compilano una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando il membro **dwStringFormat** sul \_ valore binario STRINGFORMAT e aggiungendo il membro aggiuntivo seguente:

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

Il membro **DeviceID** è l'identificatore di un dispositivo MIDI chiuso. Questo identificatore viene usato in una chiamata alla funzione [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) per aprire il dispositivo per l'output. È possibile usare l'handle del dispositivo risultante per riprodurre dati MIDI alla riga o al dispositivo telefonico.

Per altre informazioni sulle funzioni MIDI, vedere [**funzioni multimediali**](../multimedia/multimedia-functions.md).

 

 
