---
title: Commutatori
description: Commutatori
ms.assetid: ab92d30d-97ab-4229-aed8-1080b6e6dc88
keywords:
- mixer audio, controlli
- mixer audio, commutatori
- mixer, controlli
- mixer, commutatori
- Cambia controlli
- Struttura MIXERCONTROLDETAILS_BOOLEAN
- Controllo booleano
- Button (controllo)
- controllo on/off
- controllo mono
- controllo della sonorità
- controllo avanzato stereo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d65bb2a14a0e7dc527fab0e628035839855934
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872398"
---
# <a name="switches"></a>Commutatori

I controlli commutatore sono due opzioni di stato. Questi controlli utilizzano la [**struttura \_ booleana MIXERCONTROLDETAILS**](/previous-versions//dd757295(v=vs.85)) per recuperare e impostare le proprietà del controllo. Nella tabella seguente vengono descritti i tipi di opzioni.



| Controllo         | Descrizione                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Boolean         | Opzione generica. Può essere impostato su **true** o **false**.                                                                                                                                                                           |
| Pulsante          | Impostare su **true** per tutti i pulsanti che devono essere gestiti dal driver come se fossero stati premuti. Se il valore è **false**, non viene eseguita alcuna azione.                                                                                         |
| Attivato/Disattivato          | Opzione alternativa rappresentata da un elemento grafico diverso da quello usato per l'opzione booleana. Può essere impostata su ON o OFF.                                                                                                    |
| Disattiva audio            | Disattiva una linea audio (evitando il flusso di dati della linea) o consente la riproduzione dei dati audio. Questa opzione viene spesso usata per consentire il controllo delle linee che si nutrono nel mixer.                                                        |
| Mono            | Passa dall'output mono a quello stereo per una linea audio stereo. Impostare su OFF per riprodurre i dati stereo come canali separati. Impostare su ON per combinare i dati di entrambi i canali in una linea audio mono.                                            |
| Sonorità        | Aumenta i bassi volumi bassi per una linea audio. Impostare su ON per aumentare i bassi volume basso. Impostare su OFF per impostare i livelli di volume sul normale. La quantità di Boost è specifica dell'hardware. Per ulteriori informazioni, vedere la documentazione relativa al dispositivo mixer. |
| Enhanced Stereo | Aumenta la separazione stereo. Impostare su ON per aumentare la separazione stereo. Impostare su OFF per nessun miglioramento.                                                                                                                                  |



 

 

 