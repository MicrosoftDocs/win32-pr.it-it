---
title: Pulsante (controlli di Windows)
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli Button. Un pulsante è un controllo su cui l'utente può fare clic per fornire l'input a un'applicazione.
ms.assetid: vs|controls|~\controls\buttons\buttons.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babe31ec9f11ee445167e57394da0fa88fd781dd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474830"
---
# <a name="button-windows-controls"></a>Pulsante (controlli di Windows)

Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli Button. Un *pulsante* è un controllo su cui l'utente può fare clic per fornire l'input a un'applicazione.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                       | Contenuto                                                                                                           |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Messaggi dei pulsanti](button-messages.md)      | In questo argomento vengono illustrati i messaggi utilizzati con i pulsanti.<br/>                                               |
| [Stati del pulsante](button-states.md)          | Questa sezione illustra in che modo la selezione di un pulsante modifica lo stato e il modo in cui l'applicazione deve rispondere.<br/> |
| [Tipi di pulsante](button-types-and-styles.md) | In questo argomento vengono illustrati i diversi tipi di pulsanti.<br/>                                                    |
| [Uso di pulsanti](using-buttons.md)          | In questa sezione viene illustrato come eseguire determinate attività associate ai pulsanti.<br/>                            |



 

### <a name="functions"></a>Funzioni



| Argomento                                            | Contenuto                                                                                                                                                                                                  |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton)         | Modifica lo stato di selezione di un controllo Button.<br/>                                                                                                                                                   |
| [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton)     | Aggiunge un segno di spunta a (controlla) un pulsante di opzione specificato in un gruppo e rimuove un segno di spunta da (Cancella) tutti gli altri pulsanti di opzione nel gruppo. <br/>                                                |
| [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) | La funzione [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) determina se un controllo Button è selezionato o se un controllo pulsante a tre stati è selezionato, non selezionato o indeterminato. <br/> |



 

### <a name="macros"></a>Macro



