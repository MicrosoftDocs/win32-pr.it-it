---
title: Barra degli strumenti
description: In questa sezione sono contenute informazioni sugli elementi di programmazione utilizzati con i controlli della barra degli strumenti.
ms.assetid: vs|controls|~\controls\toolbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e0cadd2eb1560d3486073810e86a143b7fccca5
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103732095"
---
# <a name="toolbar"></a>Barra degli strumenti

In questa sezione sono contenute informazioni sugli elementi di programmazione utilizzati con i controlli della barra degli strumenti.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                                   | Contenuto                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sui controlli Toolbar](toolbar-controls-overview.md) | Una barra degli strumenti è un controllo che contiene uno o più pulsanti. Ogni pulsante, quando viene fatto clic da un utente, invia un messaggio di comando alla finestra padre. In genere, i pulsanti in una barra degli strumenti corrispondono agli elementi nel menu dell'applicazione e forniscono all'utente un ulteriore modo più diretto di accedere ai controlli di un'applicazione.<br/> |
| [Utilizzo di controlli Toolbar](using-toolbar-controls.md)    | Questo argomento contiene i dettagli di implementazione e il codice di esempio per l'uso di controlli Toolbar nelle applicazioni.<br/>                                                                                                                                                                                                                  |



 

### <a name="functions"></a>Funzioni



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Contenuto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-createmappedbitmap"><strong>CreateMappedBitmap</strong></a></td>
<td>Crea una bitmap da utilizzare in una barra degli strumenti. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex"><strong>CreateToolbarEx</strong></a></td>
<td>Crea una finestra della barra degli strumenti e aggiunge i pulsanti specificati alla barra degli strumenti.
<blockquote>
[!Note]<br />
Questa funzione è deprecata perché non supporta tutte le funzionalità delle barre degli strumenti. In alternativa, usare <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>CreateWindowEx</strong></a> . Per esempi, vedere <a href="using-toolbar-controls.md">uso dei controlli Toolbar</a>.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a>Messaggi



