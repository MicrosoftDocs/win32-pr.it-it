---
title: Finestre di dialogo Trova e Sostituisci
description: Visualizza una finestra di dialogo non modale che consente all'utente di specificare una stringa da ricercare, nonché le opzioni da utilizzare per la ricerca di testo in un documento.
ms.assetid: c8c035bf-795d-42a7-abc6-168dea43e6e9
keywords:
- Interfaccia utente di Windows, input utente
- Interfaccia utente di Windows, libreria finestra di dialogo comune
- input utente, libreria finestra di dialogo comune
- acquisizione dell'input dell'utente, libreria finestra di dialogo comune
- Libreria finestra di dialogo comune
- finestre di dialogo comuni
- Trova - finestra di dialogo
- Sostituisci (finestra di dialogo)
- personalizzazione della finestra di dialogo Trova
- personalizzazione della finestra di dialogo Sostituisci
- finestre di dialogo predefinite
- finestre di dialogo, trova
- finestre di dialogo, Sostituisci
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e3cf2c5217d586c0a5ada74fb7dd72aaca5f804
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104555361"
---
# <a name="find-and-replace-dialog-boxes"></a>Finestre di dialogo Trova e Sostituisci

Visualizza una finestra di dialogo non modale che consente all'utente di specificare una stringa da ricercare, nonché le opzioni da utilizzare per la ricerca di testo in un documento. La finestra di dialogo **Sostituisci** consente all'utente di specificare una stringa da cercare e una stringa di sostituzione, nonché le opzioni per controllare l'operazione.

Per creare e visualizzare una finestra di dialogo **trova** , inizializzare una struttura [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) e passare la struttura alla funzione [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) . Nella figura seguente viene illustrata una tipica finestra di dialogo **trova** .

![Trova-finestra di dialogo](images/finddialogboxxp.png)

Per creare e visualizzare una finestra di dialogo **Sostituisci** , inizializzare una struttura [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) e passare la struttura alla funzione [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) . Nella figura seguente viene illustrata una tipica finestra di dialogo **Sostituisci** .

![Sostituisci finestra di dialogo](images/replacedialogboxxp.png)

Diversamente dalle altre finestre di dialogo comuni, le finestre di dialogo **trova** e **Sostituisci** non sono modali. Una finestra di dialogo non modale consente all'utente di passare dalla finestra di dialogo alla finestra che la ha creata. Questa opzione è utile per consentire all'utente di cercare una stringa, passare alla finestra dell'applicazione per lavorare sulla stringa e tornare alla finestra di dialogo per cercare un'altra stringa senza ripetere il comando necessario per aprire la finestra di dialogo.

