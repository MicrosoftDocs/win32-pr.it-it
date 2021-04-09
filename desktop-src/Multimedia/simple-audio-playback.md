---
title: Riproduzione audio semplice
description: Riproduzione audio semplice
ms.assetid: 51a0244d-123d-4efe-92e9-972e914cef78
keywords:
- audio multimediale, forma d'onda
- audio, forma d'onda
- audio Waveform, riproduzione semplice
- MessageBeep (funzione)
- sndPlaySound (funzione)
- Funzione PlaySound, riproduzione semplice
- audio multimediale, funzione PlaySound
- audio, funzione PlaySound
- audio Waveform, funzione PlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256feded06de4ee92ee415f14bb08adc7fb4456e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956417"
---
# <a name="simple-audio-playback"></a>Riproduzione audio semplice

È possibile usare le funzioni seguenti per riprodurre l'audio della forma d'onda nell'applicazione in una singola chiamata di funzione.



| Funzione                                                      | Descrizione                                                                                                         |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [MessageBeep](/windows/win32/api/winuser/nf-winuser-messagebeep) | Riproduce il suono che corrisponde a un livello di avviso di sistema specificato.                                                 |
| [**sndPlaySound**](/previous-versions//dd798676(v=vs.85))                          | Riproduce il suono che corrisponde al suono di sistema immesso nel registro di sistema o al contenuto del file specificato. |
| [**PlaySound**](/previous-versions//dd743680(v=vs.85))                                | Fornisce tutte le funzionalità di [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) e può accedere direttamente alle risorse.           |



 

La funzione **MessageBeep** è una parte standard dell'API Win32. Poiché le sue funzionalità sono molto limitate e sono documentate altrove, non vengono discusse qui.

Le funzioni elencate supportano le seguenti origini dell'audio della forma d'onda:

-   Waveform-file audio associati ai livelli di avviso di sistema
-   Waveform-file audio specificati da voci nel registro di sistema
-   Risorse WAVE in memoria
-   Waveform-file audio specificati per nome

Le funzioni [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) e [**PlaySound**](/previous-versions//dd743680(v=vs.85)) caricano in memoria un intero file audio e di forma d'onda e, in effetti, limitano le dimensioni del file che è possibile riprodurre. Usare **sndPlaySound** e **PlaySound** per riprodurre file audio con forma d'onda di dimensioni ridotte, fino a circa 100.000. Queste due funzioni richiedono anche che i dati audio siano in un formato riproducibile da uno dei driver audio della forma d'onda, incluso il mapper wave.

Per i file audio di dimensioni maggiori, usare i servizi MCI (Media Control Interface). Per ulteriori informazioni, vedere [MCI](mci.md).

 

 