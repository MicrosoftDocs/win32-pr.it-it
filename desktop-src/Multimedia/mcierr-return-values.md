---
title: Valori restituiti da MCIERR
description: Valori restituiti da MCIERR
ms.assetid: 61f7b128-b4f7-4385-9daf-e2bc9fb36e24
keywords:
- Windows multimediali, MCIERR restituisce valori
- multimedia,MCIERR return values
- informazioni di riferimento sul contenuto multimediale, valori restituiti da MCIERR
- informazioni di riferimento per i dati multimediali, valori restituiti da MCIERR
- MCIERR return values,about
- MciSendCommand - funzione
- Funzione mciSendString
- Windows multimediali, errori
- elementi multimediali, errori
- informazioni di riferimento sul contenuto multimediale, errori
- informazioni di riferimento per i contenuti multimediali, errori
- Valori restituiti da Media Control Interface (MCI), MCIERR
- MCI (Media Control Interface),MCIERR return values
- informazioni di riferimento per i valori restituiti mci,MCIERR
- Riferimento MCI, valori restituiti da MCIERR
- Media Control Interface (MCI), errori
- MCI (Media Control Interface),errori
- informazioni di riferimento per MCI, errori
- riferimento MCI, errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57fc8426b264f68d7a6ab793e365d529774c931e72d89536b40b22592728a2ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783411"
---
# <a name="mcierr-return-values"></a>Valori restituiti da MCIERR

Le [**funzioni mciSendCommand**](/previous-versions//dd757160(v=vs.85)) [**e mciSendString**](/previous-versions//dd757161(v=vs.85)) restituiscono zero se hanno esito positivo; In caso contrario, restituiscono **un valore DWORD** che contiene uno dei valori di errore seguenti nella parola in basso.

-   [Errori MCI generali](general-mci-errors.md)
-   [Errori mciSendString](mcisendstring-errors.md)
-   [Errori di video digitali](digital-video-errors.md)
-   [Errori di Sequencer](sequencer-errors.md)
-   [Errori audio-waveform](waveform-audio-errors.md)

È possibile ottenere una descrizione dei singoli valori restituiti passando i valori restituiti alla [**funzione mciGetErrorString.**](/previous-versions//dd757158(v=vs.85))

 

 