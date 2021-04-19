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
# <a name="edit-control-styles"></a><span data-ttu-id="5daf1-103">Modificare gli stili del controllo</span><span class="sxs-lookup"><span data-stu-id="5daf1-103">Edit Control Styles</span></span>

<span data-ttu-id="5daf1-104">Per creare un controllo di modifica usando la funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificare la classe Edit, le costanti di stile della finestra appropriate e una combinazione degli stili del controllo di modifica seguenti.</span><span class="sxs-lookup"><span data-stu-id="5daf1-104">To create an edit control using the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specify the EDIT class, appropriate window style constants, and a combination of the following edit control styles.</span></span> <span data-ttu-id="5daf1-105">Una volta creato il controllo, questi stili non possono essere modificati, ad eccezione di quanto indicato.</span><span class="sxs-lookup"><span data-stu-id="5daf1-105">After the control has been created, these styles cannot be modified, except as noted.</span></span>

## <a name="example"></a><span data-ttu-id="5daf1-106">Esempio</span><span class="sxs-lookup"><span data-stu-id="5daf1-106">Example</span></span>

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

<span data-ttu-id="5daf1-107">Esempio di [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/netds/winsock/ipxchat/IpxChat.c) in GitHub.</span><span class="sxs-lookup"><span data-stu-id="5daf1-107">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/netds/winsock/ipxchat/IpxChat.c) on GitHub.</span></span>

