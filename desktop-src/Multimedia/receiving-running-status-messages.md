---
title: Ricezione Running-Status messaggi
description: Ricezione Running-Status messaggi
ms.assetid: 4f2e8e41-89f6-45e3-ae16-47b856f0e63e
keywords:
- MIDI (Musical Instrument Digital Interface), stato di esecuzione
- MIDI (Musical Instrument Digital Interface), stato di esecuzione
- registrazione di audio MIDI, stato di esecuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4d782e1e25c718ddd177d1d9baf471d0715d70680b65920052e85d6fffc551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371346"
---
# <a name="receiving-running-status-messages"></a>Ricezione Running-Status messaggi

La *specifica MIDI Files 1.0*  standard consente l'uso dello stato di esecuzione quando un messaggio ha lo stesso byte di stato del messaggio precedente. Quando si usa lo stato di esecuzione, è possibile omettere il byte di stato dei messaggi successivi. Tutti i driver di dispositivo di input MIDI sono necessari per espandere i messaggi usando lo stato di esecuzione in messaggi completi, in modo da ricevere sempre messaggi MIDI completi da un driver di dispositivo di input MIDI.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione dell'audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 




