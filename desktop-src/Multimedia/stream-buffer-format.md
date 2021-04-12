---
title: Formato del buffer del flusso
description: Formato del buffer del flusso
ms.assetid: 4b24c12e-b43f-492e-a000-af4f59d5e16f
keywords:
- MIDI (Musical Instrument Digital Interface), buffer di flusso
- MIDI (Musical Instrument Digital Interface), buffer di flusso
- buffer di flusso, formato
- Struttura MIDIHDR
- Struttura MIDIEVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801a7f0dbeabd0d7aebeae0387af415a831e4658
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398854"
---
# <a name="stream-buffer-format"></a>Formato del buffer del flusso

Il membro **lpData** della struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) punta a un buffer del flusso e il membro **dwBufferLength** specifica le dimensioni effettive del buffer. Il membro **dwBytesRecorded** di **MIDIHDR** specifica il numero di byte nel buffer usati effettivamente dagli eventi MIDI; Questo valore deve essere minore o uguale al valore specificato da **dwBufferLength**.

Ogni evento MIDI nel buffer del flusso viene specificato da una struttura [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) , che contiene l'ora per l'evento, un identificatore di flusso, un codice evento e, quando appropriato, i parametri per l'evento. Ognuna di queste strutture **MIDIEVENT** deve iniziare con un limite di parola doppia. Se necessario, i byte di riempimento devono essere aggiunti alla fine della struttura per garantire che il successivo venga avviato su un limite di parola doppia.

 

 