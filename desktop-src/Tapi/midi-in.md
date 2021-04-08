---
description: La classe del dispositivo MIDI/in è costituita da sequencer MIDI usati per l'input. Per accedere a questi dispositivi, è possibile usare le funzioni MIDI descritte nel Software Development Kit (SDK) della piattaforma.
ms.assetid: 8997a391-bf61-4ec9-8ffc-fe3e6b92d63a
title: MIDI/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d8119990af37cb030211b7dcc3a75d5261411f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749538"
---
# <a name="midiin"></a>MIDI/in

La classe del dispositivo MIDI/in è costituita da sequencer MIDI usati per l'input. Per accedere a questi dispositivi, è possibile usare le funzioni MIDI descritte nel Software Development Kit (SDK) della piattaforma.

Le funzioni [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) compilano una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando il membro **dwStringFormat** sul \_ valore binario STRINGFORMAT e aggiungendo il membro aggiuntivo seguente:

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

Il membro **DeviceID** è l'identificatore di un dispositivo MIDI chiuso. Questo identificatore viene usato in una chiamata alla funzione [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) per aprire il dispositivo per l'input. È possibile usare l'handle del dispositivo risultante per registrare i dati MIDI dalla linea o dal dispositivo telefonico.

Per altre informazioni sulle funzioni MIDI, vedere [**funzioni multimediali**](../multimedia/multimedia-functions.md).

 

 
