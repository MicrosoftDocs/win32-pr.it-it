---
title: Valori restituiti MCIERR
description: Valori restituiti MCIERR
ms.assetid: 61f7b128-b4f7-4385-9daf-e2bc9fb36e24
keywords:
- Windows Multimedia, valori restituiti MCIERR
- Multimedia, valori restituiti MCIERR
- riferimento multimediale, valori restituiti MCIERR
- riferimento per i valori restituiti multimediali, MCIERR
- MCIERR valori restituiti, informazioni
- mciSendCommand (funzione)
- mciSendString (funzione)
- Windows Multimedia, errori
- Multimedia, errori
- riferimenti multimediali, errori
- informazioni di riferimento per i contenuti multimediali, errori
- Media Control Interface (MCI), valori restituiti MCIERR
- MCI (interfaccia di controllo multimediale), valori restituiti MCIERR
- riferimento per MCI, valori restituiti MCIERR
- Riferimento a MCI, valori restituiti MCIERR
- Interfaccia di controllo multimediale (MCI), errori
- MCI (interfaccia di controllo multimediale), errori
- informazioni di riferimento per MCI, errori
- Riferimento a MCI, errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8912284b98b2aacb60905e3fef4dc32705a5656
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299715"
---
# <a name="mcierr-return-values"></a>Valori restituiti MCIERR

Le funzioni [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) e [**mciSendString**](/previous-versions//dd757161(v=vs.85)) restituiscono zero se hanno esito positivo; in caso contrario, restituiscono un valore **DWORD** che contiene uno dei seguenti valori di errore nella parola bassa.

-   [Errori generali di MCI](general-mci-errors.md)
-   [Errori mciSendString](mcisendstring-errors.md)
-   [Errori video digitali](digital-video-errors.md)
-   [Errori del sequencer](sequencer-errors.md)
-   [Waveform-errori audio](waveform-audio-errors.md)

È possibile ottenere una descrizione dei singoli valori restituiti passando i valori restituiti alla funzione [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) .

 

 