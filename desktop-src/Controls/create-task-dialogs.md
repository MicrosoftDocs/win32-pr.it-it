---
title: Come creare finestre di dialogo attività
description: Viene creata e visualizzata una finestra di dialogo attività usando la funzione TaskDialog o taskDialogIndirect.
ms.assetid: CCEFF52F-D501-4145-9799-0A9C529017E1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f6f74f1922330cae1550fda1a9ad6d451221452017f3856ae5e859948019828
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504021"
---
# <a name="how-to-create-task-dialogs"></a>Come creare finestre di dialogo attività

Viene creata e visualizzata una finestra di dialogo attività usando la [**funzione TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog) o [**taskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="taskdialog"></a>Finestra di dialogo Attività

La **funzione TaskDialog** è adatta per finestre di dialogo semplici che presentano informazioni testuali e chiedono una scelta standard. Questa funzione di creazione non supporta barre di stato, caselle di controllo, piè di pagina, pulsanti di espansione/compressione, pulsanti personalizzati o pulsanti di opzione.

### <a name="taskdialogindirect"></a>TaskDialogIndirect

La **funzione TaskDialogIndirect** è più potente, supporta tutti gli elementi dell'interfaccia disponibili e consente anche di acquisire eventi in una routine di callback in modo che l'applicazione possa aggiornare un indicatore di stato o rispondere a un clic di un collegamento ipertestuale o di un pulsante.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di finestre di dialogo attività](using-task-dialogs.md)
</dt> </dl>

 

 




