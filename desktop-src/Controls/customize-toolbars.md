---
title: Come personalizzare le barre degli strumenti
description: La maggior parte delle applicazioni basate su Windows utilizza i controlli della barra degli strumenti per fornire agli utenti un comodo accesso alla funzionalità del programma.
ms.assetid: 0CE2988E-D887-433B-BFB2-5F3442E8E1B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091451a139cf846b1106916f28c165d6640699eb
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "104046460"
---
# <a name="how-to-customize-toolbars"></a>Come personalizzare le barre degli strumenti

La maggior parte delle applicazioni basate su Windows utilizza i controlli della barra degli strumenti per fornire agli utenti un comodo accesso alla funzionalità del programma. Tuttavia, le barre degli strumenti statiche presentano alcune carenze, ad esempio uno spazio troppo piccolo per visualizzare efficacemente tutti gli strumenti disponibili. La soluzione a questo problema consiste nel rendere le barre degli strumenti dell'applicazione personalizzabili dall'utente. Quindi, gli utenti possono scegliere di visualizzare solo gli strumenti necessari e possono organizzarli in modo da adattarli ai propri Workstyle personali.

> [!Note]  
> Non è possibile personalizzare le barre degli strumenti nelle finestre di dialogo.

 

Per abilitare la personalizzazione, includere il flag di stile controlli comuni [**\_ regolabili CCS**](common-control-styles.md) quando si crea il controllo Toolbar. Esistono due approcci di base per la personalizzazione:

-   Finestra di dialogo di personalizzazione. Questa finestra di dialogo fornita dal sistema rappresenta l'approccio più semplice. Fornisce agli utenti un'interfaccia utente grafica che consente di aggiungere, eliminare o spostare icone.
-   Trascinamento e rilascio di strumenti. L'implementazione della funzionalità di trascinamento della selezione consente agli utenti di spostare gli strumenti in un'altra posizione sulla barra degli strumenti o di eliminarli trascinandoli dalla barra degli strumenti. Fornisce agli utenti un modo rapido e semplice per organizzare la barra degli strumenti, ma non consente l'aggiunta di strumenti.

È possibile implementare entrambi gli approcci, a seconda delle esigenze dell'applicazione. Nessuno di questi due approcci alla personalizzazione fornisce un meccanismo incorporato, ad esempio un pulsante Annulla o Annulla, per ripristinare lo stato precedente della barra degli strumenti. Per archiviare lo stato di prepersonalizzazione della barra degli strumenti, è necessario usare in modo esplicito l'API del controllo Toolbar. Se necessario, è possibile utilizzare le informazioni archiviate in un secondo momento per ripristinare lo stato originale della barra degli strumenti.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="customization-dialog-box"></a>Finestra di dialogo personalizzazione

La finestra di dialogo personalizzazione viene fornita dal controllo Toolbar per offrire agli utenti un modo semplice per aggiungere, spostare o eliminare strumenti. Gli utenti possono avviarlo facendo doppio clic sulla barra degli strumenti. Le applicazioni possono avviare la finestra di dialogo di personalizzazione a livello di programmazione inviando la barra degli strumenti a un messaggio di personalizzazione [**TB \_**](tb-customize.md) .

Nella figura seguente viene illustrato un esempio della finestra di dialogo di personalizzazione della barra degli strumenti.

![Screenshot di una finestra con una barra degli strumenti a tre elementi e una finestra di dialogo con elenchi dei pulsanti disponibili e correnti della barra degli strumenti](images/tb-customdlg.png)

Gli strumenti nella casella di riepilogo a destra sono quelli attualmente presenti sulla barra degli strumenti. Inizialmente, questo elenco conterrà gli strumenti specificati quando si crea la barra degli strumenti. Nella casella di riepilogo a sinistra sono contenuti gli strumenti che è possibile aggiungere alla barra degli strumenti. L'applicazione è responsabile del popolamento dell'elenco (ad eccezione del separatore, visualizzato automaticamente).

Il controllo Toolbar informa l'applicazione che sta avviando una finestra di dialogo di personalizzazione inviando la finestra padre a un codice di notifica [TBN \_ BEGINADJUST](tbn-beginadjust.md) seguito da un codice di notifica [TBN \_ INITCUSTOMIZE](tbn-initcustomize.md) . Nella maggior parte dei casi, non è necessario che l'applicazione risponda a questi codici di notifica. Tuttavia, se non si desidera che la finestra di dialogo Personalizza barra degli strumenti visualizzi un pulsante?, gestire TBN \_ INITCUSTOMIZE restituendo TBNRF \_ HIDEHELP.

