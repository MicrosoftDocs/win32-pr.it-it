---
title: Modifica del volume di Audio-Devices ausiliari
description: Modifica del volume di Audio-Devices ausiliari
ms.assetid: d7357900-132c-4758-8bc2-a890aead01c3
keywords:
- audio Waveform, modifica del volume del dispositivo audio ausiliario
- modifica del volume del dispositivo audio ausiliario
- audio ausiliario, modifica del volume del dispositivo
- interfaccia audio ausiliaria
- dispositivi audio ausiliari, modifica del volume
- audio ausiliario, interfaccia
- audio ausiliario, dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f80c499f18b60f0919214c91eeec834ed72c3e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727319"
---
# <a name="changing-the-volume-of-auxiliary-audio-devices"></a>Modifica del volume di Audio-Devices ausiliari

Windows fornisce le funzioni seguenti per eseguire query e impostare il volume per i dispositivi audio ausiliari.



| Funzione                             | Descrizione                                                                    |
|--------------------------------------|--------------------------------------------------------------------------------|
| [**auxGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume) | Recupera l'impostazione corrente del volume del dispositivo di output ausiliario specificato. |
| [**auxSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume) | Imposta il volume del dispositivo di output ausiliario specificato.                      |



 

Non tutti i dispositivi audio ausiliari supportano le modifiche del volume. Alcuni dispositivi sono in grado di supportare singole modifiche dei volumi nei canali sinistro e destro.

Il volume viene specificato in un valore di parola doppia, come per le funzioni di controllo del volume Waveform-Audio e MIDI. Quando il formato audio è stereo, i 16 bit superiori specificano il volume relativo del canale destro e i 16 bit inferiori specificano il volume relativo del canale sinistro. Per i dispositivi che non supportano il controllo del volume del canale sinistro e destro, i 16 bit inferiori specificano il livello del volume e i 16 bit superiori vengono ignorati.

I valori a livello di volume variano da 0x0 (silenzioso) a 0xFFFF (volume massimo) e vengono interpretati come logaritmicamente. L'aumento del volume percepito è lo stesso quando si aumenta il livello di volume da 0x5000 a 0x6000, come da 0x4000 a 0x5000.

 

 