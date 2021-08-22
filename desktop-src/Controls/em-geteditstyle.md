---
title: EM_GETEDITSTYLE messaggio (Richedit.h)
description: Recupera i flag di stile di modifica correnti.
ms.assetid: 568e51a4-0767-4a59-bf34-bc0281b5fe65
keywords:
- EM_GETEDITSTYLE di controllo Windows messaggio
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
ms.openlocfilehash: cb34e4912ff00d76abf8db4c631296836ad9adaf83853aa064c34b11e7f71e20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019709"
---
# <a name="em_geteditstyle-message"></a>Messaggio \_ EM GETEDITSTYLE

Recupera i flag di stile di modifica correnti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce i flag di stile di modifica correnti, che possono includere uno o più dei valori seguenti:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Codice restituito</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>SES_BEEPONMAXTEXT</strong></dt> </dl></td>
<td>Rich Edit chiamerà il beeper di sistema se l'utente tenta di immettere più caratteri del massimo.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_BIDI</strong></dt> </dl></td>
<td>Attiva l'elaborazione bidirezionale. Questa opzione viene attivata automaticamente da Rich Edit se uno degli stili di finestra seguenti è attivo: <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RIGHT</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RTLREADING</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_LEFTSCROLLBAR</strong></a>. Questa impostazione è tuttavia utile per gestire questi stili di finestra quando si usa un'implementazione personalizzata di <a href="/windows/desktop/api/Textserv/nl-textserv-itexthost"><strong>ITextHost</strong></a> (impostazione predefinita: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_CTFALLOWEMBED</strong></dt> </dl></td>
<td><strong>Windows XP con SP1:</strong>consente l'inserimento di oggetti incorporati tramite TSF (impostazione predefinita: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_CTFALLOWPROOFING</strong></dt> </dl></td>
<td><strong>Windows XP con SP1:</strong>consente suggerimenti per gli strumenti di correzione di TSF (impostazione predefinita: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_CTFALLOWSMARTTAG</strong></dt> </dl></td>
<td><strong>Windows XP con SP1:</strong>consente suggerimenti smarttag TSF (impostazione predefinita: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_CTFNOLOCK</strong></dt> </dl></td>
<td><strong>Windows 8:</strong>non consentire l'accesso in lettura/scrittura del blocco TSF. Ciò sospende l'input TSF. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_DEFAULTLATINLIGA</strong></dt> </dl></td>
<td><strong>Windows 8:</strong>i tipi di carattere con una legatura fi vengono visualizzati con le funzionalità OpenType predefinite, con conseguente miglioramento della tipografia (impostazione predefinita: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_DRAFTMODE</strong></dt> </dl></td>
<td><strong>Windows XP con SP1:</strong>usare i tipi di carattere in modalità bozza per visualizzare il testo. La modalità bozza è un'opzione di accessibilità in cui il controllo visualizza il testo con un singolo tipo di carattere. il tipo di carattere è determinato dall'impostazione di sistema per il tipo di carattere usato nelle finestre di messaggio. Ad esempio, gli utenti accessibili possono leggere il testo più facilmente se è uniforme, anziché una combinazione di tipi di carattere e stili (impostazione predefinita: 0). <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_EMULATE10</strong></dt> </dl></td>
<td><strong>Windows 8:</strong>emulare il comportamento di RichEdit 1.0. <br/>
<blockquote>
[!Note]<br />
Se si vuole effettivamente questo comportamento, usare il Windows riched32.dll anziché riched20.dll o msftedit.dll. Riched32.dll aveva più funzionalità.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_EMULATESYSEDIT</strong></dt> </dl></td>
<td>Quando questo bit è on, Rich Edit tenta di emulare il controllo di modifica del sistema (impostazione predefinita: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_EXTENDBACKCOLOR</strong></dt> </dl></td>
<td>Estende il colore di sfondo fino ai bordi del rettangolo client (impostazione predefinita: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_HIDEGRIDLINES</strong></dt> </dl></td>
<td><strong>Windows XP con SP1:</strong>se la larghezza delle linee della griglia della tabella è zero, le linee della griglia non vengono visualizzate. Equivale alla funzionalità Nascondi griglia nel menu tabella di Word (impostazione predefinita: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_HYPERLINKTOOLTIPS</strong></dt> </dl></td>
<td><strong>Windows 8:</strong>quando il cursore si trova su un collegamento, visualizzare una descrizione comando con l'indirizzo del collegamento di destinazione (impostazione predefinita: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_LOGICALCARET</strong></dt> </dl></td>
<td><strong>Windows 8:</strong>fornire informazioni sul punto di accesso logico anziché una bitmap del punto di caret come descritto in <a href="/windows/desktop/api/Textserv/nf-textserv-itexthost-txsetcaretpos"><strong>ITextHost::TxSetCaretPos</strong></a> (impostazione predefinita: 0). <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_LOWERCASE</strong></dt> </dl></td>
<td>Converte tutti i caratteri di input in lettere minuscole (impostazione predefinita: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_MAPCPS</strong></dt> </dl></td>
<td>Obsoleta. Non usare.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_MULTISELECT</strong></dt> </dl></td>
<td><strong>Windows 8:</strong>abilitare la selezione multipla con singole selezioni del mouse effettuate mentre si preme CTRL (impostazione predefinita: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_NOEALINEHEIGHTADJUST</strong></dt> </dl></td>
<td><strong>Windows 8:</strong>non regolare l'altezza della riga per il testo dell'Asia orientale (impostazione predefinita: 0 che regola l'altezza della riga del 15%). <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_NOFOCUSLINKNOTIFY</strong></dt> </dl></td>
<td>Invia <a href="en-link.md">EN_LINK</a> notifica dai collegamenti che non hanno lo stato attivo.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_NOIME</strong></dt> </dl></td>
<td>Non consente gli IME per questa istanza del controllo Rich Edit (impostazione predefinita: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_NOINPUTSEQUENCECHK</strong></dt> </dl></td>
<td>Quando questo bit è on, Rich Edit non verifica la sequenza di testo digitato. Alcune lingue, ad esempio tailandese e taiwanese, richiedono la verifica dell'ordine della sequenza di input prima di inviarlo all'archivio di backup (impostazione predefinita: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_SCROLLONKILLFOCUS</strong></dt> </dl></td>
<td>Quando si verifica KillFocus, scorrere fino all'inizio del testo (posizione del carattere uguale a 0) (impostazione predefinita: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_SMARTDRAGDROP</strong></dt> </dl></td>
<td><strong>Windows 8:</strong>aggiungere o eliminare uno spazio in base al contesto durante l'eliminazione del testo (impostazione predefinita: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_USECRLF</strong></dt> </dl></td>
<td>Obsoleta. Non usare.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_WORDDRAGDROP</strong></dt> </dl></td>
<td><strong>Windows 8:</strong>se word select è attivo, assicurarsi che la posizione di rilascio sia in corrispondenza di un limite di parola (impostazione predefinita: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_UPPERCASE</strong></dt> </dl></td>
<td>Converte tutti i caratteri di input in lettere maiuscole (impostazione predefinita: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_USEAIMM</strong></dt> </dl></td>
<td>Usa il componente metodo di input IMM attivo fornito con Internet Explorer 4.0 o versione successiva (impostazione predefinita: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_USEATFONT</strong></dt> </dl></td>
<td><strong>Windows XP con SP1:</strong>usa un tipo di carattere @, progettato per il testo verticale. viene usato con lo stile <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> finestra. Il nome di un tipo di carattere @ inizia con il simbolo @, ad esempio &quot; @Batang &quot; , (impostazione predefinita: 0, ma viene attivato automaticamente per il layout verticale del testo). <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_USECTF</strong></dt> </dl></td>
<td><strong>Windows XP con SP1:</strong>attiva il supporto di TSF. (impostazione predefinita: 0)<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_XLTCRCRLFTOCR</strong></dt> </dl></td>
<td>Attiva la conversione di CRCRL in CRS. Quando questo bit è on e un file viene letto, tutte le istanze di CRCRLF verranno convertite internamente in CR hard. Ciò influirà sulla disposizione del testo. Si noti che se tale file viene salvato come testo normale, i CRS verranno sostituiti da CRLF. Questo è lo standard .txt per il testo normale (impostazione predefinita: 0, che elimina CRCRLF in input). <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Componente ridistribuibile<br/>          | Rich Edit 3.0<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ SETEDITSTYLE**](em-seteditstyle.md)
</dt> </dl>

 

