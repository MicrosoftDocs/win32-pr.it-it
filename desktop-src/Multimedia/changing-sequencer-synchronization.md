---
title: Modifica della sincronizzazione del sequencer
description: Modifica della sincronizzazione del sequencer
ms.assetid: 5c3acb47-e6cc-4957-a306-7039ec110827
keywords:
- MCI_SET messaggio di comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bffdc1606624f63fa05a9cc03c68fe64781620f
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/12/2021
ms.locfileid: "106320055"
---
# <a name="changing-sequencer-synchronization"></a>Modifica della sincronizzazione del sequencer

> [!NOTE]
> Comunicazione senza distorsione Microsoft supporta un ambiente diversificato e di inclusione.  All'interno di questo documento sono presenti riferimenti alla parola "slave". La [Guida di stile di Microsoft per le comunicazioni di Bias-Free](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) riconosce questo aspetto come una parola di esclusione.  Questo testo viene usato in quanto è attualmente il wording utilizzato all'interno del software. Per coerenza, questo documento contiene questa parola. Quando questa parola viene rimossa dal software, il documento verrà corretto per essere allineato.

Per modificare la modalità di sincronizzazione di un dispositivo Sequencer, utilizzare il messaggio di comando [**\_ set MCI**](mci-set.md) con \_ i \_ \_ \_ \_ \_ flag slave set master e MCI Seq set Per specificare le modalità di sincronizzazione master e subordinata, vengono usati due membri della struttura [**parametri di MCI \_ \_ set \_**](mci-seq-set-parms.md) , **dwMaster** e **dwSlave**.

La modalità di sincronizzazione master controlla le informazioni di sincronizzazione inviate dal sequencer a una porta di output. Di seguito sono riportate le costanti per il membro **dwMaster** e le modalità di sincronizzazione master corrispondenti.



| Costante        | Modalità di sincronizzazione                                                                             |
|-----------------|--------------------------------------------------------------------------------------------------|
| \_MIDI seq \_ MIDI  | Sincronizzazione MIDI. Inviare le informazioni di temporizzazione alla porta di output usando i messaggi di clock temporizzati MIDI.   |
| sequenza di MCI \_ seq \_ | Sincronizzazione SMPTE. Inviare le informazioni di temporizzazione alla porta di output usando i messaggi MIDI del trimestre. |
| \_nessuno Seq seq \_  | Nessuna sincronizzazione. Non inviare informazioni sull'intervallo.                                                  |



 

La modalità di sincronizzazione subordinata controlla il punto in cui Sequencer ottiene le informazioni sull'intervallo per riprodurre un file MIDI. Di seguito sono riportate le costanti per il membro **dwSlave** e le corrispondenti modalità di sincronizzazione subordinata.



| Costante        | Modalità di sincronizzazione                                                                                                                               |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| \_file SEQ di MCI \_  | Sincronizzazione file. Ottenere informazioni sulla tempistica dal file MIDI.                                                                                       |
| \_MIDI seq \_ MIDI  | Sincronizzazione MIDI. Ottenere informazioni sulla tempistica dalla porta di input usando i messaggi di clock temporizzati MIDI.                                                     |
| sequenza di MCI \_ seq \_ | Sincronizzazione SMPTE. Ottenere informazioni sulla tempistica dalla porta di input usando i messaggi MIDI del trimestre.                                                   |
| \_nessuno Seq seq \_  | Nessuna sincronizzazione. Ottenere informazioni sui tempi solo dai comandi MCI e ignorare le informazioni di temporizzazione, ad esempio le modifiche del tempo, presenti nel file MIDI. |



 

> [!Note]  
> Attualmente, per la sincronizzazione principale, MCI MIDI Sequencer supporta solo la modalità Nessuna sincronizzazione (MCI \_ seq \_ None). Per la sincronizzazione subordinata, supporta solo la modalità di sincronizzazione file ( \_ \_ file SEQ di MCI) e la modalità Nessuna sincronizzazione (MCI \_ seq \_ None).

 

 

 




