---
title: Messaggi
description: Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per notifiche e messaggi di input del puntatore specifici.
ms.assetid: 65F4DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 076ba9d8b33bf2848d6088c4bac42b60ce9e19646abe5163358f25b063250b9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756953"
---
# <a name="messages"></a>Messaggi

Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per messaggi e notifiche di [input del puntatore specifici.](messages-and-notifications-portal.md)

## <a name="in-this-section"></a>Contenuto della sezione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>[<strong>DM_POINTERHITTEST</strong>] (dm-pointerhittest.md)<br/></td>
<td>Inviato a una finestra, quando viene rilevato l'input del puntatore per la prima volta, per determinare la destinazione di input più probabile per [la manipolazione diretta.](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal) <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_NCPOINTERDOWN</strong>] (wm-ncpointerdown.md)<br/></td>
<td>Pubblicato quando un puntatore contatta l'area non client di una finestra. Il messaggio è destinato alla finestra sulla quale il puntatore contatta. Il puntatore viene acquisito in modo implicito nella finestra in modo che la finestra continui a ricevere input per il puntatore fino a quando non interrompe il contatto. <br/> Se una finestra ha acquisito questo puntatore, questo messaggio non viene pubblicato. Viene invece inviato un [<strong>WM_POINTERDOWN</strong>](wm-pointerdown.md) alla finestra che ha acquisito questo puntatore. <br/>
<blockquote>
[!Important]<br />
Le app desktop devono essere in grado di riconoscere DPI. Se l'app non è in grado di riconoscere DPI, le coordinate dello schermo contenute nei messaggi del puntatore e nelle strutture correlate potrebbero apparire inesatte a causa della virtualizzazione DPI. La virtualizzazione DPI offre il supporto automatico del ridimensionamento per le applicazioni che non supportano DPI ed è attiva per impostazione predefinita (gli utenti possono disattivarla). Per altre informazioni, vedere [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_NCPOINTERUP</strong>] (wm-ncpointerup.md)<br/></td>
<td>Pubblicato quando un puntatore che ha effettuato il contatto sull'area non client di una finestra interrompe il contatto. Il messaggio è destinato alla finestra sulla quale il puntatore contatta e il puntatore è, a quel punto, acquisito in modo implicito nella finestra in modo che la finestra continui a ricevere input per il puntatore fino a quando non interrompe il contatto, inclusa la notifica [<strong>WM_NCPOINTERUP</strong>](wm-ncpointerup.md). <br/> Se una finestra ha acquisito questo puntatore, questo messaggio non viene pubblicato. Viene invece inviato un [<strong>WM_POINTERUP</strong>](wm-pointerup.md) alla finestra che ha acquisito questo puntatore. <br/>
<blockquote>
[!Important]<br />
Le app desktop devono essere in grado di riconoscere DPI. Se l'app non è in grado di riconoscere DPI, le coordinate dello schermo contenute nei messaggi del puntatore e nelle strutture correlate potrebbero apparire inesatte a causa della virtualizzazione DPI. La virtualizzazione DPI offre il supporto automatico del ridimensionamento per le applicazioni che non supportano DPI ed è attiva per impostazione predefinita (gli utenti possono disattivarla). Per altre informazioni, vedere [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_NCPOINTERUPDATE</strong>] (wm-ncpointerupdate.md)<br/></td>
<td>Pubblicato per fornire un aggiornamento su un puntatore che ha effettuato il contatto sull'area non client di una finestra o quando un contatto non incapsulato al passaggio del mouse si sposta sull'area non client di una finestra. Durante il passaggio del puntatore, il messaggio è destinato a qualsiasi finestra su cui si trova il puntatore. Mentre il puntatore è in contatto con la superficie, il puntatore viene acquisito in modo implicito nella finestra sulla quale il puntatore ha contattato e tale finestra continua a ricevere input per il puntatore fino a quando non interrompe il contatto. <br/> Se una finestra ha acquisito questo puntatore, questo messaggio non viene pubblicato. Viene invece inviato un [<strong>WM_POINTERUPDATE</strong>](wm-pointerupdate.md) alla finestra che ha acquisito questo puntatore.<br/>
<blockquote>
[!Important]<br />
Le app desktop devono essere in grado di riconoscere DPI. Se l'app non è in grado di riconoscere DPI, le coordinate dello schermo contenute nei messaggi del puntatore e nelle strutture correlate potrebbero apparire inesatte a causa della virtualizzazione DPI. La virtualizzazione DPI offre il supporto automatico del ridimensionamento per le applicazioni che non supportano DPI ed è attiva per impostazione predefinita (gli utenti possono disattivarla). Per altre informazioni, vedere [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_PARENTNOTIFY</strong>] (wm-parentnotify.md)<br/></td>
<td>Inviato a una finestra quando si verifica un'azione significativa in una finestra discendente. Questo messaggio viene ora esteso per includere<strong>l'evento</strong>[ WM_POINTERDOWN ](wm-pointerdown.md). Quando viene creata la finestra figlio, il sistema invia [<strong>WM_PARENTNOTIFY</strong>](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) subito prima della funzione [<strong>CreateWindow</strong>](/windows/win32/api/winuser/nf-winuser-createwindowa) o [<strong>CreateWindowEx</strong>](/windows/win32/api/winuser/nf-winuser-createwindowexa) che crea la finestra. Quando la finestra figlio viene distrutta, il sistema invia il messaggio prima di qualsiasi elaborazione per eliminare la finestra.<br/> Una finestra riceve questo messaggio tramite la funzione [<strong>WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)). <br/>
<blockquote>
[!Important]<br />
Le app desktop devono essere in grado di riconoscere DPI. Se l'app non è in grado di riconoscere DPI, le coordinate dello schermo contenute nei messaggi del puntatore e nelle strutture correlate potrebbero apparire inesatte a causa della virtualizzazione DPI. La virtualizzazione DPI offre il supporto automatico del ridimensionamento per le applicazioni che non supportano DPI ed è attiva per impostazione predefinita (gli utenti possono disattivarla). Per altre informazioni, vedere [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERACTIVATE</strong>] (wm-pointeractivate.md)<br/></td>
<td>Inviato a una finestra inattiva quando un puntatore primario genera un<strong>[WM_POINTERDOWN</strong>](wm-pointerdown.md) sulla finestra. Finché il messaggio rimane non gestito, si sposta verso l'alto nella catena di finestre padre fino a raggiungere la finestra di primo livello. Le applicazioni possono rispondere a questo messaggio per specificare se devono essere attivate.<br/> Una finestra riceve questo messaggio tramite la funzione [<strong>WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)). <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERCAPTURECHANGED</strong>] (wm-pointercapturechanged.md)<br/></td>
<td>Inviato a una finestra che sta perdendo l'acquisizione di un puntatore di input.<br/> Una finestra riceve questo messaggio tramite la funzione [<strong>WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERDEVICECHANGE</strong>] (wm-pointerdevicechange.md)<br/></td>
<td>Inviato a una finestra quando viene apportata una modifica alle impostazioni di un monitor a cui è collegato un digitalizzatore. Questo messaggio contiene informazioni relative al ridimensionamento della modalità di visualizzazione. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERDEVICEINRANGE</strong>] (wm-pointerdeviceinrange.md)<br/></td>
<td>Inviato a una finestra quando viene rilevato un dispositivo puntatore nell'intervallo di un digitalizzatore di input. Questo messaggio contiene informazioni relative al dispositivo e alla relativa prossimità. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERDEVICEOUTOFRANGE</strong>] (wm-pointerdeviceoutofrange.md)<br/></td>
<td>Inviato a una finestra quando un dispositivo puntatore ha lasciato l'intervallo di un digitalizzatore di input. Questo messaggio contiene informazioni relative al dispositivo e alla relativa prossimità. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERDOWN</strong>] (wm-pointerdown.md)<br/></td>
<td>Pubblicato quando un puntatore contatta l'area client di una finestra. Questo messaggio di input è destinato alla finestra su cui il puntatore contatta e il puntatore viene acquisito in modo implicito nella finestra in modo che la finestra continui a ricevere input per il puntatore fino a quando non interrompe il contatto. <br/> Una finestra riceve questo messaggio tramite la funzione [<strong>WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).<br/>
<blockquote>
[!Important]<br />
Le app desktop devono essere in grado di riconoscere DPI. Se l'app non è in grado di riconoscere DPI, le coordinate dello schermo contenute nei messaggi del puntatore e nelle strutture correlate potrebbero apparire inesatte a causa della virtualizzazione DPI. La virtualizzazione DPI offre il supporto automatico del ridimensionamento per le applicazioni che non supportano DPI ed è attiva per impostazione predefinita (gli utenti possono disattivarla). Per altre informazioni, vedere [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERENTER</strong>] (wm-pointerenter.md)<br/></td>
<td>Inviato a una finestra quando un nuovo puntatore entra nell'intervallo di rilevamento sulla finestra (passaggio del mouse) o quando un puntatore esistente si sposta entro i limiti della finestra. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERLEAVE</strong>] (wm-pointerleave.md)<br/></td>
<td>Inviato a una finestra quando un puntatore lascia l'intervallo di rilevamento sulla finestra (passaggio del mouse) o quando un puntatore si sposta all'esterno dei limiti della finestra. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERROUTEDAWAY</strong>] (wm-pointerroutedaway.md)<br/></td>
<td>Si verifica nel processo che riceve l'input quando l'input del puntatore viene indirizzato a un altro processo.<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERROUTEDRELEASED</strong>] (wm-pointerroutedreleased.md)<br/></td>
<td>Inviato a tutti i processi (configurati per il concatenamento tra processi tramite [<strong>AddContentWithCrossProcessChaining</strong>](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) e non gestendo attualmente l'input del puntatore) mai associati a un ID puntatore specifico, quando viene ricevuto un messaggio [<strong>WM_POINTERUP</strong>](wm-pointerup.md) nel processo corrente. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERROUTEDTO</strong>] (wm-pointerroutedto.md)<br/></td>
<td>Inviato quando l'input del puntatore in corso, per un ID puntatore esistente, passa da un processo a un altro attraverso il contenuto configurato per il concatenamento tra processi ([<strong>AddContentWithCrossProcessChaining</strong>](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERUP</strong>] (wm-pointerup.md)<br/></td>
<td>Pubblicato quando un puntatore che ha effettuato il contatto sull'area client di una finestra interrompe il contatto. Questo messaggio di input è destinato alla finestra su cui il puntatore contatta e il puntatore viene acquisito in modo implicito nella finestra in modo che la finestra continui a ricevere messaggi di input,<strong>inclusa</strong>la notifica [ WM_POINTERUP ](wm-pointerup.md) per il puntatore fino a quando non interrompe il contatto. <br/> Una finestra riceve questo messaggio tramite la funzione [<strong>WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)). <br/>
<blockquote>
[!Important]<br />
Le app desktop devono essere in grado di riconoscere DPI. Se l'app non è in grado di riconoscere DPI, le coordinate dello schermo contenute nei messaggi del puntatore e nelle strutture correlate potrebbero apparire inesatte a causa della virtualizzazione DPI. La virtualizzazione DPI offre il supporto automatico del ridimensionamento per le applicazioni che non supportano DPI ed è attiva per impostazione predefinita (gli utenti possono disattivarla). Per altre informazioni, vedere [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERUPDATE</strong>] (wm-pointerupdate.md)<br/></td>
<td>Inviato per fornire un aggiornamento su un puntatore che ha effettuato il contatto sull'area client di una finestra o su un puntatore non incapsulato al passaggio del mouse sull'area client di una finestra. Durante il passaggio del puntatore, il messaggio è destinato a qualsiasi finestra su cui si trova il puntatore. Mentre il puntatore è in contatto con la superficie, il puntatore viene acquisito in modo implicito nella finestra sulla quale il puntatore ha contattato e tale finestra continua a ricevere input per il puntatore fino a quando non interrompe il contatto. <br/>
<blockquote>
[!Important]<br />
Le app desktop devono essere in grado di riconoscere DPI. Se l'app non è in grado di riconoscere DPI, le coordinate dello schermo contenute nei messaggi del puntatore e nelle strutture correlate potrebbero apparire inesatte a causa della virtualizzazione DPI. La virtualizzazione DPI offre il supporto automatico del ridimensionamento per le applicazioni che non supportano DPI ed è attiva per impostazione predefinita (gli utenti possono disattivarla). Per altre informazioni, vedere [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERWHEEL</strong>] (wm-pointerwheel.md)<br/></td>
<td>Inserito nella finestra con lo stato attivo della tastiera in primo piano quando viene ruotata una rotellina di scorrimento. <br/> Una finestra riceve questo messaggio tramite la relativa funzione [<strong>WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).<br/>
<blockquote>
[!Important]<br />
Le app desktop devono essere in grado di riconoscere DPI. Se l'app non è in grado di riconoscere DPI, le coordinate dello schermo contenute nei messaggi dell'indicatore di misura e nelle strutture correlate potrebbero apparire inaccurate a causa della virtualizzazione DPI. La virtualizzazione DPI offre il supporto per il ridimensionamento automatico per le applicazioni che non sono in grado di riconoscere DPI ed è attiva per impostazione predefinita (gli utenti possono disattivarla). Per altre informazioni, vedere [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERHWHEEL</strong>] (wm-pointerhwheel.md)<br/></td>
<td>Inviato alla finestra con lo stato attivo della tastiera in primo piano quando viene ruotata una rotellina di scorrimento orizzontale. <br/> Una finestra riceve questo messaggio tramite la relativa funzione [<strong>WindowProc</strong>](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).<br/>
<blockquote>
[!Important]<br />
Le app desktop devono essere in grado di riconoscere DPI. Se l'app non è in grado di riconoscere DPI, le coordinate dello schermo contenute nei messaggi dell'indicatore di misura e nelle strutture correlate potrebbero apparire inaccurate a causa della virtualizzazione DPI. La virtualizzazione DPI offre il supporto per il ridimensionamento automatico per le applicazioni che non sono in grado di riconoscere DPI ed è attiva per impostazione predefinita (gli utenti possono disattivarla). Per altre informazioni, vedere [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_TOUCHHITTESTING</strong>] (wm-touchhittesting.md)<br/></td>
<td>Inviato a una finestra con un tocco verso il basso per determinare la destinazione del tocco più probabile. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sul messaggio di input del puntatore](wmpointer-reference.md)
</dt> </dl>

 

