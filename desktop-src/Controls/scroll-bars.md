---
title: ScrollBar
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con le barre di scorrimento.
ms.assetid: vs|controls|~\controls\scrollbars\scrollbars.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38cf549a37fd5d4a271f6e12642a9bfd45b65d79
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730607"
---
# <a name="scroll-bar"></a>ScrollBar

Questa sezione contiene informazioni sugli elementi di programmazione usati con le barre di scorrimento. Una finestra può visualizzare un oggetto dati, ad esempio un documento o una bitmap, più grande dell'area client della finestra. Quando viene fornito con una *barra di scorrimento*, l'utente può scorrere un oggetto dati nell'area client per visualizzare le parti dell'oggetto che si estendono oltre i bordi della finestra.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                      | Contenuto                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sulle barre di scorrimento](about-scroll-bars.md) | Una barra di scorrimento è costituita da un albero ombreggiato con un pulsante freccia a ogni estremità e una *casella di scorrimento* (talvolta denominata Thumb) tra i pulsanti freccia.<br/>                                                                                                                                                                     |
| [Uso delle barre di scorrimento](using-scroll-bars.md) | Quando si crea una finestra sovrapposta, popup o figlio, è possibile aggiungere barre di scorrimento standard usando la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e specificando [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles), [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles)o entrambi gli stili.<br/> |



 

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
<td><a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a></td>
<td>La funzione <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a> Abilita o Disabilita una o entrambe le frecce della barra di scorrimento. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo"><strong>GetScrollBarInfo</strong></a></td>
<td>La funzione <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo"><strong>GetScrollBarInfo</strong></a> recupera le informazioni sulla barra di scorrimento specificata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a></td>
<td>La funzione <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> recupera i parametri di una barra di scorrimento, incluse le posizioni di scorrimento minime e massime, le dimensioni della pagina e la posizione della casella di scorrimento (Thumb).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a></td>
<td>La funzione <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> recupera la posizione corrente della casella di scorrimento (Thumb) nella barra di scorrimento specificata. La posizione corrente è un valore relativo che dipende dall'intervallo di scorrimento corrente. Se, ad esempio, l'intervallo di scorrimento è compreso tra 0 e 100 e la casella di scorrimento si trova al centro della barra, la posizione corrente è 50.
<blockquote>
[!Note]<br />
La funzione <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> è fornita per compatibilità con le versioni precedenti. Le nuove applicazioni devono usare la funzione <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a></td>
<td>La funzione <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> recupera le posizioni correnti minime e massime della casella di scorrimento (Thumb) per la barra di scorrimento specificata.
<blockquote>
[!Note]<br />
La funzione <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> viene fornita solo per la compatibilità. Le nuove applicazioni devono usare la funzione <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-scrolldc"><strong>ScrollDC</strong></a></td>
<td>La funzione <a href="/windows/desktop/api/Winuser/nf-winuser-scrolldc"><strong>ScrollDC</strong></a> scorre un rettangolo di bit orizzontalmente e verticalmente. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindow"><strong>ScrollWindow</strong></a></td>
<td>La funzione <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindow"><strong>ScrollWindow</strong></a> scorre il contenuto dell'area client della finestra specificata.
<blockquote>
[!Note]<br />
La funzione <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindow"><strong>ScrollWindow</strong></a> è fornita per compatibilità con le versioni precedenti. Le nuove applicazioni devono usare la funzione <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindowex"><strong>ScrollWindowEx</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindowex"><strong>ScrollWindowEx</strong></a></td>
<td>La funzione <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindowex"><strong>ScrollWindowEx</strong></a> scorre il contenuto dell'area client della finestra specificata. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a></td>
<td>La funzione <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> imposta i parametri di una barra di scorrimento, incluse le posizioni di scorrimento minime e massime, le dimensioni della pagina e la posizione della casella di scorrimento (Thumb). La funzione ridisegnato inoltre la barra di scorrimento, se richiesto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a></td>
<td>La funzione <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> imposta la posizione della casella di scorrimento (Thumb) nella barra di scorrimento specificata e, se richiesto, ridisegni la barra di scorrimento in modo da riflettere la nuova posizione della casella di scorrimento.
<blockquote>
[!Note]<br />
La funzione <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> è fornita per compatibilità con le versioni precedenti. Le nuove applicazioni devono usare la funzione <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a></td>
<td>La funzione <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> imposta le posizioni minime e massime della casella di scorrimento per la barra di scorrimento specificata.
<blockquote>
[!Note]<br />
La funzione <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> è fornita per compatibilità con le versioni precedenti. Le nuove applicazioni devono usare la funzione <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a></td>
<td>La funzione <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a> Mostra o nasconde la barra di scorrimento specificata. <br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a>Messaggi



