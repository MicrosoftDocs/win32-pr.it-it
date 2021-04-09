---
title: Come ottenere l'input dell'utente da una finestra di dialogo attività
description: Per completare un'attività, gli utenti inviano i dettagli dell'attività all'applicazione configurando i controlli all'interno della finestra di dialogo attività e quindi facendo clic su un pulsante di comando (in genere OK).
ms.assetid: 73CD8FBF-95C9-43C8-B9D8-3823840C23A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd53c8051747187123821211ac7e17c9915b5fd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963511"
---
# <a name="how-to-get-user-input-from-a-task-dialog"></a>Come ottenere l'input dell'utente da una finestra di dialogo attività

Per completare un'attività, gli utenti inviano i dettagli dell'attività all'applicazione configurando i controlli all'interno della finestra di dialogo attività e quindi facendo clic su un pulsante di comando (in genere **OK**).

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="getting-user-input-from-a-task-dialog"></a>Recupero dell'input utente da una finestra di dialogo attività

È possibile identificare il pulsante su cui è stato fatto clic esaminando il parametro *pnButton* della funzione chiamante. È anche possibile identificare il pulsante di opzione selezionato dal parametro *pnRadioButton* di [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)e lo stato della casella di controllo della verifica dal parametro *pfVerificationFlagChecked* .

I clic sui pulsanti e i collegamenti ipertestuali vengono ricevuti dalla funzione [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) sotto forma di [ \_ pulsante TDN \_ selezionato](tdn-button-clicked.md) e [ \_ collegamento ipertestuale TDN \_ fatto clic](tdn-hyperlink-clicked.md) su notifiche. Se la funzione di callback restituisce \_ OK dopo aver gestito una notifica di un pulsante, la finestra di dialogo attività viene chiusa e l'identificatore di comando del pulsante viene restituito in *pnButton*. Se si restituisce \_ false oppure non si dispone di una funzione di callback, la finestra di dialogo attività rimane aperta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo delle finestre di dialogo delle attività](using-task-dialogs.md)
</dt> </dl>

 

 