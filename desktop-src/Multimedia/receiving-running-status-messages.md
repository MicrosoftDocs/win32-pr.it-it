---
title: Ricezione di messaggi di Running-Status
description: Ricezione di messaggi di Running-Status
ms.assetid: 4f2e8e41-89f6-45e3-ae16-47b856f0e63e
keywords:
- MIDI (Musical Instrument Digital Interface), stato di esecuzione
- MIDI (Musical Instrument Digital Interface), stato di esecuzione
- registrazione audio MIDI, stato di esecuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0a4d12a19f525a6fa673747063774bf4507d65b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395382"
---
# <a name="receiving-running-status-messages"></a>Ricezione di messaggi di Running-Status

La specifica dei *file MIDI Standard 1,0* consente di utilizzare *lo stato di esecuzione* quando un messaggio ha lo stesso byte di stato del messaggio precedente. Quando si utilizza lo stato di esecuzione, il byte di stato dei messaggi successivi può essere omesso. Tutti i driver di dispositivo di input MIDI sono necessari per espandere i messaggi utilizzando lo stato di esecuzione in messaggi completi, in modo da ricevere sempre messaggi MIDI completi da un driver di dispositivo di input MIDI.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 