| Argomento                                                         | Contenuto                                                                                                                                                                                                |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TB \_ ADDBITMAP**](tb-addbitmap.md)                         | Aggiunge una o più immagini all'elenco di immagini dei pulsanti disponibili per una barra degli strumenti. <br/>                                                                                                               |
| [**TB \_ ADDBUTTONS**](tb-addbuttons.md)                       | Aggiunge uno o più pulsanti a una barra degli strumenti.<br/>                                                                                                                                                       |
| [**TB \_ ADDSTRING**](tb-addstring.md)                         | Aggiunge una nuova stringa al pool di stringhe della barra degli strumenti.<br/>                                                                                                                                              |
| [**\_ridimensionamento automatico TB**](tb-autosize.md)                           | Determina il ridimensionamento di una barra degli strumenti. <br/>                                                                                                                                                             |
| [**TB \_ BUTTONCOUNT**](tb-buttoncount.md)                     | Recupera un conteggio dei pulsanti attualmente presenti sulla barra degli strumenti. <br/>                                                                                                                                  |
| [**TB \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md)           | Specifica la dimensione della struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) . <br/>                                                                                                                           |
| [**TB \_ CHANGEBITMAP**](tb-changebitmap.md)                   | Modifica la bitmap per un pulsante in una barra degli strumenti.<br/>                                                                                                                                                |
| [**TB \_ CHECKBUTTON**](tb-checkbutton.md)                     | Controlla o deseleziona un pulsante specificato in una barra degli strumenti.<br/>                                                                                                                                              |
| [**TB \_ COMMANDTOINDEX**](tb-commandtoindex.md)               | Recupera l'indice in base zero per il pulsante associato all'identificatore di comando specificato. <br/>                                                                                             |
| [**\_personalizzazione TB**](tb-customize.md)                         | Consente di visualizzare la finestra di dialogo **Personalizza barra degli strumenti** .<br/>                                                                                                                                               |
| [**TB \_ DELETEBUTTON**](tb-deletebutton.md)                   | Elimina un pulsante dalla barra degli strumenti. <br/>                                                                                                                                                          |
| [**TB \_ ENABLEBUTTON**](tb-enablebutton.md)                   | Abilita o Disabilita il pulsante specificato in una barra degli strumenti.<br/>                                                                                                                                       |
| [**TB \_ GETANCHORHIGHLIGHT**](tb-getanchorhighlight.md)       | Recupera l'impostazione dell'evidenziazione dell'ancoraggio per una barra degli strumenti. <br/>                                                                                                                                       |
| [**TB \_ GETbitmap**](tb-getbitmap.md)                         | Recupera l'indice della bitmap associata a un pulsante in una barra degli strumenti. <br/>                                                                                                                    |
| [**TB \_ GETBITMAPFLAGS**](tb-getbitmapflags.md)               | Recupera i flag che descrivono il tipo di bitmap da utilizzare.<br/>                                                                                                                             |
| [**GetButton TB \_**](tb-getbutton.md)                         | Recupera le informazioni sul pulsante specificato in una barra degli strumenti.<br/>                                                                                                                               |
| [**TB \_ GETBUTTONINFO**](tb-getbuttoninfo.md)                 | Recupera le informazioni estese per un pulsante in una barra degli strumenti. <br/>                                                                                                                                   |
| [**TB \_ GETBUTTONSIZE**](tb-getbuttonsize.md)                 | Recupera la larghezza e l'altezza correnti dei pulsanti della barra degli strumenti, in pixel. <br/>                                                                                                                       |
| [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)                 | Recupera il testo visualizzato di un pulsante su una barra degli strumenti.<br/>                                                                                                                                         |
| [**TB \_ GETCOLORSCHEME**](tb-getcolorscheme.md)               | Recupera le informazioni sulla combinazione di colori dal controllo Toolbar. <br/>                                                                                                                            |
| [**TB \_ GETDISABLEDIMAGELIST**](tb-getdisabledimagelist.md)   | Recupera l'elenco di immagini utilizzato da un controllo Toolbar per visualizzare i pulsanti inattivi. <br/>                                                                                                           |
| [**TB \_ GETEXTENDEDSTYLE**](tb-getextendedstyle.md)           | Recupera gli stili estesi per un controllo Toolbar. <br/>                                                                                                                                        |
| [**TB \_ GETHOTIMAGELIST**](tb-gethotimagelist.md)             | Recupera l'elenco di immagini utilizzato da un controllo Toolbar per visualizzare i pulsanti di scelta rapida.<br/>                                                                                                                 |
| [**TB \_ GETHOTITEM**](tb-gethotitem.md)                       | Recupera l'indice dell'elemento attivo in una barra degli strumenti. <br/>                                                                                                                                           |
| [**TB \_ GETIDEALSIZE**](tb-getidealsize.md)                   | Ottiene la dimensione ideale della barra degli strumenti.<br/>                                                                                                                                                          |
| [**TB \_ GETimages**](tb-getimagelist.md)                   | Recupera l'elenco di immagini utilizzato da un controllo Toolbar per visualizzare i pulsanti nello stato predefinito. Un controllo toolbar utilizza questo elenco immagini per visualizzare i pulsanti quando non sono attivi o disabilitati.<br/> |
| [**TB \_ GETIMAGELISTCOUNT**](tb-getimagelistcount.md)         | Ottiene il numero di elenchi di immagini associate alla barra degli strumenti.<br/>                                                                                                                                  |
| [**TB \_ GETINSERTMARK**](tb-getinsertmark.md)                 | Recupera il segno di inserimento corrente per la barra degli strumenti. <br/>                                                                                                                                       |
| [**TB \_ GETINSERTMARKCOLOR**](tb-getinsertmarkcolor.md)       | Recupera il colore utilizzato per tracciare il segno di inserimento per la barra degli strumenti. <br/>                                                                                                                        |
| [**TB \_ GETITEMDROPDOWNRECT**](tb-getitemdropdownrect.md)     | Ottiene il rettangolo di delimitazione della finestra a discesa per un elemento della barra degli strumenti con stile [**\_ elenco a discesa BTNS**](toolbar-control-and-button-styles.md).<br/>                                  |
| [**TB \_ GETITEMRECT**](tb-getitemrect.md)                     | Recupera il rettangolo di delimitazione di un pulsante in una barra degli strumenti. <br/>                                                                                                                                  |
| [**TB \_ GETMAXSIZE**](tb-getmaxsize.md)                       | Recupera la dimensione totale di tutti i pulsanti e i separatori visibili nella barra degli strumenti. <br/>                                                                                                       |
| [**TB \_ GETmetrics**](tb-getmetrics.md)                       | Recupera le metriche di un controllo della barra degli strumenti.<br/>                                                                                                                                                  |
| [**TB \_ GETobject**](tb-getobject.md)                         | Recupera l'oggetto [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) per un controllo Toolbar. <br/>                                                                                                                     |
| [**TB \_ GETpadding**](tb-getpadding.md)                       | Recupera la spaziatura interna per un controllo Toolbar. <br/>                                                                                                                                                |
| [**TB \_ GETPRESSEDIMAGELIST**](tb-getpressedimagelist.md)     | Ottiene l'elenco di immagini utilizzato da un controllo Toolbar per visualizzare i pulsanti nello stato premuto.<br/>                                                                                                       |
| [**GetRect TB \_**](tb-getrect.md)                             | Recupera il rettangolo di delimitazione per un pulsante della barra degli strumenti specificato. <br/>                                                                                                                            |
| [**TB \_ GETrows**](tb-getrows.md)                             | Recupera il numero di righe di pulsanti in una barra degli strumenti con lo stile [**\_ wrapable TBSTYLE**](toolbar-control-and-button-styles.md) . <br/>                                        |
| [**TB \_ GETstate**](tb-getstate.md)                           | Recupera le informazioni sullo stato del pulsante specificato in una barra degli strumenti, ad esempio se è abilitato, premuto o selezionato. <br/>                                                             |
| [**TB \_ GETstring**](tb-getstring.md)                         | Recupera una stringa dal pool di stringhe di una barra degli strumenti.<br/>                                                                                                                                             |
| [**TB \_ GETstyle**](tb-getstyle.md)                           | Recupera gli stili attualmente in uso per un controllo Toolbar. <br/>                                                                                                                                |
| [**TB \_ GETTEXTROWS**](tb-gettextrows.md)                     | Recupera il numero massimo di righe di testo che è possibile visualizzare su un pulsante della barra degli strumenti. <br/>                                                                                                        |
| [**TB \_ GETtooltips**](tb-gettooltips.md)                     | Recupera l'handle per il controllo ToolTip, se presente, associato alla barra degli strumenti. <br/>                                                                                                           |
| [**TB \_ GETUNICODEFORMAT**](tb-getunicodeformat.md)           | Recupera il flag del formato carattere Unicode per il controllo. <br/>                                                                                                                                |
| [**TB \_ HASACCELERATOR**](tb-hasaccelerator.md)               | **Progettato per uso interno; sconsigliato per l'utilizzo nelle applicazioni.**<br/> Recupera un conteggio dei pulsanti della barra degli strumenti con il carattere di accelerazione specificato. <br/>                      |
| [**TB \_ HIDEBUTTON**](tb-hidebutton.md)                       | Nasconde o Mostra il pulsante specificato in una barra degli strumenti.<br/>                                                                                                                                            |
| [**( \_ HITTEST) TB**](tb-hittest.md)                             | Determina se un punto si trova in un controllo Toolbar. <br/>                                                                                                                                         |
| [**TB \_ INdeterminato**](tb-indeterminate.md)                 | Imposta o cancella lo stato indeterminato del pulsante specificato in una barra degli strumenti.<br/>                                                                                                                 |
| [**TB \_ INSERTBUTTON**](tb-insertbutton.md)                   | Inserisce un pulsante in una barra degli strumenti.<br/>                                                                                                                                                               |
| [**TB \_ INSERTMARKHITTEST**](tb-insertmarkhittest.md)         | Recupera le informazioni sul segno di inserimento per un punto in una barra degli strumenti. <br/>                                                                                                                          |
| [**TB \_ ISBUTTONCHECKED**](tb-isbuttonchecked.md)             | Determina se il pulsante specificato in una barra degli strumenti è selezionato. <br/>                                                                                                                            |
| [**TB \_ ISBUTTONENABLED**](tb-isbuttonenabled.md)             | Determina se il pulsante specificato in una barra degli strumenti è abilitato. <br/>                                                                                                                            |
| [**TB \_ ISBUTTONHIDDEN**](tb-isbuttonhidden.md)               | Determina se il pulsante specificato in una barra degli strumenti è nascosto. <br/>                                                                                                                             |
| [**TB \_ ISBUTTONHIGHLIGHTED**](tb-isbuttonhighlighted.md)     | Controlla lo stato di evidenziazione di un pulsante della barra degli strumenti. <br/>                                                                                                                                             |
| [**TB \_ ISBUTTONINDETERMINATE**](tb-isbuttonindeterminate.md) | Determina se il pulsante specificato in una barra degli strumenti è indeterminato. <br/>                                                                                                                      |
| [**TB \_ ISBUTTONPRESSED**](tb-isbuttonpressed.md)             | Determina se viene premuto il pulsante specificato in una barra degli strumenti. <br/>                                                                                                                            |
| [**TB \_ LOADIMAGES**](tb-loadimages.md)                       | Carica le immagini dei pulsanti definite dal sistema nell'elenco immagini di un controllo Toolbar.<br/>                                                                                                                      |
| [**TB \_ MAPACCELERATOR**](tb-mapaccelerator.md)               | Determina l'ID del pulsante che corrisponde al carattere dell'acceleratore specificato.<br/>                                                                                                     |
| [**TB \_ MARKBUTTON**](tb-markbutton.md)                       | Imposta lo stato di evidenziazione di un pulsante specificato in un controllo Toolbar.<br/>                                                                                                                             |
| [**TB \_ MOVEBUTTON**](tb-movebutton.md)                       | Sposta un pulsante da un indice a un altro. <br/>                                                                                                                                                   |
| [**TB \_ PRESSBUTTON**](tb-pressbutton.md)                     | Preme o rilascia il pulsante specificato in una barra degli strumenti.<br/>                                                                                                                                       |
| [**TB \_ REPLACEBITMAP**](tb-replacebitmap.md)                 | Sostituisce una bitmap esistente con una nuova bitmap.<br/>                                                                                                                                               |
| [**TB \_ SAVERESTORE**](tb-saverestore.md)                     | Inviare questo messaggio per avviare il salvataggio o il ripristino di uno stato della barra degli strumenti.<br/>                                                                                                                           |
| [**TB \_ SETANCHORHIGHLIGHT**](tb-setanchorhighlight.md)       | Imposta l'impostazione dell'evidenziazione di ancoraggio per una barra degli strumenti. <br/>                                                                                                                                            |
| [**TB \_ SETBITMAPSIZE**](tb-setbitmapsize.md)                 | Imposta la dimensione delle immagini bitmap da aggiungere a una barra degli strumenti. <br/>                                                                                                                             |
| [**TB \_ SETBOUNDINGSIZE**](tb-setboundingsize.md)             | **Progettato per uso interno; sconsigliato per l'utilizzo nelle applicazioni.**<br/> Imposta la dimensione di delimitazione per un controllo della barra degli strumenti a più colonne. <br/>                                               |
| [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md)                 | Imposta le informazioni per un pulsante esistente in una barra degli strumenti.<br/>                                                                                                                                    |
| [**TB \_ SETBUTTONSIZE**](tb-setbuttonsize.md)                 | Imposta la dimensione dei pulsanti in una barra degli strumenti.<br/>                                                                                                                                                       |
| [**TB \_ SETBUTTONWIDTH**](tb-setbuttonwidth.md)               | Imposta le larghezze minime e massime del pulsante nel controllo Toolbar.<br/>                                                                                                                           |
| [**TB \_ SETCMDID**](tb-setcmdid.md)                           | Imposta l'identificatore del comando di un pulsante della barra degli strumenti. <br/>                                                                                                                                            |
| [**TB \_ SETCOLORSCHEME**](tb-setcolorscheme.md)               | Imposta le informazioni sulla combinazione di colori per il controllo Toolbar. <br/>                                                                                                                                  |
| [**TB \_ SETDISABLEDIMAGELIST**](tb-setdisabledimagelist.md)   | Imposta l'elenco di immagini che il controllo toolbar utilizzerà per visualizzare i pulsanti disabilitati. <br/>                                                                                                          |
| [**TB \_ SETDRAWTEXTFLAGS**](tb-setdrawtextflags.md)           | Imposta i flag di disegno del testo per la barra degli strumenti. <br/>                                                                                                                                                |
| [**TB \_ SETEXTENDEDSTYLE**](tb-setextendedstyle.md)           | Imposta gli stili estesi per un controllo Toolbar. <br/>                                                                                                                                             |
| [**TB \_ SETHOTIMAGELIST**](tb-sethotimagelist.md)             | Imposta l'elenco di immagini che il controllo toolbar utilizzerà per visualizzare i pulsanti di scelta rapida.<br/>                                                                                                                |
| [**TB \_ SETHOTITEM**](tb-sethotitem.md)                       | Imposta l'elemento attivo in una barra degli strumenti.<br/>                                                                                                                                                              |
| [**TB \_ SETHOTITEM2**](tb-sethotitem2.md)                     | Imposta l'elemento attivo in una barra degli strumenti.<br/>                                                                                                                                                              |
| [**\_FILEimagine TB**](tb-setimagelist.md)                   | Imposta l'elenco di immagini utilizzato dalla barra degli strumenti per visualizzare i pulsanti che si trovano nello stato predefinito.<br/>                                                                                                |
| [**rientro TB \_**](tb-setindent.md)                         | Imposta il rientro per il primo pulsante in un controllo Toolbar. <br/>                                                                                                                             |
| [**TB \_ SETINSERTMARK**](tb-setinsertmark.md)                 | Imposta il segno di inserimento corrente per la barra degli strumenti. <br/>                                                                                                                                            |
| [**TB \_ SETINSERTMARKCOLOR**](tb-setinsertmarkcolor.md)       | Imposta il colore utilizzato per creare il segno di inserimento per la barra degli strumenti. <br/>                                                                                                                             |
| [**TB \_ SETLISTGAP**](tb-setlistgap.md)                       | Imposta la distanza tra i pulsanti della barra degli strumenti su una barra degli strumenti specifica.<br/>                                                                                                                         |
| [**TB \_ SETMAXTEXTROWS**](tb-setmaxtextrows.md)               | Imposta il numero massimo di righe di testo visualizzate su un pulsante della barra degli strumenti. <br/>                                                                                                                         |
| [**\_metriche TB**](tb-setmetrics.md)                       | Imposta la metrica di un controllo della barra degli strumenti.<br/>                                                                                                                                                       |
| [**\_spaziatura interna TB**](tb-setpadding.md)                       | Imposta la spaziatura interna per un controllo Toolbar.<br/>                                                                                                                                                      |
| [**\_elemento padre TB**](tb-setparent.md)                         | Imposta la finestra a cui il controllo Toolbar invia i codici di notifica. <br/>                                                                                                                      |
| [**TB \_ SETPRESSEDIMAGELIST**](tb-setpressedimagelist.md)     | Imposta l'elenco di immagini utilizzato dalla barra degli strumenti per visualizzare i pulsanti che si trovano in uno stato premuto.<br/>                                                                                                    |
| [**\_righe TB**](tb-setrows.md)                             | Imposta il numero di righe di pulsanti in una barra degli strumenti.<br/>                                                                                                                                             |
| [**TB di \_ stato**](tb-setstate.md)                           | Imposta lo stato del pulsante specificato in una barra degli strumenti.<br/>                                                                                                                                        |
| [**TB- \_ stile**](tb-setstyle.md)                           | Imposta lo stile per un controllo della barra degli strumenti. <br/>                                                                                                                                                       |
| [**\_descrizioni comando TB**](tb-settooltips.md)                     | Associa un controllo ToolTip a una barra degli strumenti. <br/>                                                                                                                                                |
| [**TB \_ SETUNICODEFORMAT**](tb-setunicodeformat.md)           | Imposta il flag di formato carattere Unicode per il controllo. Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover ricreare il controllo. <br/>    |
| [**TB \_ SETWINDOWTHEME**](tb-setwindowtheme.md)               | Imposta lo stile di visualizzazione di un controllo Toolbar.<br/>                                                                                                                                                  |
| [**TB \_ TRANSLATEACCELERATOR**](tb-translateaccelerator.md)   | Passa un messaggio della tastiera alla barra degli strumenti.<br/>                                                                                                                                                    |



 

