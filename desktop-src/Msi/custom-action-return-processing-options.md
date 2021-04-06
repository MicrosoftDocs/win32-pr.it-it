---
description: In questo argomento vengono identificati i flag di opzione che è possibile utilizzare per controllare l'elaborazione del thread azione personalizzato.
ms.assetid: a09b3a0e-564e-41aa-af0d-2e46776f291b
title: Opzioni di elaborazione della restituzione dell'azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f8664ff489280993a7fc52117f3d19bccb023b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885525"
---
# <a name="custom-action-return-processing-options"></a>Opzioni di elaborazione della restituzione dell'azione personalizzata

In questo argomento vengono identificati i flag di opzione che è possibile utilizzare per controllare l'elaborazione del thread azione personalizzato. I flag vengono usati per specificare che i thread delle azioni principale e personalizzata vengono eseguiti in modo sincrono (Windows Installer attende il completamento del thread dell'azione personalizzato prima di riprendere il thread di installazione principale) o in modo asincrono (Windows Installer esegue l'azione personalizzata contemporaneamente mentre l'installazione principale continua).

Per abilitare i flag di opzione, aggiungere il valore identificato nella tabella seguente al valore nel campo Type della [tabella CustomAction](customaction-table.md).



| Costante                                                           | Valore esadecimale             | Decimal | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------|-------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (nessuna)                                                             | 0x00000000              | +0      | Esecuzione sincrona che ha esito negativo se il codice di uscita non è 0 (zero). <br/> Se il flag msidbCustomActionTypeContinue non è impostato, l'azione personalizzata deve restituire uno dei valori restituiti descritti in [valori restituiti dell'azione personalizzata](custom-action-return-values.md).<br/>                                                                                                                                                                                                                             |
| **msidbCustomActionTypeContinue**                                  | 0x00000040              | + 64     | Esecuzione sincrona che ignora il codice di uscita e continua.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **msidbCustomActionTypeAsync**                                     | 0x00000080              | + 128    | Esecuzione asincrona che attende il codice di uscita alla fine della sequenza.<br/> Questa opzione non può essere usata con [installazioni simultanee](concurrent-installations.md), [attività di rollback](rollback-custom-actions.md)o [azioni personalizzate di script](scripts.md).<br/>                                                                                                                                                                                                                                |
| **msidbCustomActionTypeAsync**  +  **msidbCustomActionTypeContinue** | 0x00000040 + 0x00000080 | +192    | Esecuzione asincrona che non attende il completamento.<br/> L'esecuzione continua dopo l'Windows Installer terminata.<br/> Questa opzione può essere usata solo con le azioni personalizzate del tipo EXE, ovvero [i file eseguibili](executable-files.md). <br/> Tutti gli altri tipi di azioni personalizzate possono essere asincroni solo all'interno della sessione di installazione e devono terminare l'installazione.<br/> Questa opzione non può essere utilizzata con [installazioni simultanee](concurrent-installations.md).<br/> |



 

 

 




