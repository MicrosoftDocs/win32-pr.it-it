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
# <a name="em_geteditstyle-message"></a>\_Messaggio di riedito em

Recupera i flag di stile di modifica correnti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

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
<td>La funzionalità Rich Edit chiamerà il cicalino di sistema se l'utente tenta di immettere un numero di caratteri superiore al massimo consentito.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_BIDI</strong></dt> </dl></td>
<td>Attiva l'elaborazione bidirezionale. Questa operazione viene attivata automaticamente da Rich Edit se uno degli stili della finestra seguenti è attivo: <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RIGHT</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RTLREADING</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_LEFTSCROLLBAR</strong></a>. Questa impostazione è tuttavia utile per la gestione di questi stili di finestra quando si usa un'implementazione personalizzata di <a href="/windows/desktop/api/Textserv/nl-textserv-itexthost"><strong>ITextHost</strong></a> (valore predefinito: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_CTFALLOWEMBED</strong></dt> </dl></td>
<td><strong>Windows XP con SP1</strong>: consente l'inserimento di oggetti incorporati tramite TSF (valore predefinito: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_CTFALLOWPROOFING</strong></dt> </dl></td>
<td><strong>Windows XP con SP1</strong>: consente suggerimenti per la prova di TSF (valore predefinito: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_CTFALLOWSMARTTAG</strong></dt> </dl></td>
<td><strong>Windows XP con SP1</strong>: consente i suggerimenti per gli SMARTTAG di TSF (valore predefinito: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_CTFNOLOCK</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: non consentire l'accesso in lettura/scrittura del blocco TSF. Questa operazione sospende l'input di TSF. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_DEFAULTLATINLIGA</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: i tipi di carattere con una legatura Fi vengono visualizzati con le funzionalità OpenType predefinite, ottenendo una tipografia migliorata (impostazione predefinita: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_DRAFTMODE</strong></dt> </dl></td>
<td><strong>Windows XP con SP1</strong>: usare i tipi di carattere della modalità bozza per visualizzare il testo. La modalità bozza è un'opzione di accessibilità in cui il controllo Visualizza il testo con un solo tipo di carattere. il tipo di carattere è determinato dall'impostazione di sistema per il tipo di carattere utilizzato nelle finestre di messaggio. Ad esempio, gli utenti accessibili possono leggere più facilmente il testo se è uniforme, anziché una combinazione di tipi di carattere e stili (valore predefinito: 0). <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_EMULATE10</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: emulare il comportamento richedit 1,0. <br/>
<blockquote>
[!Note]<br />
Se si desidera effettivamente questo comportamento, utilizzare il riched32.dll Windows anziché riched20.dll o msftedit.dll. Riched32.dll aveva più funzionalità.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_EMULATESYSEDIT</strong></dt> </dl></td>
<td>Quando questo bit è impostato su on, Rich Edit tenta di emulare il controllo di modifica del sistema (valore predefinito: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_EXTENDBACKCOLOR</strong></dt> </dl></td>
<td>Estende il colore di sfondo fino ai bordi del rettangolo client (valore predefinito: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_HIDEGRIDLINES</strong></dt> </dl></td>
<td><strong>Windows XP con SP1</strong>: se la larghezza della griglia della tabella è pari a zero, le griglie non vengono visualizzate. Equivale alla caratteristica Nascondi griglie nel menu tabella di Word (valore predefinito: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_HYPERLINKTOOLTIPS</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: quando il cursore si trova su un collegamento, Visualizza una descrizione comando con l'indirizzo del collegamento di destinazione (valore predefinito: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_LOGICALCARET</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: specificare le informazioni logiche sul punto di inserimento anziché una bitmap del cursore, come descritto in <a href="/windows/desktop/api/Textserv/nf-textserv-itexthost-txsetcaretpos"><strong>ITextHost:: TxSetCaretPos</strong></a> (valore predefinito: 0). <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_LOWERCASE</strong></dt> </dl></td>
<td>Converte tutti i caratteri di input in minuscolo (valore predefinito: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_MAPCPS</strong></dt> </dl></td>
<td>Obsoleta. Non usare.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_MULTISELECT</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: abilitare la selezione a più selezioni con le selezioni del mouse effettuate mentre viene premuto il tasto Ctrl (valore predefinito: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_NOEALINEHEIGHTADJUST</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: non modificare l'altezza della riga per il testo asiatico orientale (valore predefinito: 0 che regola l'altezza della riga del 15%). <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_NOFOCUSLINKNOTIFY</strong></dt> </dl></td>
<td>Invia <a href="en-link.md">EN_LINK</a> notifica da collegamenti che non hanno lo stato attivo.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_NOIME</strong></dt> </dl></td>
<td>Non consente gli IME per questa istanza del controllo Rich Edit (valore predefinito: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_NOINPUTSEQUENCECHK</strong></dt> </dl></td>
<td>Quando questo bit è on, Rich Edit non verifica la sequenza di testo tipizzato. Per alcune lingue, ad esempio Thai e vietnamita, è necessario verificare l'ordine di sequenza di input prima di inviarlo all'archivio di backup (valore predefinito: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_SCROLLONKILLFOCUS</strong></dt> </dl></td>
<td>Quando si verifica KillFocus, scorrere fino all'inizio del testo (posizione del carattere uguale a 0) (valore predefinito: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_SMARTDRAGDROP</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: aggiungere o eliminare uno spazio in base al contesto quando si elimina il testo (valore predefinito: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_USECRLF</strong></dt> </dl></td>
<td>Obsoleta. Non usare.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_WORDDRAGDROP</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: se Word Select è attivo, verificare che il percorso di rilascio sia in corrispondenza di un confine di parola (valore predefinito: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_UPPERCASE</strong></dt> </dl></td>
<td>Converte tutti i caratteri di input in lettere maiuscole (valore predefinito: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_USEAIMM</strong></dt> </dl></td>
<td>Usa il componente metodo di input IMM attivo fornito con Internet Explorer 4,0 o versione successiva (valore predefinito: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_USEATFONT</strong></dt> </dl></td>
<td><strong>Windows XP con SP1</strong>: usa un tipo di carattere @, progettato per il testo verticale. viene utilizzato con lo stile della finestra <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> . Il nome di un @ font inizia con il simbolo @, ad esempio &quot; @Batang &quot; (valore predefinito: 0, ma viene attivato automaticamente per il layout del testo verticale). <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_USECTF</strong></dt> </dl></td>
<td><strong>Windows XP con SP1</strong>: attiva il supporto di TSF. (valore predefinito: 0)<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_XLTCRCRLFTOCR</strong></dt> </dl></td>
<td>Attiva la conversione di CRCRLFs in CRs. Quando questo bit è acceso e viene letto un file, tutte le istanze di CRCRLF verranno convertite internamente in un CRs rigido. Questa operazione influirà sul ritorno a capo del testo. Si noti che se tale file viene salvato come testo normale, il CRs verrà sostituito da CRLFs. Si tratta dello standard. txt per testo normale (valore predefinito: 0, che Elimina CRCRLFs nell'input). <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Componente ridistribuibile<br/>          | Modifica avanzata 3,0<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETEDITSTYLE em**](em-seteditstyle.md)
</dt> </dl>

 

