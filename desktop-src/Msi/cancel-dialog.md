---
description: Una finestra di dialogo Annulla conferma che l'utente desidera terminare l'installazione. Si tratta di una finestra di dialogo modale.
ms.assetid: 5dab4315-721e-417d-91e0-b38653a65c23
title: Annulla finestra di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1022a7613f3f5341d8c833b7cbe2645ce871aeb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311000"
---
# <a name="cancel-dialog"></a>Annulla finestra di dialogo

Una finestra di dialogo **Annulla** conferma che l'utente desidera terminare l'installazione. Si tratta di una finestra di dialogo modale.

Questo tipo di finestra di dialogo contiene in genere un [controllo di testo](text-control.md) e due [pulsanti](pushbutton-control.md). I due pulsanti consentono all'utente di scegliere di tornare all'ultima finestra di dialogo o di confermare la chiusura dell'installazione.

Il ControlEvent [EndDialog](enddialog-controlevent.md) è collegato a questi due pulsanti nella [tabella ControlEvent](controlevent-table.md). Il parametro *return* del ControlEvent EndDialog è collegato a uno dei pulsanti e causa la terminazione della finestra di dialogo **Cancel** e lo stato attivo per tornare alla finestra di dialogo precedente. Il parametro *Exit* è collegato al pulsante Other e fa in modo che l'interfaccia utente restituisca il controllo al programma di installazione con il codice appropriato che indica che l'utente desidera uscire. Il programma di installazione viene quindi arrestato e viene visualizzata la [finestra di dialogo UserExit](userexit-dialog.md).

 

 



