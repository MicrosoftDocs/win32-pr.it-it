---
title: Come personalizzare le barre degli strumenti
description: La maggior Windows applicazioni basate su applicazioni basate su usano i controlli della barra degli strumenti per fornire agli utenti un comodo accesso alla funzionalità del programma.
ms.assetid: 0CE2988E-D887-433B-BFB2-5F3442E8E1B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f098880676fc0404df2a68694dc80b8601c21926d94ff594029321bafb1528a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929547"
---
# <a name="how-to-customize-toolbars"></a>Come personalizzare le barre degli strumenti

La maggior Windows applicazioni basate su applicazioni basate su usano i controlli della barra degli strumenti per fornire agli utenti un comodo accesso alla funzionalità del programma. Tuttavia, le barre degli strumenti statiche hanno alcune lacune, ad esempio troppo poco spazio per visualizzare in modo efficace tutti gli strumenti disponibili. La soluzione a questo problema consiste nel rendere personalizzabili dall'utente le barre degli strumenti dell'applicazione. Gli utenti possono quindi scegliere di visualizzare solo gli strumenti necessari e di organizzarli in base al proprio stile di lavoro personale.

> [!Note]  
> Le barre degli strumenti nelle finestre di dialogo non possono essere personalizzate.

 

Per abilitare la personalizzazione, includere il flag di stile [**\_ CCS ADJUSTABLE**](common-control-styles.md) common controls quando si crea il controllo barra degli strumenti. Esistono due approcci di base alla personalizzazione:

-   Finestra di dialogo di personalizzazione. Questa finestra di dialogo fornita dal sistema è l'approccio più semplice. Offre agli utenti un'interfaccia utente grafica che consente di aggiungere, eliminare o spostare icone.
-   Strumenti di trascinamento della selezione. L'implementazione della funzionalità di trascinamento della selezione consente agli utenti di spostare gli strumenti in un'altra posizione sulla barra degli strumenti o di eliminarli trascinandoli fuori dalla barra degli strumenti. Offre agli utenti un modo rapido e semplice per organizzare la barra degli strumenti, ma non consente loro di aggiungere strumenti.

È possibile implementare un approccio o entrambi, a seconda delle esigenze dell'applicazione. Nessuno di questi due approcci alla personalizzazione fornisce un meccanismo predefinito, ad esempio un pulsante Annulla o Annulla, per ripristinare lo stato precedente della barra degli strumenti. È necessario usare in modo esplicito l'API del controllo barra degli strumenti per archiviare lo stato di pre-percustomizzazione della barra degli strumenti. Se necessario, è possibile usare queste informazioni archiviate in un secondo momento per ripristinare lo stato originale della barra degli strumenti.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="customization-dialog-box"></a>Finestra di dialogo Personalizzazione

La finestra di dialogo di personalizzazione viene fornita dal controllo barra degli strumenti per offrire agli utenti un modo semplice per aggiungere, spostare o eliminare strumenti. Gli utenti possono avviarlo facendo doppio clic sulla barra degli strumenti. Le applicazioni possono avviare la finestra di dialogo di personalizzazione a livello di codice inviando al controllo della barra degli strumenti [**un messaggio \_ TB CUSTOMIZE.**](tb-customize.md)

Nella figura seguente viene illustrato un esempio della finestra di dialogo di personalizzazione della barra degli strumenti.

![Screenshot di una finestra con una barra degli strumenti a tre elementi e una finestra di dialogo con gli elenchi dei pulsanti della barra degli strumenti disponibili e correnti](images/tb-customdlg.png)

Gli strumenti nella casella di riepilogo a destra sono quelli attualmente disponibili sulla barra degli strumenti. Inizialmente, questo elenco conterrà gli strumenti specificati quando si crea la barra degli strumenti. La casella di riepilogo a sinistra contiene gli strumenti disponibili per l'aggiunta alla barra degli strumenti. L'applicazione è responsabile del popolamento dell'elenco(diverso dal separatore, che viene visualizzato automaticamente).

Il controllo barra degli strumenti notifica all'applicazione che sta avviando una finestra di dialogo di personalizzazione inviando alla finestra padre un codice di notifica [TBN \_ BEGINADJUST](tbn-beginadjust.md) seguito da un codice di notifica [TBN \_ INITCUSTOMIZE.](tbn-initcustomize.md) Nella maggior parte dei casi, l'applicazione non deve rispondere a questi codici di notifica. Tuttavia, se non si desidera che nella finestra di dialogo Personalizza barra degli strumenti sia visualizzato un pulsante ? , gestire TBN INITCUSTOMIZE tramite la restituzione di \_ TBNRF \_ HIDEHELP.

