---
title: Finestre di dialogo Trova e sostituisci
description: Visualizza una finestra di dialogo non modabile che consente all'utente di specificare una stringa da cercare, nonché le opzioni da usare per la ricerca di testo in un documento.
ms.assetid: c8c035bf-795d-42a7-abc6-168dea43e6e9
keywords:
- Windows Interfaccia utente,input utente
- Windows Interfaccia utente,Common Dialog Box Library
- input utente,Libreria di finestre di dialogo comuni
- acquisizione dell'input dell'utente, libreria di finestre di dialogo comune
- Libreria di finestre di dialogo comune
- finestre di dialogo comuni
- Trova - finestra di dialogo
- Sostituisci (finestra di dialogo)
- personalizzazione della finestra di dialogo Trova
- personalizzazione della finestra di dialogo Sostituisci
- finestre di dialogo predefinite
- finestre di dialogo, Trova
- finestre di dialogo,Sostituisci
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59bc5da5a8780a4f08bbf4bf757e1703d8d9120fdefe9d1730e515ffc6feae40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118503490"
---
# <a name="find-and-replace-dialog-boxes"></a>Finestre di dialogo Trova e sostituisci

Visualizza una finestra di dialogo non modabile che consente all'utente di specificare una stringa da cercare, nonché le opzioni da usare per la ricerca di testo in un documento. La **finestra di** dialogo Sostituisci consente all'utente di specificare una stringa da cercare e una stringa di sostituzione, nonché le opzioni per controllare l'operazione.

Per creare e visualizzare una **finestra di** dialogo Trova, inizializzare una [**struttura FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) e passare la struttura alla [**funzione FindText.**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) Nella figura seguente viene illustrata una tipica **finestra di dialogo** Trova.

![Finestra di dialogo Trova](images/finddialogboxxp.png)

Per creare e visualizzare una **finestra di** dialogo Sostituisci, inizializzare una [**struttura FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) e passare la struttura alla [**funzione ReplaceText.**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) Nella figura seguente viene illustrata una **tipica finestra di** dialogo Sostituisci.

![Sostituisci - finestra di dialogo](images/replacedialogboxxp.png)

A differenza di altre finestre di dialogo comuni, **le finestre di** dialogo Trova e sostituisci sono non modali.  Una finestra di dialogo non modabile consente all'utente di passare dalla finestra di dialogo alla finestra che la ha creata. Ciò è utile per consentire all'utente di cercare una stringa, passare alla finestra dell'applicazione per lavorare sulla stringa e tornare alla finestra di dialogo per cercare un'altra stringa senza ripetere il comando necessario per aprire la finestra di dialogo.

Se la [**funzione FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) o [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) crea correttamente la finestra di dialogo, restituisce un handle alla finestra di dialogo. È possibile utilizzare questo handle per spostare e comunicare con la finestra di dialogo. Se la funzione non può creare la finestra di dialogo, restituisce **NULL.** È possibile determinare la causa di un errore chiamando la [**funzione CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) per recuperare il valore di errore esteso.

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Messaggio registrato FINDMSGSTRING](#the-findmsgstring-registered-message)
-   [Personalizzazione della finestra di dialogo Trova o sostituisci](#customizing-the-find-or-replace-dialog-box)

## <a name="the-findmsgstring-registered-message"></a>Messaggio registrato FINDMSGSTRING

Prima di creare  **una finestra** di dialogo Trova o sostituisci, è necessario chiamare la funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere un identificatore di messaggio per il [**messaggio registrato FINDMSGSTRING.**](findmsgstring.md) È quindi possibile usare l'identificatore per rilevare ed elaborare i messaggi inviati dalla finestra di dialogo. Quando l'utente fa clic sul  pulsante Trova successivo **,** Sostituiscio Sostituisci tutto in una finestra di dialogo, la procedura della finestra di dialogo invia un messaggio **FINDMSGSTRING** alla routine della finestra della finestra proprietaria. Quando si crea la finestra di dialogo, il **membro hwndOwner** della [**struttura FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) identifica la finestra proprietaria.

Il *parametro lParam* di un [**messaggio FINDMSGSTRING**](findmsgstring.md) è un puntatore alla struttura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) specificata al momento della creazione della finestra di dialogo. Prima di inviare il messaggio, la finestra di dialogo imposta i membri di questa struttura con l'input utente più recente, inclusa la stringa da cercare, la stringa di sostituzione (se presente) e le opzioni per l'operazione di ricerca e sostituzione.

In un [**messaggio FINDMSGSTRING**](findmsgstring.md) il membro **Flags** della struttura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) include uno dei flag seguenti per indicare l'evento che ha causato il messaggio.



| Contrassegno               | Significato                                                                                                                                                                                                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FR \_ DIALOGTERM** | La finestra di dialogo è in chiusura. Dopo l'elaborazione del messaggio da parte della finestra proprietaria, un handle per la finestra di dialogo non è più valido.                                                                                    |
| **FR \_ FINDNEXT**   | L'utente ha fatto clic **sul pulsante Trova** successivo in una finestra **di** dialogo Trova **o** sostituisci . Il **membro lpstrFindWhat** specifica la stringa da cercare.                                                         |
| **FR \_ REPLACE**    | L'utente ha fatto clic **sul pulsante** Sostituisci in una **finestra di** dialogo Sostituisci. Il **membro lpstrFindWhat** specifica la stringa da sostituire e il membro **lpstrReplaceWith** specifica la stringa di sostituzione.     |
| **FR \_ REPLACEALL** | L'utente ha fatto clic **sul pulsante Sostituisci** tutto in una finestra di **dialogo** Sostituisci. Il **membro lpstrFindWhat** specifica la stringa da sostituire e il membro **lpstrReplaceWith** specifica la stringa di sostituzione. |



 