### <a name="notifications"></a>Notifiche



| Argomento                                                            | Contenuto                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ char (barra degli strumenti)](nm-char-toolbar.md)                        | Inviato dalla barra degli strumenti quando riceve un messaggio [**WM \_ char**](/windows/desktop/inputdev/wm-char) . Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                                                                                       |
| [\_Clic su Nm (barra degli strumenti)](nm-click-toolbar.md)                      | Inviato da un controllo Toolbar quando l'utente fa clic su un elemento con il pulsante sinistro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                                                                                     |
| [\_CUSTOMDRAW Nm (barra degli strumenti)](nm-customdraw-toolbar.md)            | Inviato dalla barra degli strumenti per notificare alla finestra padre le operazioni di disegno. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                                                                                              |
| [\_DBLCLK Nm (barra degli strumenti)](nm-dblclk-toolbar.md)                    | Notifica alla finestra padre di un controllo Toolbar che l'utente ha fatto doppio clic con il pulsante sinistro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                                             |
| [\_KeyDown Nm (barra degli strumenti)](nm-keydown-toolbar.md)                  | Inviato da un controllo quando il controllo ha lo stato attivo della tastiera e l'utente preme un tasto. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                                                 |
| [\_LDOWN Nm](nm-ldown-toolbar.md)                                | Notifica alla finestra padre di una barra degli strumenti che è stato premuto il pulsante sinistro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                                                                                        |
| [\_RCLICK Nm (barra degli strumenti)](nm-rclick-toolbar.md)                    | Inviato da un controllo Toolbar quando l'utente fa clic sulla barra degli strumenti con il pulsante destro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                                                                                |
| [\_RDBLCLK Nm (barra degli strumenti)](nm-rdblclk-toolbar.md)                  | Notifica alla finestra padre di un controllo che l'utente ha fatto doppio clic con il pulsante destro del mouse all'interno del controllo. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                                                         |
| [\_RELEASEDCAPTURE Nm (barra degli strumenti)](nm-releasedcapture-toolbar-.md) | Notifica alla finestra padre di un controllo della barra degli strumenti che il controllo sta rilasciando l'acquisizione del mouse. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                                               |
| [\_TOOLTIPSCREATED Nm (barra degli strumenti)](nm-tooltipscreated-toolbar-.md) | Notifica alla finestra padre di una barra degli strumenti che la barra degli strumenti ha creato un controllo ToolTip. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                                                    |
| [\_BEGINADJUST TBN](tbn-beginadjust.md)                          | Notifica alla finestra padre di una barra degli strumenti che l'utente ha iniziato a personalizzare una barra degli strumenti. Questo codice di messaggio viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                                                          |
| [\_BEGINDRAG TBN](tbn-begindrag.md)                              | Notifica alla finestra padre di una barra degli strumenti che l'utente ha iniziato a trascinare un pulsante in una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                                            |
| [\_CUSTHELP TBN](tbn-custhelp.md)                                | Notifica alla finestra padre di una barra degli strumenti che l'utente ha scelto il pulsante della guida nella finestra di dialogo Personalizza barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                                                       |
| [\_DELETINGBUTTON TBN](tbn-deletingbutton.md)                    | Inviato da un controllo Toolbar quando un pulsante sta per essere eliminato. <br/>                                                                                                                                                                                                                                                |
| [\_trascinamento TBN](tbn-dragout.md)                                  | Inviato da un controllo Toolbar quando l'utente fa clic su un pulsante e quindi sposta il cursore dal pulsante. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                                     |
| [TBN \_ DRAGOVER](tbn-dragover.md)                                | Verifica se deve essere inviato un messaggio [**TB \_ MARKBUTTON**](tb-markbutton.md) per un pulsante trascinato. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                                           |
| [\_elenco a discesa TBN](tbn-dropdown.md)                                | Inviato da un controllo Toolbar quando l'utente fa clic su un pulsante a discesa. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                                                                     |
| [\_DUPACCELERATOR TBN](tbn-dupaccelerator.md)                    | Verifica se un tasto di scelta rapida può essere utilizzato su due o più barre degli strumenti attive. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                                                                                      |
| [\_ENDADJUST TBN](tbn-endadjust.md)                              | Notifica alla finestra padre di una barra degli strumenti che l'utente ha interrotto la personalizzazione di una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                                                   |
| [\_ENDDRAG TBN](tbn-enddrag.md)                                  | Notifica alla finestra padre della barra degli strumenti che l'utente ha interrotto il trascinamento di un pulsante in una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                                        |
| [\_GETBUTTONINFO TBN](tbn-getbuttoninfo.md)                      | Recupera le informazioni di personalizzazione della barra degli strumenti e notifica alla finestra padre della barra degli strumenti le modifiche apportate alla barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                        |
| [\_GETDISPINFO TBN](tbn-getdispinfo.md)                          | Recupera le informazioni di visualizzazione per un elemento della barra degli strumenti. Questa notifica viene inviata sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .<br/>                                                                                                                                                                           |
| [\_GETINFOTIP TBN](tbn-getinfotip.md)                            | Recupera le informazioni infotip per un elemento della barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                                                                                                                      |
| [TBN \_ GETobject](tbn-getobject.md)                              | Inviato da un controllo Toolbar che usa lo [**stile \_ REGISTERDROP TBSTYLE**](toolbar-control-and-button-styles.md) per richiedere un oggetto destinazione di rilascio quando il puntatore passa su uno dei pulsanti. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/> |
| [\_HOTITEMCHANGE TBN](tbn-hotitemchange.md)                      | Inviato da un controllo Toolbar quando viene modificato l'elemento attivo (evidenziato). Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                                                                    |
| [\_INITCUSTOMIZE TBN](tbn-initcustomize.md)                      | Notifica alla finestra padre di una barra degli strumenti che la personalizzazione è stata avviata. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                                                                                                       |
| [\_MAPACCELERATOR TBN](tbn-mapaccelerator.md)                    | Richiede l'indice del pulsante sulla barra degli strumenti corrispondente al carattere dell'acceleratore specificato. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                                                                  |
| [\_QUERYDELETE TBN](tbn-querydelete.md)                          | Notifica alla finestra padre della barra degli strumenti se un pulsante può essere eliminato da una barra degli strumenti mentre l'utente personalizza la barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                        |
| [\_QUERYINSERT TBN](tbn-queryinsert.md)                          | Notifica alla finestra padre della barra degli strumenti se un pulsante può essere inserito a sinistra del pulsante specificato mentre l'utente sta personalizzando una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                     |
| [reimpostazione TBN \_](tbn-reset.md)                                      | Notifica alla finestra padre della barra degli strumenti che l'utente ha reimpostato il contenuto della finestra di dialogo Personalizza barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                                                          |
| [\_ripristino TBN](tbn-restore.md)                                  | Notifica alla finestra padre di una barra degli strumenti che è in corso il ripristino di una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                                                                                 |
| [\_Salva TBN](tbn-save.md)                                        | Notifica alla finestra padre di una barra degli strumenti che è in corso il salvataggio di una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                                                                                    |
| [\_TOOLBARCHANGE TBN](tbn-toolbarchange.md)                      | Notifica alla finestra padre della barra degli strumenti che l'utente ha personalizzato una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/>                                                                                                                                          |
| [\_WRAPACCELERATOR TBN](tbn-wrapaccelerator.md)                  | Richiede l'indice del pulsante in una o più barre degli strumenti corrispondenti al carattere dell'acceleratore specificato. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                                                         |
| [\_WRAPHOTITEM TBN](tbn-wraphotitem.md)                          | Notifica a un'applicazione due o più barre degli strumenti che l'elemento critico sta per cambiare. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/>                                                                                                                                |



 

