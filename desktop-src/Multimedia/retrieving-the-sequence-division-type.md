---
title: Recupero del tipo di divisione sequenza
description: Recupero del tipo di divisione sequenza
ms.assetid: 9c7e3482-93a3-4f9c-8b70-a9c733de14fe
keywords:
- MIDI (Musical Instrument Digital Interface), tipo divisione sequenza
- MIDI (Musical Instrument Digital Interface), tipo divisione sequenza
- MCI MIDI sequencer, tipo di divisione
- Comando MCI_STATUS
- tipo divisione sequenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6586a33fe4a5225fdcdca21e413104388d5831d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955420"
---
# <a name="retrieving-the-sequence-division-type"></a>Recupero del tipo di divisione sequenza

Il *tipo di divisione* di una sequenza MIDI determina la quantità di tempo tra gli eventi MIDI nella sequenza. Per determinare il tipo di divisione di una sequenza, utilizzare il comando [**MCI \_ status**](mci-status.md) e impostare il membro **dwItem** della [**struttura \_ \_ parametri stato MCI**](mci-status-parms.md) su MCI \_ seq \_ status \_ DIVTYPE.

Se il comando di **\_ stato MCI** ha esito positivo, il membro **dwReturn** della struttura **\_ \_ parametri stato MCI** conterrà uno dei valori seguenti per indicare il tipo di divisione.



| Valore                        | Tipo divisione                     |
|------------------------------|-----------------------------------|
| PPQN per MCI \_ seq \_ div \_          | PPQN (note parti per trimestre)     |
| MCI \_ seq \_ div \_ SMPTE \_ 24     | SMPTE, 24 fps (fotogrammi al secondo) |
| MCI \_ seq \_ div \_ \_ 25     | SMPTE, 25 fps                     |
| MCI \_ seq \_ div \_ \_ 30     | SMPTE, 30 fps                     |
| MCI \_ seq \_ div \_ SMPTE \_ 30DROP | SMPTE, 30 fps drop frame          |



 

È necessario essere a conoscenza del tipo di divisione di una sequenza per modificare o eseguire una query sul tempo. Non è possibile modificare il tipo di divisione di una sequenza usando MCI Sequencer.

 

 