Il controllo Toolbar raccoglie quindi le informazioni necessarie per inizializzare la finestra di dialogo inviando tre serie di codici di notifica, nell'ordine seguente:

-   Un codice di notifica [ \_ QUERYINSERT TBN](tbn-queryinsert.md) per ciascun pulsante della barra degli strumenti per determinare dove possono essere inseriti i pulsanti. Restituisce **false** per impedire l'inserimento di un pulsante a sinistra del pulsante specificato nel messaggio di notifica. Se si restituisce **false** a tutti i \_ codici di notifica TBN QUERYINSERT, la finestra di dialogo non verrà visualizzata.
-   Un codice di notifica [TBN \_ QUERYDELETE](tbn-querydelete.md) per ogni strumento attualmente sulla barra degli strumenti. Restituisce **true** se è possibile eliminare uno strumento oppure **false** in caso contrario.
-   Una serie di codici di notifica [ \_ GETBUTTONINFO di TBN](tbn-getbuttoninfo.md) per popolare l'elenco dei pulsanti disponibili. Per aggiungere un pulsante all'elenco, compilare la struttura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) che viene passata con il codice di notifica e restituire **true**. Quando non sono disponibili altri strumenti da aggiungere, restituire **false**. Si noti che è possibile restituire informazioni per i pulsanti già presenti sulla barra degli strumenti. questi pulsanti non verranno aggiunti all'elenco.

Viene quindi visualizzata la finestra di dialogo e l'utente può iniziare a personalizzare la barra degli strumenti.

Quando la finestra di dialogo è aperta, l'applicazione può ricevere diversi codici di notifica, a seconda delle azioni dell'utente:

-   [TBN \_ QUERYINSERT](tbn-queryinsert.md). L'utente ha modificato il percorso di uno strumento sulla barra degli strumenti o ha aggiunto uno strumento. Restituisce **false** per impedire che lo strumento venga inserito in tale posizione.
-   [TBN \_ DELETINGBUTTON](tbn-deletingbutton.md). L'utente sta per rimuovere uno strumento dalla barra degli strumenti.
-   [TBN \_ CUSTHELP](tbn-custhelp.md). L'utente ha fatto clic sul pulsante della guida.
-   [TBN \_ TOOLBARCHANGE](tbn-toolbarchange.md). L'utente ha aggiunto, spostato o eliminato uno strumento.
-   [TBN \_ Reimpostazione](tbn-reset.md). L'utente ha fatto clic sul pulsante Reimposta.

Dopo che la finestra di dialogo viene distrutta, l'applicazione riceverà un codice di notifica [ \_ ENDADJUST TBN](tbn-endadjust.md) .

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



### <a name="dragging-and-dropping-tools"></a>Trascinamento e rilascio di strumenti

Gli utenti possono anche ridisporre i pulsanti di una barra degli strumenti premendo il tasto MAIUSC e trascinando il pulsante in un'altra posizione. Il processo di trascinamento della selezione viene gestito automaticamente dal controllo Toolbar. Viene visualizzata un'immagine fantasma del pulsante mentre viene trascinata e la barra degli strumenti viene riordinata dopo l'eliminazione. Gli utenti non possono aggiungere pulsanti in questo modo, ma possono eliminare un pulsante rilasciandolo dalla barra degli strumenti.

Sebbene il controllo Toolbar normalmente esegue questa operazione automaticamente, invia anche l'applicazione due codici di notifica: [TBN \_ QUERYDELETE](tbn-querydelete.md) e [TBN \_ QUERYINSERT](tbn-queryinsert.md). Per controllare il processo di trascinamento della selezione, gestire questi codici di notifica come segue:

-   Il codice di notifica [ \_ QUERYDELETE di TBN](tbn-querydelete.md) viene inviato non appena l'utente tenta di spostare il pulsante, prima che il pulsante fantasma venga visualizzato. Restituisce **false** per impedire lo spostamento del pulsante. Se si restituisce **true**, l'utente potrà spostare lo strumento o eliminarlo lasciandolo fuori dalla barra degli strumenti. Se è possibile spostare uno strumento, è possibile eliminarlo. Tuttavia, se l'utente elimina uno strumento, il controllo Toolbar invierà all'applicazione un codice di notifica [TBN \_ DELETINGBUTTON](tbn-deletingbutton.md) . a questo punto è possibile scegliere di reinserire il pulsante nella posizione originale, annullando quindi l'eliminazione.
-   Il codice di notifica [ \_ QUERYINSERT di TBN](tbn-queryinsert.md) viene inviato quando l'utente tenta di rilasciare il pulsante sulla barra degli strumenti. Per evitare che il pulsante spostato da un pulsante a sinistra del pulsante specificato nella notifica restituisca **false**. Questo codice di notifica non viene inviato se l'utente rilascia lo strumento dalla barra degli strumenti.

