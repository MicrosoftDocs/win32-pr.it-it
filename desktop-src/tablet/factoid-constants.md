---
description: Definisce i valori stringa costanti usati per aumentare l'accuratezza del riconoscimento fornendo informazioni contestuali al riconoscimento.
ms.assetid: 247a1f7d-8205-4e4d-9cfc-daad9bd2191f
title: Costanti Factoid (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa748c84f8bd39f18f83e1ec72474bcfbe3017f2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883672"
---
# <a name="factoid-constants"></a>Costanti Factoid

Definisce i valori stringa costanti usati per aumentare l'accuratezza del riconoscimento fornendo informazioni contestuali al riconoscimento.




| Nome | Descrizione | 
|------|-------------|
| <span id="FACTOID_NONE"></span><span id="factoid_none"></span><dl><dt><strong>FACTOID_NONE</strong></dt></dl> | Disabilita tutti gli altri factoid e dizionari.<br /> | 
| <span id="___________FACTOID_DEFAULT_________"></span><span id="___________factoid_default_________"></span><dl><dt><strong>FACTOID_DEFAULT</strong></dt></dl> | L'impostazione Predefinita per i factoid per le lingue occidentali include il dizionario di sistema, il dizionario utente, varie punteggiatura e il factoid Web e Number. L'impostazione Predefinita per i factoid per le lingue dell'Asia orientale include tutti i caratteri supportati dal riconoscimento. <br /> | 
| <span id="___________FACTOID_SYSTEMDICTIONARY_________"></span><span id="___________factoid_systemdictionary_________"></span><dl><dt><strong>FACTOID_SYSTEMDICTIONARY</strong></dt></dl> | Indica a un sistema di riconoscimento di usare solo il dizionario di sistema.<br /> | 
| <span id="___________FACTOID_WORDLIST_________"></span><span id="___________factoid_wordlist_________"></span><dl><dt><strong>FACTOID_WORDLIST</strong></dt></dl> | Indica a un sistema di riconoscimento di usare un elenco di parole definito a livello di codice. L'elenco di parole è definito dalla <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist"><strong>proprietà WordList</strong></a> di un <a href="inkrecognizercontext-class.md"><strong>oggetto InkRecognizerContext.</strong></a> <br /><blockquote>[!Note]<br />Se una stringa viene aggiunta a un elenco di parole, vengono aggiunte in modo implicito anche le relative versioni in maiuscolo. Ad esempio, l'aggiunta di "hello" aggiunge in modo implicito "Hello" e "HELLO".</blockquote><br /> | 
| <span id="___________FACTOID_EMAIL_________"></span><span id="___________factoid_email_________"></span><dl><dt><strong>FACTOID_EMAIL</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare un indirizzo di posta elettronica.<br /><blockquote>[!Note]<br />Per questo factoid è necessario usare un indirizzo di posta elettronica completo, ad esempio " someone@example.com ". Un alias unico, ad esempio "qualcuno", non viene riconosciuto.</blockquote><br /><pre class="syntax" data-space="preserve"><code>someone@example.com</code></pre> | 
| <span id="FACTOID_WEB"></span><span id="factoid_web"></span><dl><dt><strong>FACTOID_WEB</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare un indirizzo Web.<br /><pre class="syntax" data-space="preserve"><code>`https://www.adatum.com`</code></pre> | 
| <span id="___________FACTOID_ONECHAR_________"></span><span id="___________factoid_onechar_________"></span><dl><dt><strong>FACTOID_ONECHAR</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare un singolo carattere.<br /><blockquote>[!Note]<br />Questo factoid cerca qualsiasi carattere ANSI isolato.</blockquote><br /> | 
| <span id="___________FACTOID_NUMBER_________"></span><span id="___________factoid_number_________"></span><dl><dt><strong>FACTOID_NUMBER</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare un numero.<br /><blockquote>[!Note]<br />I valori numerici includono separatori, decimali, ordinali e altri simboli numerici di uso comune.</blockquote><br /> | 
| <span id="___________FACTOID_DIGIT_________"></span><span id="___________factoid_digit_________"></span><dl><dt><strong>FACTOID_DIGIT</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare una singola cifra, da 0 a 9.<br /><pre class="syntax" data-space="preserve"><code>0, 1, 2, 3, 4, 5, 6, 7, 8, 9</code></pre> | 
| <span id="___________FACTOID_NUMBERSIMPLE_________"></span><span id="___________factoid_numbersimple_________"></span><dl><dt><strong>FACTOID_NUMBERSIMPLE</strong></dt></dl> | Fornisce un contesto numerico semplice a un riconoscitore.<br /><blockquote>[!Note]<br />Questo factoid non è supportato in questa versione di Tablet PC SDK.</blockquote><br /> | 
| <span id="___________FACTOID_CURRENCY_________"></span><span id="___________factoid_currency_________"></span><dl><dt><strong>FACTOID_CURRENCY</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare i caratteri che indicano un valore di valuta.<br /><pre class="syntax" data-space="preserve"><code>$45.95,  60,  50.25,  3000</code></pre> | 
| <span id="___________FACTOID_POSTALCODE_________"></span><span id="___________factoid_postalcode_________"></span><dl><dt><strong>FACTOID_POSTALCODE</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare i codici postali.<br /><pre class="syntax" data-space="preserve"><code>98112</code></pre> | 
| <span id="___________FACTOID_PERCENT_________"></span><span id="___________factoid_percent_________"></span><dl><dt><strong>FACTOID_PERCENT</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare le percentuali.<br /><pre class="syntax" data-space="preserve"><code>87%</code></pre> | 
| <span id="___________FACTOID_DATE_________"></span><span id="___________factoid_date_________"></span><dl><dt><strong>FACTOID_DATE</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare i caratteri che indicano una data.<br /><pre class="syntax" data-space="preserve"><code>10/30/2001, '01, 31/12, 12/99, 1999-2000</code></pre> | 
| <span id="___________FACTOID_TIME_________"></span><span id="___________factoid_time_________"></span><dl><dt><strong>FACTOID_TIME</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare i caratteri che indicano un'ora.<br /><pre class="syntax" data-space="preserve"><code>12:23:00 PM, 12:30, 24:30, 12:23:01, 1:12 A.M.</code></pre> | 
| <span id="___________FACTOID_TELEPHONE_________"></span><span id="___________factoid_telephone_________"></span><dl><dt><strong>FACTOID_TELEPHONE</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare i caratteri che indicano un numero di telefono.<br /><pre class="syntax" data-space="preserve"><code>123 555 0190, 0-123-206 555 0190, (206)555-0190</code></pre> | 
| <span id="___________FACTOID_FILENAME_________"></span><span id="___________factoid_filename_________"></span><dl><dt><strong>FACTOID_FILENAME</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare i caratteri che denotano un nome di file.<br /><pre class="syntax" data-space="preserve"><code>mydocument.doc, c:\myfolder\file.c</code></pre> | 
| <span id="___________FACTOID_UPPERCHAR_________"></span><span id="___________factoid_upperchar_________"></span><dl><dt><strong>FACTOID_UPPERCHAR</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare un singolo carattere maiuscolo: da A a Z.<br /> | 
| <span id="___________FACTOID_LOWERCHAR_________"></span><span id="___________factoid_lowerchar_________"></span><dl><dt><strong>FACTOID_LOWERCHAR</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare un singolo carattere minuscolo: da A a Z.<br /><blockquote>[!Note]<br />Questo factoid non è supportato in questa versione di Tablet PC SDK.</blockquote><br /> | 
| <span id="___________FACTOID_PUNCCHAR_________"></span><span id="___________factoid_puncchar_________"></span><dl><dt><strong>FACTOID_PUNCCHAR</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare i caratteri di punteggiatura.<br /><blockquote>[!Note]<br />Questo factoid non è supportato in questa versione di Tablet PC SDK.</blockquote><br /> | 
| <span id="FACTOID_JAPANESECOMMON"></span><span id="factoid_japanesecommon"></span><dl><dt><strong>FACTOID_JAPANESECOMMON</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare caratteri Kanji, Katakana e Hiragana di uso comune.<br /> | 
| <span id="FACTOID_CHINESESIMPLECOMMON"></span><span id="factoid_chinesesimplecommon"></span><dl><dt><strong>FACTOID_CHINESESIMPLECOMMON</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare i caratteri in cinese semplificato di uso comune.<br /> | 
| <span id="FACTOID_CHINESETRADITIONALCOMMON"></span><span id="factoid_chinesetraditionalcommon"></span><dl><dt><strong>FACTOID_CHINESETRADITIONALCOMMON</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare i caratteri in cinese tradizionale di uso comune.<br /> | 
| <span id="FACTOID_KOREANCOMMON"></span><span id="factoid_koreancommon"></span><dl><dt><strong>FACTOID_KOREANCOMMON</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare i caratteri coreani di uso comune.<br /> | 
| <span id="FACTOID_HIRAGANA"></span><span id="factoid_hiragana"></span><dl><dt><strong>FACTOID_HIRAGANA</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare solo caratteri Hiragana.<br /> | 
| <span id="FACTOID_KATAKANA"></span><span id="factoid_katakana"></span><dl><dt><strong>FACTOID_KATAKANA</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare solo caratteri Katakana.<br /> | 
| <span id="FACTOID_KANJICOMMON"></span><span id="factoid_kanjicommon"></span><dl><dt><strong>FACTOID_KANJICOMMON</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare i caratteri Kanji di uso comune.<br /> | 
| <span id="FACTOID_KANJIRARE"></span><span id="factoid_kanjirare"></span><dl><dt><strong>FACTOID_KANJIRARE</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare caratteri Kanji usati raramente.<br /><blockquote>[!Note]<br />Questo factoid non è supportato in questa versione di Tablet PC SDK.</blockquote><br /> | 
| <span id="FACTOID_BOPOMOFO"></span><span id="factoid_bopomofo"></span><dl><dt><strong>FACTOID_BOPOMOFO</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare i caratteri Bopomofo.<br /> | 
| <span id="FACTOID_JAMO"></span><span id="factoid_jamo"></span><dl><dt><strong>FACTOID_JAMO</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare i caratteri Jamo di compatibilità Hangul.<br /> | 
| <span id="FACTOID_HANGULCOMMON"></span><span id="factoid_hangulcommon"></span><dl><dt><strong>FACTOID_HANGULCOMMON</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare i caratteri Hangul di uso comune.<br /> | 
| <span id="FACTOID_HANGULRARE"></span><span id="factoid_hangulrare"></span><dl><dt><strong>FACTOID_HANGULRARE</strong></dt></dl> | Indica a un sistema di riconoscimento di cercare i caratteri Hangul usati raramente.<br /><blockquote>[!Note]<br />Questo factoid non è supportato in questa versione di Tablet PC SDK.</blockquote><br /> | 




## <a name="remarks"></a>Commenti

In C++ è possibile accedere a queste costanti nel file di intestazione Msinkaut.h, che si trova nella directory systemdrive : Programmi Microsoft Tablet PC Platform SDK Include se l'SDK è stato installato nel percorso &lt; &gt; \\ \\ \\ predefinito.

> [!Note]  
> Queste costanti sono WCHAR, non BSTR. Devono essere convertiti in BSTR prima di usarli come parametri per i metodi oggetto. Per altre informazioni sul tipo di dati BSTR, vedere [Uso della libreria COM.](using-the-com-library.md)

 

> [!Note]  
> Per i riconoscitori di script latini, i factoid definiti in questa classe vengono forniti solo per la compatibilità con le versioni precedenti. Per i nuovi progetti di sviluppo, si consiglia di usare i valori definiti nella [funzione SetInputScope.](/windows/desktop/api/inputscope/nf-inputscope-setinputscope) Per informazioni dettagliate, vedere [Uso del contesto per migliorare l'accuratezza.](using-context-to-improve-accuracy.md)

 

Usare questi identificatori per specificare il factoid da usare durante il riconoscimento.

Le combinazioni di factoid seguenti sono supportate solo per le lingue occidentali. Non dispongono di definizioni separate, ma sono input di valori letterali stringa accettabili per la proprietà [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) di oggetti che usano factoid. Queste costanti stringa factoid consentono all'input di corrispondere a uno qualsiasi dei factoid nell'espressione.



| Combinazione               | Definizione                                                |
|---------------------------|-----------------------------------------------------------|
| "WEB \| WORDLIST"           | Factoid Web o elenco di parole.                         |
| "INVIA MESSAGGIO \| DI POSTA ELETTRONICA A WORDLIST"         | Factoid email o elenco di parole.                       |
| "FILENAME \| WEB \| WORDLIST" | Factoid nome file, factoid Web o elenco di parole. |



 

Se si usa il [controllo InkEdit,](inkedit-control-reference.md) il factoid può essere impostato come proprietà del controllo.

Se si usano le API della piattaforma Tablet PC, è possibile impostare la proprietà [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) su un [**oggetto InkRecognizerContext.**](inkrecognizercontext-class.md)

In alternativa, è possibile impostare questa proprietà con la costante stringa factoid effettiva.

> [!Note]  
> Per le costanti stringa factoid viene fatto distinzione tra maiuscole e minuscole. Per altre informazioni sui factoid e su come usarli, vedere Uso del contesto per migliorare [l'accuratezza.](using-context-to-improve-accuracy.md) Per determinare se un factoid è disponibile in una lingua specifica, vedere [Factoid supportati dalla versione 1.](supported-factoids-from-version-1.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe InkRecognizeContext della proprietà Factoid \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)
</dt> <dt>

[**Classe \[ PenInputPanel della proprietà Factoid\]**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)
</dt> <dt>

[**Controllo \[ InkEdit della proprietà Factoid\]**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)
</dt> <dt>

[Uso del contesto per migliorare l'accuratezza](using-context-to-improve-accuracy.md)
</dt> <dt>

[Factoid supportati dalla versione 1](supported-factoids-from-version-1.md)
</dt> </dl>

 

