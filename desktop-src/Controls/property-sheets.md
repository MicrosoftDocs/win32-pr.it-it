---
title: Informazioni sulle finestre delle proprietà
description: Una finestra delle proprietà è una finestra che consente all'utente di visualizzare e modificare le proprietà di un elemento.
ms.assetid: 93676a64-7980-48cd-8615-23b14a118e1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241d5ed4299a0771d9f2b4df6f17929474c7f4868edf7bcaf1ade5baa7e572b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914716"
---
# <a name="about-property-sheets"></a>Informazioni sulle finestre delle proprietà

Una *finestra delle proprietà* è una finestra che consente all'utente di visualizzare e modificare le proprietà di un elemento. Ad esempio, un'applicazione foglio di calcolo può usare una finestra delle proprietà per consentire all'utente di impostare le proprietà del tipo di carattere e del bordo di una cella o per visualizzare e impostare le proprietà di un dispositivo, ad esempio un'unità disco, una stampante o un mouse.

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Nozioni di base sulla finestra delle proprietà](#property-sheet-basics)
-   [Finestre di dialogo della finestra delle proprietà](#property-sheet-dialog-boxes)
-   [Pagine](#pages)
-   [Creazione di una finestra delle proprietà](#property-sheet-creation)
-   [Aggiunta e rimozione di pagine](#adding-and-removing-pages)
-   [Titolo ed etichette di pagina della finestra delle proprietà](#property-sheet-title-and-page-labels)
-   [Attivazione della pagina](#page-activation)
-   [Pulsante ?](#help-button)
    -   [Rimozione del pulsante ? della barra del titolo](#removing-the-caption-bar-help-button)
-   [Pulsanti OK, Annulla e Applica](#ok-cancel-and-apply-buttons)
-   [Procedure guidate](#wizards)

## <a name="property-sheet-basics"></a>Nozioni di base sulla finestra delle proprietà

Per implementare le finestre delle proprietà nell'applicazione, includere il file di intestazione Prsht.h nel progetto. Prsht.h contiene tutti gli identificatori usati con le finestre delle proprietà.

Una finestra delle proprietà contiene una o più finestre figlio sovrapposte denominate pagine, ognuna delle quali contiene finestre dei controlli per l'impostazione di un gruppo di proprietà correlate. Ad esempio, una pagina può contenere i controlli per l'impostazione delle proprietà del tipo di carattere di un elemento, inclusi lo stile del tipo, le dimensioni del punto, il colore e così via. Ogni pagina ha una scheda che l'utente può selezionare per portare la pagina in primo piano nella finestra delle proprietà. Ad esempio, l'Date-Time pannello di controllo visualizza la finestra delle proprietà seguente.

![Screenshot di una finestra delle proprietà con due schede, una delle quali mostra un orologio e un controllo calendario mensile](images/propsheet1.png)

Una finestra delle proprietà standard con più pagine a schede consente all'utente di accedere in modo casuale a tutte le proprietà. Se è più appropriato impostare le proprietà in sequenza, è possibile usare una procedura [guidata](#wizards).

## <a name="property-sheet-dialog-boxes"></a>Finestre di dialogo della finestra delle proprietà

Una finestra delle proprietà e le pagine in essa contenute sono effettivamente finestre di dialogo. La finestra delle proprietà è una finestra di dialogo definita dal sistema che gestisce le pagine e fornisce un contenitore comune. Una finestra delle proprietà può essere modale o non modale. Include un frame, una barra del titolo e quattro pulsanti: **OK**, **Annulla**, **Applica** e (facoltativamente) **Guida**. Le procedure della finestra di dialogo per le pagine ricevono codici di notifica sotto forma di messaggi [**WM \_ NOTIFY**](wm-notify.md) quando l'utente fa clic sui pulsanti.

> [!NOTE]  
> Non tutte le informazioni contenute in questa sezione si applicano alle procedure guidate, che hanno un aspetto e un comportamento leggermente diversi. Ad esempio, le procedure guidate hanno un set diverso di pulsanti e nessuna scheda. Per altre informazioni, vedere [Creazione guidata](wizards.md).

Ogni pagina di una finestra delle proprietà è una finestra di dialogo non modali definita dall'applicazione che gestisce le finestre dei controlli utilizzate per visualizzare e modificare le proprietà di un elemento. Specificare il modello di finestra di dialogo utilizzato per creare ogni pagina, nonché la procedura della finestra di dialogo che gestisce i controlli e imposta le proprietà dell'elemento corrispondente.

Una finestra delle proprietà invia codici di notifica alla routine della finestra di dialogo per una pagina quando la pagina ottiene o perde l'attivazione e quando l'utente fa clic sul pulsante **OK** **,** Annulla **,** Applica o **Guida.** Le notifiche vengono inviate sotto forma di [**messaggi WM \_ NOTIFY.**](wm-notify.md) Il *parametro lParam* è l'indirizzo di una [**struttura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che include l'handle di finestra per la finestra di dialogo della finestra delle proprietà.

Alcuni codici di notifica richiedono che una pagina restituirà **TRUE** o **FALSE** in risposta al [**messaggio WM \_ NOTIFY.**](wm-notify.md) A tale scopo, la pagina deve usare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) per impostare il valore **\_ MSGRESULT DWL** per la finestra di dialogo della pagina su **TRUE** o **FALSE.**

## <a name="pages"></a>Pagine

Una finestra delle proprietà deve contenere almeno una pagina, ma non può contenere più del valore di **MAXPROPPAGES** come definito nei Windows di intestazione. Ogni pagina ha un indice in base zero assegnato dalla finestra delle proprietà in base all'ordine in cui la pagina viene aggiunta alla finestra delle proprietà. Gli indici vengono utilizzati nei messaggi inviati alla finestra delle proprietà.

Una pagina delle proprietà può contenere una finestra di dialogo annidata. In caso contrario, è necessario includere lo stile [**WS \_ EX \_ CONTROLPARENT**](/windows/desktop/winmsg/extended-window-styles) per la finestra di dialogo di primo livello e chiamare la funzione [**IsDialogMessage**](/windows/desktop/api/winuser/nf-winuser-isdialogmessagea) con l'handle per la finestra di dialogo padre. Ciò garantisce che l'utente possa usare i tasti di scelta rapida e i tasti di spostamento della finestra di dialogo per spostare lo stato attivo sui controlli nella finestra di dialogo annidata.

Ogni pagina ha un'icona e un'etichetta corrispondenti. La finestra delle proprietà crea una scheda per ogni pagina e visualizza l'icona e l'etichetta nella scheda. È previsto che tutte le pagine della finestra delle proprietà usino un tipo di carattere nonbold. Per assicurarsi che il tipo di carattere non sia in grassetto, specificare lo stile **DS \_ 3DLOOK** nel modello di finestra di dialogo.

La routine della finestra di dialogo per una pagina non deve chiamare la [**funzione EndDialog.**](/windows/desktop/api/winuser/nf-winuser-enddialog) Questa operazione elimina l'intera finestra delle proprietà, non solo la pagina.

Le dimensioni minime per una pagina della finestra delle proprietà sono 212 unità di dialogo orizzontalmente e 114 unità di dialogo verticalmente. Se una finestra di dialogo della pagina è più piccola di questa, la pagina verrà ingrandita fino a quando non soddisfa le dimensioni minime. Il file di intestazione Prsht.h contiene tre set di dimensioni consigliate per le pagine della finestra delle proprietà, come illustrato nella tabella seguente.

|  Dimensione                |   Descrizione                                                   |
|----------------------|-----------------------------------------------------------------|
| **PROP \_ SM \_ CXDLG**  | Larghezza, in unità di finestra di dialogo, di una piccola pagina della finestra delle proprietà.         |
| **PROP \_ SM \_ CYDLG**  | Altezza, in unità di finestra di dialogo, di una piccola pagina della finestra delle proprietà.        |
| **PROP \_ MED \_ CXDLG** | Larghezza, in unità di dialogo, di una pagina della finestra delle proprietà di medie dimensioni.  |
| **PROP \_ MED \_ CYDLG** | Altezza, in unità di dialogo, di una pagina della finestra delle proprietà di medie dimensioni. |
| **PROP \_ LG \_ CXDLG**  | Larghezza, in unità di finestra di dialogo, di una pagina della finestra delle proprietà di grandi dimensioni.         |
| **PROP \_ LG \_ CYDLG**  | Altezza, in unità di finestra di dialogo, di una pagina della finestra delle proprietà di grandi dimensioni.        |

L'uso di queste dimensioni consigliate consente di garantire la coerenza visiva tra l'applicazione e altre applicazioni Windows Microsoft.

Nell'editor Microsoft Visual Studio risorse è possibile creare una pagina delle dimensioni appropriate nella finestra **di dialogo** Aggiungi risorsa. Espandere il nodo Finestra di dialogo e **selezionare IDD \_ PROPPAGE \_ LARGE**, **IDD \_ PROPPAGE \_ MEDIUM** o **IDD \_ PROPPAGE \_ SMALL**.

La finestra delle proprietà viene ridimensionata automaticamente per contenere la pagina più grande.

## <a name="property-sheet-creation"></a>Creazione di una finestra delle proprietà

Prima di creare una finestra delle proprietà, è necessario definire una o più pagine. Ciò comporta il riempimento di una struttura [**PROPSHEETPAGE**](pss-propsheetpage.md) con informazioni sulla pagina( icona, etichetta, modello di finestra di dialogo, routine della finestra di dialogo e così via) e quindi specificare l'indirizzo della struttura in una chiamata alla [**funzione CreatePropertySheetPage.**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) La funzione restituisce un handle al tipo HPROPSHEETPAGE che identifica in modo univoco la pagina.

Per creare una finestra delle proprietà, specificare l'indirizzo di una [**struttura PROPSHEETHEADER**](pss-propsheetheader.md) in una chiamata alla [**funzione PropertySheet.**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) La struttura definisce l'icona e il titolo per la finestra delle proprietà e include anche l'indirizzo di una matrice di handle HPROPSHEETPAGE che si ottengono usando [**CreatePropertySheetPage.**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) Quando **PropertySheet** crea la finestra delle proprietà, include le pagine identificate nella matrice. Le pagine vengono visualizzate nella finestra delle proprietà nello stesso ordine in cui sono contenute nella matrice.

Un altro modo per assegnare pagine a una finestra delle proprietà è specificare una matrice di [**strutture PROPSHEETPAGE**](pss-propsheetpage.md) anziché una matrice di handle **HPROPSHEETPAGE.** In questo caso, [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) crea handle per le pagine prima di aggiungerli alla finestra delle proprietà.

Quando viene creata una pagina, la relativa routine della finestra di dialogo riceve un [**messaggio WM \_ INITDIALOG.**](/windows/desktop/dlgbox/wm-initdialog) Il parametro *lParam del* messaggio è un puntatore a una copia della [**struttura PROPSHEETPAGE**](pss-propsheetpage.md) definita al momento della creazione della pagina. In particolare, quando viene creata una pagina, il membro **lParam** della struttura può essere usato per passare informazioni definite dall'applicazione alla routine della finestra di dialogo. Ad eccezione del membro **lParam,** questa struttura deve essere considerata di sola lettura. La modifica di un valore diverso **da lParam** avrà conseguenze imprevedibili.

Quando il sistema passa successivamente una copia della struttura [**PROPSHEETPAGE**](pss-propsheetpage.md) della pagina all'applicazione, usa lo stesso puntatore. Tutte le modifiche alla struttura verranno passate. Poiché il **membro lParam** viene ignorato dal sistema, può essere modificato per inviare informazioni ad altre parti dell'applicazione. È ad esempio possibile usare **lParam** per passare informazioni alla funzione di callback [*PropSheetPageProc della*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) pagina.

[**PropertySheet imposta**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) automaticamente le dimensioni e la posizione iniziale di una finestra delle proprietà. La posizione è basata sulla posizione della finestra proprietaria e le dimensioni sono basate sulla pagina più grande specificata nella matrice di pagine al momento della creazione della finestra delle proprietà. Se si vuole che le pagine corrispondano alla larghezza dei quattro pulsanti nella parte inferiore della finestra delle proprietà, impostare la larghezza della pagina più ampia su 190 unità di dialogo.

Le dimensioni di una finestra delle proprietà vengono calcolate dalle proprietà *width* *e height* del modello di finestra di dialogo nel file di risorse. Per [**altri dettagli,**](/windows/desktop/menurc/dialog-resource) vedere Dialog Resource [**(Risorsa DIALOG)**](/windows/desktop/menurc/dialogex-resource) o DIALOGEX Resource (Risorsa DIALOG). Si noti, tuttavia, che per motivi di compatibilità, le dimensioni vengono calcolate in relazione al tipo di carattere MS Shell Dlg anziché al tipo di carattere usato dalla pagina. Se si progetta una pagina che usa un altro tipo di carattere, è possibile usare uno dei suggerimenti seguenti.

-   Modificare le dimensioni del modello di finestra di dialogo per compensare la differenza di dimensioni tra il tipo di carattere MS Shell Dlg e il tipo di carattere effettivamente utilizzato dalla pagina. Ad esempio, se si sceglie un tipo di carattere la cui larghezza è doppia rispetto a MS Shell Dlg, impostare la proprietà width del modello di finestra di dialogo su il doppio dell'uso normale.
-   Usare un [**modello DIALOGEX**](/windows/desktop/menurc/dialogex-resource) e impostare lo stile della finestra **di dialogo \_ SHELLFONT DS.** In tal caso, il gestore della finestra delle proprietà interpreta le dimensioni del modello di finestra di dialogo rispetto al tipo di carattere usato dal modello di finestra di dialogo.

## <a name="adding-and-removing-pages"></a>Aggiunta e rimozione di pagine

Dopo aver creato una finestra delle proprietà, un'applicazione può aggiungere una pagina alla fine del set di pagine esistente inviando un messaggio [**\_ ADDPAGE PSM.**](psm-addpage.md) Per inserire una pagina tra pagine esistenti, inviare un messaggio [**\_ InsertPage di PropSheet.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) Si noti che le dimensioni della finestra delle proprietà non possono cambiare dopo che è stata creata. Le pagine aggiunte o inserite non devono essere più grandi della pagina più grande attualmente nella finestra delle proprietà. Per rimuovere una pagina, inviare un [**messaggio \_ REMOVEPAGE PSM.**](psm-removepage.md)

Quando si definisce una pagina, è possibile specificare l'indirizzo di una funzione di callback [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) chiamata dalla finestra delle proprietà durante la creazione o la rimozione della pagina. *L'uso di PropSheetPageProc* offre la possibilità di eseguire operazioni di inizializzazione e pulizia per singole pagine.

> [!NOTE]  
> Durante la modifica dell'elenco di pagine nella finestra delle proprietà vengono eseguiti diversi messaggi e una chiamata di funzione. Durante l'esecuzione di questa azione, il tentativo di modificare l'elenco di pagine avrà risultati imprevedibili. Non aggiungere, inserire o rimuovere pagine nell'implementazione di [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka)o durante la gestione delle notifiche e dei messaggi Windows seguenti.
>
> -   [PSN \_ APPLY](psn-apply.md)
> -   [PSN \_ KILLACTIVE](psn-killactive.md)
> -   [PSN \_ RESET](psn-reset.md)
> -   [PSN \_ SETACTIVE](psn-setactive.md)
> -   [PSN \_ WIZBACK](psn-wizback.md)
> -   [PSN \_ WIZNEXT](psn-wiznext.md)
> -   [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog)
> -   [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)

Se è necessario modificare una pagina della finestra delle proprietà durante la gestione di uno di questi messaggi o mentre [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) è in esecuzione, inviare un messaggio Windows privato. L'applicazione non riceverà il messaggio fino al termine delle attività da parte del gestore della finestra delle proprietà. A questo punto sarà possibile modificare l'elenco di pagine in modo sicuro.

Quando una finestra delle proprietà viene distrutta, elimina automaticamente tutte le pagine che sono state aggiunte. Le pagine vengono distrutte in ordine inverso rispetto a quello specificato nella matrice usata per creare le pagine. Per eliminare una pagina creata dalla funzione [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) ma non aggiunta alla finestra delle proprietà, usare la [**funzione DestroyPropertySheetPage.**](/windows/desktop/api/Prsht/nf-prsht-destroypropertysheetpage)

## <a name="property-sheet-title-and-page-labels"></a>Titolo ed etichette di pagina della finestra delle proprietà

Specificare il titolo di una finestra delle proprietà nella [**struttura PROPSHEETHEADER**](pss-propsheetheader.md) usata per creare la finestra delle proprietà. Se il **membro dwFlags** include il valore **\_ PSH PROPTITLE,** la finestra delle proprietà aggiunge il suffisso "Properties" o il prefisso "Properties for", a seconda della versione. È possibile modificare il titolo dopo aver creato una finestra delle proprietà usando il [**messaggio \_ SETTITLE PSM.**](psm-settitle.md) In una procedura guidata di Questo messaggio può essere usato per modificare dinamicamente il titolo di una pagina interna.

Per impostazione predefinita, una finestra delle proprietà usa la stringa del nome specificata nel modello di finestra di dialogo come etichetta per una pagina. È possibile eseguire l'override della stringa del nome includendo il valore **\_ PSP USETITLE** nel membro **dwFlags** della [**struttura PROPSHEETPAGE**](pss-propsheetpage.md) che definisce la pagina. Quando **si specifica \_ PSP USETITLE,** il membro **pszTitle** deve contenere l'indirizzo della stringa di etichetta per la pagina.

## <a name="page-activation"></a>Attivazione della pagina

Una finestra delle proprietà può avere una sola pagina attiva alla volta. La pagina con l'attivazione si trova in primo piano dello stack di pagine sovrapposto. L'utente attiva una pagina selezionando la relativa scheda. Un'applicazione attiva una pagina usando il [**messaggio \_ SETCURSEL PSM.**](psm-setcursel.md)

La finestra delle proprietà invia il codice di notifica [ \_ KILLACTIVE psn](psn-killactive.md) alla pagina che sta per perdere l'attivazione. In risposta, la pagina deve convalidare tutte le modifiche apportate dall'utente alla pagina. Se la pagina richiede un input utente aggiuntivo prima di perdere l'attivazione, usare la [**funzione SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) per impostare il **valore \_ MSGRESULT DWL** della pagina su **TRUE.** Inoltre, la pagina deve visualizzare una finestra di messaggio che descrive il problema e fornisce l'azione consigliata. Impostare **DWL \_ MSGRESULT** su **FALSE** quando è possibile perdere l'attivazione.

Prima che la pagina che sta per ottenere l'attivazione sia visibile, la finestra delle proprietà invia il codice di notifica [ \_ PSN SETACTIVE](psn-setactive.md) alla pagina. La pagina deve rispondere inizializzando le finestre di controllo.

## <a name="help-button"></a>Pulsante ?

Le finestre delle proprietà possono visualizzare due pulsanti della Guida: un pulsante ? della finestra delle proprietà visualizzato nella parte inferiore del frame, accanto ai pulsanti **OK** Annulla Applica e un pulsante standard della barra del titolo che fornisce la Guida sensibile al /  /  contesto.

Il pulsante ? della finestra delle proprietà è facoltativo e può essere abilitato pagina per pagina. Per visualizzare il pulsante ? della finestra delle proprietà per una o più pagine:

-   Impostare il flag **\_ HASHELP PSH** nel **membro dwFlags** della struttura [**PROPSHEETHEADER**](pss-propsheetheader.md) della finestra delle proprietà.
-   Per ogni pagina che visualizza un pulsante ? , impostare il flag **\_ HASHELP PSP** nel membro **dwFlags** della struttura [**PROPSHEETPAGE della**](pss-propsheetpage.md) pagina.

Quando l'utente fa clic sul pulsante ? , la pagina attiva riceve un codice [di notifica della \_ Guida psn.](psn-help.md) La pagina deve rispondere visualizzando le informazioni della Guida, in genere chiamando la [**funzione WinHelp.**](/windows/desktop/api/winuser/nf-winuser-winhelpa)

### <a name="removing-the-caption-bar-help-button"></a>Rimozione del pulsante ? della barra del titolo

Il pulsante ? della barra del titolo viene visualizzato per impostazione predefinita, in modo che la Guida sensibile al contesto sia sempre disponibile per i pulsanti OK/Annulla/Applica. Tuttavia, questo pulsante può essere rimosso, se necessario. Per rimuovere il pulsante ? della barra del titolo di una finestra delle proprietà:

-   Per le versioni dei controlli comuni precedenti alla [versione 5.80,](common-control-versions.md)è necessario implementare una funzione [**di callback della finestra delle proprietà**](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback).
-   Per la [versione 5.80](common-control-versions.md) e successive dei controlli comuni, è sufficiente impostare il flag PSH NOCONTEXTHELP nel membro \_ **dwFlags** della struttura [**PROPSHEETHEADER**](pss-propsheetheader.md) della finestra delle proprietà. Tuttavia, se è necessaria la compatibilità con le versioni precedenti dei controlli comuni, è necessario implementare la funzione di callback .

Per implementare una funzione di callback della finestra delle proprietà che rimuove il pulsante ? della barra del titolo:

-   Impostare il flag **\_ USECALLBACK PSH** nel **membro dwFlags** della struttura [**PROPSHEETHEADER**](pss-propsheetheader.md) della finestra delle proprietà.
-   Impostare il **membro pfnCallBack** della [**struttura PROPSHEETHEADER**](pss-propsheetheader.md) in modo che punti alla funzione di callback.
-   Implementare la funzione di callback. Quando questa funzione riceve il messaggio **\_ PRECREATE PSCB,** riceve anche un puntatore al modello di finestra di dialogo della finestra delle proprietà. Rimuovere lo **stile DS \_ CONTEXTHELP** da questo modello.

L'esempio seguente illustra come implementare una funzione di callback di questo tipo:

```cpp
int CALLBACK RemoveContextHelpProc(HWND hwnd, UINT message, LPARAM lParam)
{
    switch (message) 
    {
    case PSCB_PRECREATE:
        // Remove the DS_CONTEXTHELP style from the
        // dialog box template
        if (((LPDLGTEMPLATEEX)lParam)->signature ==    
           0xFFFF)
           {
            ((LPDLGTEMPLATEEX)lParam)->style 
            &= ~DS_CONTEXTHELP;
        }
        else {
            ((LPDLGTEMPLATE)lParam)->style 
            &= ~DS_CONTEXTHELP;
        }
        return TRUE;
    }
    return TRUE;
}
```

Se la [**struttura DLGTEMPLATEEX**](/windows/desktop/dlgbox/dlgtemplateex) non è definita, includere la dichiarazione seguente:

```cpp
#include <pshpack1.h>

typedef struct DLGTEMPLATEEX
{
    WORD dlgVer;
    WORD signature;
    DWORD helpID;
    DWORD exStyle;
    DWORD style;
    WORD cDlgItems;
    short x;
    short y;
    short cx;
    short cy;
} DLGTEMPLATEEX, *LPDLGTEMPLATEEX;

#include <poppack.h>
```

## <a name="ok-cancel-and-apply-buttons"></a>Pulsanti OK, Annulla e Applica

I **pulsanti OK** e **Applica** sono simili. entrambe indirizzano le pagine di una finestra delle proprietà per convalidare e applicare le modifiche delle proprietà apportate dall'utente. L'unica differenza è che facendo clic **sul pulsante OK** la finestra delle proprietà viene distrutta dopo l'applicazione delle modifiche.

Quando l'utente fa  clic sul pulsante **OK** o Applica, la finestra delle proprietà invia una notifica [ \_ KILLACTIVE PSN](psn-killactive.md) alla pagina attiva, offrendo la possibilità di convalidare le modifiche dell'utente. Se le modifiche sono valide, la pagina deve chiamare la [**funzione SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con il **valore \_ MSGRESULT DWL** impostato su **FALSE.** Se le modifiche dell'utente non sono valide, la pagina deve impostare **DWL \_ MSGRESULT** su **TRUE** e visualizzare una finestra di dialogo che informa l'utente del problema. La pagina rimane attiva fino a quando non imposta **DWL \_ MSGRESULT** su **FALSE** in risposta a un messaggio \_ KILLACTIVE psn.

Dopo che una pagina risponde a una notifica [ \_ KILLACTIVE di PSN](psn-killactive.md) impostando **DWL \_ MSGRESULT** su **FALSE,** la finestra delle proprietà invierà una notifica [PSN \_ APPLY](psn-apply.md) a ogni pagina. Quando una pagina riceve questa notifica, deve applicare le nuove proprietà all'elemento corrispondente. Per indicare alla finestra delle proprietà che le modifiche sono valide per la pagina, chiamare [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con **DWL \_ MSGRESULT** impostato su **PSNRET \_ NOERROR.** Se le modifiche non sono valide per la pagina, restituisce un errore. In questo modo si impedisce che la finestra delle proprietà venga distrutta e lo stato attivo viene restituito alla pagina che ha ricevuto la notifica PSN APPLY o alla pagina che aveva lo stato attivo quando è stato premuto il pulsante \_ Applica.  Per restituire un errore e indicare quale pagina riceverà lo stato attivo, impostare **DWL \_ MSGRESULT** su uno dei valori seguenti.

-   **PSNRET \_ NON VALIDO.** La finestra delle proprietà non verrà distrutta e lo stato attivo verrà restituito a questa pagina.
-   **PSNRET \_ \_NOCHANGEPAGE NON VALIDO.** La finestra delle proprietà non verrà distrutta e lo stato attivo verrà restituito alla pagina che aveva lo stato attivo quando è stato premuto il pulsante.

Un'applicazione può usare [**il messaggio \_ PSM APPLY**](psm-apply.md) per simulare la selezione del **pulsante** Applica.

Il **pulsante** Applica viene inizialmente disabilitato quando una pagina diventa attiva, a indicare che non sono ancora presenti modifiche alle proprietà da applicare. Quando la pagina riceve l'input tramite uno dei relativi controlli che indica che l'utente ha modificato una proprietà, la pagina deve inviare il messaggio [**PSM \_ CHANGED**](psm-changed.md) alla finestra delle proprietà. Il messaggio fa sì che la finestra delle proprietà abiliti il **pulsante** Applica. Se successivamente l'utente  fa  clic sul pulsante Applica o Annulla, la pagina deve reinizializzare i controlli e quindi inviare il messaggio [**\_ PSM UNCHANGED**](psm-unchanged.md) per disabilitare nuovamente **il pulsante** Applica.

A volte **il pulsante** Applica fa sì che una pagina appoia una modifica a una finestra delle proprietà e la modifica non può essere annullata. In questo caso, la pagina deve inviare il [**messaggio \_ CANCELTOCLOSE del PSM**](psm-canceltoclose.md) alla finestra delle proprietà. Il messaggio fa sì che la finestra delle proprietà cambi il testo del pulsante **OK** in "Chiudi", a indicare che le modifiche applicate non possono essere annullate.

In alcuni casi una pagina apporta una modifica alla configurazione di sistema che richiede Windows riavvio del sistema o del sistema prima che la modifica venga attivata. Dopo aver apportato tale modifica, una pagina deve inviare il messaggio [**\_ RESTARTWINDOWS o**](psm-restartwindows.md) [**\_ REBOOTSYSTEM del PSM**](psm-rebootsystem.md) alla finestra delle proprietà. Questi messaggi determinano la restituzione del valore **ID \_ PSRESTARTWINDOWS** o **\_ PSREBOOTSYSTEM** da parte della funzione [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) dopo l'eliminazione della finestra delle proprietà.

Quando un utente  fa clic sul pulsante Annulla, la finestra delle proprietà invia il codice di notifica [PSN \_ RESET](psn-reset.md) a tutte le pagine, a indicare che la finestra delle proprietà sta per essere distrutta. Una pagina deve usare la notifica per eseguire operazioni di pulizia.

## <a name="wizards"></a>Procedure guidate

Una procedura guidata è un tipo speciale di finestra delle proprietà. Le procedure guidate sono progettate per presentare le pagine una alla volta in una sequenza controllata dall'applicazione. Invece di selezionare da un gruppo di pagine facendo clic su una scheda, gli utenti passano avanti e indietro nella sequenza, una pagina alla volta, facendo clic sui pulsanti. Ad esempio, la schermata seguente mostra la pagina iniziale dell'Aggiunta guidata hardware:

![Screenshot della pagina iniziale di una procedura guidata](images/wizard97.png)

Lo screenshot seguente mostra la prima pagina di una procedura guidata di Aero, il nuovo stile introdotto in Windows Vista.

![Screenshot della prima pagina di una procedura guidata di aero](images/wizardaero.png)

Per [una descrizione](wizards.md) completa delle procedure guidate, vedere Creazione guidata.
