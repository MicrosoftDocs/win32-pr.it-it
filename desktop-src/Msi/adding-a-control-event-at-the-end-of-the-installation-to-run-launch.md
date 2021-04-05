---
description: Il programma di installazione esegue la sequenza di installazione guidata dell'esempio solo se viene usato il livello di interfaccia utente completo per installare l'applicazione.
ms.assetid: 323d62ae-333b-49fd-96a1-55b228c8ab2c
title: Aggiunta di un evento di controllo alla fine dell'installazione per l'esecuzione dell'avvio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 545901c4cfd0936f63078d5ad56586022fb4ec4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967301"
---
# <a name="adding-a-control-event-at-the-end-of-the-installation-to-run-launch"></a>Aggiunta di un evento di controllo alla fine dell'installazione per l'esecuzione dell'avvio

Il programma di installazione esegue la sequenza di installazione guidata dell'esempio solo se viene usato il livello di [*interfaccia utente completo*](f-gly.md) per installare l'applicazione. L'ultima finestra di dialogo della sequenza di finestra di dialogo di esempio è una finestra di dialogo di [uscita](exit-dialog.md) denominata ExitDialog. Quando un utente interagisce con il pulsante OK in ExitDialog, questa prima pubblica un [EndDialog ControlEvent](enddialog-controlevent.md) che restituisce il controllo al programma di installazione. Il controllo pubblica quindi un [ControlEvent DoAction](doaction-controlevent.md) che esegue l'azione personalizzata Launch. Ogni evento di controllo richiede un record nella [tabella ControlEvent](controlevent-table.md). Vedere [Panoramica di ControlEvent](controlevent-overview.md).

[Tabella ControlEvent](controlevent-table.md)



| Finestra di dialogo     | controllo\_ | Evento     | Argomento | Condizione                     | Ordering |
|------------|-----------|-----------|----------|-------------------------------|----------|
| ExitDialog | OK        | EndDialog | Return   | 1                             | 1        |
| ExitDialog | OK        | DoAction  | Launch   | NON installato e $Tutorial = 3 | 2        |



 

La condizione sul controllo DoAction garantisce che l'azione personalizzata venga eseguita solo durante la prima installazione dell'applicazione e che venga installata localmente. La frase $Tutorial = 3 indica che lo stato dell'azione del componente tutorial è impostato su local. Vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).

Questa operazione completa l'esempio.

 

 



