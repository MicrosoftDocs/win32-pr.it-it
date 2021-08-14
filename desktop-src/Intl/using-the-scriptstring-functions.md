---
description: Per un'applicazione che si occupa di testo non formattato, Uniscribe fornisce le funzioni \* ScriptString.
ms.assetid: bfbba5df-ce06-4012-a7b1-55d8ea580942
title: Uso delle funzioni ScriptString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6685af7dad2c9e1b8d0cf460d526155f967a9105e1b107047afb99c18a5124f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118389407"
---
# <a name="using-the-scriptstring-functions"></a>Uso delle funzioni ScriptString

Per un'applicazione che si occupa di testo non formattato, Uniscribe fornisce le funzioni **ScriptString \** _. Queste funzioni sono simili [a _ *ExtTextOut* *](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)e [**GetTextExtent**](/cpp/mfc/reference/cdc-class#gettextextent), ma forniscono il supporto completo di script complessi, incluso il posizionamento del punto di inserimento. Queste funzioni sono simili alle altre funzioni Uniscribe, ma sono personalizzate in base ai requisiti più semplici dell'elaborazione del testo normale.

Nella tabella seguente vengono fornite informazioni **dettagliate sulle funzioni ScriptString \*** e su eventuali controparti nelle altre funzioni Uniscribe.



<table>
<thead>
<tr class="header">
<th>Funzione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse"><strong>ScriptStringAnalyse</strong></a></td>
<td>Analizza il testo normale. Questa funzione corrisponde alle funzioni seguenti:<br/> <dl><a href="/windows/desktop/api/Usp10/nf-usp10-scriptitemize"><strong>ScriptItemize</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptshape"><strong>ScriptShape</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptplace"><strong>ScriptPlace</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptbreak"><strong>ScriptBreak</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptjustify"><strong>ScriptJustify</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptlayout"><strong>ScriptLayout</strong></a><br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox"><strong>ScriptStringCPtoX</strong></a></td>
<td>Recupera la coordinata x per una posizione di carattere. Questa funzione corrisponde a <a href="/windows/desktop/api/Usp10/nf-usp10-scriptcptox"><strong>ScriptCPtoX</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringfree"><strong>ScriptStringFree</strong></a></td>
<td>Libera una struttura <a href="script-string-analysis.md"><strong>SCRIPT_STRING_ANALYSIS</strong></a> struttura .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths"><strong>ScriptStringGetLogicalWidths</strong></a></td>
<td>Converte la larghezza dell'oggetto visivo in larghezze logiche. Questa funzione corrisponde a <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths"><strong>ScriptGetLogicalWidths.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder"><strong>ScriptStringGetOrder</strong></a></td>
<td>Mappe le posizioni dei glifi dei caratteri in modo simile a <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a>, solo per uso legacy. Questa funzione non funziona correttamente con gli script che generano più di un glifo per ogni punto di codice.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringout"><strong>ScriptStringOut</strong></a></td>
<td>Visualizza testo normale. Questa funzione corrisponde a <a href="/windows/desktop/api/Usp10/nf-usp10-scripttextout"><strong>ScriptTextOut.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars"><strong>ScriptString_pcOutChars</strong></a></td>
<td>Restituisce un puntatore alla lunghezza di una stringa di testo normale ritagliata.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr"><strong>ScriptString_pLogAttr</strong></a></td>
<td>Restituisce un puntatore al buffer degli attributi logici per una stringa di testo normale analizzata.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize"><strong>ScriptString_pSize</strong></a></td>
<td>Restituisce un puntatore alle dimensioni (larghezza e altezza) di una stringa di testo normale analizzata.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate"><strong>ScriptStringValidate</strong></a></td>
<td>Identifica sequenze di punti di codice non valide nello script specificato. Questa funzione è diversa da <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a>, che identifica i punti di codice non presenti in un tipo di carattere.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp"><strong>ScriptStringXtoCP</strong></a></td>
<td>Converte una coordinata x in una posizione di carattere. Questa funzione corrisponde a <a href="/windows/desktop/api/Usp10/nf-usp10-scriptxtocp"><strong>ScriptXtoCP</strong></a>.</td>
</tr>
</tbody>
</table>

Per visualizzare solo testo normale senza modifiche, un'applicazione deve chiamare [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse), [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout)e quindi [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree). Le altre funzioni vengono usate per modificare il testo normale prima della visualizzazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 