Il controllo barra degli strumenti raccoglie quindi le informazioni necessarie per inizializzare la finestra di dialogo inviando tre serie di codici di notifica, nell'ordine seguente:

-   Codice [di notifica TBN \_ QUERYINSERT](tbn-queryinsert.md) per ogni pulsante sulla barra degli strumenti per determinare dove è possibile inserire i pulsanti. Restituisce **FALSE** per impedire l'inserimento di un pulsante a sinistra del pulsante specificato nel messaggio di notifica. Se si restituisce **FALSE a** tutti i codici di notifica TBN QUERYINSERT, la finestra di dialogo \_ non verrà visualizzata.
-   Codice [di notifica \_ QUERYDELETE TBN](tbn-querydelete.md) per ogni strumento attualmente disponibile sulla barra degli strumenti. Restituisce **TRUE** se è possibile eliminare uno strumento oppure **FALSE** in caso contrario.
-   Serie di codici [di notifica \_ TBN GETBUTTONINFO](tbn-getbuttoninfo.md) per popolare l'elenco dei pulsanti disponibili. Per aggiungere un pulsante all'elenco, compilare la [**struttura NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) passata con il codice di notifica e restituire **TRUE.** Quando non sono disponibili altri strumenti da aggiungere, restituire **FALSE.** Si noti che è possibile restituire informazioni per i pulsanti già presenti sulla barra degli strumenti. questi pulsanti non verranno aggiunti all'elenco.

Viene quindi visualizzata la finestra di dialogo e l'utente può iniziare a personalizzare la barra degli strumenti.

Quando la finestra di dialogo è aperta, l'applicazione può ricevere diversi codici di notifica, a seconda delle azioni dell'utente:

-   [TBN \_ QUERYINSERT](tbn-queryinsert.md). L'utente ha modificato la posizione di uno strumento sulla barra degli strumenti o ha aggiunto uno strumento. Restituisce **FALSE** per impedire l'inserimento dello strumento in tale posizione.
-   [TBN \_ DELETINGBUTTON](tbn-deletingbutton.md). L'utente sta per rimuovere uno strumento dalla barra degli strumenti.
-   [TBN \_ CUSTHELP](tbn-custhelp.md). L'utente ha fatto clic sul pulsante ? .
-   [TBN \_ TOOLBARCHANGE](tbn-toolbarchange.md). L'utente ha aggiunto, spostato o eliminato uno strumento.
-   [TBN \_ RESET](tbn-reset.md). L'utente ha fatto clic sul pulsante Reimposta.

Dopo l'eliminazione della finestra di dialogo, l'applicazione riceverà un codice di notifica [ \_ TBN ENDADJUST.](tbn-endadjust.md)

Nell'esempio di codice seguente viene illustrato un modo per implementare la personalizzazione della barra degli strumenti.


```C++
// The buttons are stored in an array of TBBUTTON structures. 
//
// Constants such as STD_FILENEW are identifiers for the 
// built-in bitmaps that have already been assigned as the toolbar's 
// image list.
//
// Constants such as IDM_NEW are application-defined command identifiers.

TBBUTTON allButtons[] = 
    {
        { MAKELONG(STD_FILENEW,  ImageListID), IDM_NEW,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"New" },
        { MAKELONG(STD_FILEOPEN, ImageListID), IDM_OPEN,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Open"},
        { MAKELONG(STD_FILESAVE, ImageListID), IDM_SAVE,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Save"},
        { MAKELONG(STD_CUT,      ImageListID), IDM_CUT,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Cut" },
        { MAKELONG(STD_COPY,     ImageListID), IDM_COPY,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Copy"},
        { MAKELONG(STD_PASTE,    ImageListID), IDM_PASTE, TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Paste"}
    };

// The following appears in the window's message handler.

case WM_NOTIFY: 
    {
        switch (((LPNMHDR)lParam)->code) 
        {
        
        case TBN_GETBUTTONINFO:  
            {
                LPTBNOTIFY lpTbNotify = (LPTBNOTIFY)lParam;

                // Pass the next button from the array. There is no need to filter out buttons
                // that are already used—they will be ignored.
                
                int buttonCount = sizeof(allButtons) / sizeof(TBBUTTON);
                
                if (lpTbNotify->iItem < buttonCount)
                {
                    lpTbNotify->tbButton = allButtons[lpTbNotify->iItem];
                    return TRUE;
                }
                
                else
                
                {
                    return FALSE;  // No more buttons.
                }
            }
            
            break;

            case TBN_QUERYINSERT:
            
            case TBN_QUERYDELETE:
                return TRUE; 
        }
    }
```