| Argomento                                                                         | Contenuto                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Pulsante \_ Abilita**](/windows/desktop/api/Windowsx/nf-windowsx-button_enable)                                       | Abilita o Disabilita un pulsante.<br/>                                                                                                                                                                                                          |
| [**Pulsante \_ GetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck)                                   | Ottiene lo stato di selezione di un pulsante di opzione o di una casella di controllo. È possibile usare questa macro o inviare il messaggio [**BM \_ GetCheck**](bm-getcheck.md) in modo esplicito. <br/>                                                                                       |
| [**Pulsante \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize)                           | Ottiene le dimensioni del pulsante che meglio si adatta al testo e all'immagine, se è presente un elenco di immagini. È possibile usare questa macro o inviare il [**messaggio \_ GETIDEALSIZE di BCM**](bcm-getidealsize.md) in modo esplicito. <br/>                                      |
| [**Pulsante \_ Getimagine**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist)                           | Ottiene la [**struttura \_ ImageList del pulsante**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) che descrive l'elenco di immagini impostato per un controllo Button. È possibile usare questa macro o inviare in modo esplicito il messaggio [**BCM \_ getimagine**](bcm-getimagelist.md) . <br/> |
| [**Pulsante \_ Getnote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote)                                     | Ottiene il testo della nota associata a un pulsante di collegamento al comando. È possibile usare questa macro o inviare in modo esplicito il messaggio [**BCM \_ getnote**](bcm-getnote.md) .<br/>                                                                            |
| [**Pulsante \_ GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength)                         | Ottiene la lunghezza del testo della nota che può essere visualizzato nella descrizione di un collegamento di comando. Usare questa macro o inviare il [**messaggio \_ GETNOTELENGTH di BCM**](bcm-getnotelength.md) in modo esplicito.<br/>                                           |
| [**Pulsante \_ GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo)                           | Ottiene informazioni per un controllo pulsante di divisione specificato. Usare questa macro o inviare il [**messaggio \_ GETSPLITINFO di BCM**](bcm-getsplitinfo.md) in modo esplicito.<br/>                                                                                    |
| [**Pulsante \_ GetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate)                                   | Ottiene lo stato di selezione di un pulsante di opzione o di una casella di controllo. È possibile usare questa macro o inviare il messaggio [**BM \_ GetState**](bm-getstate.md) in modo esplicito. <br/>                                                                                       |
| [**Pulsante \_ GetText**](/windows/desktop/api/Windowsx/nf-windowsx-button_gettext)                                     | Ottiene il testo di un pulsante.<br/>                                                                                                                                                                                                             |
| [**Pulsante \_ GetTextLength**](/windows/desktop/api/Windowsx/nf-windowsx-button_gettextlength)                         | Ottiene il numero di caratteri nel testo di un pulsante.<br/>                                                                                                                                                                                 |
| [**Pulsante \_ GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin)                         | Ottiene i margini utilizzati per creare il testo in un controllo Button. È possibile usare questa macro o inviare il [**messaggio \_ GETTEXTMARGIN di BCM**](bcm-gettextmargin.md) in modo esplicito. <br/>                                                                        |
| [**Controllo del pulsante \_**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck)                                   | Imposta lo stato di selezione di un pulsante di opzione o di una casella di controllo. È possibile usare questa macro o inviare il messaggio di [**\_ controllo BM**](bm-setcheck.md) in modo esplicito. <br/>                                                                                       |
| [**Pulsante \_ SetDropDownState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate)                   | Imposta lo stato di elenco a discesa per un pulsante specificato con stile [**BS \_ SPLITBUTTON**](button-styles.md). Usare questa macro o inviare il [**messaggio \_ SETDROPDOWNSTATE di BCM**](bcm-setdropdownstate.md) in modo esplicito. <br/>           |
| [**Pulsante \_ SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) | Imposta lo stato di elevazione richieste per un pulsante o un collegamento di comando specificato per visualizzare un'icona con privilegi elevati. Usare questa macro o inviare in modo esplicito il messaggio [**BCM \_ seshield**](bcm-setshield.md) . <br/>                                          |
| [**\_Diimages Button**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist)                           | Assegna un elenco di immagini a un controllo Button. È possibile usare questa macro o inviare in modo esplicito il messaggio di oggetto [**BCM \_**](bcm-setimagelist.md) . <br/>                                                                                       |
| [**\_Nota pulsante**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote)                                     | Imposta il testo della nota associata a un pulsante di collegamento del comando specificato. È possibile usare questa macro o inviare in modo esplicito il messaggio di [**\_ Nota BCM**](bcm-setnote.md) .<br/>                                                                  |
| [**Pulsante \_ SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo)                           | Imposta le informazioni per un controllo pulsante di divisione specificato. Usare questa macro o inviare il [**messaggio \_ SETSPLITINFO di BCM**](bcm-setsplitinfo.md) in modo esplicito.<br/>                                                                                    |
| [**Stato del pulsante \_**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate)                                   | Imposta lo stato di evidenziazione di un pulsante. Lo stato di evidenziazione indica se il pulsante è evidenziato come se l'utente avesse eseguito il push. È possibile utilizzare questa macro o inviare il messaggio di [**\_ stato BM**](bm-setstate.md) in modo esplicito. <br/>        |
| [**Pulsante di \_ stile**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle)                                   | Imposta lo stile di un pulsante. È possibile usare questa macro o inviare in modo esplicito il messaggio [**BM \_ Sestyle**](bm-setstyle.md) . <br/>                                                                                                                |
| [**Testo del pulsante \_**](/windows/desktop/api/Windowsx/nf-windowsx-button_settext)                                     | Imposta il testo di un pulsante.<br/>                                                                                                                                                                                                             |
| [**Pulsante \_ SetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_settextmargin)                         | Imposta i margini per il disegno di testo in un controllo Button. È possibile usare questa macro o inviare il [**messaggio \_ SETTEXTMARGIN di BCM**](bcm-settextmargin.md) in modo esplicito. <br/>                                                                         |



 

