---
title: Recupero della posizione di riproduzione corrente
description: Recupero della posizione di riproduzione corrente
ms.assetid: a08fe5da-8945-486f-9413-877c7d13d5de
keywords:
- audio waveform, posizione di riproduzione corrente
- interfaccia waveform-audio, posizione di riproduzione corrente
- riproduzione di file waveform-audio, posizione di riproduzione corrente
- Funzione waveOutGetPosition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85bc46e476786625ccae51802e0b720379a935110eb37d941c4c76d69d94783
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689051"
---
# <a name="retrieving-the-current-playback-position"></a>Recupero della posizione di riproduzione corrente

È possibile monitorare la posizione di riproduzione corrente all'interno del file durante la riproduzione dell'audio della forma d'onda usando la [**funzione waveOutGetPosition.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition)

Per i dispositivi waveform-audio, gli esempi sono il formato orario preferito in cui rappresentare la posizione corrente. Di conseguenza, la posizione corrente di un dispositivo waveform-audio viene specificata come numero di campioni per un canale dall'inizio del file waveform-audio. Per eseguire una query sulla posizione corrente di un dispositivo waveform-audio, impostare il membro **wType** della struttura [**MMTIME**](/previous-versions//dd757347(v=vs.85)) su TIME SAMPLES e passare questa struttura a \_ **waveOutGetPosition**.

La **struttura MMTIME** può rappresentare l'ora in uno o più formati diversi, tra cui millisecondi, esempi, SMPTE (Society of Motion Picture and Television Engineers) e formati di puntatore di brano MIDI. Il **membro wType** specifica il formato usato per rappresentare l'ora. Prima di chiamare una funzione che usa la **struttura MMTIME,** è necessario impostare **wType** per indicare il formato dell'ora richiesto. Assicurarsi di controllare **wType dopo** la chiamata per verificare se il formato dell'ora richiesto è supportato. Se il formato ora richiesto non è supportato, il driver di dispositivo specifica l'ora in un formato di ora alternativo e modifica il membro **wType** nel formato di ora selezionato.

Per altre informazioni sulla **struttura MMTIME,** vedere [Timer multimediali](multimedia-timers.md).

 

 