| Argomento                                                 | Contenuto                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_frecce abilitate SBM \_**](sbm-enable-arrows.md)      | Un'applicazione invia il messaggio di [**\_ Abilitazione della \_ freccia SBM**](sbm-enable-arrows.md) per abilitare o disabilitare una o entrambe le frecce di un controllo barra di scorrimento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**\_GETPOS SBM**](sbm-getpos.md)                     | Il [**messaggio \_ GETPOS SBM**](sbm-getpos.md) viene inviato per recuperare la posizione corrente della casella di scorrimento di un controllo barra di scorrimento. La posizione corrente è un valore relativo che dipende dall'intervallo di scorrimento corrente. Se, ad esempio, l'intervallo di scorrimento è compreso tra 0 e 100 e la casella di scorrimento si trova al centro della barra, la posizione corrente è 50. <br/> Le applicazioni non devono inviare direttamente questo messaggio. Devono invece usare la funzione [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) . Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Le applicazioni che implementano un controllo barra di scorrimento personalizzato devono rispondere a questi messaggi affinché la funzione **GetScrollPos** funzioni correttamente.<br/> |
| [**GetRange di SBM \_**](sbm-getrange.md)                 | Il messaggio [**SBM \_ GetRange**](sbm-getrange.md) viene inviato per recuperare i valori di posizione minimo e massimo per il controllo barra di scorrimento. <br/> Le applicazioni non devono inviare direttamente questo messaggio. Devono invece usare la funzione [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) . Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Le applicazioni che implementano un controllo barra di scorrimento personalizzato devono rispondere a questi messaggi affinché la funzione **GetScrollRange** funzioni correttamente.<br/>                                                                                                                                                                                                              |
| [**\_GETSCROLLBARINFO SBM**](sbm-getscrollbarinfo.md) | Inviato da un'applicazione per recuperare informazioni sulla barra di scorrimento specificata.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**\_GETSCROLLINFO SBM**](sbm-getscrollinfo.md)       | Il [**messaggio \_ GETSCROLLINFO SBM**](sbm-getscrollinfo.md) viene inviato per recuperare i parametri di una barra di scorrimento. <br/> Le applicazioni non devono inviare direttamente questo messaggio. Devono invece usare la funzione [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) . Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Le applicazioni che implementano un controllo barra di scorrimento personalizzato devono rispondere a questi messaggi affinché la funzione **GetScrollInfo** funzioni correttamente.<br/>                                                                                                                                                                                                                                           |
| [**\_SETPOS SBM**](sbm-setpos.md)                     | Il [**messaggio \_ SETPOS SBM**](sbm-setpos.md) viene inviato per impostare la posizione della casella di scorrimento (Thumb) e, se richiesto, per ricreare la barra di scorrimento in modo da riflettere la nuova posizione della casella di scorrimento. <br/> Le applicazioni non devono inviare direttamente questo messaggio. Devono invece usare la funzione [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) . Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Le applicazioni che implementano un controllo barra di scorrimento personalizzato devono rispondere a questi messaggi affinché la funzione **SetScrollPos** funzioni correttamente.<br/>                                                                                                                                                                  |
| [**\_SEtrange SBM**](sbm-setrange.md)                 | Il messaggio [**SBM \_ SetRange**](sbm-setrange.md) viene inviato per impostare i valori di posizione minimo e massimo per il controllo barra di scorrimento. <br/> Le applicazioni non devono inviare direttamente questo messaggio. Devono invece usare la funzione [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) . Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Le applicazioni che implementano un controllo barra di scorrimento personalizzato devono rispondere a questi messaggi affinché la funzione **SetScrollRange** funzioni correttamente.<br/>                                                                                                                                                                                                                   |
| [**\_SETRANGEREDRAW SBM**](sbm-setrangeredraw.md)     | Un'applicazione invia il [**messaggio \_ SETRANGEREDRAW SBM**](sbm-setrangeredraw.md) a un controllo barra di scorrimento per impostare i valori minimo e massimo della posizione e per ricreare il controllo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**\_SETSCROLLINFO SBM**](sbm-setscrollinfo.md)       | Il [**messaggio \_ SETSCROLLINFO SBM**](sbm-setscrollinfo.md) viene inviato per impostare i parametri di una barra di scorrimento. <br/> Le applicazioni non devono inviare direttamente questo messaggio. Devono invece usare la funzione [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) . Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Le applicazioni che implementano un controllo barra di scorrimento personalizzato devono rispondere a questi messaggi affinché la funzione **SetScrollInfo** funzioni correttamente.<br/>                                                                                                                                                                                                                                            |



 

