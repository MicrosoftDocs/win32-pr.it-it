---
title: Modificare gli stili del controllo (winuser. h)
description: Per creare un controllo di modifica usando la funzione CreateWindow o CreateWindowEx, specificare la classe EDIT, le costanti di stile della finestra appropriate e una combinazione degli stili del controllo di modifica seguenti.
ms.assetid: 336c69b7-bc23-4b93-8968-ad63a1703385
topic_type:
- apiref
api_name:
- ES_AUTOHSCROLL
- ES_AUTOVSCROLL
- ES_CENTER
- ES_LEFT
- ES_LOWERCASE
- ES_MULTILINE
- ES_NOHIDESEL
- ES_NUMBER
- ES_OEMCONVERT
- ES_PASSWORD
- ES_READONLY
- ES_RIGHT
- ES_UPPERCASE
- ES_WANTRETURN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 9b255aee665c32f9a14be4946dee0122dad626bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327245"
---
# <a name="edit-control-styles"></a>Modificare gli stili del controllo

Per creare un controllo di modifica usando la funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificare la classe Edit, le costanti di stile della finestra appropriate e una combinazione degli stili del controllo di modifica seguenti. Una volta creato il controllo, questi stili non possono essere modificati, ad eccezione di quanto indicato.

## <a name="example"></a>Esempio

```cpp
LRESULT MsgCreate(HWND hwnd, UINT uMessage, WPARAM wparam, LPARAM lparam)
{
    lparam;
    wparam;
    uMessage;

    // Create Edit control for typing to be sent to server
    if (NULL == (hOutWnd = CreateWindow("EDIT",
                           NULL,
                           WS_BORDER | WS_CHILD | WS_VISIBLE | WS_VSCROLL | ES_LEFT | 
                           ES_MULTILINE | ES_AUTOVSCROLL,
                           0,0,0,0,
                           hwnd,
                           (HMENU) ID_OUTBOX,
                           (HINSTANCE) GetWindowLongPtr(hwnd, GWLP_HINSTANCE),
                           NULL)))
        return FALSE;
    return TRUE;
}
```

Esempio di [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/netds/winsock/ipxchat/IpxChat.c) in GitHub.

