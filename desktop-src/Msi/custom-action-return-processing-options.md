---
description: In questo argomento vengono identificati i flag di opzione che è possibile utilizzare per controllare l'elaborazione del thread dell'azione personalizzata.
ms.assetid: a09b3a0e-564e-41aa-af0d-2e46776f291b
title: Opzioni di elaborazione della restituzione dell'azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2dd719271e6291decbd2123d5cf1525121769704b3fc4177c8b301662697689
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947979"
---
# <a name="custom-action-return-processing-options"></a>Opzioni di elaborazione della restituzione dell'azione personalizzata

In questo argomento vengono identificati i flag di opzione che è possibile utilizzare per controllare l'elaborazione del thread dell'azione personalizzata. I flag vengono usati per specificare che i thread dell'azione principale e personalizzata vengono eseguiti in modo sincrono (il programma di installazione di Windows attende il completamento del thread dell'azione personalizzata prima di riprendere il thread di installazione principale) o in modo asincrono (il programma di installazione di Windows esegue l'azione personalizzata simultaneamente mentre l'installazione principale continua).

Per abilitare i flag di opzione, aggiungere il valore identificato nella tabella seguente al valore nel campo Tipo della [tabella CustomAction](customaction-table.md).



| Costante                                                           | Valore esadecimale             | Decimal | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------|-------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (nessuna)                                                             | 0x00000000              | +0      | Esecuzione sincrona che ha esito negativo se il codice di uscita è diverso da 0 (zero). <br/> Se il flag msidbCustomActionTypeContinue non è impostato, l'azione personalizzata deve restituire uno dei valori restituiti descritti in Valori restituiti dell'azione [personalizzata.](custom-action-return-values.md)<br/>                                                                                                                                                                                                                             |
| **msidbCustomActionTypeContinue**                                  | 0x00000040              | +64     | Esecuzione sincrona che ignora il codice di uscita e continua.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **msidbCustomActionTypeAsync**                                     | 0x00000080              | +128    | Esecuzione asincrona che attende il codice di uscita alla fine della sequenza.<br/> Questa opzione non può essere usata con [installazioni simultanee,](concurrent-installations.md) [azioni personalizzate di rollback](rollback-custom-actions.md)o azioni personalizzate [script.](scripts.md)<br/>                                                                                                                                                                                                                                |
| **msidbCustomActionTypeAsync**  +  **msidbCustomActionTypeContinue** | 0x00000040 + 0x00000080 | +192    | Esecuzione asincrona che non attende il completamento.<br/> L'esecuzione continua dopo Windows del programma di installazione.<br/> Questa opzione può essere utilizzata solo con le azioni personalizzate di tipo EXE, ad esempio i [file eseguibili](executable-files.md). <br/> Tutti gli altri tipi di azioni personalizzate possono essere asincroni solo all'interno della sessione di installazione e devono terminare per terminare l'installazione.<br/> Questa opzione non può essere usata con [installazioni simultanee.](concurrent-installations.md)<br/> |



 

 

 




