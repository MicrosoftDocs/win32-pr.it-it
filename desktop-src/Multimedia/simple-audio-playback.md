---
title: Riproduzione audio semplice
description: Riproduzione audio semplice
ms.assetid: 51a0244d-123d-4efe-92e9-972e914cef78
keywords:
- audio multimediale, forma d'onda
- audio, forma d'onda
- audio waveform, riproduzione semplice
- Funzione MessageBeep
- Funzione sndPlaySound
- Funzione PlaySound, riproduzione semplice
- audio multimediale, funzione PlaySound
- audio, funzione PlaySound
- audio waveform, funzione PlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6388f9800f93080e995ae537c2458a22da033ab2149b4bfca114c25025d97434
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688691"
---
# <a name="simple-audio-playback"></a>Riproduzione audio semplice

È possibile usare le funzioni seguenti per riprodurre audio waveform nell'applicazione in una singola chiamata di funzione.



| Funzione                                                      | Descrizione                                                                                                         |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [MessageBeep](/windows/win32/api/winuser/nf-winuser-messagebeep) | Riproduce il suono che corrisponde a un livello di avviso di sistema specificato.                                                 |
| [**sndPlaySound**](/previous-versions//dd798676(v=vs.85))                          | Riproduce il suono che corrisponde al suono di sistema immesso nel Registro di sistema o al contenuto del file specificato. |
| [**Playsound**](/previous-versions//dd743680(v=vs.85))                                | Fornisce tutte le funzionalità di [**sndPlaySound e**](/previous-versions//dd798676(v=vs.85)) può accedere direttamente alle risorse.           |



 

La **funzione MessageBeep** è una parte standard dell'API Win32. Poiché le relative funzionalità sono molto limitate e sono documentate altrove, non sono descritte qui.

Le funzioni elencate supportano le origini seguenti di audio waveform:

-   File audio Waveform associati ai livelli di avviso di sistema
-   File audio Waveform specificati dalle voci nel Registro di sistema
-   Risorse WAVE in memoria
-   File audio Waveform specificati in base al nome

Le [**funzioni sndPlaySound**](/previous-versions//dd798676(v=vs.85)) e [**PlaySound**](/previous-versions//dd743680(v=vs.85)) caricano un intero file audio waveform in memoria e, di fatto, limitano le dimensioni del file che possono riprodurre. Usare **sndPlaySound** e **PlaySound** per riprodurre file audio waveform di piccole dimensioni, fino a circa 100.000. Queste due funzioni richiedono anche che i dati audio siano in un formato riproducibile da uno dei driver audio waveform installati, incluso il mapper delle onde.

Per file audio di dimensioni maggiori, usare i servizi Media Control Interface (MCI). Per altre informazioni, vedere [MCI.](mci.md)

 

 