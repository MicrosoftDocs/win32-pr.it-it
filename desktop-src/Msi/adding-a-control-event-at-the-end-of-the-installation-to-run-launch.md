---
description: Il programma di installazione esegue la sequenza dell'installazione guidata dell'esempio solo se per installare l'applicazione viene usato il livello completo dell'interfaccia utente.
ms.assetid: 323d62ae-333b-49fd-96a1-55b228c8ab2c
title: Aggiunta di un evento di controllo alla fine dell'installazione per l'esecuzione dell'avvio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0cf2a32a30187ea263bd2e3530e6eaae7d236e111826cbcab2461746d9c8e48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078221"
---
# <a name="adding-a-control-event-at-the-end-of-the-installation-to-run-launch"></a>Aggiunta di un evento di controllo alla fine dell'installazione per l'esecuzione dell'avvio

Il programma di installazione esegue la sequenza dell'installazione guidata dell'esempio solo se [*per*](f-gly.md) installare l'applicazione viene usato il livello completo dell'interfaccia utente. L'ultima finestra di dialogo della sequenza di dialogo di esempio è una [finestra di dialogo di uscita](exit-dialog.md) denominata ExitDialog. Quando un utente interagisce con il pulsante OK in ExitDialog, pubblica prima di tutto [un oggetto ControlEvent EndDialog](enddialog-controlevent.md) che restituisce il controllo al programma di installazione. Il controllo pubblica quindi un [Oggetto ControlEvent DoAction che](doaction-controlevent.md) esegue l'azione personalizzata Launch. Ogni evento di controllo richiede un record nella [tabella ControlEvent](controlevent-table.md). Vedere [Cenni preliminari su ControlEvent.](controlevent-overview.md)

[Tabella ControlEvent](controlevent-table.md)



| Finestra di dialogo     | controllo\_ | Event     | Argomento | Condition                     | Ordering |
|------------|-----------|-----------|----------|-------------------------------|----------|
| Finestra di dialogo ExitDialog | OK        | EndDialog | Return   | 1                             | 1        |
| Finestra di dialogo ExitDialog | OK        | DoAction  | Launch   | NOT Installed AND $Tutorial=3 | 2        |



 

La condizione nel controllo DoAction garantisce che l'azione personalizzata venga eseguita solo durante la prima installazione dell'applicazione e che venga installata localmente. La frase $Tutorial=3 indica che lo stato dell'azione del componente Tutorial è impostato su locale. Vedere [Sintassi delle istruzioni condizionali.](conditional-statement-syntax.md)

L'esempio è stato completato.

 

 



