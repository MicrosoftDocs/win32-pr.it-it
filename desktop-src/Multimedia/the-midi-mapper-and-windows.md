---
title: Il mapper MIDI e Windows
description: Il mapper MIDI e Windows
ms.assetid: a077f935-e085-4148-9975-7926ac018f0c
keywords:
- MIDI (Musical Instrument Digital Interface), Mapper MIDI
- MIDI (Musical Instrument Digital Interface), MIDI Mapper
- Mapper MIDI, architettura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951ad3cee4fb37de6ecbfdc4f81860afcb9f589d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046677"
---
# <a name="the-midi-mapper-and-windows"></a>Il mapper MIDI e Windows

Il mapper MIDI è parte del software di sistema. Nella figura seguente viene illustrato il modo in cui il mapper MIDI si riferisce ad altri elementi dei servizi audio.

![relazione tra il mapper MIDI e altri elementi dell'immagine dei servizi audio](images/mmap-a01.gif)

Dal punto di vista di un'applicazione, il mapper MIDI si presenta come un altro dispositivo di output MIDI. Il mapper MIDI riceve i messaggi inviati dalle funzioni di output MIDI di basso livello [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) e [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg). Il mapper MIDI modifica questi messaggi e li reindirizza a un dispositivo di output MIDI in base alla mappa di configurazione MIDI corrente. La mappa di installazione MIDI corrente viene selezionata dall'utente tramite l'opzione pannello di controllo MIDI. Solo l'utente può selezionare la mappa di installazione corrente. le applicazioni non possono modificare la mappa di installazione corrente.

 

 