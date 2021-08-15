---
title: Ricezione Time-Stamped messaggi MIDI
description: Ricezione Time-Stamped messaggi MIDI
ms.assetid: a91c85fe-f9c4-4cf6-b0bb-49aa8ed45644
keywords:
- Instrument Digital Interface (MIDI), messaggi con timestamp
- MIDI (Instrument Digital Interface), messaggi con timestamp
- registrazione di audio MIDI, messaggi con timestamp
- messaggi MIDI con timestamp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec36628a417c19824e25c7ad013da9c539fe88cb6e58fd829a32205bce35679
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371291"
---
# <a name="receiving-time-stamped-midi-messages"></a>Ricezione Time-Stamped messaggi MIDI

A causa del ritardo tra il momento in cui il driver di dispositivo riceve un messaggio MIDI e l'ora in cui l'applicazione riceve il messaggio, i driver di dispositivo di input MIDI contrassegnano il messaggio MIDI con l'ora di ricezione del messaggio. I timestamp MIDI, definiti come ora di ricezione del primo byte del messaggio, sono specificati in millisecondi. La [**funzione midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) reimposta i timestamp per un dispositivo su zero.

Come indicato in precedenza, per ricevere timestamp con input MIDI, è necessario usare una funzione di callback. Il *parametro dwParam2* della funzione di callback specifica il timestamp per i dati associati ai messaggi MIM [**\_ DATA**](mim-data.md) [**MIM \_ LONGDATA.**](mim-longdata.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 