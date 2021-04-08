---
title: Apertura di dispositivi di input MIDI
description: Apertura di dispositivi di input MIDI
ms.assetid: fd6ebd0c-6985-49d3-8015-a636d4c70ff3
keywords:
- MIDI (Musical Instrument Digital Interface), dispositivi di input
- MIDI (Musical Instrument Digital Interface), dispositivi di input
- registrazione audio MIDI, dispositivi di input
- Dispositivi di input MIDI
- MIDI (Musical Instrument Digital Interface), apertura di dispositivi di input
- MIDI (Musical Instrument Digital Interface), apertura di dispositivi di input
- registrazione audio MIDI, apertura di dispositivi di input
- apertura di dispositivi di input MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4c1271cee1e6a47c35f8c555932d87d1055065
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726319"
---
# <a name="opening-midi-input-devices"></a>Apertura di dispositivi di input MIDI

Per aprire un dispositivo di input MIDI per la registrazione, usare la funzione [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) . Questa funzione apre il dispositivo associato all'identificatore di dispositivo specificato e restituisce un handle del dispositivo aperto scrivendo l'handle in una posizione di memoria specificata.

Se si usa il flag di stato i/ \_ \_ o MIDI con **midiInOpen**, il sistema usa il messaggio [**\_ MOREDATA MIM**](mim-moredata.md) per avvisare la funzione di callback dell'applicazione quando non elabora i dati MIDI in modo sufficientemente veloce da restare al passo con il driver di dispositivo di input. Il messaggio [**\_ \_ MOREDATA in mm MIM**](mm-mim-moredata.md) esegue lo stesso processo con callback di finestra. Tuttavia, per motivi di prestazioni, la maggior parte delle applicazioni utilizzerà funzioni di callback anziché callback di finestra. Se l'applicazione elabora i dati MIDI in un thread separato, l'aumento della priorità del thread può avere un impatto significativo sulla capacità dell'applicazione di rimanere al passo con il flusso di dati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 