Se l'utente tenta di trascinare un pulsante senza premere anche il tasto MAIUSC, il controllo Toolbar non gestirà l'operazione di trascinamento della selezione. Tuttavia, invierà all'applicazione un codice di notifica [ \_ BEGINDRAG TBN](tbn-begindrag.md) per indicare l'inizio di un'operazione di trascinamento e un codice di notifica [TBN \_ ENDDRAG](tbn-enddrag.md) per indicare la fine. Se si vuole abilitare questa forma di trascinamento della selezione, l'applicazione deve gestire questi codici di notifica, fornire l'interfaccia utente necessaria e modificare la barra degli strumenti per riflettere le modifiche.

### <a name="saving-and-restoring-toolbars"></a>Salvataggio e ripristino delle barre degli strumenti

Nel processo di personalizzazione di una barra degli strumenti, è possibile che l'applicazione debba salvare le informazioni in modo da ripristinare lo stato originale della barra degli strumenti. Per avviare il salvataggio o il ripristino dello stato di una barra degli strumenti, inviare il controllo Toolbar a [**TB \_ SAVERESTORE**](tb-saverestore.md) messaggio con *lParam* impostato su **true**. Il valore *lParam* di questo messaggio specifica se si richiede un'operazione di salvataggio o di ripristino. Una volta inviato il messaggio, esistono due modi per gestire l'operazione di salvataggio/ripristino:

-   Con i controlli comuni [versione 4,72](common-control-versions.md) e precedenti, è necessario implementare un gestore [ \_ GETBUTTONINFO TBN](tbn-getbuttoninfo.md) . Il controllo Toolbar invia questo codice di notifica per richiedere informazioni su ogni pulsante mentre viene ripristinato.
-   La versione 5,80 include un'opzione Salva/Ripristina. All'inizio del processo, quando ogni pulsante viene salvato o ripristinato, l'applicazione riceverà un codice di notifica [TBN \_ Save](tbn-save.md) o [TBN \_ Restore](tbn-restore.md) . Per utilizzare questa opzione, è necessario implementare i gestori delle notifiche per fornire le informazioni sulla bitmap e sullo stato necessarie per salvare o ripristinare lo stato della barra degli strumenti.

Gli Stati della barra degli strumenti vengono salvati in un flusso di dati costituito da blocchi di dati definiti dalla shell in alternanza con blocchi di dati definiti dall'applicazione. Un blocco di dati di ogni tipo viene archiviato per ciascun pulsante, insieme a un blocco facoltativo di dati globali che le applicazioni possono inserire all'inizio del flusso. Durante il processo di salvataggio, il gestore di [ \_ salvataggio TBN](tbn-save.md) aggiunge i blocchi definiti dall'applicazione al flusso di dati. Durante il processo di ripristino, il gestore di [ \_ ripristino TBN](tbn-restore.md) legge ogni blocco e fornisce alla shell le informazioni necessarie per ricostruire la barra degli strumenti.

### <a name="how-to-handle-a-tbn_save-notification"></a>Come gestire una notifica di \_ salvataggio TBN

Il primo codice di notifica di [ \_ salvataggio TBN](tbn-save.md) viene inviato all'inizio del processo di salvataggio. Prima di salvare i pulsanti, i membri della struttura [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) vengono impostati come illustrato nella tabella seguente.



| Membro       | Impostazione                                                                                                                                                                                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **iItem**    | –1                                                                                                                                                                                                                                                                                                                                                 |
| **cbData**   | Quantità di memoria necessaria per i dati definiti dalla Shell.                                                                                                                                                                                                                                                                                                |
| **cButtons** | Numero di pulsanti.                                                                                                                                                                                                                                                                                                                             |
| **pData**    | Quantità calcolata di memoria necessaria per i dati definiti dall'applicazione. Si includono in genere alcuni dati globali, oltre ai dati per ogni pulsante. Aggiungere tale valore a **cbData** e allocare memoria sufficiente a **pData** per contenerlo.                                                                                                                      |
| **pCurrent** | Primo byte non usato nel flusso di dati. Se non sono necessarie informazioni sulla barra degli strumenti globali, impostare **pCurrent**  =  **pData** in modo che punti all'inizio del flusso di dati. Se sono necessarie informazioni sulla barra degli strumenti globali, archiviarle in **pData**, quindi impostare **pCurrent** sull'inizio della parte inutilizzata del flusso di dati prima di restituire. |



 

