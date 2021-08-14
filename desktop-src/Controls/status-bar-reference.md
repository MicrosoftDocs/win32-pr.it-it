---
title: Barra di stato
description: Questa sezione contiene informazioni sugli elementi di programmazione utilizzati con i controlli barra di stato.
ms.assetid: 77923055-9d00-4528-bda7-b602a26b577f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1be3ea518b63118fc80b02b382943c40ba2fd13b15713488b351b5d6cc827e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696491"
---
# <a name="status-bar"></a>Barra di stato

Questa sezione contiene informazioni sugli elementi di programmazione utilizzati con i controlli barra di stato.

### <a name="overviews"></a>Cenni preliminari



| Argomento                          | Contenuto                                                                                                                                                   |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Barre di stato](status-bars.md) | Una *barra di stato* è una finestra orizzontale nella parte inferiore di una finestra padre in cui un'applicazione può visualizzare vari tipi di informazioni sullo stato.<br/> |



 

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
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa"><strong>CreateStatusWindow</strong></a></td>
<td>Crea una finestra di stato, in genere utilizzata per visualizzare lo stato di un'applicazione. La finestra viene in genere visualizzata nella parte inferiore della finestra padre e contiene il testo specificato.
<blockquote>
[!Note]<br />
questa funzione è obsoleta. In <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa"><strong>alternativa, usare CreateWindow.</strong></a>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a></td>
<td>La <a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>funzione DrawStatusText</strong></a> disegna il testo specificato nello stile di una finestra di stato con bordi.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-menuhelp"><strong>MenuHelp</strong></a></td>
<td>Elabora <a href="/windows/desktop/menurc/wm-menuselect"><strong>WM_MENUSELECT</strong></a> e <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> messaggi e visualizza il testo della Guida sul menu corrente nella finestra di stato specificata.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a>Messaggi



| Argomento                                               | Contenuto                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SB \_ GETBORDERS**](sb-getborders.md)             | Recupera le larghezze correnti dei bordi orizzontale e verticale di una finestra di stato. <br/>                                                                                                  |
| [**SB \_ GETICON**](sb-geticon.md)                   | Recupera l'icona per una parte in una barra di stato. <br/>                                                                                                                                           |
| [**SB \_ GETPARTS**](sb-getparts.md)                 | Recupera un conteggio delle parti in una finestra di stato. Il messaggio recupera anche la coordinata del bordo destro del numero specificato di parti. <br/>                                         |
| [**SB \_ GETRECT**](sb-getrect.md)                   | Recupera il rettangolo di delimitazione di una parte in una finestra di stato. <br/>                                                                                                                           |
| [**SB \_ GETTEXT**](sb-gettext.md)                   | Il [**messaggio \_ SB GETTEXT**](sb-gettext.md) recupera il testo dalla parte specificata di una finestra di stato. <br/>                                                                             |
| [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md)       | Il [**messaggio SB \_ GETTEXTLENGTH**](sb-gettextlength.md) recupera la lunghezza, in caratteri, del testo dalla parte specificata di una finestra di stato. <br/>                                   |
| [**SB \_ GETTIPTEXT**](sb-gettiptext.md)             | Recupera il testo della descrizione comando per una parte in una barra di stato. La barra di stato deve essere creata con lo stile [**SBT \_ TOOLTIPS**](status-bar-styles.md) per abilitare le descrizioni comando. <br/>         |
| [**SB \_ GETUNICODEFORMAT**](sb-getunicodeformat.md) | Recupera il flag di formato carattere Unicode per il controllo . <br/>                                                                                                                             |
| [**SB \_ ISSIMPLE**](sb-issimple.md)                 | Controlla un controllo barra di stato per determinare se è in modalità semplice. <br/>                                                                                                                        |
| [**SB \_ SETBKCOLOR**](sb-setbkcolor.md)             | Imposta il colore di sfondo in una barra di stato. <br/>                                                                                                                                               |
| [**SB \_ SETICON**](sb-seticon.md)                   | Imposta l'icona per una parte in una barra di stato. <br/>                                                                                                                                                |
| [**SB \_ SETMINHEIGHT**](sb-setminheight.md)         | Imposta l'altezza minima dell'area di disegno di una finestra di stato. <br/>                                                                                                                               |
| [**SB \_ SETPARTS**](sb-setparts.md)                 | Imposta il numero di parti in una finestra di stato e la coordinata del bordo destro di ogni parte. <br/>                                                                                           |
| [**SB \_ SETTEXT**](sb-settext.md)                   | Il messaggio SETTEXT SB \_ imposta il testo nella parte specificata di una finestra di stato.<br/>                                                                                                           |
| [**SB \_ SETTIPTEXT**](sb-settiptext.md)             | Imposta il testo della descrizione comando per una parte in una barra di stato. La barra di stato deve essere stata creata con lo [**stile SBT \_ TOOLTIPS**](status-bar-styles.md) per abilitare le descrizioni comando.<br/>        |
| [**SB \_ SETUNICODEFORMAT**](sb-setunicodeformat.md) | Imposta il flag di formato carattere Unicode per il controllo . Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover creare nuovamente il controllo. <br/> |
| [**SB \_ SIMPLE**](sb-simple.md)                     | Specifica se una finestra di stato visualizza testo semplice o tutte le parti della finestra impostate da un messaggio [**\_ SETPARTS SB**](sb-setparts.md) precedente. <br/>                                       |



 

### <a name="notifications"></a>Notifiche



| Argomento                                                 | Contenuto                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CLICK (barra di stato)](nm-click-status-bar.md)     | Notifica alla finestra padre di un controllo barra di stato che l'utente ha fatto clic con il pulsante sinistro del mouse all'interno del controllo. [NM \_ CLICK (barra di stato)](nm-click-status-bar.md) viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)<br/>              |
| [NM \_ DBLCLK (barra di stato)](nm-dblclk-status-bar.md)   | Notifica alla finestra padre di un controllo barra di stato che l'utente ha fatto doppio clic sul pulsante sinistro del mouse all'interno del controllo. Questa notifica viene inviata sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)<br/>                                       |
| [NM \_ RCLICK (barra di stato)](nm-rclick-status-bar.md)   | Notifica alla finestra padre di un controllo barra di stato che l'utente ha fatto clic con il pulsante destro del mouse all'interno del controllo. Questa notifica viene inviata sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)<br/>                                             |
| [NM \_ RDBLCLK (barra di stato)](nm-rdblclk-status-bar.md) | Notifica alle finestre padre di un controllo barra di stato che l'utente ha fatto doppio clic sul pulsante destro del mouse all'interno del controllo. [NM \_ RDBLCLK (barra di stato)](nm-rdblclk-status-bar.md) viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)<br/> |
| [SBN \_ SIMPLEMODECHANGE](sbn-simplemodechange.md)     | Inviato da un controllo barra di stato quando la modalità semplice cambia a causa di un [**messaggio SB \_**](sb-simple.md) SIMPLE. Questa notifica viene inviata sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                        |



 

### <a name="constants"></a>Costanti



| Argomento                                      | Contenuto                                                                                                              |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Stili della barra di stato](status-bar-styles.md) | Questa sezione elenca gli stili, oltre agli stili di finestra standard, supportati dai controlli *barra di* stato. <br/> |



 

 

