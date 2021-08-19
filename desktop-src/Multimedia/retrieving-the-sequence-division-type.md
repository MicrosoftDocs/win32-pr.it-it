---
title: Recupero del tipo di divisione della sequenza
description: Recupero del tipo di divisione della sequenza
ms.assetid: 9c7e3482-93a3-4f9c-8b70-a9c733de14fe
keywords:
- MidI (Musical Instrument Digital Interface), sequence division type
- MIDI (Musical Instrument Digital Interface),sequence division type
- Sequencer MIDI MCI, tipo di divisione
- MCI_STATUS comando
- Tipo di divisione di sequenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b28bb7e32097b888cdd3dec739eaccfc2a37dfe14060168fb11f0a7ca3d00e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801805"
---
# <a name="retrieving-the-sequence-division-type"></a>Recupero del tipo di divisione della sequenza

Il *tipo di* divisione di una sequenza MIDI determina la quantità di tempo tra gli eventi MIDI nella sequenza. Per determinare il tipo di divisione di una sequenza, usare il comando [**MCI \_ STATUS**](mci-status.md) e impostare il membro **dwItem** della struttura [**MCI \_ STATUS \_ PARMS**](mci-status-parms.md) su MCI \_ SEQ \_ STATUS \_ DIVTYPE .

Se il **comando MCI \_ STATUS** ha esito positivo, il membro **dwReturn** della struttura **MCI \_ STATUS \_ PARMS** conterrà uno dei valori seguenti per indicare il tipo di divisione.



| Valore                        | Tipo di divisione                     |
|------------------------------|-----------------------------------|
| MCI \_ SEQ \_ DIV \_ PPQN          | PPQN (nota parti per trimestre)     |
| MCI \_ SEQ \_ DIV \_ SMPTE \_ 24     | SMPTE, 24 fps (fotogrammi al secondo) |
| MCI \_ SEQ \_ DIV \_ SMPTE \_ 25     | SMPTE, 25 fps                     |
| MCI \_ SEQ \_ DIV \_ SMPTE \_ 30     | SMPTE, 30 fps                     |
| MCI \_ SEQ \_ DIV \_ SMPTE \_ 30DROP | SMPTE, drop frame da 30 fps          |



 

Per modificare o eseguire query sul tempo, è necessario conoscere il tipo di divisione di una sequenza. Non è possibile modificare il tipo di divisione di una sequenza usando il sequencer MCI.

 

 




