---
title: Arresto, sospensione e riavvio della riproduzione
description: Arresto, sospensione e riavvio della riproduzione
ms.assetid: 39751342-63bc-4e68-bf9e-38665db8a05c
keywords:
- audio della forma d'onda, arresto della riproduzione
- waveform-interfaccia audio, arresto della riproduzione
- riproduzione di file audio Waveform, arresto della riproduzione
- audio della forma d'onda, sospensione della riproduzione
- waveform-interfaccia audio, sospensione della riproduzione
- riproduzione di file audio Waveform, sospensione della riproduzione
- audio della forma d'onda, riavvio della riproduzione
- waveform-interfaccia audio, riavvio della riproduzione
- riproduzione di file audio Waveform, riavvio della riproduzione
- waveOutPause (funzione)
- waveOutReset (funzione)
- waveOutRestart (funzione)
- arresto della forma d'onda-riproduzione audio
- sospensione delle forme d'onda-riproduzione audio
- riavvio della forma d'onda-riproduzione audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6a4756a08317923056114259588a95bc62e97f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117602"
---
# <a name="stopping-pausing-and-restarting-playback"></a>Arresto, sospensione e riavvio della riproduzione

È possibile arrestare o sospendere la riproduzione durante la riproduzione dell'audio della forma d'onda. Una volta sospesa la riproduzione, è possibile riavviarla. Windows fornisce le funzioni seguenti per controllare la riproduzione dell'audio e della forma d'onda.



| Funzione                                 | Descrizione                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------------|
| [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)     | Sospende la riproduzione in un dispositivo di output waveform-audio.                                          |
| [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)     | Interrompe la riproduzione in un dispositivo di output waveform-audio e contrassegna tutti i blocchi di dati in sospeso come completato. |
| [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart) | Riprende la riproduzione in un dispositivo di output della forma d'onda-audio in pausa.                                  |



 

La sospensione di un dispositivo audio Waveform con [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) potrebbe non essere immediata; è possibile che il driver completi la riproduzione del blocco corrente prima di sospendere la riproduzione.

In genere, non appena viene inviato il primo blocco di dati waveform-audio tramite la funzione [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) , il dispositivo Waveform-Audio inizia la riproduzione. Se non si desidera che il suono inizi immediatamente a riprodurre, chiamare **waveOutPause** prima di chiamare **waveOutWrite**. Quindi, quando si desidera iniziare a riprodurre i dati audio della forma d'onda, chiamare [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart).

Non è possibile usare **waveOutRestart** per riavviare un dispositivo che è stato arrestato con [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset); è necessario usare **waveOutWrite** per inviare il primo blocco di dati per riprendere la riproduzione nel dispositivo.

 

 