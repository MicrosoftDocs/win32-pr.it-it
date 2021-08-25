---
title: Informazioni sulle finestre di dialogo attività
description: Una finestra di dialogo attività è una finestra di dialogo che può essere usata per visualizzare informazioni e ricevere input semplice dall'utente.
ms.assetid: vs|controls|~\controls\toolbar\taskdialogsoverview.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2367e3cadff68f10af9d883d4ed7959e4e862a6f406a83361ea2f40b2f69c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061431"
---
# <a name="about-task-dialogs"></a>Informazioni sulle finestre di dialogo attività

Una finestra di dialogo attività è una finestra di dialogo che può essere usata per visualizzare informazioni e ricevere input semplice dall'utente. Analogamente a una finestra di messaggio, viene formattata dal sistema operativo in base ai parametri impostati. Tuttavia, una finestra di dialogo attività ha molte più funzionalità rispetto a una finestra di messaggio.

> [!Note]  
> Le finestre di dialogo attività richiedono il modello apartment a thread singolo (STA).

 

## <a name="parts-of-a-task-dialog"></a>Parti di una finestra di dialogo attività

Una finestra di dialogo attività è costituita da diversi elementi, la maggior parte dei quali sono facoltativi. La figura seguente mostra le varie parti di una finestra di dialogo attività.

![Screenshot di una finestra che mostra vari pulsanti, incluso uno accanto al testo del controllo compresso](images/taskdialog.jpg)

Nella figura seguente l'utente ha fatto clic sul pulsante accanto al testo del controllo compresso, causando la visualizzazione di testo alternativo in questa posizione e nel piè di pagina.

![screenshot della finestra precedente, ma con due righe di testo di controllo espanso](images/taskdialogexpand.jpg)

Le illustrazioni illustrano le parti seguenti:



| Parte                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                          | Membro TASKDIALOGCONFIG                                    |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| Titolo della finestra           | Didascalia della finestra.                                                                                                                                                                                                                                                                                                                                                               | **pszWindowTitle**                                         |
| Icona principale              | Icona grande che indica lo scopo della finestra di dialogo attività.                                                                                                                                                                                                                                                                                                                          | **hMainIcon** o **pszMainIcon**                           |
| Istruzione main       | Testo dell'entità.                                                                                                                                                                                                                                                                                                                                                                      | **pszMainInstruction**                                     |
| Content                | Testo aggiuntivo.                                                                                                                                                                                                                                                                                                                                                                          | **pszContent**                                             |
| Barra di stato           | Barra animata che mostra lo stato di avanzamento di un'attività.                                                                                                                                                                                                                                                                                                                                | **dwFlags**                                                |
| Pulsanti di opzione          | Opzioni definite dall'applicazione per l'utente.                                                                                                                                                                                                                                                                                                                                            | **pRadioButtons**                                          |
| Pulsante personalizzato          | Pulsante che non è uno dei pulsanti comuni. Può trattarsi di un pulsante normale o, come illustrato nella figura, di un collegamento di comando con un massimo di due righe di testo.                                                                                                                                                                                                                    | **pButtons**                                               |
| Pulsante Espandi/Comprimi | Pulsante che può essere usato per alternare il testo del controllo compresso definito dall'applicazione (ad esempio "Visualizza altri dettagli") e il testo del controllo espanso, che può essere su due o più righe. Quando il testo del controllo viene espanso, viene visualizzato anche il testo aggiuntivo in **pszExpandedInformation,** dopo il testo del contenuto o (come illustrato nella seconda illustrazione) nel piè di pagina. | **pszCollapsedControlText** e **pszExpandedControlText** |
| Casella di controllo Verifica | Casella di controllo, accompagnata da testo definito dall'applicazione, per scelte semplici, ad esempio "Non visualizzare più questa finestra di dialogo".                                                                                                                                                                                                                                                                     | **pszVerificationText**                                    |
| Icona piè di pagina            | Icona piccola che indica lo scopo del testo del piè di pagina.                                                                                                                                                                                                                                                                                                                          | **hFooterIcon** o **pszFooterIcon**                       |
| Testo piè di pagina            | Testo aggiuntivo. Nelle illustrazioni il testo contiene un collegamento ipertestuale.                                                                                                                                                                                                                                                                                                                | **pszFooter**                                              |
| Pulsante Comune          | Un pulsante standard; nelle illustrazioni, il pulsante OK.                                                                                                                                                                                                                                                                                                                              | **dwCommonButtons**                                        |



 

 

 




