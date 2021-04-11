---
title: Recupero della posizione di riproduzione corrente
description: Recupero della posizione di riproduzione corrente
ms.assetid: a08fe5da-8945-486f-9413-877c7d13d5de
keywords:
- audio Waveform, posizione corrente di riproduzione
- waveform-interfaccia audio, posizione corrente di riproduzione
- riproduzione di file audio Waveform, posizione corrente di riproduzione
- waveOutGetPosition (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28737cfc292dc8779b21756f38813642b82e452
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336862"
---
# <a name="retrieving-the-current-playback-position"></a>Recupero della posizione di riproduzione corrente

È possibile monitorare la posizione di riproduzione corrente all'interno del file durante la riproduzione dell'audio della forma d'onda usando la funzione [**waveOutGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition) .

Per i dispositivi Waveform-Audio, gli esempi rappresentano il formato ora preferito in cui rappresentare la posizione corrente. In questo modo, la posizione corrente di un dispositivo di forma d'onda-audio viene specificata come numero di campioni per un canale a partire dall'inizio del file audio della forma d'onda. Per eseguire una query sulla posizione corrente di un dispositivo audio Waveform, impostare il membro **wType** della struttura [**MMTIME**](/previous-versions//dd757347(v=vs.85)) su \_ Samples Time e passare la struttura a **waveOutGetPosition**.

La struttura **MMTIME** può rappresentare il tempo in uno o più formati diversi, tra cui millisecondi, esempi, SMPTE (società di Motion Picture e ingegneri televisivi) e formati di puntatore del brano MIDI. Il membro **wType** specifica il formato utilizzato per rappresentare l'ora. Prima di chiamare una funzione che usa la struttura **MMTIME** , è necessario impostare **wType** per indicare il formato di ora richiesto. Assicurarsi di controllare **wType** dopo la chiamata per verificare se il formato ora richiesto è supportato. Se il formato tempo richiesto non è supportato, il driver di dispositivo specifica l'ora in un formato di ora alternativo e modifica il membro **wType** nel formato di ora selezionato.

Per ulteriori informazioni sulla struttura **MMTIME** , vedere la pagina relativa ai [timer multimediali](multimedia-timers.md).

 

 