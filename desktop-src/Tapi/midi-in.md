---
description: La classe di dispositivo midi/in è costituita da sequencer MIDI usati per l'input. È possibile accedere a questi dispositivi usando le funzioni MIDI, descritte in Platform Software Development Kit (SDK).
ms.assetid: 8997a391-bf61-4ec9-8ffc-fe3e6b92d63a
title: midi/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d309fe510b08a1e86ef6a00b34a9e3d3282c993babe78eb45aeb6ebb0dab1eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659951"
---
# <a name="midiin"></a>midi/in

La classe di dispositivo midi/in è costituita da sequencer MIDI usati per l'input. È possibile accedere a questi dispositivi usando le funzioni MIDI, descritte in Platform Software Development Kit (SDK).

Le [**funzioni lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) riempiono una struttura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) impostando il membro **dwStringFormat** sul valore STRINGFORMAT BINARY e aggiungendo \_ questo membro aggiuntivo:

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

Il **membro DeviceId** è l'identificatore di un dispositivo MIDI chiuso. Questo identificatore viene utilizzato in una chiamata alla [**funzione midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) per aprire il dispositivo per l'input. È possibile usare l'handle del dispositivo risultante per registrare i dati MIDI dal dispositivo linea o telefono.

Per altre informazioni sulle funzioni MIDI, vedere [**Funzioni multimediali**](../multimedia/multimedia-functions.md).

 

 