### <a name="structures"></a>Strutture



| Argomento                                      | Contenuto                                                                                                                                                                                                                                                                |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COLORMAP**](/windows/desktop/api/Commctrl/ns-commctrl-colormap)               | Contiene le informazioni utilizzate dalla funzione [**CreateMappedBitmap**](/windows/desktop/api/Commctrl/nf-commctrl-createmappedbitmap) per eseguire il mapping dei colori della bitmap. <br/>                                                                                                                                 |
| [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw)   | Contiene informazioni specifiche di un codice di notifica [ \_ CUSTOMDRAW Nm](nm-customdraw-toolbar.md) inviato da un controllo Toolbar. <br/>                                                                                                                                |
| [**NMTBDISPINFO**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa)       | Contiene e riceve le informazioni di visualizzazione per un elemento della barra degli strumenti. Questa struttura viene utilizzata con il codice di notifica [ \_ GETDISPINFO di TBN](tbn-getdispinfo.md) . <br/>                                                                                                    |
| [**NMTBGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa)   | Contiene e riceve informazioni infotip per un elemento della barra degli strumenti. Questa struttura viene utilizzata con il codice di notifica [ \_ GETINFOTIP di TBN](tbn-getdispinfo.md) . <br/>                                                                                                     |
| [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem)         | Contiene informazioni usate con il codice di notifica [ \_ HOTITEMCHANGE di TBN](tbn-hotitemchange.md) . <br/>                                                                                                                                                           |
| [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore)         | Consente alle applicazioni di estrarre le informazioni inserite in [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) quando è stato salvato lo stato della barra degli strumenti. Questa struttura viene passata alle applicazioni quando ricevono un codice di notifica del [ \_ ripristino TBN](tbn-restore.md) .<br/>             |
| [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave)               | Questa struttura viene passata alle applicazioni quando ricevono un codice di notifica di [ \_ salvataggio TBN](tbn-save.md) . Contiene informazioni sul pulsante attualmente salvato. Le applicazioni possono modificare i valori dei membri per salvare informazioni aggiuntive. <br/> |
| [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara)             | Contiene le informazioni utilizzate per elaborare i codici di notifica della barra degli strumenti. Questa struttura sostituisce la struttura **TBNOTIFY** . <br/>                                                                                                                                      |
| [**TBADDBITMAP**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap)         | Aggiunge una bitmap che contiene immagini di pulsanti a una barra degli strumenti.<br/>                                                                                                                                                                                                      |
| [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)               | Contiene informazioni su un pulsante in una barra degli strumenti.<br/>                                                                                                                                                                                                            |
| [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa)       | Contiene o riceve informazioni per un pulsante specifico in una barra degli strumenti.<br/>                                                                                                                                                                                         |
| [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark)       | Contiene informazioni sul segno di inserimento in un controllo Toolbar. <br/>                                                                                                                                                                                            |
| [**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics)             | Definisce la metrica di una barra degli strumenti utilizzata per compattare o espandere gli elementi della barra degli strumenti.<br/>                                                                                                                                                                            |
| [**TBREPLACEBITMAP**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap) | Utilizzato con il messaggio [**TB \_ REPLACEBITMAP**](tb-replacebitmap.md) per sostituire una bitmap della barra degli strumenti con un'altra.<br/>                                                                                                                                              |
| [**TBSAVEPARAMS**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa)       | Specifica il percorso nel registro di sistema in cui il messaggio [**TB \_ SAVERESTORE**](tb-saverestore.md) archivia e recupera le informazioni sullo stato di una barra degli strumenti. <br/>                                                                                           |



 