### <a name="dragging-and-dropping-tools"></a>Strumenti di trascinamento della selezione

Gli utenti possono anche ridisporre i pulsanti su una barra degli strumenti premendo MAIUSC e trascinando il pulsante in un'altra posizione. Il processo di trascinamento della selezione viene gestito automaticamente dal controllo barra degli strumenti. Visualizza un'immagine fantasma del pulsante mentre viene trascinato e ridispone la barra degli strumenti dopo che è stato rilasciato. Gli utenti non possono aggiungere pulsanti in questo modo, ma possono eliminare un pulsante eliminandolo dalla barra degli strumenti.

Anche se il controllo barra degli strumenti esegue normalmente questa operazione automaticamente, invia anche all'applicazione due codici di notifica: [TBN \_ QUERYDELETE](tbn-querydelete.md) e [TBN \_ QUERYINSERT](tbn-queryinsert.md). Per controllare il processo di trascinamento della selezione, gestire questi codici di notifica come indicato di seguito:

-   Il codice di notifica [ \_ TBN QUERYDELETE](tbn-querydelete.md) viene inviato non appena l'utente tenta di spostare il pulsante, prima che venga visualizzato il pulsante fantasma. Restituisce **FALSE** per impedire lo spostamento del pulsante. Se si restituisce **TRUE,** l'utente potrà spostare lo strumento o eliminarlo eliminandolo dalla barra degli strumenti. Se uno strumento può essere spostato, può essere eliminato. Tuttavia, se l'utente elimina uno strumento, il controllo barra degli strumenti invierà all'applicazione un codice di notifica [TBN \_ DELETINGBUTTON,](tbn-deletingbutton.md) a questo punto è possibile scegliere di reinserire il pulsante nella posizione originale, annullando così l'eliminazione.
-   Il [codice di notifica \_ TBN QUERYINSERT](tbn-queryinsert.md) viene inviato quando l'utente tenta di rilasciare il pulsante sulla barra degli strumenti. Per evitare che il pulsante spostato venga rilasciato a sinistra del pulsante specificato nella notifica, restituire **FALSE.** Questo codice di notifica non viene inviato se l'utente rilascia lo strumento dalla barra degli strumenti.

Se l'utente tenta di trascinare un pulsante senza premere anche MAIUSC, il controllo barra degli strumenti non gestirà l'operazione di trascinamento della selezione. Tuttavia, invierà all'applicazione un codice di notifica [TBN \_ BEGINDRAG](tbn-begindrag.md) per indicare l'inizio di un'operazione di trascinamento e un codice di notifica [TBN \_ ENDDRAG](tbn-enddrag.md) per indicare la fine. Se si desidera abilitare questa forma di trascinamento della selezione, l'applicazione deve gestire questi codici di notifica, fornire l'interfaccia utente necessaria e modificare la barra degli strumenti in modo da riflettere eventuali modifiche.

### <a name="saving-and-restoring-toolbars"></a>Salvataggio e ripristino delle barre degli strumenti

Durante il processo di personalizzazione di una barra degli strumenti, l'applicazione potrebbe dover salvare le informazioni in modo da ripristinare lo stato originale della barra degli strumenti. Per avviare il salvataggio o il ripristino di uno stato della barra degli strumenti, inviare al controllo della barra degli strumenti un messaggio [**\_ TB SAVERESTORE**](tb-saverestore.md) con *l'opzione lParam* impostata su **TRUE.** Il *valore lParam* di questo messaggio specifica se si richiede un'operazione di salvataggio o ripristino. Dopo l'invio del messaggio, è possibile gestire l'operazione di salvataggio/ripristino in due modi:

-   Con i controlli [comuni versione 4.72](common-control-versions.md) e precedenti, è necessario implementare un gestore [ \_ GETBUTTONINFO TBN.](tbn-getbuttoninfo.md) Il controllo barra degli strumenti invia questo codice di notifica per richiedere informazioni su ogni pulsante durante il ripristino.
-   La versione 5.80 include un'opzione di salvataggio/ripristino. All'inizio del processo e quando ogni pulsante viene salvato o ripristinato, l'applicazione riceverà un codice di notifica [TBN \_ SAVE](tbn-save.md) o [TBN \_ RESTORE.](tbn-restore.md) Per usare questa opzione, è necessario implementare gestori di notifica per fornire la bitmap e le informazioni sullo stato necessarie per salvare o ripristinare correttamente lo stato della barra degli strumenti.

Gli stati della barra degli strumenti vengono salvati in un flusso di dati costituito da blocchi di dati definiti dalla shell alternati a blocchi di dati definiti dall'applicazione. Un blocco di dati di ogni tipo viene archiviato per ogni pulsante, insieme a un blocco facoltativo di dati globali che le applicazioni possono inserire all'inizio del flusso. Durante il processo di salvataggio, il gestore [TBN \_ SAVE](tbn-save.md) aggiunge i blocchi definiti dall'applicazione al flusso di dati. Durante il processo di ripristino, il gestore [TBN \_ RESTORE](tbn-restore.md) legge ogni blocco e fornisce alla shell le informazioni necessarie per ricostruire la barra degli strumenti.

### <a name="how-to-handle-a-tbn_save-notification"></a>Come gestire una notifica TBN \_ SAVE

Il primo [codice di notifica TBN \_ SAVE](tbn-save.md) viene inviato all'inizio del processo di salvataggio. Prima di salvare i pulsanti, i membri della [**struttura NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) vengono impostati come illustrato nella tabella seguente.



| Membro       | Impostazione                                                                                                                                                                                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **iItem**    | –1                                                                                                                                                                                                                                                                                                                                                 |
| **cbData**   | Quantità di memoria necessaria per i dati definiti dalla shell.                                                                                                                                                                                                                                                                                                |
| **cButtons** | Numero di pulsanti.                                                                                                                                                                                                                                                                                                                             |
| **pData**    | Quantità calcolata di memoria necessaria per i dati definiti dall'applicazione. In genere, si includono alcuni dati globali, oltre ai dati per ogni pulsante. Aggiungere tale valore a **cbData** e allocare memoria sufficiente a **pData** per contenere tutto.                                                                                                                      |
| **pCurrent** | Primo byte inutilizzato nel flusso di dati. Se non sono necessarie informazioni globali sulla barra degli strumenti, impostare **pCurrent** pData in modo che punti  =   all'inizio del flusso di dati. Se sono necessarie informazioni globali sulla barra degli strumenti, archiviarla in **pData**, quindi impostare **pCurrent** sull'inizio della parte inutilizzata del flusso di dati prima della restituzione. |



 

Se si desidera aggiungere alcune informazioni globali sulla barra degli strumenti, inserire le informazioni all'inizio del flusso di dati. Far **avanzare pCurrent** alla fine dei dati globali in modo che punti all'inizio della parte inutilizzata del flusso di dati e restituirla.

Dopo la restituzione, shell inizia a salvare le informazioni sul pulsante. Aggiunge i dati definiti dalla shell per il primo pulsante in **pCurrent** e quindi sposta **pCurrent** all'inizio della parte inutilizzata.

Dopo il salvataggio di ogni pulsante, viene inviato un codice di notifica [TBN \_ SAVE](tbn-save.md) e [**viene restituito NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) con questi membri impostati come indicato di seguito.



| Membro                       | Impostazione                                                                                                                                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **iItem**                    | Indice in base zero del numero del pulsante.                                                                                                                                                                                                                           |
| **pCurrent**                 | Puntatore al primo byte inutilizzato nel flusso di dati. Se si desidera archiviare informazioni aggiuntive sul pulsante, archiviarlo nella posizione a cui punta **pCurrent** e aggiornare **pCurrent** in modo che punti alla prima parte inutilizzata del flusso di dati dopo tale operazione. |
| [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) | Struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) che descrive il pulsante che viene salvato.                                                                                                                                                                              |



 

