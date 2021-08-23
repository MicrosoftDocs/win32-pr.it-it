---
title: Formato del buffer di flusso
description: Formato del buffer di flusso
ms.assetid: 4b24c12e-b43f-492e-a000-af4f59d5e16f
keywords:
- Instrument Digital Interface (MIDI), buffer di flusso
- MIDI (Instrument Digital Interface), buffer di flusso
- buffer di flusso, formato
- Struttura MIDIHDR
- Struttura MIDIEVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 072c2541ab6b731686fc63c59b11b0dfff529ef9cab347d41fbddf13e9b60b04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688501"
---
# <a name="stream-buffer-format"></a>Formato del buffer di flusso

Il **membro lpData** della struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) punta a un buffer di flusso e il membro **dwBufferLength** specifica le dimensioni effettive di questo buffer. Il **membro dwBytesRecorded** di **MIDIHDR** specifica il numero di byte nel buffer effettivamente usati dagli eventi MIDI. Questo valore deve essere minore o uguale al valore specificato da **dwBufferLength**.

Ogni evento MIDI nel buffer del flusso viene specificato da una struttura [**MIDIEVENT,**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) che contiene l'ora dell'evento, un identificatore di flusso, un codice evento e, quando appropriato, i parametri per l'evento. Ognuna di queste **strutture MIDIEVENT** deve iniziare su un limite doubleword. Se necessario, i byte di riempimento devono essere aggiunti alla fine della struttura per garantire che quello successivo inizi su un limite doubleword.

 

 