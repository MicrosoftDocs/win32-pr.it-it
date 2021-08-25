---
title: Modifica del volume delle Audio-Devices
description: Modifica del volume delle Audio-Devices
ms.assetid: d7357900-132c-4758-8bc2-a890aead01c3
keywords:
- audio waveform, modifica del volume del dispositivo audio ausiliario
- modifica del volume del dispositivo audio ausiliario
- audio ausiliario, modifica del volume del dispositivo
- interfaccia audio ausiliaria
- dispositivi audio ausiliari, modifica del volume
- audio ausiliario, interfaccia
- audio ausiliario, dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02ca4ceaf8e8a8b2f84ea69be437145f0f92b375904a0121c17abc7870fa831
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808111"
---
# <a name="changing-the-volume-of-auxiliary-audio-devices"></a>Modifica del volume delle Audio-Devices

Windows fornisce le funzioni seguenti per eseguire query e impostare il volume per i dispositivi audio ausiliari.



| Funzione                             | Descrizione                                                                    |
|--------------------------------------|--------------------------------------------------------------------------------|
| [**auxGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume) | Recupera l'impostazione del volume corrente del dispositivo di output ausiliario specificato. |
| [**auxSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume) | Imposta il volume del dispositivo di output ausiliario specificato.                      |



 

Non tutti i dispositivi audio ausiliari supportano le modifiche del volume. Alcuni dispositivi possono supportare singole modifiche del volume sia a sinistra che a destra.

Il volume viene specificato in un valore doubleword, come con le funzioni di controllo del volume waveform-audio e MIDI. Quando il formato audio è stereo, i 16 bit superiori specificano il volume relativo del canale destro e i 16 bit inferiori specificano il volume relativo del canale sinistro. Per i dispositivi che non supportano il controllo del volume del canale sinistro e destro, i 16 bit inferiori specificano il livello del volume e i 16 bit superiori vengono ignorati.

I valori a livello di volume 0x0 (silenzio) 0xFFFF (volume massimo) e vengono interpretati logaritmicamente. L'aumento del volume percepito è lo stesso quando si aumenta il livello di volume da 0x5000 a 0x6000 come da 0x4000 a 0x5000.

 

 