### <a name="messages"></a>Messaggi



| Argomento                                                 | Contenuto                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_GETIDEALSIZE BCM**](bcm-getidealsize.md)         | Ottiene le dimensioni del pulsante che meglio si adatta al testo e all'immagine, se è presente un elenco di immagini. È possibile inviare questo messaggio in modo esplicito o usare il [**pulsante \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) macro.<br/>                                                                                   |
| [**BCM \_ GETimages**](bcm-getimagelist.md)         | Ottiene la [**struttura \_ ImageList del pulsante**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) che descrive l'elenco di immagini assegnato a un controllo Button. È possibile inviare questo messaggio in modo esplicito o usare la macro [**Button \_ getimagine**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) .<br/>                                                  |
| [**BCM \_ GETnote**](bcm-getnote.md)                   | Ottiene il testo della nota associata a un pulsante di collegamento al comando. È possibile inviare questo messaggio in modo esplicito o usare la macro del [**pulsante \_ getnote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) .<br/>                                                                                                                        |
| [**\_GETNOTELENGTH BCM**](bcm-getnotelength.md)       | Ottiene la lunghezza del testo della nota che può essere visualizzato nella descrizione di un pulsante di collegamento al comando. Inviare questo messaggio in modo esplicito o tramite il [**pulsante \_ GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength) macro.<br/>                                                                           |
| [**\_GETSPLITINFO BCM**](bcm-getsplitinfo.md)         | Ottiene informazioni per un controllo pulsante di divisione. Inviare questo messaggio in modo esplicito o tramite il [**pulsante \_ GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) macro. <br/>                                                                                                                                    |
| [**\_GETTEXTMARGIN BCM**](bcm-gettextmargin.md)       | Ottiene i margini utilizzati per creare il testo in un controllo Button. È possibile inviare questo messaggio in modo esplicito o usare il [**pulsante \_ GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) macro.<br/>                                                                                                                     |
| [**\_SETDROPDOWNSTATE BCM**](bcm-setdropdownstate.md) | Imposta lo stato di elenco a discesa per un pulsante con lo stile [**\_ elenco a discesa TBSTYLE**](toolbar-control-and-button-styles.md). Inviare questo messaggio in modo esplicito o tramite il [**pulsante \_ SetDropDownState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) macro.<br/>                                        |
| [**\_SEimagine BCM**](bcm-setimagelist.md)         | Assegna un elenco di immagini a un controllo Button. È possibile inviare questo messaggio in modo esplicito o [**usare \_ la macro Button**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) .<br/>                                                                                                                                    |
| [**\_Nota BCM**](bcm-setnote.md)                   | Imposta il testo della nota associata a un pulsante di collegamento al comando. È possibile inviare questo messaggio in modo esplicito o usare la macro di [**pulsanti \_**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) .<br/>                                                                                                                        |
| [**seshield BCM \_**](bcm-setshield.md)               | Imposta lo stato di elevazione richieste per un pulsante o un collegamento di comando specificato per visualizzare un'icona con privilegi elevati. Inviare questo messaggio in modo esplicito o tramite il [**pulsante \_ SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) macro.<br/>                                                  |
| [**\_SETSPLITINFO BCM**](bcm-setsplitinfo.md)         | Imposta le informazioni per un controllo pulsante di divisione. Inviare questo messaggio in modo esplicito o tramite il [**pulsante \_ SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) macro.<br/>                                                                                                                                     |
| [**\_SETTEXTMARGIN BCM**](bcm-settextmargin.md)       | Il messaggio [**BCM \_ SETTEXTMARGIN**](bcm-settextmargin.md) imposta i margini per il disegno di testo in un controllo Button. <br/>                                                                                                                                                                      |
| [**\_fare clic su BM**](bm-click.md)                         | Simula l'utente che fa clic su un pulsante. Questo messaggio fa in modo che il pulsante riceva i messaggi [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) e [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) e la finestra padre del pulsante per ricevere un codice di notifica [ \_ fatto clic su BN](bn-clicked.md) .<br/> |
| [**GetCheck BM \_**](bm-getcheck.md)                   | Ottiene lo stato di selezione di un pulsante di opzione o di una casella di controllo. È possibile inviare questo messaggio in modo esplicito o usare la macro del [**pulsante \_ GetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) .<br/>                                                                                                                                  |
| [**BM \_ GETimage**](bm-getimage.md)                   | Recupera un handle per l'immagine (icona o bitmap) associata al pulsante.<br/>                                                                                                                                                                                                             |
| [**BM \_ GETstate**](bm-getstate.md)                   | Recupera lo stato di un pulsante o di una casella di controllo. È possibile inviare questo messaggio in modo esplicito o usare il [**pulsante \_ GetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) macro.<br/>                                                                                                                                         |
| [**\_controllo BM**](bm-setcheck.md)                   | Imposta lo stato di selezione di un pulsante di opzione o di una casella di controllo. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro di [**\_ controllo Button**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) .<br/>                                                                                                                             |
| [**\_SETDONTCLICK BM**](bm-setdontclick.md)           | Imposta un flag su un pulsante di opzione che controlla la generazione di BN che hanno [ \_ fatto clic su](bn-clicked.md) messaggi quando il pulsante riceve lo stato attivo.<br/>                                                                                                                                                     |
| [**\_immagine BM**](bm-setimage.md)                   | Associa una nuova immagine (icona o bitmap) a un pulsante.<br/>                                                                                                                                                                                                                                 |
| [**STATO di BM \_**](bm-setstate.md)                   | Imposta lo stato di evidenziazione di un pulsante. Lo stato di evidenziazione indica se il pulsante è evidenziato come se l'utente avesse eseguito il push. È possibile inviare questo messaggio in modo esplicito o usare la macro di [**\_ stato del pulsante**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) .<br/>                                                   |
| [**distile BM \_**](bm-setstyle.md)                   | Imposta lo stile di un pulsante. È possibile inviare questo messaggio in modo esplicito o usare la macro di [**\_ tipo Button**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) .<br/>                                                                                                                                                           |



 