### <a name="notifications"></a>Notifiche



| Argomento                                                 | Contenuto                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CTLCOLORSCROLLBAR WM**](wm-ctlcolorscrollbar.md) | Il messaggio [**WM \_ CTLCOLORSCROLLBAR**](wm-ctlcolorscrollbar.md) viene inviato alla finestra padre di un controllo barra di scorrimento quando il controllo sta per essere disegnato. Rispondendo a questo messaggio, la finestra padre può utilizzare l'handle del contesto di visualizzazione per impostare il colore di sfondo del controllo barra di scorrimento. <br/> Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . <br/> |
| [**\_HSCROLL WM**](wm-hscroll.md)                     | Il messaggio [**WM \_ HSCROLL**](wm-hscroll.md) viene inviato a una finestra quando si verifica un evento Scroll nella barra di scorrimento orizzontale standard della finestra. Questo messaggio viene inoltre inviato al proprietario di un controllo barra di scorrimento orizzontale quando si verifica un evento di scorrimento nel controllo. <br/> Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . <br/>                                        |
| [**\_VSCROLL WM**](wm-vscroll.md)                     | Il messaggio [**WM \_ VSCROLL**](wm-vscroll.md) viene inviato a una finestra quando si verifica un evento Scroll nella barra di scorrimento verticale standard della finestra. Questo messaggio viene inoltre inviato al proprietario di un controllo barra di scorrimento verticale quando si verifica un evento di scorrimento nel controllo. <br/> Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . <br/>                                            |



 

### <a name="structures"></a>Strutture



| Argomento                                  | Contenuto                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) | La struttura [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) contiene informazioni sulla barra di scorrimento.<br/>                                                                                                                                                                                                                                                           |
| [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)       | La struttura [**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo) contiene i parametri della barra di scorrimento che devono essere impostati dalla funzione [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) (o dal messaggio [**SBM \_ SetScrollInfo**](sbm-setscrollinfo.md) ) o recuperati dalla funzione [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) (o dal messaggio [**SBM \_ GetScrollInfo**](sbm-getscrollinfo.md) ). <br/> |



 

### <a name="constants"></a>Costanti



| Argomento                                                      | Contenuto                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Stili del controllo barra di scorrimento](scroll-bar-control-styles.md) | Per creare un controllo barra di scorrimento usando la funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificare la classe ScrollBar, le costanti di stile della finestra appropriate e una combinazione degli stili del controllo barra di scorrimento seguenti. Alcuni stili creano un controllo barra di scorrimento che usa una larghezza o un'altezza predefinita. Tuttavia, quando si chiama **CreateWindow** o **CreateWindowEx**, è necessario specificare sempre le coordinate x e y e le altre dimensioni della barra di scorrimento. <br/> |



 

 

