---
title: Informazioni sulle finestre delle proprietà
description: Una finestra delle proprietà è una finestra che consente all'utente di visualizzare e modificare le proprietà di un elemento.
ms.assetid: 93676a64-7980-48cd-8615-23b14a118e1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3256959b588e2109740033692c0c528889fc939f
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2021
ms.locfileid: "106323860"
---
# <a name="about-property-sheets"></a>Informazioni sulle finestre delle proprietà

Una finestra delle *Proprietà* è una finestra che consente all'utente di visualizzare e modificare le proprietà di un elemento. Ad esempio, un'applicazione per fogli di calcolo può utilizzare una finestra delle proprietà per consentire all'utente di impostare le proprietà relative al tipo di carattere e al bordo di una cella o di visualizzare e impostare le proprietà di un dispositivo, ad esempio un'unità disco, una stampante o un mouse.

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Nozioni fondamentali sulla finestra delle proprietà](#property-sheet-basics)
-   [Finestre di dialogo della finestra delle proprietà](#property-sheet-dialog-boxes)
-   [Pagine](#pages)
-   [Creazione della finestra delle proprietà](#property-sheet-creation)
-   [Aggiunta e rimozione di pagine](#adding-and-removing-pages)
-   [Titolo della finestra delle proprietà e etichette di pagina](#property-sheet-title-and-page-labels)
-   [Attivazione pagina](#page-activation)
-   [Pulsante della Guida](#help-button)
    -   [Rimozione del pulsante Guida della barra del titolo](#removing-the-caption-bar-help-button)
-   [Pulsanti OK, Annulla e applica](#ok-cancel-and-apply-buttons)
-   [Procedure guidate](#wizards)

## <a name="property-sheet-basics"></a>Nozioni fondamentali sulla finestra delle proprietà

Per implementare le finestre delle proprietà nell'applicazione, includere il file di intestazione Prsht. h nel progetto. Prsht. h contiene tutti gli identificatori utilizzati con le finestre delle proprietà.

Una finestra delle proprietà contiene una o più finestre figlio sovrapposte denominate pagine, ognuna delle quali contiene finestre di controllo per l'impostazione di un gruppo di proprietà correlate. Ad esempio, una pagina può contenere i controlli per l'impostazione delle proprietà del tipo di carattere di un elemento, inclusi lo stile del tipo, la dimensione del punto, il colore e così via. Ogni pagina contiene una scheda che l'utente può selezionare per portare la pagina in primo piano della finestra delle proprietà. Ad esempio, l'applicazione del pannello di controllo Date-Time Visualizza la finestra delle proprietà seguente.

![Screenshot di una finestra delle proprietà con due schede, una delle quali Mostra un orologio e un controllo calendario mensile](images/propsheet1.png)

Una finestra delle proprietà standard con più pagine a schede consente all'utente di accedere a tutte le proprietà in modo casuale. Se è più appropriato avere le proprietà impostate in sequenza, è possibile usare una [procedura guidata](#wizards).

## <a name="property-sheet-dialog-boxes"></a>Finestre di dialogo della finestra delle proprietà

Una finestra delle proprietà e le pagine in essa contenute sono in effetti finestre di dialogo. La finestra delle proprietà è una finestra di dialogo definita dal sistema che gestisce le pagine e fornisce un contenitore comune. Una finestra di dialogo della finestra delle proprietà può essere modale o non modale. Include un frame, una barra del titolo e quattro pulsanti: **OK**, **Annulla**, **applica** e (facoltativamente) la **Guida**. Le procedure della finestra di dialogo per le pagine ricevono i codici di notifica sotto forma di [**WM \_ Notify**](wm-notify.md) quando l'utente fa clic sui pulsanti.

> [!NOTE]  
> Non tutte le informazioni contenute in questa sezione si applicano alle procedure guidate, che hanno un aspetto e un comportamento leggermente diversi. Ad esempio, le procedure guidate hanno un set di pulsanti diverso e nessuna tabulazione. Per ulteriori informazioni, vedere [creazione di procedure guidate](wizards.md).

Ogni pagina in una finestra delle proprietà è una finestra di dialogo non modale definita dall'applicazione che gestisce le finestre di controllo usate per visualizzare e modificare le proprietà di un elemento. Viene fornito il modello della finestra di dialogo utilizzato per creare ogni pagina, nonché la routine della finestra di dialogo che gestisce i controlli e imposta le proprietà dell'elemento corrispondente.

Una finestra delle proprietà Invia i codici di notifica alla routine della finestra di dialogo per una pagina quando la pagina sta ottenendo o perde l'attivazione e quando l'utente fa clic sul pulsante **OK**, **Annulla**, **applica** o **Guida** . Le notifiche vengono inviate sotto forma di messaggi [**di \_ notifica WM**](wm-notify.md) . Il parametro *lParam* è l'indirizzo di una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che include l'handle della finestra alla finestra delle proprietà.

Alcuni codici di notifica richiedono una pagina per restituire **true** o **false** in risposta al messaggio [**di \_ notifica WM**](wm-notify.md) . A tale scopo, la pagina deve usare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) per impostare il valore di **\_ MSGRESULT DWL** per la finestra di dialogo della pagina su **true** o **false**.

## <a name="pages"></a>Pagine

Una finestra delle proprietà deve contenere almeno una pagina, ma non può contenere più del valore di **MAXPROPPAGES** , come definito nei file di intestazione di Windows. Ogni pagina dispone di un indice in base zero a cui viene assegnata la finestra delle proprietà in base all'ordine in cui la pagina viene aggiunta alla finestra delle proprietà. Gli indici vengono utilizzati nei messaggi inviati alla finestra delle proprietà.

Una pagina delle proprietà può contenere una finestra di dialogo nidificata. In tal caso, è necessario includere lo stile [**WS \_ ex \_ CONTROLPARENT**](/windows/desktop/winmsg/extended-window-styles) per la finestra di dialogo di primo livello e chiamare la funzione [**IsDialogMessage**](/windows/desktop/api/winuser/nf-winuser-isdialogmessagea) con l'handle per la finestra di dialogo padre. In questo modo, l'utente può utilizzare i tasti di scelta e i tasti di spostamento della finestra di dialogo per spostare lo stato attivo sui controlli nella finestra di dialogo nidificata.

Ogni pagina presenta un'icona e un'etichetta corrispondenti. La finestra delle proprietà crea una scheda per ogni pagina e visualizza l'icona e l'etichetta nella scheda. Per tutte le pagine della finestra delle proprietà si prevede di utilizzare un tipo di carattere non grassetto. Per assicurarsi che il tipo di carattere non sia in grassetto, specificare lo stile **DS \_ 3DLOOK** nel modello della finestra di dialogo.

La routine della finestra di dialogo per una pagina non deve chiamare la funzione [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) . Questa operazione eliminerà l'intera finestra delle proprietà, non solo la pagina.

Le dimensioni minime per una pagina della finestra delle proprietà sono le unità di dialogo 212 orizzontalmente e 114 in verticale. Se una finestra di dialogo della pagina è inferiore a questa, la pagina verrà ingrandita fino a quando non sarà conforme alla dimensione minima. Il file di intestazione Prsht. h contiene tre set di dimensioni consigliate per le pagine della finestra delle proprietà, come illustrato nella tabella seguente.

|  Dimensione                |   Descrizione                                                   |
|----------------------|-----------------------------------------------------------------|
| **PROP \_ SM \_ CXDLG**  | Larghezza, in unità di dialogo, di una pagina della finestra delle proprietà piccola.         |
| **PROP \_ SM \_ CYDLG**  | Altezza, in unità di dialogo, di una pagina della finestra delle proprietà piccola.        |
| **PROP \_ Med \_ CXDLG** | Larghezza, in unità di dialogo, di una pagina della finestra delle proprietà di medie dimensioni.  |
| **PROP \_ Med \_ CYDLG** | Altezza, in unità di dialogo, di una pagina della finestra delle proprietà di medie dimensioni. |
| **PROP \_ LG \_ CXDLG**  | Larghezza, in unità di dialogo, di una pagina della finestra delle proprietà di grandi dimensioni.         |
| **PROP \_ LG \_ CYDLG**  | Altezza, in unità di dialogo, di una pagina della finestra delle proprietà di grandi dimensioni.        |

L'utilizzo di queste dimensioni consigliate consente di garantire la coerenza visiva tra l'applicazione e altre applicazioni Microsoft Windows.

In Microsoft Visual Studio editor risorse è possibile creare una pagina con le dimensioni appropriate nella finestra di dialogo **Aggiungi risorsa** . Espandere il nodo della finestra di dialogo e selezionare **IDD di \_ \_ grandi dimensioni**, il **\_ \_ supporto** per le pagine IDD o **IDD \_ \_**.

La finestra delle proprietà viene ridimensionata automaticamente per adattarsi alla pagina più grande.

## <a name="property-sheet-creation"></a>Creazione della finestra delle proprietà

Prima di creare una finestra delle proprietà, è necessario definire una o più pagine. Ciò implica la compilazione di una struttura [**PROPSHEETPAGE**](pss-propsheetpage.md) con le informazioni sulla pagina, la relativa icona, l'etichetta, il modello di finestra di dialogo, la procedura della finestra di dialogo e così via, quindi specificando l'indirizzo della struttura in una chiamata alla funzione [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) . La funzione restituisce un handle al tipo HPROPSHEETPAGE che identifica in modo univoco la pagina.

Per creare una finestra delle proprietà, è necessario specificare l'indirizzo di una struttura [**PROPSHEETHEADER**](pss-propsheetheader.md) in una chiamata alla funzione [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) . La struttura definisce l'icona e il titolo per la finestra delle proprietà e include anche l'indirizzo di una matrice di handle HPROPSHEETPAGE ottenuti usando [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea). Quando **PropertySheet** crea la finestra delle proprietà, include le pagine identificate nella matrice. Le pagine vengono visualizzate nella finestra delle proprietà nello stesso ordine in cui sono contenute nella matrice.

Un altro modo per assegnare le pagine a una finestra delle proprietà è specificare una matrice di strutture [**PROPSHEETPAGE**](pss-propsheetpage.md) anziché una matrice di handle **HPROPSHEETPAGE** . In questo caso, [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) crea handle per le pagine prima di aggiungerli alla finestra delle proprietà.

Quando viene creata una pagina, la relativa routine della finestra di dialogo riceve un messaggio [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) . Il parametro *lParam* del messaggio è un puntatore a una copia della struttura [**PROPSHEETPAGE**](pss-propsheetpage.md) definita al momento della creazione della pagina. In particolare, quando viene creata una pagina, il membro **lParam** della struttura può essere utilizzato per passare informazioni definite dall'applicazione alla routine della finestra di dialogo. Fatta eccezione per il membro **lParam** , questa struttura deve essere trattata come di sola lettura. La modifica di un valore diverso da **lParam** avrà conseguenze imprevedibili.

Quando il sistema passa successivamente una copia della struttura [**PROPSHEETPAGE**](pss-propsheetpage.md) della pagina all'applicazione, USA lo stesso puntatore. Tutte le modifiche apportate alla struttura verranno passate insieme. Poiché il membro **lParam** viene ignorato dal sistema, può essere modificato per inviare informazioni ad altre parti dell'applicazione. È possibile, ad esempio, usare **lParam** per passare informazioni alla funzione di callback [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) della pagina.

[**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) imposta automaticamente le dimensioni e la posizione iniziale di una finestra delle proprietà. La posizione è basata sulla posizione della finestra proprietaria e le dimensioni sono basate sulla pagina più grande specificata nella matrice di pagine al momento della creazione della finestra delle proprietà. Se si desidera che le pagine corrispondano alla larghezza dei quattro pulsanti nella parte inferiore della finestra delle proprietà, impostare la larghezza della pagina più ampia su 190 unità di dialogo.

Le dimensioni di una finestra delle proprietà vengono calcolate dalle proprietà *Width* e *Height* del modello di finestra di dialogo nel file di risorse. Per ulteriori informazioni, vedere [**risorsa finestra di dialogo**](/windows/desktop/menurc/dialog-resource) o [**risorsa DIALOGEX**](/windows/desktop/menurc/dialogex-resource) . Si noti, tuttavia, che, per motivi di compatibilità, le dimensioni vengono calcolate rispetto al tipo di carattere MS Shell Dlg anziché al tipo di carattere utilizzato dalla pagina. Se si progetta una pagina che usa un altro tipo di carattere, è possibile usare uno dei suggerimenti seguenti.

-   Modificare le dimensioni del modello di finestra di dialogo per compensare la differenza di dimensione tra il tipo di carattere MS Shell Dlg e il tipo di carattere effettivamente utilizzato nella pagina. Se, ad esempio, si sceglie un tipo di carattere che è il doppio della larghezza di MS Shell Dlg, impostare la proprietà Width del modello di finestra di dialogo sul doppio utilizzo normale.
-   Usare un modello [**DIALOGEX**](/windows/desktop/menurc/dialogex-resource) e impostare lo stile della finestra di dialogo **DS \_ SHELLFONT** . In tal caso, il gestore della finestra delle proprietà interpreta le dimensioni del modello di finestra di dialogo relative al tipo di carattere utilizzato dal modello di finestra di dialogo.

## <a name="adding-and-removing-pages"></a>Aggiunta e rimozione di pagine

Dopo la creazione di una finestra delle proprietà, un'applicazione può aggiungere una pagina alla fine del set di pagine esistente inviando un messaggio [**\_ ADDPAGE di PSM**](psm-addpage.md) . Per inserire una pagina tra le pagine esistenti, inviare un messaggio [**PropSheet \_ InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) . Si noti che le dimensioni della finestra delle proprietà non possono essere modificate dopo la creazione. Le pagine aggiunte o inserite non devono essere più grandi della pagina più grande attualmente nella finestra delle proprietà. Per rimuovere una pagina, inviare un messaggio [**PSM \_ REMOVEPAGE**](psm-removepage.md) .

Quando si definisce una pagina, è possibile specificare l'indirizzo di una funzione di callback [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) chiamata dalla finestra delle proprietà durante la creazione o la rimozione della pagina. L'uso di *PropSheetPageProc* offre la possibilità di eseguire operazioni di inizializzazione e pulizia per le singole pagine.

> [!NOTE]  
> Un numero di messaggi e una chiamata di funzione si verificano durante la modifica dell'elenco di pagine da parte della finestra delle proprietà. Durante l'esecuzione di questa azione, il tentativo di modificare l'elenco di pagine avrà risultati imprevedibili. Non aggiungere, inserire o rimuovere pagine nell'implementazione di [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka)o quando si gestiscono le notifiche e i messaggi di Windows seguenti.
>
> -   [\_applica PSN](psn-apply.md)
> -   [\_KILLACTIVE PSN](psn-killactive.md)
> -   [ripristino di PSN \_](psn-reset.md)
> -   [seactive PSN \_](psn-setactive.md)
> -   [\_WIZBACK PSN](psn-wizback.md)
> -   [\_WIZNEXT PSN](psn-wiznext.md)
> -   [**\_INITDIALOG WM**](/windows/desktop/dlgbox/wm-initdialog)
> -   [**eliminazione di WM \_**](/windows/desktop/winmsg/wm-destroy)

Se si verifica la necessità di modificare una pagina della finestra delle proprietà mentre si gestisce uno di questi messaggi o mentre [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) è in esecuzione, pubblicare un messaggio di Windows privato. L'applicazione non riceverà il messaggio fino al termine delle attività da parte del gestore della finestra delle proprietà. in questo modo sarà possibile modificare l'elenco delle pagine in modo sicuro.

Quando una finestra delle proprietà viene distrutta, Elimina automaticamente tutte le pagine che sono state aggiunte. Le pagine vengono eliminate in ordine inverso rispetto a quello specificato nella matrice usata per creare le pagine. Per eliminare definitivamente una pagina creata dalla funzione [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) ma che non è stata aggiunta alla finestra delle proprietà, usare la funzione [**DestroyPropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-destroypropertysheetpage) .

## <a name="property-sheet-title-and-page-labels"></a>Titolo della finestra delle proprietà e etichette di pagina

È possibile specificare il titolo di una finestra delle proprietà nella struttura [**PROPSHEETHEADER**](pss-propsheetheader.md) usata per creare la finestra delle proprietà. Se il membro **dwFlags** include il **valore \_ PROPTITLE di PSH** , nella finestra delle proprietà viene aggiunto il suffisso "Properties" o il prefisso "Properties for", a seconda della versione. È possibile modificare il titolo dopo la creazione di una finestra delle proprietà usando il messaggio di proprietà [**PSM \_**](psm-settitle.md) . In una procedura guidata Aero questo messaggio può essere usato per modificare dinamicamente il titolo di una pagina interna.

Per impostazione predefinita, una finestra delle proprietà utilizza la stringa del nome specificata nel modello della finestra di dialogo come etichetta per una pagina. È possibile eseguire l'override della stringa del nome includendo il valore **\_ USETITLE di PSP** nel membro **dwFlags** della struttura [**PROPSHEETPAGE**](pss-propsheetpage.md) che definisce la pagina. Quando si specifica **PSP \_ USETITLE** , il membro **pszTitle** deve contenere l'indirizzo della stringa di etichetta per la pagina.

## <a name="page-activation"></a>Attivazione pagina

Una finestra delle proprietà può avere una sola pagina attiva alla volta. La pagina con l'attivazione è in primo piano dello stack di pagine sovrapposto. L'utente attiva una pagina selezionando la relativa scheda; un'applicazione attiva una pagina usando il messaggio di [**errore \_ PSM**](psm-setcursel.md) .

La finestra delle proprietà Invia il codice di notifica [ \_ KILLACTIVE PSN](psn-killactive.md) alla pagina che sta per perdere l'attivazione. In risposta, la pagina deve convalidare tutte le modifiche apportate dall'utente alla pagina. Se la pagina richiede un input utente aggiuntivo prima di perdere l'attivazione, utilizzare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) per impostare il valore **\_ MSGRESULT di DWL** della pagina su **true**. Inoltre, nella pagina deve essere visualizzata una finestra di messaggio che descrive il problema e fornisce l'azione consigliata. Impostare **DWL \_ MSGRESULT** su **false** quando è accettabile perdere l'attivazione.

Prima che la pagina che sta ottenendo l'attivazione sia visibile, la finestra delle proprietà Invia il codice di notifica [ \_ seattivo PSN](psn-setactive.md) alla pagina. La pagina deve rispondere inizializzando le finestre di controllo.

## <a name="help-button"></a>Pulsante della Guida

Le finestre delle proprietà possono visualizzare due pulsanti della guida: un pulsante della guida della finestra delle proprietà visualizzato nella parte inferiore del frame, accanto ai pulsanti **OK** / **Annulla** / **applicazione** e un pulsante barra del titolo standard che fornisce la Guida sensibile al contesto.

Il pulsante della guida della finestra delle proprietà è facoltativo e può essere abilitato in una pagina in base alla pagina. Per visualizzare il pulsante della guida della finestra delle proprietà per una o più pagine:

-   Impostare il flag **PSH \_ HasHelp** nel membro **dwFlags** della struttura [**PROPSHEETHEADER**](pss-propsheetheader.md) della finestra delle proprietà.
-   Per ogni pagina in cui viene visualizzato un pulsante della guida, impostare il flag **\_ HasHelp PSP** nel membro **dwFlags** della struttura [**PROPSHEETPAGE**](pss-propsheetpage.md) della pagina.

Quando l'utente fa clic sul pulsante?, la pagina attiva riceve un codice di notifica della [ \_ Guida di PSN](psn-help.md) . La pagina deve rispondere visualizzando le informazioni della guida, in genere chiamando la funzione [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) .

### <a name="removing-the-caption-bar-help-button"></a>Rimozione del pulsante Guida della barra del titolo

Il pulsante della guida della barra del titolo viene visualizzato per impostazione predefinita, in modo che la Guida sensibile al contesto sia sempre disponibile per i pulsanti OK/Annulla/Applica. Questo pulsante, tuttavia, può essere rimosso, se necessario. Per rimuovere il pulsante della guida della barra del titolo della finestra delle proprietà:

-   Per le versioni dei controlli comuni precedenti alla [versione 5,80](common-control-versions.md), è necessario implementare una [**funzione di callback della finestra delle proprietà**](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback).
-   Per la [versione 5,80](common-control-versions.md) e successive dei controlli comuni, è possibile impostare semplicemente il \_ flag PSH NOCONTEXTHELP nel membro **dwFlags** della struttura [**PROPSHEETHEADER**](pss-propsheetheader.md) della finestra delle proprietà. Tuttavia, se è necessaria la compatibilità con le versioni precedenti dei controlli comuni, è necessario implementare la funzione di callback.

Per implementare una funzione di callback della finestra delle proprietà che rimuove il pulsante della guida della barra del titolo:

-   Impostare il flag **PSH \_ USECALLBACK** nel membro **dwFlags** della struttura [**PROPSHEETHEADER**](pss-propsheetheader.md) della finestra delle proprietà.
-   Impostare il membro **pfnCallBack** della struttura [**PROPSHEETHEADER**](pss-propsheetheader.md) in modo che punti alla funzione di callback.
-   Implementare la funzione di callback. Quando questa funzione riceve il messaggio di **\_ precreazione PSCB** , riceve anche un puntatore al modello della finestra di dialogo della finestra delle proprietà. Rimuovere lo stile **DS \_ CONTEXTHELP** da questo modello.

Nell'esempio seguente viene illustrato come implementare una funzione di callback di questo tipo:

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

Se la struttura [**DLGTEMPLATEEX**](/windows/desktop/dlgbox/dlgtemplateex) non è definita, includere la dichiarazione seguente:

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

## <a name="ok-cancel-and-apply-buttons"></a>Pulsanti OK, Annulla e applica

I pulsanti **OK** e **applica** sono simili; entrambi indirizzano le pagine di una finestra delle proprietà per convalidare e applicare le modifiche delle proprietà apportate dall'utente. L'unica differenza consiste nel fatto che facendo clic sul pulsante **OK** la finestra delle proprietà viene eliminata definitivamente dopo l'applicazione delle modifiche.

Quando l'utente fa clic sul pulsante **OK** o **applica** , la finestra delle proprietà Invia una notifica [ \_ KILLACTIVE PSN](psn-killactive.md) alla pagina attiva, offrendo la possibilità di convalidare le modifiche apportate dall'utente. Se le modifiche sono valide, è necessario che la pagina chiami la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con il valore **DWL \_ MSGRESULT** impostato su **false**. Se le modifiche apportate dall'utente non sono valide, la pagina deve impostare **DWL \_ MSGRESULT** su **true** e visualizzare una finestra di dialogo che informa l'utente del problema. La pagina rimane attiva fino a quando non imposta **DWL \_ MSGRESULT** su **false** in risposta a un \_ messaggio KILLACTIVE PSN.

Dopo che una pagina risponde a una notifica di [ \_ KILLACTIVE PSN](psn-killactive.md) impostando **DWL \_ MSGRESULT** su **false**, la finestra delle proprietà invierà una notifica di [ \_ applicazione di PSN](psn-apply.md) a ogni pagina. Quando una pagina riceve la notifica, deve applicare le nuove proprietà all'elemento corrispondente. Per indicare alla finestra delle proprietà che le modifiche sono valide per la pagina, chiamare [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con **DWL \_ MSGRESULT** impostato su **PSNRET \_ NOERROR**. Se le modifiche non sono valide per la pagina, viene restituito un errore. In questo modo si impedisce l'eliminazione della finestra delle proprietà e viene restituito lo stato attivo alla pagina che ha ricevuto la notifica di applicazione di PSN \_ o alla pagina con lo stato attivo quando è stato premuto il pulsante **applica** . Per restituire un errore e indicare la pagina che riceve lo stato attivo, impostare **DWL \_ MSGRESULT** su uno dei valori seguenti.

-   **PSNRET \_ NON valido**. La finestra delle proprietà non verrà eliminata definitivamente e lo stato attivo verrà restituito a questa pagina.
-   **PSNRET \_ \_NOCHANGEPAGE non valido**. La finestra delle proprietà non verrà eliminata definitivamente e lo stato attivo verrà restituito alla pagina con lo stato attivo quando è stato premuto il pulsante.

Un'applicazione può usare il messaggio [**PSM \_ Apply**](psm-apply.md) per simulare la selezione del pulsante **applica** .

Il pulsante **applica** viene inizialmente disabilitato quando una pagina diventa attiva, a indicare che non sono ancora presenti modifiche di proprietà da applicare. Quando la pagina riceve l'input tramite uno dei relativi controlli che indica che l'utente ha modificato una proprietà, è necessario che la pagina invii il messaggio [**PSM \_ modificato**](psm-changed.md) alla finestra delle proprietà. Il messaggio fa sì che la finestra delle proprietà abiliti il pulsante **applica** . Se l'utente fa clic sul pulsante **applica** o **Annulla** , la pagina deve reinizializzare i controlli e quindi inviare il messaggio [**PSM non \_ modificato**](psm-unchanged.md) per disabilitare di nuovo il pulsante **applica** .

In alcuni casi il pulsante **applica** comporta la modifica di una pagina in una finestra delle proprietà e la modifica non può essere annullata. Quando si verifica questo problema, la pagina deve inviare il messaggio [**\_ CANCELTOCLOSE di PSM**](psm-canceltoclose.md) alla finestra delle proprietà. Il messaggio fa in modo che la finestra delle proprietà modifichi il testo del pulsante **OK** in "close", a indicare che le modifiche applicate non possono essere annullate.

Talvolta una pagina apporta una modifica alla configurazione di sistema che richiede il riavvio di Windows o il riavvio del sistema prima che la modifica possa essere applicata. Dopo avere apportato una modifica di questo tipo, una pagina deve inviare il messaggio [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) o [**PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md) alla finestra delle proprietà. Questi messaggi fanno sì che la funzione [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) restituisca il valore **ID \_ PSRESTARTWINDOWS** o **ID \_ PSREBOOTSYSTEM** dopo che la finestra delle proprietà è stata eliminata.

Quando un utente fa clic sul pulsante **Annulla** , la finestra delle proprietà Invia il codice di notifica di [ \_ reimpostazione di PSN](psn-reset.md) a tutte le pagine, a indicare che la finestra delle proprietà sta per essere distrutta. Per eseguire operazioni di pulizia, una pagina deve utilizzare la notifica.

## <a name="wizards"></a>Procedure guidate

Una procedura guidata è un tipo speciale di finestra delle proprietà. Le procedure guidate sono progettate per presentare le pagine una alla volta in una sequenza controllata dall'applicazione. Anziché selezionare un gruppo di pagine facendo clic su una scheda, gli utenti si spostano avanti e indietro nella sequenza, una pagina alla volta, facendo clic sui pulsanti. Ad esempio, la schermata seguente mostra la pagina iniziale dell'aggiunta guidata hardware:

![screenshot della pagina iniziale di una procedura guidata](images/wizard97.png)

Lo screenshot seguente mostra la prima pagina di una procedura guidata Aero, il nuovo stile introdotto in Windows Vista.

![screenshot della prima pagina di una procedura guidata Aero](images/wizardaero.png)

Per una descrizione completa delle procedure guidate, vedere [creazione di procedure guidate](wizards.md) .
