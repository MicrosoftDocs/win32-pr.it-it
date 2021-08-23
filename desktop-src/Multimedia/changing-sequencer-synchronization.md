---
title: Modifica della sincronizzazione di Sequencer
description: Modifica della sincronizzazione di Sequencer
ms.assetid: 5c3acb47-e6cc-4957-a306-7039ec110827
keywords:
- MCI_SET messaggio di comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f7f31544b7b9ceb00109551718b9984dd2aa506557848e0d63e77724c4be32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526421"
---
# <a name="changing-sequencer-synchronization"></a>Modifica della sincronizzazione di Sequencer

> [!NOTE]
> Comunicazione senza distorsioni Microsoft supporta un ambiente diversificato e inclusiva.  All'interno di questo documento sono presenti riferimenti alla parola "slave". La Guida di stile di Microsoft [per Bias-Free comunicazioni](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) è una parola di esclusione.  Questa formulazione viene usata in quanto è attualmente la formulazione usata all'interno del software. Per coerenza, questo documento contiene questa parola. Quando questa parola viene rimossa dal software, il documento verrà corretto in modo che sia allineato.

Per modificare la modalità di sincronizzazione di un dispositivo Sequencer, usare il messaggio di comando [**MCI \_ SET**](mci-set.md) con i flag MCI SEQ SET MASTER e \_ \_ \_ MCI \_ SEQ \_ SET \_ SLAVE. Due membri nella [**struttura MCI \_ SEQ \_ SET \_ PARMS,**](mci-seq-set-parms.md) **dwMaster** e **dwMastere**, vengono usati per specificare le modalità di sincronizzazione master e subordinata.

La modalità di sincronizzazione master controlla le informazioni di sincronizzazione inviate dal sequencer a una porta di output. Di seguito sono riportate le costanti per il **membro dwMaster** e le modalità di sincronizzazione master corrispondenti.



| Costante        | Modalità di sincronizzazione                                                                             |
|-----------------|--------------------------------------------------------------------------------------------------|
| MCI \_ SEQ \_ MIDI  | Sincronizzazione MIDI. Inviare informazioni sull'intervallo alla porta di output usando i messaggi di clock midi.   |
| MCI \_ SEQ \_ SMPTE | Sincronizzazione SMPTE. Inviare informazioni di intervallo alla porta di output usando messaggi midi frame MIDI. |
| MCI \_ SEQ \_ NONE  | Nessuna sincronizzazione. Non inviare informazioni sull'intervallo.                                                  |



 

La modalità di sincronizzazione subordinata controlla dove sequencer ottiene le informazioni di intervallo per riprodurre un file MIDI. Di seguito sono riportate le costanti per il **membro dwSync** e le modalità di sincronizzazione subordinate corrispondenti.



| Costante        | Modalità di sincronizzazione                                                                                                                               |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| MCI \_ SEQ \_ FILE  | Sincronizzazione file. Ottenere informazioni sugli intervalli dal file MIDI.                                                                                       |
| MCI \_ SEQ \_ MIDI  | Sincronizzazione MIDI. Ottenere informazioni sugli intervalli dalla porta di input usando i messaggi di clock midi.                                                     |
| MCI \_ SEQ \_ SMPTE | Sincronizzazione SMPTE. Ottenere informazioni sugli intervalli dalla porta di input usando i messaggi mid-frame MIDI.                                                   |
| MCI \_ SEQ \_ NONE  | Nessuna sincronizzazione. Ottenere informazioni sulla temporizzazione solo dai comandi MCI e ignorare le informazioni di intervallo (ad esempio le modifiche temporali) presenti nel file MIDI. |



 

> [!Note]  
> Attualmente, per la sincronizzazione master, il sequencer MIDI MCI supporta solo la modalità Nessuna sincronizzazione (MCI \_ SEQ \_ NONE). Per la sincronizzazione subordinata, supporta solo la modalità di sincronizzazione file (MCI SEQ FILE) e la modalità \_ \_ Nessuna sincronizzazione (MCI \_ SEQ \_ NONE).

 

 

 




