---
title: Errori Waveform-Audio
description: Errori Waveform-Audio
ms.assetid: c898552a-a60a-4deb-ab4a-ed74b08a7d05
keywords:
- Valori restituiti MCIERR, errori audio e forma d'onda
- Guida di riferimento multimediale, errori audio e forma d'onda
- informazioni di riferimento per i file multimediali, le forme di errore audio
- MCI (Media Control Interface), errori audio e Waveform
- MCI (interfaccia di controllo multimediale), errori audio e Waveform
- informazioni di riferimento per MCI, errori audio e Waveform
- Riferimento a MCI, errori audio e forma d'onda
- Interfaccia di controllo multimediale (MCI), errori
- MCI (interfaccia di controllo multimediale), errori
- informazioni di riferimento per MCI, errori
- Riferimento a MCI, errori
- waveform-errori audio
- Forma d'onda MCI-errori audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf64e8cd4ec6d061422bcf14d17dfb4c4317ee4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044309"
---
# <a name="waveform-audio-errors"></a>Errori Waveform-Audio

I seguenti valori restituiti aggiuntivi vengono definiti per i dispositivi audio e la forma d'onda MCI:



| Valore                             | Significato                                                                                                                                                             |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_INPUTSINUSE Wave \_ MCIERR         | Sono in uso tutti i dispositivi waveform che possono registrare file nel formato corrente. Attendere fino a quando uno di questi dispositivi non è disponibile; quindi, riprovare.                              |
| \_INPUTSUNSUITABLE Wave \_ MCIERR    | Nessun dispositivo waveform installato può registrare i file nel formato corrente. Usare l'opzione drivers nel pannello di controllo per installare un dispositivo di registrazione della forma d'onda appropriato. |
| \_INPUTUNSPECIFIED Wave \_ MCIERR    | È possibile specificare qualsiasi dispositivo di registrazione della forma d'onda compatibile.                                                                                                           |
| \_OUTPUTSINUSE Wave \_ MCIERR        | Sono in uso tutti i dispositivi waveform che possono riprodurre file nel formato corrente. Attendere fino a quando uno di questi dispositivi non è disponibile; quindi, riprovare.                                |
| \_OUTPUTSUNSUITABLE Wave \_ MCIERR   | Nessun dispositivo waveform installato può riprodurre file nel formato corrente. Usare l'opzione drivers nel pannello di controllo per installare un dispositivo waveform adatto.             |
| \_OUTPUTUNSPECIFIED Wave \_ MCIERR   | È possibile specificare qualsiasi dispositivo compatibile per la riproduzione di forme d'onda.                                                                                                            |
| \_SETINPUTINUSE Wave \_ MCIERR       | Il dispositivo waveform corrente è in uso. Attendere fino a quando il dispositivo non è disponibile; quindi, riprovare a impostare il dispositivo per la registrazione.                                              |
| \_SETINPUTUNSUITABLE Wave \_ MCIERR  | Il dispositivo usato per registrare una forma d'onda non è in grado di riconoscere il formato dati.                                                                                     |
| \_SETOUTPUTINUSE Wave \_ MCIERR      | Il dispositivo waveform corrente è in uso. Attendere fino a quando il dispositivo non è disponibile; quindi, riprovare a impostare il dispositivo per la riproduzione.                                               |
| \_SETOUTPUTUNSUITABLE Wave \_ MCIERR | Il dispositivo utilizzato per riprodurre una forma d'onda non è in grado di riconoscere il formato dati.                                                                                   |



 

 

 