Se la funzione [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) o [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) crea correttamente la finestra di dialogo, viene restituito un handle per la finestra di dialogo. È possibile utilizzare questo handle per lo spostamento e la comunicazione con la finestra di dialogo. Se la funzione non è in grado di creare la finestra di dialogo, restituisce **null**. È possibile determinare la provocazione di un errore chiamando la funzione [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) per recuperare il valore di errore esteso.

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Messaggio registrato FINDMSGSTRING](#the-findmsgstring-registered-message)
-   [Personalizzazione della finestra di dialogo Trova o Sostituisci](#customizing-the-find-or-replace-dialog-box)

## <a name="the-findmsgstring-registered-message"></a>Messaggio registrato FINDMSGSTRING

Prima di creare una finestra di dialogo **trova** o **Sostituisci** , è necessario chiamare la funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere un identificatore di messaggio per il messaggio [**FINDMSGSTRING**](findmsgstring.md) registrato. È quindi possibile utilizzare l'identificatore per rilevare ed elaborare i messaggi inviati dalla finestra di dialogo. Quando l'utente fa clic sul pulsante **Trova successivo**, **Sostituisci** o **Sostituisci tutto** in una finestra di dialogo, la routine della finestra di dialogo Invia un messaggio **FINDMSGSTRING** alla routine della finestra proprietaria. Quando si crea la finestra di dialogo, il membro **hwndOwner** della struttura [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) identifica la finestra proprietaria.

Il parametro *lParam* di un messaggio [**FINDMSGSTRING**](findmsgstring.md) è un puntatore alla struttura [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) specificata al momento della creazione della finestra di dialogo. Prima di inviare il messaggio, la finestra di dialogo Imposta i membri di questa struttura con l'input dell'utente più recente, inclusa la stringa da cercare, la stringa di sostituzione (se presente) e le opzioni per l'operazione di ricerca e sostituzione.

In un messaggio [**FINDMSGSTRING**](findmsgstring.md) , il membro **Flags** della struttura [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) include uno dei flag seguenti per indicare l'evento che ha causato il messaggio.



| Contrassegno               | Significato                                                                                                                                                                                                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FR \_ DIALOGTERM** | La finestra di dialogo sta per essere chiusa. Quando la finestra proprietaria elabora questo messaggio, un handle per la finestra di dialogo non è più valido.                                                                                    |
| **FR \_ TrovaSuccessivo**   | L'utente ha fatto clic sul pulsante **Trova successivo** in una finestra di dialogo **trova** o **Sostituisci** . Il membro **lpstrFindWhat** specifica la stringa da cercare.                                                         |
| **FR \_ Sostituisci**    | L'utente ha fatto clic sul pulsante **Sostituisci** in una finestra di dialogo **Sostituisci** . Il membro **lpstrFindWhat** specifica la stringa da sostituire e il membro **lpstrReplaceWith** specifica la stringa di sostituzione.     |
| **FR \_ REPLACEALL** | L'utente ha fatto clic sul pulsante **Sostituisci tutto** in una finestra di dialogo **Sostituisci** . Il membro **lpstrFindWhat** specifica la stringa da sostituire e il membro **lpstrReplaceWith** specifica la stringa di sostituzione. |



 

Per un messaggio **Trova successivo** o **Sostituisci tutto** , il membro **Flags** può includere qualsiasi combinazione dei flag seguenti per indicare le opzioni di ricerca.



| Contrassegno              | Significato                                                                                                                                                                                                                                                                                          |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FR \_ giù**      | Se impostato, viene selezionato il pulsante **giù** dei pulsanti di opzione direzione, che indica che l'utente desidera eseguire la ricerca dalla posizione corrente fino alla fine del documento. Se **fr \_ Down** non è impostato, viene selezionato il pulsante **su** in modo che l'utente desideri eseguire la ricerca all'inizio del documento.       |
| **FR \_ MATCHCASE** | Se impostata, viene selezionata la casella di controllo **maiuscole/minuscole** , che indica che l'utente desidera che la ricerca venga fatta distinzione tra maiuscole e minuscole Se **fr \_ MATCHCASE** non è impostato, la casella di controllo viene deselezionata, in modo che la ricerca non possa fare distinzione tra maiuscole e minuscole.                                                                       |
| **FR \_ WHOLEWORD** | Se impostata, la casella di controllo trova **solo parola intera** è selezionata, a indicare che l'utente desidera eseguire la ricerca solo di parole intere che corrispondono alla stringa di ricerca. Se **fr \_ WHOLEWORD** non è impostato, la casella di controllo è deselezionata, quindi è necessario cercare anche frammenti di parola che corrispondono alla stringa di ricerca. |



 

## <a name="customizing-the-find-or-replace-dialog-box"></a>Personalizzazione della finestra di dialogo Trova o Sostituisci

Per personalizzare una finestra di dialogo **trova** o **Sostituisci** , è possibile utilizzare uno dei metodi seguenti:

-   Specificare i valori nella struttura [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) quando si crea la finestra di dialogo
-   Fornire un modello personalizzato
-   Fornire una routine hook

Quando si crea una finestra di dialogo **trova** o **Sostituisci** , è possibile impostare i flag nel membro **Flags** della struttura [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) per nascondere o disabilitare i controlli delle opzioni di ricerca. Ad esempio, è possibile impostare il \_ flag fr NOMATCHCASE per disabilitare la casella di controllo **maiuscole/minuscole** o impostare il \_ flag fr HIDEMATCHCASE per nasconderlo.

È possibile specificare un modello personalizzato per una finestra di dialogo **trova** o **Sostituisci** , ad esempio se si desidera includere controlli aggiuntivi che siano univoci per l'applicazione. Le funzioni [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) e [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) usano il modello personalizzato al posto del modello predefinito.

**Per fornire un modello personalizzato per una finestra di dialogo Trova o Sostituisci**

1.  Creare il modello personalizzato modificando il modello predefinito specificato nel file FindText. dlg. Gli identificatori di controllo utilizzati nel modello di finestra di dialogo **trova** o **Sostituisci** predefinito vengono definiti nel file Dlgs. h.
2.  Utilizzare la struttura [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) per abilitare il modello nel modo seguente:
    -   -   Se il modello personalizzato è una risorsa in un'applicazione o in una libreria a collegamento dinamico, impostare il \_ flag fr ENABLETEMPLATE nel membro **Flags** . Usare i membri **HINSTANCE** e **lpTemplateName** della struttura per identificare il modulo e il nome della risorsa.

            oppure

        -   Se il modello personalizzato è già in memoria, impostare il \_ flag fr ENABLETEMPLATEHANDLE. Usare il membro **HINSTANCE** per identificare l'oggetto memoria che contiene il modello.

È possibile specificare una procedura di hook [**FRHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc) per una finestra di dialogo **trova** o **Sostituisci** . La procedura hook può elaborare i messaggi inviati alla finestra di dialogo. Se si usa un modello personalizzato per definire controlli aggiuntivi, è necessario fornire una procedura di hook per elaborare l'input per i controlli.

**Per abilitare una procedura di hook per una finestra di dialogo Trova o Sostituisci**

1.  Impostare il \_ flag fr ENABLEHOOK nel membro **Flags** della struttura [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) .
2.  Specificare l'indirizzo della routine hook nel membro **lpfnHook** .

Dopo l'elaborazione del messaggio [**WM \_ INITDIALOG**](wm-initdialog.md) , la routine della finestra di dialogo Invia un messaggio **WM \_ INITDIALOG** alla routine hook. Il parametro *lParam* di questo messaggio è un puntatore alla struttura [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) utilizzata per inizializzare la finestra di dialogo.

Se la routine hook restituisce **false** in risposta al messaggio [**WM \_ INITDIALOG**](wm-initdialog.md) , la finestra di dialogo non verrà visualizzata a meno che non venga visualizzata dalla procedura hook. A tale scopo, eseguire prima qualsiasi altra operazione di disegno, quindi chiamare le funzioni [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) e [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) . Nel codice seguente ne viene illustrato un esempio:


```
// We've returned FALSE in response to WM_INITDIALOG. 
// We've performed any other paint operations. 
// Now we display the dialog box. 
ShowWindow(hDlg, SW_SHOWNORMAL); 
UpdateWindow(hDlg); 
```



 

 