---
description: Una finestra di dialogo Errore è una finestra di dialogo modale che visualizza un messaggio di errore. In ogni installazione possono essere presenti più finestre di dialogo Errore.
ms.assetid: 11d4fe8b-ec5f-4576-95e5-c86344f0195c
title: Finestra di dialogo di errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8582996ad4380d8adc62f684f638092857b45d464e7e8ef150c1fed141027f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692501"
---
# <a name="error-dialog"></a>Finestra di dialogo di errore

Una finestra di dialogo Errore è una finestra di dialogo modale che visualizza un messaggio di errore. In ogni installazione possono essere presenti più finestre di dialogo Errore.

È necessario impostare una proprietà ErrorDialog che specifica la finestra di dialogo da usare. Se questa proprietà non è impostata o non punta a una finestra di dialogo Errore valida, i messaggi di errore non verranno visualizzati. In questo caso, l'errore viene registrato solo con un avviso relativo alla finestra di dialogo mancante.

In una finestra di dialogo Errore deve essere impostato il [bit di stile Finestra di dialogo di](error-dialog-style-bit.md) errore. La finestra di dialogo deve avere [un controllo Text](text-control.md) denominato ErrorText. Il record della finestra di dialogo Errore nella [tabella Dialog deve](dialog-table.md) contenere il controllo ErrorText immesso nel campo Control \_ First.

La finestra di dialogo deve contenere [sette controlli PushButton.](pushbutton-control.md) Tutti questi pulsanti specificano [EndDialog](enddialog-controlevent.md) ControlEvent nella [tabella ControlEvent](controlevent-table.md). Ogni pulsante specifica uno degli attributi seguenti: **ErrorAbort**, **ErrorCancel**, **ErrorIgnore**, **ErrorNo**, **ErrorOk**, **ErrorRetry**, **ErrorSes**.

> [!Note]  
> Lo stato attivo di questi controlli non deve essere collegato tramite l'uso della colonna Control \_ Next nella tabella [Control](control-table.md).

 

Questi pulsanti devono essere posizionati approssimativamente nella stessa posizione nella finestra di dialogo perché, quando viene creata, viene creato solo un subset di questi sette pulsanti, a seconda del messaggio. La coordinata X dei pulsanti viene modificata in modo che i pulsanti visualizzati siano spaziati uniformemente. La coordinata Y, l'altezza e la larghezza dei pulsanti rimangono invariate. Poiché i pulsanti sono disposti orizzontalmente, nessun altro controllo può essere posizionato nella stessa area orizzontale della finestra di dialogo.

Per una finestra di dialogo Errore, i campi \_ Control Default (Controllo predefinito) e Control Cancel \_ (Annulla controllo) nella [tabella Dialog (Finestra](dialog-table.md) di dialogo) vengono ignorati. Il campo Control \_ First per una finestra di dialogo Errore deve specificare il controllo ErrorText.

Se in [questa finestra di](icon-control.md) dialogo è incluso un controllo Icona denominato ErrorIcon, vengono visualizzate le icone Windows standard seguenti:

-   ERRORE IDI \_ in risposta ai messaggi imtFatalExit.
-   AVVISO IDI \_ in risposta ai messaggi imtError e imtWarning.
-   IDI \_ INFORMATION in risposta ai messaggi imtOutOfDiskSpace.

Il controllo ErrorIcon deve essere creato con l'attributo del controllo [FixedSize](fixedsize-control-attribute.md) impostato per evitare il ridimensionamento non corretto delle icone Windows standard.

 

 