### <a name="constants"></a>Costanti



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Contenuto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="toolbar-button-states.md">Stati del pulsante della barra degli strumenti</a></td>
<td>Questa sezione elenca gli Stati che possono essere presenti in un pulsante della barra degli strumenti. <br/></td>
</tr>
<tr class="even">
<td><a href="toolbar-control-and-button-styles.md">Stili del pulsante e del controllo Toolbar</a></td>
<td>Gli stili della finestra seguenti sono specifici per le barre degli strumenti. Vengono combinati con altri stili della finestra quando viene creata la barra degli strumenti.<br/> <strong>Nota</strong> Per i controlli comuni <a href="common-control-versions.md">versione 6,00</a>, se si usa uno <a href="themes-overview.md">stile di visualizzazione</a> con la barra degli strumenti, i pulsanti sono sempre trasparenti indipendentemente dall'impostazione dello stile. In caso contrario, il comportamento della trasparenza è normale come indicato dall'utilizzo dello stile <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_FLAT</strong></a> o <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_TRANSPARENT</strong></a> .
<blockquote>
[!Note]<br />
Comctl32.dll versione 6 non è ridistribuibile ma è incluso in Windows o versioni successive. Per usare Comctl32.dll versione 6, specificarla in un manifesto. Per altre informazioni sui manifesti, vedere <a href="cookbook-overview.md">Abilitazione degli stili di visualizzazione</a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="toolbar-extended-styles.md">Stili estesi della barra degli strumenti</a></td>
<td>Questa sezione elenca gli stili estesi supportati dai controlli della barra degli strumenti.<br/></td>
</tr>
<tr class="even">
<td><a href="toolbar-standard-button-image-index-values.md">Valori di indice dell'immagine del pulsante standard della barra degli strumenti</a></td>
<td>In questa sezione vengono specificati i valori di indice delle immagini all'interno di bitmap standard.<br/></td>
</tr>
</tbody>
</table>



 