### <a name="notifications"></a>Notifiche



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
<td><a href="bcn-dropdown.md">BCN_DROPDOWN</a></td>
<td>Inviato quando l'utente fa clic su una freccia a discesa di un pulsante. La finestra padre del controllo riceve questo codice di notifica sotto forma di messaggio di <a href="wm-notify.md"><strong>WM_NOTIFY</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="bcn-hotitemchange.md">BCN_HOTITEMCHANGE</a></td>
<td>Notifica al proprietario del controllo Button che il mouse entra o esce dall'area client del controllo Button. Il controllo Button invia questo codice di notifica sotto forma di messaggio di <a href="wm-notify.md"><strong>WM_NOTIFY</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="bn-clicked.md">BN_CLICKED</a></td>
<td>Inviato quando l'utente fa clic su un pulsante. <br/> La finestra padre del pulsante riceve il codice di notifica <a href="bn-clicked.md">BN_CLICKED</a> tramite il messaggio di <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> . <br/></td>
</tr>
<tr class="even">
<td><a href="bn-dblclk.md">BN_DBLCLK</a></td>
<td>Inviato quando l'utente fa doppio clic su un pulsante. Questo codice di notifica viene inviato automaticamente per i pulsanti <a href="button-styles.md"><strong>BS_USERBUTTON</strong></a>, <a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a>e <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> . Altri tipi di pulsante inviano <a href="bn-dblclk.md">BN_DBLCLK</a> solo se hanno lo stile <a href="button-styles.md"><strong>BS_NOTIFY</strong></a> .<br/> La finestra padre del pulsante riceve il codice di notifica <a href="bn-dblclk.md">BN_DBLCLK</a> tramite il messaggio di <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> . <br/></td>
</tr>
<tr class="odd">
<td><a href="bn-disable.md">BN_DISABLE</a></td>
<td>Inviato quando un pulsante è disabilitato.
<blockquote>
[!Note]<br />
Questo codice di notifica viene fornito solo per la compatibilità con le versioni di Windows a 16 bit precedenti alla versione 3,0. Le applicazioni devono utilizzare lo stile del pulsante <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> e la struttura <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>DRAWITEMSTRUCT</strong></a> per questa attività.
</blockquote>
<br/> <br/> La finestra padre del pulsante riceve il codice di notifica <a href="bn-disable.md">BN_DISABLE</a> tramite il messaggio di <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="bn-doubleclicked.md">BN_DOUBLECLICKED</a></td>
<td>Inviato quando l'utente fa doppio clic su un pulsante. Questo codice di notifica viene inviato automaticamente per i pulsanti <a href="button-styles.md"><strong>BS_USERBUTTON</strong></a>, <a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a>e <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> . Altri tipi di pulsante inviano <a href="bn-doubleclicked.md">BN_DOUBLECLICKED</a> solo se hanno lo stile <a href="button-styles.md"><strong>BS_NOTIFY</strong></a> .<br/> La finestra padre del pulsante riceve il codice di notifica <a href="bn-doubleclicked.md">BN_DOUBLECLICKED</a> tramite il messaggio di <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> . <br/></td>
</tr>
<tr class="odd">
<td><a href="bn-hilite.md">BN_HILITE</a></td>
<td>Inviato quando l'utente seleziona un pulsante.
<blockquote>
[!Note]<br />
Questo codice di notifica viene fornito solo per la compatibilità con le versioni di Windows a 16 bit precedenti alla versione 3,0. Le applicazioni devono utilizzare lo stile del pulsante <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> e la struttura <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>DRAWITEMSTRUCT</strong></a> per questa attività.
</blockquote>
<br/> <br/> La finestra padre del pulsante riceve il codice di notifica <a href="bn-hilite.md">BN_HILITE</a> tramite il messaggio di <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="bn-killfocus.md">BN_KILLFOCUS</a></td>
<td>Inviato quando un pulsante perde lo stato attivo della tastiera. Il pulsante deve avere lo stile <a href="button-styles.md"><strong>BS_NOTIFY</strong></a> per inviare il codice di notifica. <br/> La finestra padre del pulsante riceve il codice di notifica <a href="bn-killfocus.md">BN_KILLFOCUS</a> tramite il messaggio di <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> . <br/></td>
</tr>
<tr class="odd">
<td><a href="bn-paint.md">BN_PAINT</a></td>
<td>Inviato quando un pulsante deve essere disegnato.
<blockquote>
[!Note]<br />
Questo codice di notifica viene fornito solo per la compatibilità con le versioni di Windows a 16 bit precedenti alla versione 3,0. Le applicazioni devono utilizzare lo stile del pulsante <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> e la struttura <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>DRAWITEMSTRUCT</strong></a> per questa attività.
</blockquote>
<br/> <br/> La finestra padre del pulsante riceve il codice di notifica <a href="bn-paint.md">BN_PAINT</a> tramite il messaggio di <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> . <br/></td>
</tr>
<tr class="even">
<td><a href="bn-pushed.md">BN_PUSHED</a></td>
<td>Inviato quando lo stato di push di un pulsante è impostato su push.
<blockquote>
[!Note]<br />
Questo codice di notifica viene fornito solo per la compatibilità con le versioni di Windows a 16 bit precedenti alla versione 3,0. Le applicazioni devono utilizzare lo stile del pulsante <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> e la struttura <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>DRAWITEMSTRUCT</strong></a> per questa attività.
</blockquote>
<br/> <br/> La finestra padre del pulsante riceve il codice di notifica <a href="bn-pushed.md">BN_PUSHED</a> tramite il messaggio di <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="bn-setfocus.md">BN_SETFOCUS</a></td>
<td>Inviato quando un pulsante riceve lo stato attivo della tastiera. Il pulsante deve avere lo stile <a href="button-styles.md"><strong>BS_NOTIFY</strong></a> per inviare il codice di notifica. <br/> La finestra padre del pulsante riceve il codice di notifica <a href="bn-setfocus.md">BN_SETFOCUS</a> tramite il messaggio di <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="bn-unhilite.md">BN_UNHILITE</a></td>
<td>Inviato quando l'evidenziazione deve essere rimossa da un pulsante.
<blockquote>
[!Note]<br />
Questo codice di notifica viene fornito solo per la compatibilità con le versioni di Windows a 16 bit precedenti alla versione 3,0. Le applicazioni devono utilizzare lo stile del pulsante <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> e la struttura <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>DRAWITEMSTRUCT</strong></a> per questa attività.
</blockquote>
<br/> <br/> La finestra padre del pulsante riceve il codice di notifica <a href="bn-unhilite.md">BN_UNHILITE</a> tramite il messaggio di <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="bn-unpushed.md">BN_UNPUSHED</a></td>
<td>Inviato quando lo stato di push di un pulsante è impostato su non sottoposto a push.
<blockquote>
[!Note]<br />
Questo codice di notifica viene fornito solo per la compatibilità con le versioni di Windows a 16 bit precedenti alla versione 3,0. Le applicazioni devono utilizzare lo stile del pulsante <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> e la struttura <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>DRAWITEMSTRUCT</strong></a> per questa attività.
</blockquote>
<br/> <br/> La finestra padre del pulsante riceve il codice di notifica <a href="bn-unpushed.md">BN_UNPUSHED</a> tramite il messaggio di <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="nm-customdraw-button.md">NM_CUSTOMDRAW (pulsante)</a></td>
<td>Notifica alla finestra padre di un controllo Button informazioni sulle operazioni di disegni personalizzate sul pulsante. <br/> Il controllo Button invia questo codice di notifica sotto forma di messaggio di <a href="wm-notify.md"><strong>WM_NOTIFY</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="wm-ctlcolorbtn.md"><strong>WM_CTLCOLORBTN</strong></a></td>
<td>Il messaggio <a href="wm-ctlcolorbtn.md"><strong>WM_CTLCOLORBTN</strong></a> viene inviato alla finestra padre di un pulsante prima di disegnare il pulsante. La finestra padre può modificare il testo del pulsante e i colori di sfondo. Tuttavia, solo i pulsanti creati dal proprietario rispondono alla finestra padre che elabora questo messaggio. <br/></td>
</tr>
</tbody>
</table>



 

