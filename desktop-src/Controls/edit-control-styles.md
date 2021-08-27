---
title: Modificare gli stili dei controlli (Winuser.h)
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
ms.openlocfilehash: 5e1a62dba617f73efdec992f843856d80a5b39bf
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468588"
---
# <a name="edit-control-styles"></a>Modificare gli stili dei controlli

Per creare un controllo di modifica usando la [**funzione CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) specificare la classe EDIT, le costanti di stile della finestra appropriate e una combinazione degli stili del controllo di modifica seguenti. Dopo la creazione del controllo, questi stili non possono essere modificati, se non come specificato.

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

Esempio di [Windows esempi classici](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/netds/winsock/ipxchat/IpxChat.c) in GitHub.

## <a name="constants"></a>Costanti


| Costante | Descrizione | 
|----------|-------------|
| <span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl><dt><strong>ES_AUTOHSCROLL</strong></dt></dl> | Scorre automaticamente il testo a destra di 10 caratteri quando l'utente ha immesso un carattere alla fine della riga. Quando l'utente preme INVIO, il controllo scorre tutto il testo fino alla posizione zero.<br /> | 
| <span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl><dt><strong>ES_AUTOVSCROLL</strong></dt></dl> | Scorre automaticamente il testo verso l'alto di una pagina quando l'utente preme INVIO nell'ultima riga.<br /> | 
| <span id="ES_CENTER"></span><span id="es_center"></span><dl><dt><strong>ES_CENTER</strong></dt></dl> | Centra il testo in un controllo di modifica a riga singola o su più righe.<br /> | 
| <span id="ES_LEFT"></span><span id="es_left"></span><dl><dt><strong>ES_LEFT</strong></dt></dl> | Allinea il testo al margine sinistro.<br /> | 
| <span id="ES_LOWERCASE"></span><span id="es_lowercase"></span><dl><dt><strong>ES_LOWERCASE</strong></dt></dl> | Converte tutti i caratteri in lettere minuscole durante la digitazione nel controllo di modifica.<br /> Per modificare questo stile dopo la creazione del controllo, usare <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br /> | 
| <span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl><dt><strong>ES_MULTILINE</strong></dt></dl> | Designa un controllo di modifica su più righe. Il valore predefinito è il controllo di modifica a riga singola. <br /> Quando il controllo di modifica su più righe si trova in una finestra di dialogo, la risposta predefinita alla pressione del tasto INVIO è attivare il pulsante predefinito. Per usare il tasto INVIO come ritorno a capo, usare lo <a href="rich-edit-control-styles.md"><strong>ES_WANTRETURN</strong></a> testo.<br /> Quando il controllo di modifica su più righe non si trova in una finestra di dialogo e viene specificato lo stile <a href="rich-edit-control-styles.md"><strong>ES_AUTOVSCROLL,</strong></a> il controllo di modifica visualizza il maggior numero possibile di righe e scorre verticalmente quando l'utente preme INVIO. Se non si specifica <strong>ES_AUTOVSCROLL</strong>, il controllo di modifica visualizza il maggior numero possibile di righe e esepe se l'utente preme INVIO quando non è possibile visualizzare altre righe.<br /> Se si specifica lo <a href="rich-edit-control-styles.md"><strong>stile ES_AUTOHSCROLL,</strong></a> il controllo di modifica su più righe scorre automaticamente orizzontalmente quando il punto di selezione va oltre il bordo destro del controllo. Per avviare una nuova riga, l'utente deve premere INVIO. Se non si specifica <strong>ES_AUTOHSCROLL</strong>, il controllo esegue automaticamente il wrapping delle parole all'inizio della riga successiva, se necessario. Viene avviata anche una nuova riga se l'utente preme INVIO. Le dimensioni della finestra determinano la posizione del wordwrap. Se le dimensioni della finestra cambiano, la posizione del ritorno a capo cambia e il testo viene visualizzato nuovamente.<br /> I controlli di modifica su più righe possono avere barre di scorrimento. Un controllo di modifica con barre di scorrimento elabora i propri messaggi della barra di scorrimento. Si noti che i controlli di modifica senza barre di scorrimento scorrono come descritto nei paragrafi precedenti ed elaborano tutti i messaggi di scorrimento inviati dalla finestra padre.<br /> | 
| <span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl><dt><strong>ES_NOHIDESEL</strong></dt></dl> | Nega il comportamento predefinito per un controllo di modifica. Il comportamento predefinito nasconde la selezione quando il controllo perde lo stato attivo per l'input e inverte la selezione quando il controllo riceve lo stato attivo. Se si specifica <a href="rich-edit-control-styles.md"><strong>ES_NOHIDESEL</strong></a>, il testo selezionato viene invertito, anche se il controllo non ha lo stato attivo.<br /> | 
| <span id="ES_NUMBER"></span><span id="es_number"></span><dl><dt><strong>ES_NUMBER</strong></dt></dl> | Consente l'immissione di solo cifre nel controllo di modifica. Si noti che, anche con questo set, è comunque possibile incollare le non cifre nel controllo di modifica. <br /> Per modificare questo stile dopo la creazione del controllo, usare <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br /> Per convertire il testo immesso nel controllo di modifica in un valore intero, usare la <a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint"><strong>funzione GetDlgItemInt.</strong></a> Per impostare il testo del controllo di modifica sulla rappresentazione di stringa di un intero specificato, usare la <a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint"><strong>funzione SetDlgItemInt.</strong></a><br /> | 
| <span id="ES_OEMCONVERT"></span><span id="es_oemconvert"></span><dl><dt><strong>ES_OEMCONVERT</strong></dt></dl> | Converte il testo immesso nel controllo di modifica. Il testo viene convertito dal set di Windows al set di caratteri OEM e quindi al set Windows set di caratteri. Ciò garantisce la conversione corretta dei caratteri quando l'applicazione chiama la funzione <a href="/windows/desktop/api/winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a> per convertire una Windows stringa nel controllo di modifica in caratteri OEM. Questo stile è particolarmente utile per i controlli di modifica che contengono nomi di file che verranno usati nei file system che non supportano Unicode. <br /> Per modificare questo stile dopo la creazione del controllo, usare <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>. <br /> | 
| <span id="ES_PASSWORD"></span><span id="es_password"></span><dl><dt><strong>ES_PASSWORD</strong></dt></dl> | Visualizza un asterisco (*) per ogni carattere digitato nel controllo di modifica. Questo stile è valido solo per i controlli di modifica a riga singola. <br /> Per modificare i caratteri visualizzati o impostare o cancellare questo stile, usare il EM_SETPASSWORDCHAR <a href="em-setpasswordchar.md"><strong>messaggio.</strong></a> <br /><blockquote>[!Note]<br />Per usare Comctl32.dll versione 6, specificarla in un manifesto. Per altre informazioni sui manifesti, vedere <a href="cookbook-overview.md">Abilitazione degli stili di visualizzazione</a>.</blockquote><br /> | 
| <span id="ES_READONLY"></span><span id="es_readonly"></span><dl><dt><strong>ES_READONLY</strong></dt></dl> | Impedisce all'utente di digitare o modificare il testo nel controllo di modifica.<br /> Per modificare questo stile dopo la creazione del controllo, usare il EM_SETREADONLY <a href="em-setreadonly.md"><strong>messaggio.</strong></a> <br /> | 
| <span id="ES_RIGHT"></span><span id="es_right"></span><dl><dt><strong>ES_RIGHT</strong></dt></dl> | Allinea a destra il testo in un controllo di modifica a riga singola o su più righe.<br /> | 
| <span id="ES_UPPERCASE"></span><span id="es_uppercase"></span><dl><dt><strong>ES_UPPERCASE</strong></dt></dl> | Converte tutti i caratteri in lettere maiuscole durante la digitazione nel controllo di modifica. <br /> Per modificare questo stile dopo la creazione del controllo, usare <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br /> | 
| <span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl><dt><strong>ES_WANTRETURN</strong></dt></dl> | Specifica l'inserimento di un ritorno a capo quando l'utente preme INVIO durante l'immissione di testo in un controllo di modifica su più righe in una finestra di dialogo. Se non si specifica questo stile, la pressione del tasto INVIO ha lo stesso effetto della pressione del pulsante di pressione predefinito della finestra di dialogo. Questo stile non ha alcun effetto su un controllo di modifica a riga singola. <br /> Per modificare questo stile dopo la creazione del controllo, usare <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br /> | 




## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Winuser</dt> </dl> |