## <a name="constants"></a><span data-ttu-id="5daf1-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="5daf1-108">Constants</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="5daf1-109">Costante</span><span class="sxs-lookup"><span data-stu-id="5daf1-109">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="5daf1-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5daf1-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl> <span data-ttu-id="5daf1-111"><dt><strong>ES_AUTOHSCROLL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5daf1-111"><dt><strong>ES_AUTOHSCROLL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5daf1-112">Scorre automaticamente il testo a destra di 10 caratteri quando l'utente digita un carattere alla fine della riga.</span><span class="sxs-lookup"><span data-stu-id="5daf1-112">Automatically scrolls text to the right by 10 characters when the user types a character at the end of the line.</span></span> <span data-ttu-id="5daf1-113">Quando l'utente preme il tasto invio, il controllo scorre tutto il testo fino alla posizione zero.</span><span class="sxs-lookup"><span data-stu-id="5daf1-113">When the user presses the ENTER key, the control scrolls all text back to position zero.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl> <span data-ttu-id="5daf1-114"><dt><strong>ES_AUTOVSCROLL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5daf1-114"><dt><strong>ES_AUTOVSCROLL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5daf1-115">Scorre automaticamente il testo verso l'alto di una pagina quando l'utente preme il tasto invio sull'ultima riga.</span><span class="sxs-lookup"><span data-stu-id="5daf1-115">Automatically scrolls text up one page when the user presses the ENTER key on the last line.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_CENTER"></span><span id="es_center"></span><dl> <span data-ttu-id="5daf1-116"><dt><strong>ES_CENTER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5daf1-116"><dt><strong>ES_CENTER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5daf1-117">Centra il testo in un controllo di modifica a riga singola o su più righe.</span><span class="sxs-lookup"><span data-stu-id="5daf1-117">Centers text in a single-line or multiline edit control.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_LEFT"></span><span id="es_left"></span><dl> <span data-ttu-id="5daf1-118"><dt><strong>ES_LEFT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5daf1-118"><dt><strong>ES_LEFT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5daf1-119">Allinea il testo con il margine sinistro.</span><span class="sxs-lookup"><span data-stu-id="5daf1-119">Aligns text with the left margin.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_LOWERCASE"></span><span id="es_lowercase"></span><dl> <span data-ttu-id="5daf1-120"><dt><strong>ES_LOWERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5daf1-120"><dt><strong>ES_LOWERCASE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5daf1-121">Converte tutti i caratteri in minuscolo perché sono digitati nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="5daf1-121">Converts all characters to lowercase as they are typed into the edit control.</span></span><br/> <span data-ttu-id="5daf1-122">Per modificare questo stile dopo che il controllo è stato creato, usare <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5daf1-122">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl> <span data-ttu-id="5daf1-123"><dt><strong>ES_MULTILINE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5daf1-123"><dt><strong>ES_MULTILINE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5daf1-124">Definisce un controllo di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="5daf1-124">Designates a multiline edit control.</span></span> <span data-ttu-id="5daf1-125">Il valore predefinito è il controllo di modifica a riga singola.</span><span class="sxs-lookup"><span data-stu-id="5daf1-125">The default is single-line edit control.</span></span> <br/> <span data-ttu-id="5daf1-126">Quando il controllo di modifica su più righe si trova in una finestra di dialogo, la risposta predefinita per premere il tasto invio consiste nell'attivare il pulsante predefinito.</span><span class="sxs-lookup"><span data-stu-id="5daf1-126">When the multiline edit control is in a dialog box, the default response to pressing the ENTER key is to activate the default button.</span></span> <span data-ttu-id="5daf1-127">Per utilizzare il tasto invio come ritorno a capo, utilizzare lo stile <a href="rich-edit-control-styles.md"><strong>ES_WANTRETURN</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5daf1-127">To use the ENTER key as a carriage return, use the <a href="rich-edit-control-styles.md"><strong>ES_WANTRETURN</strong></a> style.</span></span><br/> <span data-ttu-id="5daf1-128">Quando il controllo di modifica su più righe non si trova in una finestra di dialogo e viene specificato lo stile <a href="rich-edit-control-styles.md"><strong>ES_AUTOVSCROLL</strong></a> , il controllo di modifica Mostra il maggior numero di righe possibile e scorre verticalmente quando l'utente preme il tasto INVIO.</span><span class="sxs-lookup"><span data-stu-id="5daf1-128">When the multiline edit control is not in a dialog box and the <a href="rich-edit-control-styles.md"><strong>ES_AUTOVSCROLL</strong></a> style is specified, the edit control shows as many lines as possible and scrolls vertically when the user presses the ENTER key.</span></span> <span data-ttu-id="5daf1-129">Se non si specifica <strong>ES_AUTOVSCROLL</strong>, il controllo di modifica Mostra il numero di righe possibile e emette un segnale acustico se l'utente preme il tasto INVIO quando non è possibile visualizzare più righe.</span><span class="sxs-lookup"><span data-stu-id="5daf1-129">If you do not specify <strong>ES_AUTOVSCROLL</strong>, the edit control shows as many lines as possible and beeps if the user presses the ENTER key when no more lines can be displayed.</span></span><br/> <span data-ttu-id="5daf1-130">Se si specifica lo stile <a href="rich-edit-control-styles.md"><strong>ES_AUTOHSCROLL</strong></a> , il controllo di modifica su più righe scorre orizzontalmente quando il cursore va oltre il bordo destro del controllo.</span><span class="sxs-lookup"><span data-stu-id="5daf1-130">If you specify the <a href="rich-edit-control-styles.md"><strong>ES_AUTOHSCROLL</strong></a> style, the multiline edit control automatically scrolls horizontally when the caret goes past the right edge of the control.</span></span> <span data-ttu-id="5daf1-131">Per avviare una nuova riga, l'utente deve premere il tasto INVIO.</span><span class="sxs-lookup"><span data-stu-id="5daf1-131">To start a new line, the user must press the ENTER key.</span></span> <span data-ttu-id="5daf1-132">Se non si specifica <strong>ES_AUTOHSCROLL</strong>, il controllo esegue automaticamente il wrapping delle parole all'inizio della riga successiva, quando necessario.</span><span class="sxs-lookup"><span data-stu-id="5daf1-132">If you do not specify <strong>ES_AUTOHSCROLL</strong>, the control automatically wraps words to the beginning of the next line when necessary.</span></span> <span data-ttu-id="5daf1-133">Viene avviata anche una nuova riga se l'utente preme il tasto INVIO.</span><span class="sxs-lookup"><span data-stu-id="5daf1-133">A new line is also started if the user presses the ENTER key.</span></span> <span data-ttu-id="5daf1-134">La dimensione della finestra determina la posizione del WordWrap.</span><span class="sxs-lookup"><span data-stu-id="5daf1-134">The window size determines the position of the Wordwrap.</span></span> <span data-ttu-id="5daf1-135">Se le dimensioni della finestra cambiano, la posizione Wordwrapping cambia e il testo viene nuovamente visualizzato.</span><span class="sxs-lookup"><span data-stu-id="5daf1-135">If the window size changes, the Wordwrapping position changes and the text is redisplayed.</span></span><br/> <span data-ttu-id="5daf1-136">I controlli di modifica su più righe possono avere barre di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="5daf1-136">Multiline edit controls can have scroll bars.</span></span> <span data-ttu-id="5daf1-137">Un controllo di modifica con barre di scorrimento elabora i propri messaggi della barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="5daf1-137">An edit control with scroll bars processes its own scroll bar messages.</span></span> <span data-ttu-id="5daf1-138">Si noti che i controlli di modifica senza barre di scorrimento scorrono come descritto nei paragrafi precedenti ed elaborano tutti i messaggi di scorrimento inviati dalla finestra padre.</span><span class="sxs-lookup"><span data-stu-id="5daf1-138">Note that edit controls without scroll bars scroll as described in the previous paragraphs and process any scroll messages sent by the parent window.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl> <span data-ttu-id="5daf1-139"><dt><strong>ES_NOHIDESEL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5daf1-139"><dt><strong>ES_NOHIDESEL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5daf1-140">Nega il comportamento predefinito per un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="5daf1-140">Negates the default behavior for an edit control.</span></span> <span data-ttu-id="5daf1-141">Il comportamento predefinito nasconde la selezione quando il controllo perde lo stato attivo per l'input e inverte la selezione quando il controllo riceve lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="5daf1-141">The default behavior hides the selection when the control loses the input focus and inverts the selection when the control receives the input focus.</span></span> <span data-ttu-id="5daf1-142">Se si specifica <a href="rich-edit-control-styles.md"><strong>ES_NOHIDESEL</strong></a>, il testo selezionato viene invertito, anche se il controllo non ha lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="5daf1-142">If you specify <a href="rich-edit-control-styles.md"><strong>ES_NOHIDESEL</strong></a>, the selected text is inverted, even if the control does not have the focus.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_NUMBER"></span><span id="es_number"></span><dl> <span data-ttu-id="5daf1-143"><dt><strong>ES_NUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5daf1-143"><dt><strong>ES_NUMBER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5daf1-144">Consente di immettere solo le cifre nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="5daf1-144">Allows only digits to be entered into the edit control.</span></span> <span data-ttu-id="5daf1-145">Si noti che, anche con questo set, è ancora possibile incollare i caratteri non alfanumerici nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="5daf1-145">Note that, even with this set, it is still possible to paste non-digits into the edit control.</span></span> <br/> <span data-ttu-id="5daf1-146">Per modificare questo stile dopo che il controllo è stato creato, usare <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5daf1-146">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/> <span data-ttu-id="5daf1-147">Per tradurre il testo immesso nel controllo di modifica in un valore integer, usare la funzione <a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint"><strong>GetDlgItemInt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5daf1-147">To translate text that was entered into the edit control to an integer value, use the <a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint"><strong>GetDlgItemInt</strong></a> function.</span></span> <span data-ttu-id="5daf1-148">Per impostare il testo del controllo di modifica sulla rappresentazione di stringa di un intero specificato, utilizzare la funzione <a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint"><strong>SetDlgItemInt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5daf1-148">To set the text of the edit control to the string representation of a specified integer, use the <a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint"><strong>SetDlgItemInt</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_OEMCONVERT"></span><span id="es_oemconvert"></span><dl> <span data-ttu-id="5daf1-149"><dt><strong>ES_OEMCONVERT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5daf1-149"><dt><strong>ES_OEMCONVERT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5daf1-150">Converte il testo immesso nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="5daf1-150">Converts text entered in the edit control.</span></span> <span data-ttu-id="5daf1-151">Il testo viene convertito dal set di caratteri di Windows al set di caratteri OEM e quindi di nuovo al set di caratteri di Windows.</span><span class="sxs-lookup"><span data-stu-id="5daf1-151">The text is converted from the Windows character set to the OEM character set and then back to the Windows character set.</span></span> <span data-ttu-id="5daf1-152">Ciò assicura la corretta conversione dei caratteri quando l'applicazione chiama la funzione <a href="/windows/desktop/api/winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a> per convertire una stringa di Windows nel controllo di modifica in caratteri OEM.</span><span class="sxs-lookup"><span data-stu-id="5daf1-152">This ensures proper character conversion when the application calls the <a href="/windows/desktop/api/winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a> function to convert a Windows string in the edit control to OEM characters.</span></span> <span data-ttu-id="5daf1-153">Questo stile è particolarmente utile per i controlli di modifica che contengono nomi file che verranno utilizzati nei file System che non supportano Unicode.</span><span class="sxs-lookup"><span data-stu-id="5daf1-153">This style is most useful for edit controls that contain file names that will be used on file systems that do not support Unicode.</span></span> <br/> <span data-ttu-id="5daf1-154">Per modificare questo stile dopo che il controllo è stato creato, usare <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5daf1-154">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_PASSWORD"></span><span id="es_password"></span><dl> <span data-ttu-id="5daf1-155"><dt><strong>ES_PASSWORD</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5daf1-155"><dt><strong>ES_PASSWORD</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5daf1-156">Visualizza un asterisco (\*) per ogni carattere digitato nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="5daf1-156">Displays an asterisk (\*) for each character typed into the edit control.</span></span> <span data-ttu-id="5daf1-157">Questo stile è valido solo per i controlli di modifica a riga singola.</span><span class="sxs-lookup"><span data-stu-id="5daf1-157">This style is valid only for single-line edit controls.</span></span> <br/> <span data-ttu-id="5daf1-158">Per modificare i caratteri visualizzati o impostare o deselezionare questo stile, utilizzare il messaggio <a href="em-setpasswordchar.md"><strong>EM_SETPASSWORDCHAR</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5daf1-158">To change the characters that is displayed, or set or clear this style, use the <a href="em-setpasswordchar.md"><strong>EM_SETPASSWORDCHAR</strong></a> message.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5daf1-159">Per usare Comctl32.dll versione 6, specificarla in un manifesto.</span><span class="sxs-lookup"><span data-stu-id="5daf1-159">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="5daf1-160">Per altre informazioni sui manifesti, vedere <a href="cookbook-overview.md">Abilitazione degli stili di visualizzazione</a>.</span><span class="sxs-lookup"><span data-stu-id="5daf1-160">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_READONLY"></span><span id="es_readonly"></span><dl> <span data-ttu-id="5daf1-161"><dt><strong>ES_READONLY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5daf1-161"><dt><strong>ES_READONLY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5daf1-162">Impedisce all'utente di digitare o modificare il testo nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="5daf1-162">Prevents the user from typing or editing text in the edit control.</span></span><br/> <span data-ttu-id="5daf1-163">Per modificare lo stile dopo la creazione del controllo, utilizzare il messaggio <a href="em-setreadonly.md"><strong>EM_SETREADONLY</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5daf1-163">To change this style after the control has been created, use the <a href="em-setreadonly.md"><strong>EM_SETREADONLY</strong></a> message.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_RIGHT"></span><span id="es_right"></span><dl> <span data-ttu-id="5daf1-164"><dt><strong>ES_RIGHT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5daf1-164"><dt><strong>ES_RIGHT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5daf1-165">Allinea a destra il testo in un controllo di modifica a riga singola o su più righe.</span><span class="sxs-lookup"><span data-stu-id="5daf1-165">Right-aligns text in a single-line or multiline edit control.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_UPPERCASE"></span><span id="es_uppercase"></span><dl> <span data-ttu-id="5daf1-166"><dt><strong>ES_UPPERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5daf1-166"><dt><strong>ES_UPPERCASE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5daf1-167">Converte tutti i caratteri in maiuscolo in quanto sono digitati nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="5daf1-167">Converts all characters to uppercase as they are typed into the edit control.</span></span> <br/> <span data-ttu-id="5daf1-168">Per modificare questo stile dopo che il controllo è stato creato, usare <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5daf1-168">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl> <span data-ttu-id="5daf1-169"><dt><strong>ES_WANTRETURN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5daf1-169"><dt><strong>ES_WANTRETURN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="5daf1-170">Specifica l'inserimento di un ritorno a capo quando l'utente preme il tasto INVIO mentre immette il testo in un controllo di modifica su più righe in una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="5daf1-170">Specifies that a carriage return be inserted when the user presses the ENTER key while entering text into a multiline edit control in a dialog box.</span></span> <span data-ttu-id="5daf1-171">Se non si specifica questo stile, premendo il tasto invio si avrà lo stesso effetto della pressione del pulsante di push predefinito della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="5daf1-171">If you do not specify this style, pressing the ENTER key has the same effect as pressing the dialog box's default push button.</span></span> <span data-ttu-id="5daf1-172">Questo stile non ha alcun effetto su un controllo di modifica a riga singola.</span><span class="sxs-lookup"><span data-stu-id="5daf1-172">This style has no effect on a single-line edit control.</span></span> <br/> <span data-ttu-id="5daf1-173">Per modificare questo stile dopo che il controllo è stato creato, usare <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5daf1-173">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="5daf1-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5daf1-174">Requirements</span></span>



| <span data-ttu-id="5daf1-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="5daf1-175">Requirement</span></span> | <span data-ttu-id="5daf1-176">Valore</span><span class="sxs-lookup"><span data-stu-id="5daf1-176">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5daf1-177">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5daf1-177">Header</span></span><br/> | <dl> <span data-ttu-id="5daf1-178"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="5daf1-178"><dt>Winuser.h</dt></span></span> </dl> |



