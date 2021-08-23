---
title: Arresto, sospensione e riavvio della riproduzione
description: Arresto, sospensione e riavvio della riproduzione
ms.assetid: 39751342-63bc-4e68-bf9e-38665db8a05c
keywords:
- audio waveform, arresto della riproduzione
- interfaccia waveform-audio, arresto della riproduzione
- riproduzione di file waveform-audio, arresto della riproduzione
- audio waveform, sospensione della riproduzione
- interfaccia waveform-audio, sospensione della riproduzione
- riproduzione di file waveform-audio, sospensione della riproduzione
- audio waveform, riavvio della riproduzione
- interfaccia waveform-audio, riavvio della riproduzione
- riproduzione di file waveform-audio, riavvio della riproduzione
- Funzione waveOutPause
- Funzione waveOutReset
- Funzione waveOutRestart
- arresto della riproduzione waveform-audio
- sospensione della riproduzione waveform-audio
- riavvio della riproduzione waveform-audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04491a676a104e288d274da7dd70eb759e363adc6476805b261a9651444bf1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688491"
---
# <a name="stopping-pausing-and-restarting-playback"></a>Arresto, sospensione e riavvio della riproduzione

È possibile arrestare o sospendere la riproduzione durante la riproduzione dell'audio della forma d'onda. Dopo che la riproduzione è stata sospesa, è possibile riavviarla. Windows fornisce le funzioni seguenti per controllare la riproduzione audio-forma d'onda.



| Funzione                                 | Descrizione                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------------|
| [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)     | Sospende la riproduzione in un dispositivo di output waveform-audio.                                          |
| [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)     | Arresta la riproduzione in un dispositivo di output waveform-audio e contrassegna tutti i blocchi di dati in sospeso come completata. |
| [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart) | Riprende la riproduzione in un dispositivo di output audio-forma d'onda sospeso.                                  |



 

La sospensione di un dispositivo waveform-audio tramite [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) potrebbe non essere immediata; il driver può terminare la riproduzione del blocco corrente prima di sospendere la riproduzione.

In genere, non appena il primo blocco di dati waveform-audio viene inviato usando la funzione [**waveOutWrite,**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) inizia la riproduzione del dispositivo waveform-audio. Se non si vuole che il suono inizi a essere riprodotto immediatamente, chiamare **waveOutPause** prima di **chiamare waveOutWrite**. Quindi, quando si vuole iniziare a riprodurre dati waveform-audio, chiamare [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart).

Non è possibile **usare waveOutRestart** per riavviare un dispositivo arrestato con [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset). è necessario usare **waveOutWrite** per inviare il primo blocco di dati per riprendere la riproduzione nel dispositivo.

 

 