### <a name="structures"></a>Strutture



| Argomento                                         | Contenuto                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PULSANTE \_ ImageList**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) | Contiene informazioni su un elenco di immagini utilizzato con un controllo Button.<br/>                                                                                                                                                                                                                                 |
| [**PULSANTE \_ SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) | Contiene informazioni che definiscono un pulsante di suddivisione (stili [**BS \_ SPLITBUTTON**](button-styles.md) e [**BS \_ DEFSPLITBUTTON**](button-styles.md) ). Usato con i messaggi [**BCM \_ GETSPLITINFO**](bcm-getsplitinfo.md) e [**BCM \_ SETSPLITINFO**](bcm-setsplitinfo.md) .<br/> |
| [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown)          | Contiene informazioni su una notifica a [ \_ discesa BCN](bcn-dropdown.md) .<br/>                                                                                                                                                                                                                                 |
| [**NMBCHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem)            | Contiene informazioni sullo spostamento del mouse su un controllo Button.<br/>                                                                                                                                                                                                                                  |



 

### <a name="constants"></a>Costanti



| Argomento                              | Contenuto                                                                                                                                                                                                                                                            |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Stili dei pulsanti](button-styles.md) | Specifica una combinazione di stili dei pulsanti. Se si crea un pulsante usando la classe BUTTON con la funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , è possibile specificare uno degli stili dei pulsanti elencati di seguito.<br/> |



 

