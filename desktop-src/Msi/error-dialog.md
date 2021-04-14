---
description: Una finestra di dialogo di errore è una finestra di dialogo modale in cui viene visualizzato un messaggio di errore. In ogni installazione può essere presente più di una finestra di dialogo di errore.
ms.assetid: 11d4fe8b-ec5f-4576-95e5-c86344f0195c
title: Finestra di dialogo di errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a153f5e6ee38235f830937d794a9ca9b81314583
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527252"
---
# <a name="error-dialog"></a>Finestra di dialogo di errore

Una finestra di dialogo di errore è una finestra di dialogo modale in cui viene visualizzato un messaggio di errore. In ogni installazione può essere presente più di una finestra di dialogo di errore.

È necessario impostare una proprietà ErrorDialog che specifichi la finestra di dialogo da usare. Se questa proprietà non è impostata o non punta a una finestra di dialogo di errore valida, i messaggi di errore non verranno visualizzati. In questo caso, l'errore viene registrato solo con un avviso sulla finestra di dialogo mancante.

Per una finestra di dialogo di errore è necessario impostare il [bit di stile della finestra di dialogo di errore](error-dialog-style-bit.md) . La finestra di dialogo deve avere un [controllo di testo](text-control.md) denominato ErrorText. Il record per la finestra di dialogo di errore nella [tabella della finestra di dialogo](dialog-table.md) deve avere il controllo ErrorText immesso nel \_ primo campo del controllo.

La finestra di dialogo deve contenere sette [pulsanti](pushbutton-control.md). Tutti questi pulsanti specificano il ControlEvent [EndDialog](enddialog-controlevent.md) nella [tabella ControlEvent](controlevent-table.md). Ogni pulsante specifica uno dei seguenti attributi: **ErrorAbort**, **ErrorCancel**, **ErrorIgnore**, **errorno**, **ErrorOk**, **ErrorRetry**, **ErrorYes**.

> [!Note]  
> Lo stato attivo di questi controlli non deve essere collegato tramite l'utilizzo della colonna del controllo \_ successiva nella [tabella del controllo](control-table.md).

 

Questi pulsanti devono essere posizionati approssimativamente nella stessa posizione della finestra di dialogo perché, al momento della creazione, viene creato solo un subset di questi sette pulsanti, a seconda del messaggio. La coordinata X dei pulsanti viene modificata in modo che i pulsanti visualizzati siano spaziati in modo uniforme. Le coordinate Y, l'altezza e la larghezza dei pulsanti sono invariate. Poiché i pulsanti sono disposti orizzontalmente, nessun altro controllo può essere posizionato nella stessa area orizzontale della finestra di dialogo.

Per una finestra di dialogo di errore, i \_ campi controllo predefinito e \_ Annulla controllo nella tabella della finestra di [dialogo](dialog-table.md) vengono ignorati. Il \_ primo campo controllo per una finestra di dialogo di errore deve specificare il controllo ErrorText.

Se in questa finestra di dialogo è incluso un [controllo icona](icon-control.md) denominato ErrorIcon, vengono visualizzate le icone di Windows standard seguenti:

-   \_Errore IDI in risposta ai messaggi imtFatalExit.
-   Avviso di IDI \_ in risposta ai messaggi imterror e imtWarning.
-   \_Informazioni di Idi in risposta ai messaggi imtOutOfDiskSpace.

Il controllo ErrorIcon deve essere creato con l' [attributo del controllo FixedSize](fixedsize-control-attribute.md) impostato in modo da evitare il ridimensionamento non corretto delle icone standard di Windows.

 

 



