---
title: Come creare finestre di dialogo attività
description: Una finestra di dialogo attività viene creata e visualizzata utilizzando la funzione TaskDialog o la funzione TaskDialogIndirect.
ms.assetid: CCEFF52F-D501-4145-9799-0A9C529017E1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ea8e3097454505acccf60c7cba3ef56c637af0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044288"
---
# <a name="how-to-create-task-dialogs"></a>Come creare finestre di dialogo attività

Una finestra di dialogo attività viene creata e visualizzata utilizzando la funzione [**taskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog) o la funzione [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="taskdialog"></a>TaskDialog

La funzione **taskDialog** è adatta per le finestre di dialogo semplici che presentano informazioni testuali e richiedono una scelta standard. Questa funzione di creazione non supporta barre di stato, caselle di controllo, piè di pagina, pulsanti di espansione/compressione, pulsanti personalizzati o pulsanti di opzione.

### <a name="taskdialogindirect"></a>TaskDialogIndirect

La funzione **TaskDialogIndirect** è più potente, supporta tutti gli elementi dell'interfaccia disponibili e consente di acquisire gli eventi in una procedura di callback in modo che l'applicazione possa aggiornare un indicatore di stato o rispondere a un clic su un collegamento ipertestuale o un pulsante.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo delle finestre di dialogo delle attività](using-task-dialogs.md)
</dt> </dl>

 

 




