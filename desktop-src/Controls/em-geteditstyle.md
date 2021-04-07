---
title: Messaggio di EM_GETEDITSTYLE (RichEdit. h)
description: Recupera i flag di stile di modifica correnti.
ms.assetid: 568e51a4-0767-4a59-bf34-bc0281b5fe65
keywords:
- Controlli di Windows Message EM_GETEDITSTYLE
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9264338ea525cc0165e1ed942d90654b95357b17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048479"
---
# <a name="em_geteditstyle-message"></a><span data-ttu-id="3e431-104">\_Messaggio di riedito em</span><span class="sxs-lookup"><span data-stu-id="3e431-104">EM\_GETEDITSTYLE message</span></span>

<span data-ttu-id="3e431-105">Recupera i flag di stile di modifica correnti.</span><span class="sxs-lookup"><span data-stu-id="3e431-105">Retrieves the current edit style flags.</span></span>

## <a name="parameters"></a><span data-ttu-id="3e431-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e431-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e431-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3e431-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e431-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3e431-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3e431-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3e431-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e431-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3e431-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e431-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e431-111">Return value</span></span>

<span data-ttu-id="3e431-112">Restituisce i flag di stile di modifica correnti, che possono includere uno o più dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="3e431-112">Returns the current edit style flags, which can include one or more of the following values:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3e431-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3e431-113">Return code</span></span></th>
<th><span data-ttu-id="3e431-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e431-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="3e431-115"><dt><strong>SES_BEEPONMAXTEXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-115"><dt><strong>SES_BEEPONMAXTEXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-116">La funzionalità Rich Edit chiamerà il cicalino di sistema se l'utente tenta di immettere un numero di caratteri superiore al massimo consentito.</span><span class="sxs-lookup"><span data-stu-id="3e431-116">Rich Edit will call the system beeper if the user attempts to enter more than the maximum characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="3e431-117"><dt><strong>SES_BIDI</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-117"><dt><strong>SES_BIDI</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-118">Attiva l'elaborazione bidirezionale.</span><span class="sxs-lookup"><span data-stu-id="3e431-118">Turns on bidirectional processing.</span></span> <span data-ttu-id="3e431-119">Questa operazione viene attivata automaticamente da Rich Edit se uno degli stili della finestra seguenti è attivo: <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RIGHT</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RTLREADING</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_LEFTSCROLLBAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3e431-119">This is automatically turned on by Rich Edit if any of the following window styles are active: <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RIGHT</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RTLREADING</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_LEFTSCROLLBAR</strong></a>.</span></span> <span data-ttu-id="3e431-120">Questa impostazione è tuttavia utile per la gestione di questi stili di finestra quando si usa un'implementazione personalizzata di <a href="/windows/desktop/api/Textserv/nl-textserv-itexthost"><strong>ITextHost</strong></a> (valore predefinito: 0).</span><span class="sxs-lookup"><span data-stu-id="3e431-120">However, this setting is useful for handling these window styles when using a custom implementation of <a href="/windows/desktop/api/Textserv/nl-textserv-itexthost"><strong>ITextHost</strong></a> (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="3e431-121"><dt><strong>SES_CTFALLOWEMBED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-121"><dt><strong>SES_CTFALLOWEMBED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-122"><strong>Windows XP con SP1</strong>: consente l'inserimento di oggetti incorporati tramite TSF (valore predefinito: 0).</span><span class="sxs-lookup"><span data-stu-id="3e431-122"><strong>Windows XP with SP1</strong>: Allow embedded objects to be inserted using TSF (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="3e431-123"><dt><strong>SES_CTFALLOWPROOFING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-123"><dt><strong>SES_CTFALLOWPROOFING</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-124"><strong>Windows XP con SP1</strong>: consente suggerimenti per la prova di TSF (valore predefinito: 0).</span><span class="sxs-lookup"><span data-stu-id="3e431-124"><strong>Windows XP with SP1</strong>: Allows TSF proofing tips (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="3e431-125"><dt><strong>SES_CTFALLOWSMARTTAG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-125"><dt><strong>SES_CTFALLOWSMARTTAG</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-126"><strong>Windows XP con SP1</strong>: consente i suggerimenti per gli SMARTTAG di TSF (valore predefinito: 0).</span><span class="sxs-lookup"><span data-stu-id="3e431-126"><strong>Windows XP with SP1</strong>: Allows TSF SmartTag tips (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="3e431-127"><dt><strong>SES_CTFNOLOCK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-127"><dt><strong>SES_CTFNOLOCK</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-128"><strong>Windows 8</strong>: non consentire l'accesso in lettura/scrittura del blocco TSF.</span><span class="sxs-lookup"><span data-stu-id="3e431-128"><strong>Windows 8</strong>: Do not allow the TSF lock read/write access.</span></span> <span data-ttu-id="3e431-129">Questa operazione sospende l'input di TSF.</span><span class="sxs-lookup"><span data-stu-id="3e431-129">This pauses TSF input.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="3e431-130"><dt><strong>SES_DEFAULTLATINLIGA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-130"><dt><strong>SES_DEFAULTLATINLIGA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-131"><strong>Windows 8</strong>: i tipi di carattere con una legatura Fi vengono visualizzati con le funzionalità OpenType predefinite, ottenendo una tipografia migliorata (impostazione predefinita: 0).</span><span class="sxs-lookup"><span data-stu-id="3e431-131"><strong>Windows 8</strong>: Fonts with an fi ligature are displayed with default OpenType features resulting in improved typography (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="3e431-132"><dt><strong>SES_DRAFTMODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-132"><dt><strong>SES_DRAFTMODE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-133"><strong>Windows XP con SP1</strong>: usare i tipi di carattere della modalità bozza per visualizzare il testo.</span><span class="sxs-lookup"><span data-stu-id="3e431-133"><strong>Windows XP with SP1</strong>: Use draft mode fonts to display text.</span></span> <span data-ttu-id="3e431-134">La modalità bozza è un'opzione di accessibilità in cui il controllo Visualizza il testo con un solo tipo di carattere. il tipo di carattere è determinato dall'impostazione di sistema per il tipo di carattere utilizzato nelle finestre di messaggio.</span><span class="sxs-lookup"><span data-stu-id="3e431-134">Draft mode is an accessibility option where the control displays the text with a single font; the font is determined by the system setting for the font used in message boxes.</span></span> <span data-ttu-id="3e431-135">Ad esempio, gli utenti accessibili possono leggere più facilmente il testo se è uniforme, anziché una combinazione di tipi di carattere e stili (valore predefinito: 0).</span><span class="sxs-lookup"><span data-stu-id="3e431-135">For example, accessible users may read text easier if it is uniform, rather than a mix of fonts and styles (default: 0).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="3e431-136"><dt><strong>SES_EMULATE10</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-136"><dt><strong>SES_EMULATE10</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-137"><strong>Windows 8</strong>: emulare il comportamento richedit 1,0.</span><span class="sxs-lookup"><span data-stu-id="3e431-137"><strong>Windows 8</strong>: Emulate RichEdit 1.0 behavior.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3e431-138">Se si desidera effettivamente questo comportamento, utilizzare il riched32.dll Windows anziché riched20.dll o msftedit.dll.</span><span class="sxs-lookup"><span data-stu-id="3e431-138">If you really want this behavior, use the Windows riched32.dll instead of riched20.dll or msftedit.dll.</span></span> <span data-ttu-id="3e431-139">Riched32.dll aveva più funzionalità.</span><span class="sxs-lookup"><span data-stu-id="3e431-139">Riched32.dll had more functionality.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="3e431-140"><dt><strong>SES_EMULATESYSEDIT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-140"><dt><strong>SES_EMULATESYSEDIT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-141">Quando questo bit è impostato su on, Rich Edit tenta di emulare il controllo di modifica del sistema (valore predefinito: 0).</span><span class="sxs-lookup"><span data-stu-id="3e431-141">When this bit is on, rich edit attempts to emulate the system edit control (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="3e431-142"><dt><strong>SES_EXTENDBACKCOLOR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-142"><dt><strong>SES_EXTENDBACKCOLOR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-143">Estende il colore di sfondo fino ai bordi del rettangolo client (valore predefinito: 0).</span><span class="sxs-lookup"><span data-stu-id="3e431-143">Extends the background color all the way to the edges of the client rectangle (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="3e431-144"><dt><strong>SES_HIDEGRIDLINES</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-144"><dt><strong>SES_HIDEGRIDLINES</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-145"><strong>Windows XP con SP1</strong>: se la larghezza della griglia della tabella è pari a zero, le griglie non vengono visualizzate.</span><span class="sxs-lookup"><span data-stu-id="3e431-145"><strong>Windows XP with SP1</strong>: If the width of table gridlines is zero, gridlines are not displayed.</span></span> <span data-ttu-id="3e431-146">Equivale alla caratteristica Nascondi griglie nel menu tabella di Word (valore predefinito: 0).</span><span class="sxs-lookup"><span data-stu-id="3e431-146">This is equivalent to the hide gridlines feature in Word's table menu (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="3e431-147"><dt><strong>SES_HYPERLINKTOOLTIPS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-147"><dt><strong>SES_HYPERLINKTOOLTIPS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-148"><strong>Windows 8</strong>: quando il cursore si trova su un collegamento, Visualizza una descrizione comando con l'indirizzo del collegamento di destinazione (valore predefinito: 0).</span><span class="sxs-lookup"><span data-stu-id="3e431-148"><strong>Windows 8</strong>: When the cursor is over a link, display a tooltip with the target link address (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="3e431-149"><dt><strong>SES_LOGICALCARET</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-149"><dt><strong>SES_LOGICALCARET</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-150"><strong>Windows 8</strong>: specificare le informazioni logiche sul punto di inserimento anziché una bitmap del cursore, come descritto in <a href="/windows/desktop/api/Textserv/nf-textserv-itexthost-txsetcaretpos"><strong>ITextHost:: TxSetCaretPos</strong></a> (valore predefinito: 0).</span><span class="sxs-lookup"><span data-stu-id="3e431-150"><strong>Windows 8</strong>: Provide logical caret information instead of a caret bitmap as described in <a href="/windows/desktop/api/Textserv/nf-textserv-itexthost-txsetcaretpos"><strong>ITextHost::TxSetCaretPos</strong></a> (default: 0).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="3e431-151"><dt><strong>SES_LOWERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-151"><dt><strong>SES_LOWERCASE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-152">Converte tutti i caratteri di input in minuscolo (valore predefinito: 0).</span><span class="sxs-lookup"><span data-stu-id="3e431-152">Converts all input characters to lowercase (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="3e431-153"><dt><strong>SES_MAPCPS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-153"><dt><strong>SES_MAPCPS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-154">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="3e431-154">Obsolete.</span></span> <span data-ttu-id="3e431-155">Non usare.</span><span class="sxs-lookup"><span data-stu-id="3e431-155">Do not use.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="3e431-156"><dt><strong>SES_MULTISELECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-156"><dt><strong>SES_MULTISELECT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-157"><strong>Windows 8</strong>: abilitare la selezione a più selezioni con le selezioni del mouse effettuate mentre viene premuto il tasto Ctrl (valore predefinito: 0).</span><span class="sxs-lookup"><span data-stu-id="3e431-157"><strong>Windows 8</strong>: Enable multiselection with individual mouse selections made while the Ctrl key is pressed (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="3e431-158"><dt><strong>SES_NOEALINEHEIGHTADJUST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-158"><dt><strong>SES_NOEALINEHEIGHTADJUST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-159"><strong>Windows 8</strong>: non modificare l'altezza della riga per il testo asiatico orientale (valore predefinito: 0 che regola l'altezza della riga del 15%).</span><span class="sxs-lookup"><span data-stu-id="3e431-159"><strong>Windows 8</strong>: Do not adjust line height for East Asian text (default: 0 which adjusts the line height by 15%).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="3e431-160"><dt><strong>SES_NOFOCUSLINKNOTIFY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-160"><dt><strong>SES_NOFOCUSLINKNOTIFY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-161">Invia <a href="en-link.md">EN_LINK</a> notifica da collegamenti che non hanno lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="3e431-161">Sends <a href="en-link.md">EN_LINK</a> notification from links that do not have focus.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="3e431-162"><dt><strong>SES_NOIME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-162"><dt><strong>SES_NOIME</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-163">Non consente gli IME per questa istanza del controllo Rich Edit (valore predefinito: 0).</span><span class="sxs-lookup"><span data-stu-id="3e431-163">Disallows IMEs for this instance of the rich edit control (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="3e431-164"><dt><strong>SES_NOINPUTSEQUENCECHK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-164"><dt><strong>SES_NOINPUTSEQUENCECHK</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-165">Quando questo bit è on, Rich Edit non verifica la sequenza di testo tipizzato.</span><span class="sxs-lookup"><span data-stu-id="3e431-165">When this bit is on, rich edit does not verify the sequence of typed text.</span></span> <span data-ttu-id="3e431-166">Per alcune lingue, ad esempio Thai e vietnamita, è necessario verificare l'ordine di sequenza di input prima di inviarlo all'archivio di backup (valore predefinito: 0).</span><span class="sxs-lookup"><span data-stu-id="3e431-166">Some languages (such as Thai and Vietnamese) require verifying the input sequence order before submitting it to the backing store (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="3e431-167"><dt><strong>SES_SCROLLONKILLFOCUS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-167"><dt><strong>SES_SCROLLONKILLFOCUS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-168">Quando si verifica KillFocus, scorrere fino all'inizio del testo (posizione del carattere uguale a 0) (valore predefinito: 0).</span><span class="sxs-lookup"><span data-stu-id="3e431-168">When KillFocus occurs, scroll to the beginning of the text (character position equal to 0) (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="3e431-169"><dt><strong>SES_SMARTDRAGDROP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-169"><dt><strong>SES_SMARTDRAGDROP</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-170"><strong>Windows 8</strong>: aggiungere o eliminare uno spazio in base al contesto quando si elimina il testo (valore predefinito: 0).</span><span class="sxs-lookup"><span data-stu-id="3e431-170"><strong>Windows 8</strong>: Add or delete a space according to the context when dropping text (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="3e431-171"><dt><strong>SES_USECRLF</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-171"><dt><strong>SES_USECRLF</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-172">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="3e431-172">Obsolete.</span></span> <span data-ttu-id="3e431-173">Non usare.</span><span class="sxs-lookup"><span data-stu-id="3e431-173">Do not use.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="3e431-174"><dt><strong>SES_WORDDRAGDROP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-174"><dt><strong>SES_WORDDRAGDROP</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-175"><strong>Windows 8</strong>: se Word Select è attivo, verificare che il percorso di rilascio sia in corrispondenza di un confine di parola (valore predefinito: 0).</span><span class="sxs-lookup"><span data-stu-id="3e431-175"><strong>Windows 8</strong>: If word select is active, ensure that the drop location is at a word boundary (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="3e431-176"><dt><strong>SES_UPPERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-176"><dt><strong>SES_UPPERCASE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-177">Converte tutti i caratteri di input in lettere maiuscole (valore predefinito: 0).</span><span class="sxs-lookup"><span data-stu-id="3e431-177">Converts all input characters to uppercase (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="3e431-178"><dt><strong>SES_USEAIMM</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-178"><dt><strong>SES_USEAIMM</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-179">Usa il componente metodo di input IMM attivo fornito con Internet Explorer 4,0 o versione successiva (valore predefinito: 0).</span><span class="sxs-lookup"><span data-stu-id="3e431-179">Uses the Active IMM input method component that ships with Internet Explorer 4.0 or later (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="3e431-180"><dt><strong>SES_USEATFONT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-180"><dt><strong>SES_USEATFONT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-181"><strong>Windows XP con SP1</strong>: usa un tipo di carattere @, progettato per il testo verticale. viene utilizzato con lo stile della finestra <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3e431-181"><strong>Windows XP with SP1</strong>: Uses an @ font, which is designed for vertical text; this is used with the <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> window style.</span></span> <span data-ttu-id="3e431-182">Il nome di un @ font inizia con il simbolo @, ad esempio &quot; @Batang &quot; (valore predefinito: 0, ma viene attivato automaticamente per il layout del testo verticale).</span><span class="sxs-lookup"><span data-stu-id="3e431-182">The name of an @ font begins with the @ symbol, for example, &quot;@Batang&quot; (default: 0, but is automatically turned on for vertical text layout).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="3e431-183"><dt><strong>SES_USECTF</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-183"><dt><strong>SES_USECTF</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-184"><strong>Windows XP con SP1</strong>: attiva il supporto di TSF.</span><span class="sxs-lookup"><span data-stu-id="3e431-184"><strong>Windows XP with SP1</strong>: Turns on TSF support.</span></span> <span data-ttu-id="3e431-185">(valore predefinito: 0)</span><span class="sxs-lookup"><span data-stu-id="3e431-185">(default: 0)</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="3e431-186"><dt><strong>SES_XLTCRCRLFTOCR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e431-186"><dt><strong>SES_XLTCRCRLFTOCR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="3e431-187">Attiva la conversione di CRCRLFs in CRs.</span><span class="sxs-lookup"><span data-stu-id="3e431-187">Turns on translation of CRCRLFs to CRs.</span></span> <span data-ttu-id="3e431-188">Quando questo bit è acceso e viene letto un file, tutte le istanze di CRCRLF verranno convertite internamente in un CRs rigido.</span><span class="sxs-lookup"><span data-stu-id="3e431-188">When this bit is on and a file is read in, all instances of CRCRLF will be converted to hard CRs internally.</span></span> <span data-ttu-id="3e431-189">Questa operazione influirà sul ritorno a capo del testo.</span><span class="sxs-lookup"><span data-stu-id="3e431-189">This will affect the text wrapping.</span></span> <span data-ttu-id="3e431-190">Si noti che se tale file viene salvato come testo normale, il CRs verrà sostituito da CRLFs.</span><span class="sxs-lookup"><span data-stu-id="3e431-190">Note that if such a file is saved as plain text, the CRs will be replaced by CRLFs.</span></span> <span data-ttu-id="3e431-191">Si tratta dello standard. txt per testo normale (valore predefinito: 0, che Elimina CRCRLFs nell'input).</span><span class="sxs-lookup"><span data-stu-id="3e431-191">This is the .txt standard for plain text (default: 0, which deletes CRCRLFs on input).</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="3e431-192">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e431-192">Requirements</span></span>



| <span data-ttu-id="3e431-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e431-193">Requirement</span></span> | <span data-ttu-id="3e431-194">Valore</span><span class="sxs-lookup"><span data-stu-id="3e431-194">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e431-195">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e431-195">Minimum supported client</span></span><br/> | <span data-ttu-id="3e431-196">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3e431-196">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3e431-197">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e431-197">Minimum supported server</span></span><br/> | <span data-ttu-id="3e431-198">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3e431-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3e431-199">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="3e431-199">Redistributable</span></span><br/>          | <span data-ttu-id="3e431-200">Modifica avanzata 3,0</span><span class="sxs-lookup"><span data-stu-id="3e431-200">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="3e431-201">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e431-201">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e431-202"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e431-202"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e431-203">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e431-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e431-204">**\_SETEDITSTYLE em**</span><span class="sxs-lookup"><span data-stu-id="3e431-204">**EM\_SETEDITSTYLE**</span></span>](em-seteditstyle.md)
</dt> </dl>

 

