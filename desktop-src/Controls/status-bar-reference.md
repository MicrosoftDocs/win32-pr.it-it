---
title: Barra di stato
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli barra di stato.
ms.assetid: 77923055-9d00-4528-bda7-b602a26b577f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca6e46f1c573b75439cc10aa27ae3245e47e3de9
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103731490"
---
# <a name="status-bar"></a>Barra di stato

Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli barra di stato.

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
<td>Crea una finestra di stato, che in genere viene utilizzata per visualizzare lo stato di un'applicazione. La finestra viene in genere visualizzata nella parte inferiore della finestra padre e contiene il testo specificato.
<blockquote>
[!Note]<br />
questa funzione è obsoleta. In alternativa, usare <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa"><strong>CreateWindow</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a></td>
<td>La funzione <a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a> disegna il testo specificato nello stile di una finestra di stato con bordi.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-menuhelp"><strong>MenuHelp</strong></a></td>
<td>Elabora <a href="/windows/desktop/menurc/wm-menuselect"><strong>WM_MENUSELECT</strong></a> e <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> i messaggi e visualizza il testo della guida sul menu corrente nella finestra di stato specificata.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a>Messaggi



| Argomento                                               | Contenuto                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SB \_ GETborders**](sb-getborders.md)             | Recupera le larghezze correnti dei bordi orizzontali e verticali di una finestra di stato. <br/>                                                                                                  |
| [**SB \_ GETicon**](sb-geticon.md)                   | Recupera l'icona per una parte in una barra di stato. <br/>                                                                                                                                           |
| [**SB \_ GETparts**](sb-getparts.md)                 | Recupera un conteggio delle parti in una finestra di stato. Il messaggio recupera inoltre la coordinata del bordo destro del numero di parti specificato. <br/>                                         |
| [**SB \_ GETrect**](sb-getrect.md)                   | Recupera il rettangolo di delimitazione di una parte in una finestra di stato. <br/>                                                                                                                           |
| [**SB \_ GETtext**](sb-gettext.md)                   | Il messaggio [**SB \_ gettext**](sb-gettext.md) Recupera il testo dalla parte specificata di una finestra di stato. <br/>                                                                             |
| [**\_GETTEXTLENGTH SB**](sb-gettextlength.md)       | Il messaggio [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) recupera la lunghezza, in caratteri, del testo dalla parte specificata di una finestra di stato. <br/>                                   |
| [**\_GETTIPTEXT SB**](sb-gettiptext.md)             | Recupera il testo della descrizione comando per una parte in una barra di stato. La barra di stato deve essere creata con lo stile della [**\_ Descrizione comando SBT**](status-bar-styles.md) per abilitare le descrizioni comandi. <br/>         |
| [**\_GETUNICODEFORMAT SB**](sb-getunicodeformat.md) | Recupera il flag del formato carattere Unicode per il controllo. <br/>                                                                                                                             |
| [**\_semplice SB**](sb-issimple.md)                 | Controlla un controllo barra di stato per determinare se è in modalità semplice. <br/>                                                                                                                        |
| [**\_SETBKCOLOR SB**](sb-setbkcolor.md)             | Imposta il colore di sfondo di una barra di stato. <br/>                                                                                                                                               |
| [**\_icona SB**](sb-seticon.md)                   | Imposta l'icona di una parte in una barra di stato. <br/>                                                                                                                                                |
| [**\_SETMINHEIGHT SB**](sb-setminheight.md)         | Imposta l'altezza minima dell'area di disegno di una finestra di stato. <br/>                                                                                                                               |
| [**sottoparti SB \_**](sb-setparts.md)                 | Imposta il numero di parti in una finestra di stato e la coordinata del bordo destro di ogni parte. <br/>                                                                                           |
| [**\_testo SB**](sb-settext.md)                   | Il messaggio SB SetText \_ imposta il testo nella parte specificata di una finestra di stato.<br/>                                                                                                           |
| [**\_SETTIPTEXT SB**](sb-settiptext.md)             | Imposta il testo della descrizione comando per una parte in una barra di stato. La barra di stato deve essere stata creata con lo stile [**SBT \_ Tooltips**](status-bar-styles.md) per abilitare le descrizioni comandi.<br/>        |
| [**\_SETUNICODEFORMAT SB**](sb-setunicodeformat.md) | Imposta il flag di formato carattere Unicode per il controllo. Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover ricreare il controllo. <br/> |
| [**\_semplice SB**](sb-simple.md)                     | Specifica se una finestra di stato Visualizza testo semplice o Visualizza tutte le parti della finestra impostate da un messaggio precedente della [**\_ parte SB**](sb-setparts.md) . <br/>                                       |



 

### <a name="notifications"></a>Notifiche



| Argomento                                                 | Contenuto                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_Clic su Nm (barra di stato)](nm-click-status-bar.md)     | Notifica alla finestra padre di un controllo barra di stato che l'utente ha fatto clic con il pulsante sinistro del mouse all'interno del controllo. [Nm \_ FARE clic su (barra di stato)](nm-click-status-bar.md) viene inviato sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .<br/>              |
| [NM \_ DBLCLK (barra di stato)](nm-dblclk-status-bar.md)   | Notifica alla finestra padre di un controllo barra di stato che l'utente ha fatto doppio clic con il pulsante sinistro del mouse all'interno del controllo. Questa notifica viene inviata sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .<br/>                                       |
| [NM \_ RCLICK (barra di stato)](nm-rclick-status-bar.md)   | Notifica alla finestra padre di un controllo barra di stato che l'utente ha fatto clic con il pulsante destro del mouse all'interno del controllo. Questa notifica viene inviata sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .<br/>                                             |
| [NM \_ RDBLCLK (barra di stato)](nm-rdblclk-status-bar.md) | Notifica alla finestra padre di un controllo barra di stato che l'utente ha fatto doppio clic con il pulsante destro del mouse all'interno del controllo. [Nm \_ RDBLCLK (barra di stato)](nm-rdblclk-status-bar.md) viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .<br/> |
| [\_SIMPLEMODECHANGE SBN](sbn-simplemodechange.md)     | Inviato da un controllo barra di stato quando la modalità semplice cambia a causa di un messaggio [**\_ semplice SB**](sb-simple.md) . Questa notifica viene inviata sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) . <br/>                                                        |



 

### <a name="constants"></a>Costanti



| Argomento                                      | Contenuto                                                                                                              |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Stili della barra di stato](status-bar-styles.md) | Questa sezione elenca gli stili, oltre agli stili standard della finestra, supportati dai controlli *barra di stato* . <br/> |



 

 

