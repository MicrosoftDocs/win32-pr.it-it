---
title: Ricezione di Time-Stamped messaggi MIDI
description: Ricezione di Time-Stamped messaggi MIDI
ms.assetid: a91c85fe-f9c4-4cf6-b0bb-49aa8ed45644
keywords:
- MIDI (Musical Instrument Digital Interface), messaggi con timestamp
- MIDI (Musical Instrument Digital Interface), messaggi con timestamp
- registrazione audio MIDI, messaggi con timestamp
- messaggi MIDI con timestamp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ead268c6d022f67a3607bb8a43a3d773bd7325
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337111"
---
# <a name="receiving-time-stamped-midi-messages"></a>Ricezione di Time-Stamped messaggi MIDI

A causa del ritardo che intercorre tra la ricezione di un messaggio MIDI da parte del driver di dispositivo e il momento in cui l'applicazione riceve il messaggio, i driver del dispositivo di input MIDI contrassegnano il messaggio MIDI con l'ora in cui il messaggio è stato ricevuto. I timestamp MIDI, definiti come l'ora in cui è stato ricevuto il primo byte del messaggio, vengono specificati in millisecondi. La funzione [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) Reimposta il timestamp di un dispositivo su zero.

Come indicato in precedenza, per ricevere timestamp con input MIDI, è necessario usare una funzione di callback. Il parametro *dwParam2* della funzione di callback specifica il timestamp per i dati associati ai [**\_ dati MIM**](mim-data.md) e ai messaggi [**\_ LONGDATA MIM**](mim-longdata.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 