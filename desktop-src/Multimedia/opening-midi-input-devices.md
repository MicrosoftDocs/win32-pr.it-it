---
title: Apertura di dispositivi di input MIDI
description: Apertura di dispositivi di input MIDI
ms.assetid: fd6ebd0c-6985-49d3-8015-a636d4c70ff3
keywords:
- Instrument Digital Interface (MIDI), dispositivi di input
- MIDI (Instrument Digital Interface), dispositivi di input
- registrazione di audio MIDI, dispositivi di input
- Dispositivi di input MIDI
- Instrument Digital Interface (MIDI), apertura di dispositivi di input
- MIDI (Instrument Digital Interface), apertura di dispositivi di input
- registrazione di audio MIDI, apertura di dispositivi di input
- apertura di dispositivi di input MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d260674194e7f066e5095e30a78c94b241a60b32304888aceb8db9ae06ccfea6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806271"
---
# <a name="opening-midi-input-devices"></a>Apertura di dispositivi di input MIDI

Per aprire un dispositivo di input MIDI per la registrazione, usare la [**funzione midiInOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) Questa funzione apre il dispositivo associato all'identificatore di dispositivo specificato e restituisce un handle del dispositivo aperto scrivendo l'handle in un percorso di memoria specificato.

Se si usa il flag MIDI IO STATUS con \_ \_ **midiInOpen,** il sistema usa il messaggio [**MIM \_ MOREDATA**](mim-moredata.md) per avvisare la funzione di callback dell'applicazione quando non elabora i dati MIDI abbastanza velocemente da restare al passo con il driver di dispositivo di input. Il [**messaggio MM \_ MIM \_ MOREDATA**](mm-mim-moredata.md) esegue lo stesso processo con i callback di finestra. Tuttavia, per motivi di prestazioni, la maggior parte delle applicazioni userà funzioni di callback anziché callback di finestra. Se l'applicazione elabora i dati MIDI in un thread separato, l'aumento della priorità del thread può avere un impatto significativo sulla capacità dell'applicazione di restare al passo con il flusso di dati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 