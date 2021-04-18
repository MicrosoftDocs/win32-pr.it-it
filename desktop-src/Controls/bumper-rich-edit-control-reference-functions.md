---
title: Funzioni Rich Edit
description: Funzioni Rich Edit
ms.assetid: 5e913cb6-d561-447f-b33e-9160a8f46cda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99f776b9a08095fa66645713e107a3d66920e80f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321665"
---
# <a name="rich-edit-functions"></a>Funzioni Rich Edit

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
<td><a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a><br/></td>
<td>La funzione <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a> è una funzione di callback definita dall'applicazione che viene utilizzata con il messaggio di <a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a><br/></td>
<td>La funzione <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a> è una funzione di callback definita dall'applicazione utilizzata con i messaggi <a href="em-streamin.md"><strong>EM_STREAMIN</strong></a> e <a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a> . Viene usato per trasferire un flusso di dati all'interno o all'esterno di un controllo Rich Edit. Il tipo <strong>EDITSTREAMCALLBACK</strong> definisce un puntatore a questa funzione di callback. <em>EditStreamCallback</em> è un segnaposto per il nome della funzione definita dall'applicazione. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a><br/></td>
<td>La funzione <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a> è una funzione di callback definita dall'applicazione utilizzata con il messaggio di <a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a> . Determina l'indice dei caratteri della parola break o la classe di caratteri e i flag di interruzioni di parola dei caratteri nel testo specificato. Il tipo <strong>EDITWORDBREAKPROCEX</strong> definisce un puntatore a questa funzione di callback. <em>EditWordBreakProcEx</em> è un segnaposto per il nome della funzione definita dall'applicazione. <br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>GetMathAlphanumeric</strong></a><br/></td>
<td>Recupera il carattere alfanumerico Unicode UTF (Unicode Transformation Format) 32 che corrisponde al carattere BMP (Basic Multilingual Plane) specificato e allo stile matematico. <br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>GetMathAlphanumericCode</strong></a><br/></td>
<td>Recupera lo stile matematico e il codice carattere BMP (Basic Multilingual Plane) verticale che corrisponde al byte finale specificato di una coppia di surrogati Math.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a><br/></td>
<td>La funzione <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a> è una funzione di callback definita dall'applicazione utilizzata con il messaggio di <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a> . Determina il modo in cui la sillabazione viene eseguita in un controllo Rich Edit di Microsoft.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>MathBuildDown</strong></a><br/></td>
<td>Converte i valori predefiniti Math, Ruby e altri oggetti inline nell'intervallo specificato in formato lineare.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>MathBuildUp</strong></a><br/></td>
<td>Converte la matematica in formato lineare in un intervallo in un form predefinito oppure modifica il form predefinito corrente. <br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>MathTranslate</strong></a><br/></td>
<td>Converte i caratteri matematici nell'intervallo specificato.<br/></td>
</tr>
<tr class="even">
<td><a href="reextendedregisterclass.md"><strong>REExtendedRegisterClass</strong></a><br/></td>
<td>Registra due nomi di classe, REListBox20W e RECombobox20W, che possono essere utilizzati per creare finestre ListBox o ComboBox modificate in modo completo. <br/>
<blockquote>
[!Note]<br />
Progettato per uso interno; sconsigliato per l'utilizzo nelle applicazioni. Questa funzione potrebbe non essere supportata nelle versioni future.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

