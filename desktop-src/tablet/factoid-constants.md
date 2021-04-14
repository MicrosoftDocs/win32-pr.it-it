---
description: Definisce valori stringa costanti usati per aumentare l'accuratezza del riconoscimento fornendo informazioni contestuali al riconoscimento.
ms.assetid: 247a1f7d-8205-4e4d-9cfc-daad9bd2191f
title: Costanti controllo controllo (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1353a4989ddfb5af3865788c0fa7fdc2d377f75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526593"
---
# <a name="factoid-constants"></a>Costanti controllo oggetto

Definisce valori stringa costanti usati per aumentare l'accuratezza del riconoscimento fornendo informazioni contestuali al riconoscimento.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Nome</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_NONE"></span><span id="factoid_none"></span><dl> <dt><strong>FACTOID_NONE</strong></dt> </dl></td>
<td style="text-align: left;">Disabilita tutti gli altri factoids e dizionari.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_DEFAULT_________"></span><span id="___________factoid_default_________"></span><dl> <dt><strong>FACTOID_DEFAULT</strong></dt> </dl></td>
<td style="text-align: left;">L'impostazione predefinita per factoids per le lingue occidentali include il dizionario di sistema, il dizionario utenti, le varie punteggiatura e il controllo del controllo Web e dei numeri. L'impostazione predefinita per factoids per le lingue asiatiche orientali include tutti i caratteri supportati dal riconoscimento. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_SYSTEMDICTIONARY_________"></span><span id="___________factoid_systemdictionary_________"></span><dl> <dt><strong>FACTOID_SYSTEMDICTIONARY</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di utilizzare solo il dizionario di sistema.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_WORDLIST_________"></span><span id="___________factoid_wordlist_________"></span><dl> <dt><strong>FACTOID_WORDLIST</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di utilizzare un elenco di parole definito a livello di codice. L'elenco di parole viene definito dalla proprietà <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist"><strong>WordList</strong></a> di un oggetto <a href="inkrecognizercontext-class.md"><strong>InkRecognizerContext</strong></a> . <br/>
<blockquote>
[!Note]<br />
Se una stringa viene aggiunta a un elenco di parole, anche le relative versioni in lettere maiuscole vengono aggiunte in modo implicito. Ad esempio, l'aggiunta di &quot; Hello &quot; aggiunge in modo implicito &quot; Hello &quot; e &quot; Hello &quot; .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_EMAIL_________"></span><span id="___________factoid_email_________"></span><dl> <dt><strong>FACTOID_EMAIL</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare un indirizzo di posta elettronica.<br/>
<blockquote>
[!Note]<br />
&quot; someone@example.com &quot; Per questo controllo oggetto è necessario usare un indirizzo di posta elettronica completo, ad esempio. Un alias solitario, ad esempio un &quot; utente &quot; , non è riconosciuto.
</blockquote>
<br/>
<pre class="syntax" data-space="preserve"><code>someone@example.com</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_WEB"></span><span id="factoid_web"></span><dl> <dt><strong>FACTOID_WEB</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare un indirizzo Web.<br/>
<pre class="syntax" data-space="preserve"><code>`https://www.adatum.com`</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_ONECHAR_________"></span><span id="___________factoid_onechar_________"></span><dl> <dt><strong>FACTOID_ONECHAR</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare un singolo carattere.<br/>
<blockquote>
[!Note]<br />
Questo controllo del controllo Cerca tutti i caratteri ANSI isolati.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_NUMBER_________"></span><span id="___________factoid_number_________"></span><dl> <dt><strong>FACTOID_NUMBER</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare un numero.<br/>
<blockquote>
[!Note]<br />
I valori numerici includono separatori, decimali, ordinali e altri simboli numerici usati comunemente.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_DIGIT_________"></span><span id="___________factoid_digit_________"></span><dl> <dt><strong>FACTOID_DIGIT</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare una singola cifra, da 0 a 9.<br/>
<pre class="syntax" data-space="preserve"><code>0, 1, 2, 3, 4, 5, 6, 7, 8, 9</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_NUMBERSIMPLE_________"></span><span id="___________factoid_numbersimple_________"></span><dl> <dt><strong>FACTOID_NUMBERSIMPLE</strong></dt> </dl></td>
<td style="text-align: left;">Fornisce un contesto numerico semplice a un riconoscimento.<br/>
<blockquote>
[!Note]<br />
Questo controllo oggetto non è supportato in questa versione di Tablet PC SDK.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_CURRENCY_________"></span><span id="___________factoid_currency_________"></span><dl> <dt><strong>FACTOID_CURRENCY</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare i caratteri che identificano un valore di valuta.<br/>
<pre class="syntax" data-space="preserve"><code>$45.95,  60,  50.25,  3000</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_POSTALCODE_________"></span><span id="___________factoid_postalcode_________"></span><dl> <dt><strong>FACTOID_POSTALCODE</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare i codici postali.<br/>
<pre class="syntax" data-space="preserve"><code>98112</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_PERCENT_________"></span><span id="___________factoid_percent_________"></span><dl> <dt><strong>FACTOID_PERCENT</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare le percentuali.<br/>
<pre class="syntax" data-space="preserve"><code>87%</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_DATE_________"></span><span id="___________factoid_date_________"></span><dl> <dt><strong>FACTOID_DATE</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare i caratteri che denotano una data.<br/>
<pre class="syntax" data-space="preserve"><code>10/30/2001, &#39;01, 31/12, 12/99, 1999-2000</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_TIME_________"></span><span id="___________factoid_time_________"></span><dl> <dt><strong>FACTOID_TIME</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare i caratteri che indicano un'ora.<br/>
<pre class="syntax" data-space="preserve"><code>12:23:00 PM, 12:30, 24:30, 12:23:01, 1:12 A.M.</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_TELEPHONE_________"></span><span id="___________factoid_telephone_________"></span><dl> <dt><strong>FACTOID_TELEPHONE</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare i caratteri che indicano un numero di telefono.<br/>
<pre class="syntax" data-space="preserve"><code>123 555 0190, 0-123-206 555 0190, (206)555-0190</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_FILENAME_________"></span><span id="___________factoid_filename_________"></span><dl> <dt><strong>FACTOID_FILENAME</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare i caratteri che denotano un nome file.<br/>
<pre class="syntax" data-space="preserve"><code>mydocument.doc, c:\myfolder\file.c</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_UPPERCHAR_________"></span><span id="___________factoid_upperchar_________"></span><dl> <dt><strong>FACTOID_UPPERCHAR</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare un singolo carattere maiuscolo: da A a Z.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_LOWERCHAR_________"></span><span id="___________factoid_lowerchar_________"></span><dl> <dt><strong>FACTOID_LOWERCHAR</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare un singolo carattere minuscolo, da A A Z.<br/>
<blockquote>
[!Note]<br />
Questo controllo oggetto non è supportato in questa versione di Tablet PC SDK.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_PUNCCHAR_________"></span><span id="___________factoid_puncchar_________"></span><dl> <dt><strong>FACTOID_PUNCCHAR</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare i caratteri di punteggiatura.<br/>
<blockquote>
[!Note]<br />
Questo controllo oggetto non è supportato in questa versione di Tablet PC SDK.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_JAPANESECOMMON"></span><span id="factoid_japanesecommon"></span><dl> <dt><strong>FACTOID_JAPANESECOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare i caratteri kanji, katakana e hiragana usati comunemente.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_CHINESESIMPLECOMMON"></span><span id="factoid_chinesesimplecommon"></span><dl> <dt><strong>FACTOID_CHINESESIMPLECOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare i caratteri in cinese semplificato usati comunemente.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_CHINESETRADITIONALCOMMON"></span><span id="factoid_chinesetraditionalcommon"></span><dl> <dt><strong>FACTOID_CHINESETRADITIONALCOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare i caratteri cinesi tradizionali usati comunemente.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KOREANCOMMON"></span><span id="factoid_koreancommon"></span><dl> <dt><strong>FACTOID_KOREANCOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare caratteri coreani usati comunemente.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_HIRAGANA"></span><span id="factoid_hiragana"></span><dl> <dt><strong>FACTOID_HIRAGANA</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare solo caratteri hiragana.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KATAKANA"></span><span id="factoid_katakana"></span><dl> <dt><strong>FACTOID_KATAKANA</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare solo caratteri Katakana.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_KANJICOMMON"></span><span id="factoid_kanjicommon"></span><dl> <dt><strong>FACTOID_KANJICOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare i caratteri kanji comunemente utilizzati.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KANJIRARE"></span><span id="factoid_kanjirare"></span><dl> <dt><strong>FACTOID_KANJIRARE</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare caratteri kanji usati raramente.<br/>
<blockquote>
[!Note]<br />
Questo controllo oggetto non è supportato in questa versione di Tablet PC SDK.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_BOPOMOFO"></span><span id="factoid_bopomofo"></span><dl> <dt><strong>FACTOID_BOPOMOFO</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare i caratteri Bopomofo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_JAMO"></span><span id="factoid_jamo"></span><dl> <dt><strong>FACTOID_JAMO</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscitore di cercare i caratteri Jamo di compatibilità hangul.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_HANGULCOMMON"></span><span id="factoid_hangulcommon"></span><dl> <dt><strong>FACTOID_HANGULCOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare i caratteri hangul utilizzati comunemente.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_HANGULRARE"></span><span id="factoid_hangulrare"></span><dl> <dt><strong>FACTOID_HANGULRARE</strong></dt> </dl></td>
<td style="text-align: left;">Indica a un riconoscimento di cercare i caratteri hangul utilizzati raramente.<br/>
<blockquote>
[!Note]<br />
Questo controllo oggetto non è supportato in questa versione di Tablet PC SDK.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

In C++ è possibile accedere a queste costanti nel file di intestazione Msinkaut. h, che si trova nella <systemdrive> \\ Directory: programmi \\ Microsoft Tablet PC Platform SDK di \\ inclusione se l'SDK è stato installato nel percorso predefinito.

> [!Note]  
> Queste costanti sono WCHAR, non BSTR. Devono essere convertiti in BSTR prima di essere usati come parametri per i metodi dell'oggetto. Per ulteriori informazioni sul tipo di dati BSTR, vedere [utilizzo della libreria com](using-the-com-library.md).

 

> [!Note]  
> Per i riconoscitori dello script latino, le factoids definite in questa classe sono fornite solo per compatibilità con le versioni precedenti. Per nuove attività di sviluppo, è consigliabile usare i valori definiti nella funzione [SetInputScope](/windows/desktop/api/inputscope/nf-inputscope-setinputscope) . Per informazioni dettagliate, vedere [utilizzo del contesto per migliorare la precisione](using-context-to-improve-accuracy.md).

 

Usare questi identificatori per specificare quale controllo del controllo deve essere usato durante il riconoscimento.

Le seguenti combinazioni di factoids sono supportate solo per le lingue occidentali. Non hanno definizioni separate, ma sono input letterali stringa accettabile [**per la proprietà del controllo**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) del controllo degli oggetti che usano factoids. Queste costanti di stringa del controllore consentono all'input di trovare la corrispondenza con qualsiasi factoids nell'espressione.



| Combinazione               | Definizione                                                |
|---------------------------|-----------------------------------------------------------|
| "WEB \| wordlist"           | Controllo Web o elenco di parole.                         |
| "messaggio di posta elettronica \| "         | Il controllo dell'indirizzo di posta elettronica o l'elenco di parole.                       |
| "nome file \| Web \| " | Controllo del nome del file o controllo dell'oggetto Web o elenco di parole. |



 

Se si utilizza il controllo [InkEdit](inkedit-control-reference.md) , il controllo dell'oggetto può essere impostato come proprietà del controllo.

Se si utilizzano le API della piattaforma Tablet PC, è possibile impostare la [**proprietà del controllo del controllo**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) su un oggetto [**InkRecognizerContext**](inkrecognizercontext-class.md) .

In alternativa, è possibile impostare questa proprietà con la costante della stringa del controllo dell'oggetto corrente.

> [!Note]  
> Le costanti di stringa del controllo del controllo sono maiuscole. Per altre informazioni su factoids e su come usarle, vedere uso del contesto per [migliorare la precisione](using-context-to-improve-accuracy.md). Per determinare se un controllo del controllo è disponibile in una lingua specifica, vedere [Supported Factoids dalla versione 1](supported-factoids-from-version-1.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkRecognizeContext proprietà di controllo \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)
</dt> <dt>

[**Proprietà del controllo del controllo della \[ Classe PenInputPanel\]**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)
</dt> <dt>

[**Controllo proprietà \[ controllo InkEdit\]**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)
</dt> <dt>

[Uso del contesto per migliorare l'accuratezza](using-context-to-improve-accuracy.md)
</dt> <dt>

[Factoids supportati dalla versione 1](supported-factoids-from-version-1.md)
</dt> </dl>

 