Per un **messaggio Trova successivo** o Sostituisci **tutto,** il **membro Flags** può includere qualsiasi combinazione dei flag seguenti per indicare le opzioni di ricerca.



| Contrassegno              | Significato                                                                                                                                                                                                                                                                                          |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FR \_ DOWN**      | Se impostato, viene **selezionato il** pulsante Giù dei pulsanti di opzione direzione, che indica che l'utente desidera eseguire la ricerca dalla posizione corrente fino alla fine del documento. Se **FR \_ DOWN non** è impostato, viene selezionato il pulsante **Up** in modo che l'utente voglia eseguire la ricerca all'inizio del documento.       |
| **FR \_ MATCHCASE** | Se impostata, la **casella di controllo Maiuscole/minuscole** è selezionata, a indicare che l'utente vuole che la ricerca dia la distinzione tra maiuscole e minuscole. Se **FR \_ MATCHCASE** non è impostato, la casella di controllo viene deselezionata in modo che la ricerca non possa fare distinzione tra maiuscole e minuscole.                                                                       |
| **FR \_ WHOLEWORD** | Se impostata, la **casella** di controllo Trova solo parola intera è selezionata, a indicare che l'utente vuole cercare solo parole intere che corrispondono alla stringa di ricerca. Se **FR \_ WHOLEWORD** non è impostato, la casella di controllo è deselezionata, quindi è necessario cercare anche frammenti di parole che corrispondono alla stringa di ricerca. |



 

## <a name="customizing-the-find-or-replace-dialog-box"></a>Personalizzazione della finestra di dialogo Trova o sostituisci

Per personalizzare una **finestra di** **dialogo** Trova o sostituisci, è possibile usare uno dei metodi seguenti:

-   Specificare i valori nella [**struttura FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) quando si crea la finestra di dialogo
-   Specificare un modello personalizzato
-   Fornire una procedura hook

Quando si crea  una **finestra di** dialogo Trova o sostituisci, è possibile impostare flag nel membro **Flags** della struttura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) per nascondere o disabilitare uno dei controlli delle opzioni di ricerca. Ad esempio, è possibile impostare il flag FR NOMATCHCASE per disabilitare la casella di controllo Maiuscole/minuscole oppure impostare il \_ flag FR  \_ HIDEMATCHCASE per nasconderlo.

È possibile fornire un modello  personalizzato per **una** finestra di dialogo Trova o sostituisci, ad esempio se si desidera includere controlli aggiuntivi univoci per l'applicazione. Le [**funzioni FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) [**e ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) usano il modello personalizzato al posto del modello predefinito.

**Per fornire un modello personalizzato per una finestra di dialogo Trova o sostituisci**

1.  Creare il modello personalizzato modificando il modello predefinito specificato nel file Findtext.dlg. Gli identificatori di controllo usati nel modello predefinito **della** finestra di **dialogo** Trova o sostituisci sono definiti nel file Dlgs.h.
2.  Usare la [**struttura FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) per abilitare il modello come segue:
    -   -   Se il modello personalizzato è una risorsa in un'applicazione o in una libreria a collegamento dinamico, impostare il \_ flag FR ENABLETEMPLATE nel **membro Flags.** Usare i **membri hInstance** **e lpTemplateName** della struttura per identificare il modulo e il nome della risorsa.

            oppure

        -   Se il modello personalizzato è già in memoria, impostare il \_ flag FR ENABLETEMPLATEHANDLE. Usare il **membro hInstance** per identificare l'oggetto memoria che contiene il modello.

È possibile specificare una procedura hook [**FRHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc) per una **finestra di** dialogo Trova **o** sostituisci. La routine hook può elaborare i messaggi inviati alla finestra di dialogo. Se si usa un modello personalizzato per definire controlli aggiuntivi, è necessario fornire una procedura hook per elaborare l'input per i controlli.

**Per abilitare una routine hook per una finestra di dialogo Trova o sostituisci**

1.  Impostare il \_ flag FR ENABLEHOOK nel **membro Flags** della [**struttura FINDREPLACE.**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
2.  Specificare l'indirizzo della procedura hook nel **membro lpfnHook.**

Dopo [**l'elaborazione del messaggio WM \_ INITDIALOG,**](wm-initdialog.md) la routine della finestra di dialogo invia un **messaggio WM \_ INITDIALOG** alla routine hook. Il *parametro lParam* di questo messaggio è un puntatore alla [**struttura FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) usata per inizializzare la finestra di dialogo.

Se la routine hook restituisce **FALSE** in risposta al messaggio [**WM \_ INITDIALOG,**](wm-initdialog.md) la finestra di dialogo non verrà visualizzata a meno che non venga visualizzata dalla procedura hook. A tale scopo, eseguire prima qualsiasi altra operazione di disegno e quindi chiamare le [**funzioni ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) [**e UpdateWindow.**](/windows/desktop/api/winuser/nf-winuser-updatewindow) Nel codice seguente ne viene illustrato un esempio:


```
// We've returned FALSE in response to WM_INITDIALOG. 
// We've performed any other paint operations. 
// Now we display the dialog box. 
ShowWindow(hDlg, SW_SHOWNORMAL); 
UpdateWindow(hDlg); 
```



 

 