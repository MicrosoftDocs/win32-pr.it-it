---
description: La classe di dispositivo midi/out è costituita da sequencer MIDI usati per l'output. È possibile accedere a questi dispositivi usando le funzioni MIDI, descritte in Platform Software Development Kit (SDK).
ms.assetid: 398119ec-2d08-4c37-a993-a9b5ce52bcc8
title: midi/out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4c0199cc7918ab9aeacb3210b6f98d5ff03fc3bca90624bee00d864727ae0fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518611"
---
# <a name="midiout"></a>midi/out

La classe di dispositivo midi/out è costituita da sequencer MIDI usati per l'output. È possibile accedere a questi dispositivi usando le funzioni MIDI, descritte in Platform Software Development Kit (SDK).

Le [**funzioni lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) riempiono una struttura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) impostando il membro **dwStringFormat** sul valore STRINGFORMAT BINARY e aggiungendo \_ questo membro aggiuntivo:

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

Il **membro DeviceId** è l'identificatore di un dispositivo MIDI chiuso. Questo identificatore viene utilizzato in una chiamata alla [**funzione midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) per aprire il dispositivo per l'output. È possibile usare l'handle del dispositivo risultante per riprodurre i dati MIDI nel dispositivo linea o telefono.

Per altre informazioni sulle funzioni MIDI, vedere [**Funzioni multimediali**](../multimedia/multimedia-functions.md).

 

 
