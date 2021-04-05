---
title: Informazioni sulle finestre di dialogo delle attività
description: Una finestra di dialogo attività è una finestra di dialogo che può essere usata per visualizzare le informazioni e ricevere input semplice dall'utente.
ms.assetid: vs|controls|~\controls\toolbar\taskdialogsoverview.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eb5cafa452a4ed653c404d053e888c6de644236
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955309"
---
# <a name="about-task-dialogs"></a>Informazioni sulle finestre di dialogo delle attività

Una finestra di dialogo attività è una finestra di dialogo che può essere usata per visualizzare le informazioni e ricevere input semplice dall'utente. Analogamente a una finestra di messaggio, viene formattata dal sistema operativo in base ai parametri impostati. Tuttavia, una finestra di dialogo attività dispone di molte più funzionalità rispetto a una finestra di messaggio.

> [!Note]  
> Per le finestre di dialogo delle attività è necessario il modello di Apartment a thread singolo (STA).

 

## <a name="parts-of-a-task-dialog"></a>Parti di una finestra di dialogo attività

Una finestra di dialogo attività è costituita da diversi elementi, la maggior parte dei quali è facoltativa. Nella figura seguente sono illustrate le varie parti di una finestra di dialogo attività.

![Screenshot di una finestra che mostra vari pulsanti, tra cui uno accanto al testo del controllo compresso](images/taskdialog.jpg)

Nell'illustrazione seguente, l'utente ha fatto clic sul pulsante accanto al testo del controllo compresso, causando il testo alternativo da visualizzare e nel piè di pagina.

![screenshot della finestra precedente, ma con due righe di testo del controllo espanso](images/taskdialogexpand.jpg)

Le illustrazioni mostrano le parti seguenti:



| Parte                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                          | Membro TASKDIALOGCONFIG                                    |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| Titolo della finestra           | Didascalia della finestra.                                                                                                                                                                                                                                                                                                                                                               | **pszWindowTitle**                                         |
| Icona principale              | Icona grande che indica lo scopo della finestra di dialogo attività.                                                                                                                                                                                                                                                                                                                          | **hMainIcon** o **pszMainIcon**                           |
| Istruzione principale       | Testo principale.                                                                                                                                                                                                                                                                                                                                                                      | **pszMainInstruction**                                     |
| Content                | Testo aggiuntivo.                                                                                                                                                                                                                                                                                                                                                                          | **pszContent**                                             |
| Barra di stato           | Barra animata che mostra lo stato di un'attività.                                                                                                                                                                                                                                                                                                                                | **dwFlags**                                                |
| Pulsanti di opzione          | Opzioni definite dall'applicazione per l'utente.                                                                                                                                                                                                                                                                                                                                            | **pRadioButtons**                                          |
| Pulsante personalizzato          | Pulsante che non è uno dei pulsanti comuni. Può trattarsi di un pulsante normale oppure, come illustrato nella figura, un collegamento di comando con un massimo di due righe di testo.                                                                                                                                                                                                                    | **pButtons**                                               |
| Pulsante Espandi/Comprimi | Pulsante che può essere usato per passare dal testo del controllo compresso definito dall'applicazione, ad esempio "vedere altri dettagli", e dal testo del controllo espanso, che può trovarsi su due o più righe. Quando il testo del controllo viene espanso, viene visualizzato anche il testo aggiuntivo in **pszExpandedInformation** , dopo il testo del contenuto o, come illustrato nella seconda illustrazione, nel piè di pagina. | **pszCollapsedControlText** e **pszExpandedControlText** |
| Casella di controllo verifica | Casella di controllo, accompagnata da testo definito dall'applicazione, per scelte semplici, ad esempio "non visualizzare più questo messaggio".                                                                                                                                                                                                                                                                     | **pszVerificationText**                                    |
| Icona piè di pagina            | Icona piccola che indica lo scopo del testo del piè di pagina.                                                                                                                                                                                                                                                                                                                          | **hFooterIcon** o **pszFooterIcon**                       |
| Testo piè di pagina            | Testo aggiuntivo. Nelle illustrazioni il testo contiene un collegamento ipertestuale.                                                                                                                                                                                                                                                                                                                | **pszFooter**                                              |
| Pulsante comune          | Un pulsante standard; nelle illustrazioni, il pulsante OK.                                                                                                                                                                                                                                                                                                                              | **dwCommonButtons**                                        |



 

 

 