Quando si riceve il codice di notifica, è necessario estrarre tutte le informazioni specifiche del pulsante necessarie da [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton). Tenere presente che quando si aggiunge un pulsante, è possibile usare il **membro dwData** di **TBBUTTON** per contenere dati specifici dell'applicazione. Caricare i dati nel flusso di dati in **pCurrent.** Far **avanzare pCurrent** alla fine dei dati, puntando nuovamente all'inizio della parte inutilizzata del flusso e restituire .

Shell passa quindi al pulsante successivo, aggiunge le informazioni a **pData,** sposta **pCurrent,** carica [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)e invia un altro codice di notifica [TBN \_ SAVE.](tbn-save.md) Questo processo continua fino a quando non vengono salvati tutti i pulsanti.

### <a name="restoring-saved-toolbars"></a>Ripristino delle barre degli strumenti salvate

Il processo di ripristino inverte fondamentalmente il processo di salvataggio. All'inizio, l'applicazione riceverà un codice di notifica [TBN \_ RESTORE](tbn-restore.md) con il membro **iItem** della struttura [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) impostato su -1. Il **membro cbData** è impostato sulla dimensione **di pData** e **cButtons** è impostato sul numero di pulsanti.

Il gestore delle notifiche deve estrarre le informazioni globali inserite all'inizio di **pData** durante il salvataggio e far avanzare **pCurrent** all'inizio del primo blocco di dati definiti dalla shell. Impostare **cBytesPerRecord sulla** dimensione dei blocchi di dati usati per salvare i dati del pulsante. Impostare **cButtons** sul numero di pulsanti e restituire .

Il successivo [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) è per il primo pulsante. Il **membro pCurrent** punta all'inizio del primo blocco di dati del pulsante e **iItem** è impostato sull'indice del pulsante. Estrarre i dati e far avanzare **pCurrent**. Caricare i dati in [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)e restituire . Per omettere un pulsante dalla barra degli strumenti ripristinata, impostare il membro **idCommand** di **TBBUTTON** su zero. Shell ripeterà il processo per i pulsanti rimanenti. Oltre ai messaggi [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) e **NMTBRESTORE,** è anche possibile usare messaggi come [TBN \_ RESET](tbn-reset.md) per salvare e ripristinare una barra degli strumenti.

L'esempio di codice seguente salva una barra degli strumenti prima che venga personalizzata e la ripristina se l'applicazione riceve un [messaggio TBN \_ RESET.](tbn-reset.md)


```C++
int               i;
LPNMHDR           lpnmhdr;
static int        nResetCount;
static LPTBBUTTON lpSaveButtons;
LPARAM            lParam;

switch( lpnmhdr->code)
{
    case TBN_BEGINADJUST: // Begin customizing the toolbar.
    {
        LPTBNOTIFY  lpTB = (LPTBNOTIFY)lparam;
       
        // Allocate memory for the button information.
        
        nResetCount   = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        lpSaveButtons = (LPTBBUTTON)GlobalAlloc(GPTR, sizeof(TBBUTTON) * nResetCount);
      
        // In case the user presses reset, save the current configuration 
        // so the original toolbar can be restored.
        
        for(i = 0; i < nResetCount; i++)
        {
            SendMessage(lpTB->hdr.hwndFrom, 
                        TB_GETBUTTON, i, 
                        (LPARAM)(lpSaveButtons + i));
        }
    }
    
    return TRUE;
   
    case TBN_RESET:
    {
        LPTBNOTIFY lpTB = (LPTBNOTIFY)lparam;
        
        int nCount, i;
    
        // Remove all of the existing buttons, starting with the last one.
        
        nCount = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        
        for(i = nCount - 1; i >= 0; i--)
        {
            SendMessage(lpTB->hdr.hwndFrom, TB_DELETEBUTTON, i, 0);
        }
      
        SendMessage(lpTB->hdr.hwndFrom,      // Restore the saved buttons.
                    TB_ADDBUTTONS, 
                    (WPARAM)nResetCount, 
                    (LPARAM)lpSaveButtons);
    }
    
    return TRUE;
   
    case TBN_ENDADJUST:                // Free up the memory you allocated.
        GlobalFree((HGLOBAL)lpSaveButtons);
        
        return TRUE;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei controlli barra degli strumenti](using-toolbar-controls.md)
</dt> <dt>

[**Valori di indice delle immagini dei pulsanti standard della barra degli strumenti**](toolbar-standard-button-image-index-values.md)
</dt> <dt>

[Windows di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




