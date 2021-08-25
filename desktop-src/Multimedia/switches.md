---
title: Commutatori
description: Commutatori
ms.assetid: ab92d30d-97ab-4229-aed8-1080b6e6dc88
keywords:
- mixer audio, controlli
- mixer audio, commutatori
- mixer, controlli
- mixer, commutatori
- cambiare i controlli
- MIXERCONTROLDETAILS_BOOLEAN struttura
- Controllo booleano
- controllo pulsante
- Controllo di on/off
- controllo mono
- controllo della voce
- Controllo avanzato stereo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336d2e23c5e6438fbc19208e3366283147462c2451a12e3ccdcae6c13fcd93d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805081"
---
# <a name="switches"></a>Commutatori

I controlli interruttore sono commutatori a due stati. Questi controlli usano la [**struttura \_ BOOLEANa MIXERCONTROLDETAILS**](/previous-versions//dd757295(v=vs.85)) per recuperare e impostare le proprietà del controllo. Nella tabella seguente vengono descritti i tipi di opzioni.



| Controllo         | Descrizione                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Boolean         | Opzione generica. Può essere impostato su **TRUE** o **FALSE.**                                                                                                                                                                           |
| Button          | Impostare su **TRUE per** tutti i pulsanti che il driver deve gestire come se fossero stati premuti. Se il valore è **FALSE,** non viene eseguita alcuna azione.                                                                                         |
| Attivato/Disattivato          | Opzione alternativa rappresentata da un elemento grafico diverso da quello usato per l'opzione booleana. Può essere impostato su ON o OFF.                                                                                                    |
| Disattiva audio            | Disattiva una linea audio (sopprimendo il flusso di dati della linea) o consente la riproduzione dei dati audio. Questo interruttore viene spesso usato per controllare le linee che si ertono nel mixer.                                                        |
| Mono            | Passa dall'output mono a quello stereo per una linea audio stereo. Impostare su OFF per riprodurre i dati stereo come canali separati. Impostare su ON per combinare i dati di entrambi i canali in una linea audio mono.                                            |
| Sonorità        | Aumenta i bassi a basso volume per una linea audio. Impostare su ON per aumentare i bassi a basso volume. Impostare su OFF per impostare i livelli di volume su normale. La quantità di boost è specifica dell'hardware. Per altre informazioni, vedere la documentazione per il dispositivo mixer. |
| Stereo migliorato | Aumenta la separazione stereo. Impostare su ON per aumentare la separazione stereo. Impostare su OFF per nessun miglioramento.                                                                                                                                  |



 

 

 