Se si desidera aggiungere informazioni sulla barra degli strumenti globali, posizionarlo all'inizio del flusso di dati. Avanzare **pCurrent** alla fine dei dati globali in modo che punti all'inizio della parte inutilizzata del flusso di dati e restituisca.

Una volta restituito, la shell inizia a salvare le informazioni sul pulsante. Aggiunge i dati definiti dalla Shell per il primo pulsante in **pCurrent** , quindi sposta **pCurrent** all'inizio della parte inutilizzata.

Dopo aver salvato ciascun pulsante, viene inviato un codice di notifica di [ \_ salvataggio TBN](tbn-save.md) e viene restituito [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) con questi membri impostati come indicato di seguito.



| Membro                       | Impostazione                                                                                                                                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **iItem**                    | Indice in base zero del numero del pulsante.                                                                                                                                                                                                                           |
| **pCurrent**                 | Puntatore al primo byte non usato nel flusso di dati. Se si desidera archiviare informazioni aggiuntive sul pulsante, archiviarle nella posizione a cui punta **pCurrent** e aggiornare **pCurrent** in modo da puntare alla prima parte non utilizzata del flusso di dati. |
| [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) | Struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) che descrive il pulsante salvato.                                                                                                                                                                              |



 

Quando si riceve il codice di notifica, è necessario estrarre tutte le informazioni specifiche del pulsante necessarie da [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton). Tenere presente che quando si aggiunge un pulsante, è possibile usare il membro **dwData** di **TBBUTTON** per conservare i dati specifici dell'applicazione. Caricare i dati nel flusso di dati in **pCurrent**. Avanzare **pCurrent** alla fine dei dati, puntando nuovamente all'inizio della parte inutilizzata del flusso e restituire.

La shell passa quindi al pulsante Avanti, aggiunge le informazioni a **pData**, sposta **PCurrent**, carica [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)e invia un altro codice di notifica di [ \_ salvataggio TBN](tbn-save.md) . Questo processo continua fino a quando non vengono salvati tutti i pulsanti.

### <a name="restoring-saved-toolbars"></a>Ripristino delle barre degli strumenti salvate

Il processo di ripristino Annulla fondamentalmente il processo di salvataggio. All'inizio, l'applicazione riceverà un codice di notifica del [ \_ ripristino TBN](tbn-restore.md) con il membro **iItem** della struttura [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) impostato su-1. Il membro **cbData** è impostato sulla dimensione di **pData** e **cButtons** è impostato sul numero di pulsanti.

Il gestore delle notifiche deve estrarre le informazioni globali inserite all'inizio di **pData** durante il salvataggio e avanzare **pCurrent** all'inizio del primo blocco di dati definiti dalla Shell. Impostare **cBytesPerRecord** sulla dimensione dei blocchi di dati usati per salvare i dati dei pulsanti. Impostare **cButtons** sul numero di pulsanti e restituire.

Il [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) successivo è per il primo pulsante. Il membro **pCurrent** punta all'inizio del primo blocco di dati dei pulsanti e **iItem** è impostato sull'indice del pulsante. Estrarre i dati e avanzare **pCurrent**. Caricare i dati in [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)e restituire. Per omettere un pulsante dalla barra degli strumenti ripristinata, impostare il membro **idCommand** di **TBBUTTON** su zero. La shell ripete il processo per i pulsanti rimanenti. Oltre ai messaggi [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) e **NMTBRESTORE** , è inoltre possibile utilizzare messaggi quali [TBN \_ Reset](tbn-reset.md) per salvare e ripristinare una barra degli strumenti.

Nell'esempio di codice seguente viene salvata una barra degli strumenti prima che venga personalizzata e viene ripristinata se l'applicazione riceve un messaggio di [ \_ reimpostazione TBN](tbn-reset.md) .


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

[Utilizzo di controlli Toolbar](using-toolbar-controls.md)
</dt> <dt>

[**Valori di indice dell'immagine del pulsante standard della barra degli strumenti**](toolbar-standard-button-image-index-values.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