## <a name="constants"></a>Costanti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Costante</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl> <dt><strong>ES_AUTOHSCROLL</strong></dt> </dl></td>
<td style="text-align: left;">Scorre automaticamente il testo a destra di 10 caratteri quando l'utente digita un carattere alla fine della riga. Quando l'utente preme il tasto invio, il controllo scorre tutto il testo fino alla posizione zero.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl> <dt><strong>ES_AUTOVSCROLL</strong></dt> </dl></td>
<td style="text-align: left;">Scorre automaticamente il testo verso l'alto di una pagina quando l'utente preme il tasto invio sull'ultima riga.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_CENTER"></span><span id="es_center"></span><dl> <dt><strong>ES_CENTER</strong></dt> </dl></td>
<td style="text-align: left;">Centra il testo in un controllo di modifica a riga singola o su più righe.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_LEFT"></span><span id="es_left"></span><dl> <dt><strong>ES_LEFT</strong></dt> </dl></td>
<td style="text-align: left;">Allinea il testo con il margine sinistro.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_LOWERCASE"></span><span id="es_lowercase"></span><dl> <dt><strong>ES_LOWERCASE</strong></dt> </dl></td>
<td style="text-align: left;">Converte tutti i caratteri in minuscolo perché sono digitati nel controllo di modifica.<br/> Per modificare questo stile dopo che il controllo è stato creato, usare <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl> <dt><strong>ES_MULTILINE</strong></dt> </dl></td>
<td style="text-align: left;">Definisce un controllo di modifica su più righe. Il valore predefinito è il controllo di modifica a riga singola. <br/> Quando il controllo di modifica su più righe si trova in una finestra di dialogo, la risposta predefinita per premere il tasto invio consiste nell'attivare il pulsante predefinito. Per utilizzare il tasto invio come ritorno a capo, utilizzare lo stile <a href="rich-edit-control-styles.md"><strong>ES_WANTRETURN</strong></a> .<br/> Quando il controllo di modifica su più righe non si trova in una finestra di dialogo e viene specificato lo stile <a href="rich-edit-control-styles.md"><strong>ES_AUTOVSCROLL</strong></a> , il controllo di modifica Mostra il maggior numero di righe possibile e scorre verticalmente quando l'utente preme il tasto INVIO. Se non si specifica <strong>ES_AUTOVSCROLL</strong>, il controllo di modifica Mostra il numero di righe possibile e emette un segnale acustico se l'utente preme il tasto INVIO quando non è possibile visualizzare più righe.<br/> Se si specifica lo stile <a href="rich-edit-control-styles.md"><strong>ES_AUTOHSCROLL</strong></a> , il controllo di modifica su più righe scorre orizzontalmente quando il cursore va oltre il bordo destro del controllo. Per avviare una nuova riga, l'utente deve premere il tasto INVIO. Se non si specifica <strong>ES_AUTOHSCROLL</strong>, il controllo esegue automaticamente il wrapping delle parole all'inizio della riga successiva, quando necessario. Viene avviata anche una nuova riga se l'utente preme il tasto INVIO. La dimensione della finestra determina la posizione del WordWrap. Se le dimensioni della finestra cambiano, la posizione Wordwrapping cambia e il testo viene nuovamente visualizzato.<br/> I controlli di modifica su più righe possono avere barre di scorrimento. Un controllo di modifica con barre di scorrimento elabora i propri messaggi della barra di scorrimento. Si noti che i controlli di modifica senza barre di scorrimento scorrono come descritto nei paragrafi precedenti ed elaborano tutti i messaggi di scorrimento inviati dalla finestra padre.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl> <dt><strong>ES_NOHIDESEL</strong></dt> </dl></td>
<td style="text-align: left;">Nega il comportamento predefinito per un controllo di modifica. Il comportamento predefinito nasconde la selezione quando il controllo perde lo stato attivo per l'input e inverte la selezione quando il controllo riceve lo stato attivo per l'input. Se si specifica <a href="rich-edit-control-styles.md"><strong>ES_NOHIDESEL</strong></a>, il testo selezionato viene invertito, anche se il controllo non ha lo stato attivo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_NUMBER"></span><span id="es_number"></span><dl> <dt><strong>ES_NUMBER</strong></dt> </dl></td>
<td style="text-align: left;">Consente di immettere solo le cifre nel controllo di modifica. Si noti che, anche con questo set, è ancora possibile incollare i caratteri non alfanumerici nel controllo di modifica. <br/> Per modificare questo stile dopo che il controllo è stato creato, usare <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br/> Per tradurre il testo immesso nel controllo di modifica in un valore integer, usare la funzione <a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint"><strong>GetDlgItemInt</strong></a> . Per impostare il testo del controllo di modifica sulla rappresentazione di stringa di un intero specificato, utilizzare la funzione <a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint"><strong>SetDlgItemInt</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_OEMCONVERT"></span><span id="es_oemconvert"></span><dl> <dt><strong>ES_OEMCONVERT</strong></dt> </dl></td>
<td style="text-align: left;">Converte il testo immesso nel controllo di modifica. Il testo viene convertito dal set di caratteri di Windows al set di caratteri OEM e quindi di nuovo al set di caratteri di Windows. Ciò assicura la corretta conversione dei caratteri quando l'applicazione chiama la funzione <a href="/windows/desktop/api/winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a> per convertire una stringa di Windows nel controllo di modifica in caratteri OEM. Questo stile è particolarmente utile per i controlli di modifica che contengono nomi file che verranno utilizzati nei file System che non supportano Unicode. <br/> Per modificare questo stile dopo che il controllo è stato creato, usare <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_PASSWORD"></span><span id="es_password"></span><dl> <dt><strong>ES_PASSWORD</strong></dt> </dl></td>
<td style="text-align: left;">Visualizza un asterisco (*) per ogni carattere digitato nel controllo di modifica. Questo stile è valido solo per i controlli di modifica a riga singola. <br/> Per modificare i caratteri visualizzati o impostare o deselezionare questo stile, utilizzare il messaggio <a href="em-setpasswordchar.md"><strong>EM_SETPASSWORDCHAR</strong></a> . <br/>
<blockquote>
[!Note]<br />
Per usare Comctl32.dll versione 6, specificarla in un manifesto. Per altre informazioni sui manifesti, vedere <a href="cookbook-overview.md">Abilitazione degli stili di visualizzazione</a>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_READONLY"></span><span id="es_readonly"></span><dl> <dt><strong>ES_READONLY</strong></dt> </dl></td>
<td style="text-align: left;">Impedisce all'utente di digitare o modificare il testo nel controllo di modifica.<br/> Per modificare lo stile dopo la creazione del controllo, utilizzare il messaggio <a href="em-setreadonly.md"><strong>EM_SETREADONLY</strong></a> . <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_RIGHT"></span><span id="es_right"></span><dl> <dt><strong>ES_RIGHT</strong></dt> </dl></td>
<td style="text-align: left;">Allinea a destra il testo in un controllo di modifica a riga singola o su più righe.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_UPPERCASE"></span><span id="es_uppercase"></span><dl> <dt><strong>ES_UPPERCASE</strong></dt> </dl></td>
<td style="text-align: left;">Converte tutti i caratteri in maiuscolo in quanto sono digitati nel controllo di modifica. <br/> Per modificare questo stile dopo che il controllo è stato creato, usare <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl> <dt><strong>ES_WANTRETURN</strong></dt> </dl></td>
<td style="text-align: left;">Specifica l'inserimento di un ritorno a capo quando l'utente preme il tasto INVIO mentre immette il testo in un controllo di modifica su più righe in una finestra di dialogo. Se non si specifica questo stile, premendo il tasto invio si avrà lo stesso effetto della pressione del pulsante di push predefinito della finestra di dialogo. Questo stile non ha alcun effetto su un controllo di modifica a riga singola. <br/> Per modificare questo stile dopo che il controllo è stato creato, usare <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Winuser. h</dt> </dl> |



