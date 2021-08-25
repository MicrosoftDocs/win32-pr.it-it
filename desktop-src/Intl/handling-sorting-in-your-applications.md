---
description: Alcune applicazioni, ad esempio Microsoft Active Directory, Microsoft Exchange e Microsoft Access, gestiscono un database ordinabile di stringhe di impostazioni locali e di lingua indicizzate in base al nome (stringa UTF-16) e ai pesi di ordinamento associati.
ms.assetid: c8fc32bd-02bd-4a40-a836-d9ad9f69c209
title: Gestione dell'ordinamento nelle applicazioni
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: 73c7ca897cb5f83e5a073205341f8b0d0f96ff2d0a9d4c7144a914cd5c96c44d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822691"
---
# <a name="handling-sorting-in-your-applications"></a>Gestione dell'ordinamento nelle applicazioni

Alcune applicazioni, ad esempio Microsoft Active Directory, Microsoft Exchange e Microsoft Access, gestiscono un database ordinabile di stringhe di impostazioni locali e di lingua indicizzate in base al nome (stringa UTF-16) e ai pesi di ordinamento associati.

[L'ordinamento](sorting.md) è in genere intuitivo per gli utenti con le proprie impostazioni locali. Tuttavia, può non essere intuitivo per gli sviluppatori di applicazioni. Questo argomento illustra le considerazioni per la gestione dell'ordinamento nelle applicazioni. L'ordinamento può essere linguistico o ordinale (non linguistico).

## <a name="sorting-functions"></a>Funzioni di ordinamento

È possibile usare un'ampia gamma di funzioni di ordinamento nelle applicazioni:

-   Funzioni di confronto tra stringhe NLS. Esempi sono [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) e [**CompareStringEx,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) [**CompareStringOrdinal,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) [**LCMapString,**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) [**LCMapStringEx,**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) [**FindNLSString,**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring) [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)e [**FindStringOrdinal.**](/windows/desktop/api/Libloaderapi/nf-libloaderapi-findstringordinal) Per [una descrizione dei problemi](security-considerations--international-features.md) di sicurezza correlati alle funzioni di confronto tra stringhe, vedere Considerazioni sulla sicurezza: funzionalità internazionali.
-   Funzioni wrapper che chiamano internamente le funzioni di confronto tra stringhe. Le funzioni più comuni sono [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) e [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia), che chiamano [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw).

In genere le funzioni di ordinamento valutano le stringhe carattere per carattere. Tuttavia, molte lingue hanno elementi di più caratteri, ad esempio la coppia di due caratteri "CH" nello spagnolo tradizionale. [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) e [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) usano l'identificatore delle impostazioni locali fornito dall'applicazione o il nome per identificare gli elementi di più caratteri. Al contrario, [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)e [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) usano le impostazioni locali dell'utente.

Un altro esempio è il taiwanese, che contiene molti elementi di due caratteri, ad esempio le lettere maiuscole, i titoli e le forme minuscole valide di "GI", che sono rispettivamente "GI, "Gi" e "gi". Uno di questi formati viene considerato come un singolo elemento di ordinamento e, se l'utilizzo di maiuscole e minuscole viene ignorato, viene confrontato come uguale. Tuttavia, poiché "gI" non è valido come singolo elemento, [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)e [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) trattano "gI" come due elementi separati.

Le funzioni [**CompareString,**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) [**CompareStringEx,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) [**lstrcmp,**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) [**lstrcmpi,**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) [**LCMapString,**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) [**LCMapStringEx,**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)e [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) usano per impostazione predefinita una tecnica di ordinamento delle parole. Per questo tipo di ordinamento, tutti i segni di punteggiatura e altri caratteri non alfanumerici, ad eccezione del trattino e dell'apostrofo, vengono prima di qualsiasi carattere alfanumerico. Il trattino e l'apostrofo vengono trattati in modo diverso dagli altri caratteri non alfanumerici per garantire che parole come "coop" e "co-op" rimangano insieme in un elenco ordinato.

Anziché un ordinamento di parole, l'applicazione può richiedere una tecnica di ordinamento delle stringhe dalle funzioni di ordinamento specificando il flag SORT \_ STRINGSORT. Un ordinamento di stringa considera il trattino e l'apostrofo come qualsiasi altro carattere non alfanumerico. Le posizioni nella sequenza di ordinamento sono precedenti ai caratteri alfanumerici.

Nella tabella seguente vengono confrontati i risultati di un ordinamento delle parole con i risultati di un ordinamento di stringa. 

| Ordinamento delle parole | Ordinamento delle stringhe |
|-----------|-------------|
| Billetta    | bill      |
| Bollette     | Billetta      |
| bill    | Bollette       |
| non può    | Non       |
| non posso      | non può      |
| Non     | non posso        |
| con       | Cooperativa       |
| Coop      | con         |
| Cooperativa     | Coop        |



 

## <a name="sort-strings-linguistically"></a>Ordinare le stringhe dal punto di vista linguistico

Le [**funzioni CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) e [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) verificano l'uguaglianza linguistica. Le applicazioni devono usare queste funzioni con le impostazioni locali corrette per l'ordinamento linguistico delle stringhe.

> [!Note]  
> Per la compatibilità con Unicode, un'applicazione deve preferire [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) o la versione Unicode di [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw). Un altro motivo per preferire [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) è che Microsoft sta eseguendo la migrazione all'uso dei nomi delle impostazioni locali anziché degli identificatori delle impostazioni locali per le nuove impostazioni locali, per motivi di interoperabilità. Qualsiasi applicazione eseguita solo in Windows Vista e versioni successive deve usare [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex).

 

Un altro modo per testare l'uguaglianza linguistica è usare [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) o [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia), che usano sempre un ordinamento di parole. La [**funzione lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) chiama [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) con il flag NORM \_ IGNORECASE, mentre [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) la chiama senza tale flag. Per una panoramica dell'uso delle funzioni wrapper, vedere [**Stringhe**](../menurc/strings.md).

Le funzioni recuperano risultati linguisticamente appropriati per tutte le impostazioni locali. Le aspettative dell'utente per impostazioni locali diverse possono variare in modo significativo nel comportamento di ordinamento, come illustrato negli esempi seguenti.

-   Molte impostazioni locali equilibrano la legatura ae (æ) con le lettere ae. Tuttavia, islandese (Islanda) la considera una lettera separata e la inserisce dopo Z nella sequenza di ordinamento.
-   L'anello A (Å) in genere viene ordinato con una semplice differenza diacritica rispetto ad A. Tuttavia, lo svedese (Svezia) inserisce l'anello A dopo Z nella sequenza di ordinamento.

Le funzioni tentano di verificare rigorosamente che i punti di codice definiti nello standard Unicode siano canonicamente uguali a una stringa di punti di codice equivalenti. Ad esempio, il punto di codice che rappresenta una "u" minuscola con una dieresi (ü) è canonicamente uguale a una "u" minuscola combinata con la dieresi (è). Si noti, tuttavia, che l'equivalenza canonica non è sempre possibile.

Poiché quasi tutti i dati immessi usando tastiere e IME (Input Method Editor) di Windows sono conformi al formato di normalizzazione C definito nello standard Unicode, la conversione dei dati in ingresso da altre piattaforme tramite le funzioni di normalizzazione Unicode NLS offre risultati più coerenti, in particolare per le impostazioni locali che usano lo script alfabeto giapponese o lo script Hangul per hangul moderno. Per altre informazioni sul supporto della normalizzazione Unicode in Windows Vista e versioni successive, vedere Uso della [normalizzazione Unicode per rappresentare stringhe](using-unicode-normalization-to-represent-strings.md).

Quando il confronto tra stringhe segue la preferenza di lingua dell'utente, ad esempio quando si ordinano gli elementi per un controllo ListView ordinato, l'applicazione può eseguire una delle operazioni seguenti:

-   Chiamare [**lstrcmp o**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) [**lstrcmpi con**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) le impostazioni locali dell'utente.
-   Chiamare [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) o [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) per definire le impostazioni locali per il confronto, passare flag aggiuntivi, incorporare caratteri Null o passare lunghezze esplicite in modo che corrispondano a parti di una stringa.

Quando i risultati del confronto devono essere coerenti indipendentemente dalle impostazioni locali, ad esempio quando si confrontano i dati recuperati con un elenco predefinito o un valore interno, l'applicazione deve usare [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) o [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) con il parametro *Locale* impostato su \_ LOCALE INVARIANT. Per [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), una delle chiamate seguenti corrisponderà anche se mystr è "INLAP". In questo caso, una chiamata con distinzione delle impostazioni locali a [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) avrà esito negativo se le impostazioni locali correnti sono di tipo taiwanese.

In Windows XP:


```C++
int iReturn = CompareString(LOCALE_INVARIANT, NORM_IGNORECASE, mystr, -1, _T("InLap"), -1);
```



Nei sistemi operativi precedenti:


```C++
DWORD lcid = MAKELCID(MAKELANGID(LANG_ENGLISH, SUBLANG_ENGLISH_US), SORT_DEFAULT);
int iReturn = CompareString(lcid, NORM_IGNORECASE, mystr, -1, _T("InLap"), -1);
```



## <a name="sort-strings-ordinally"></a>Ordinare le stringhe ordinalmente

Per l'ordinamento ordinale (non linguistico), le applicazioni devono sempre usare la [**funzione CompareStringOrdinal.**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal)

> [!Note]  
> Questa funzione è disponibile solo per Windows Vista e versioni successive.

 

[**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) confronta due stringhe [Unicode](unicode.md) per verificare l'uguaglianza binaria, anziché l'uguaglianza linguistica. Esempi di tali stringhe non linguistiche sono i nomi di file NTFS, le variabili di ambiente e i nomi di mutex, named pipe o mailslot. Fatta eccezione per l'opzione di senza distinzione tra maiuscole e minuscole, questa funzione ignora tutte le equivalenze non binarie. A differenza di altre funzioni di ordinamento, verifica l'uguaglianza di tutti i punti di codice, inclusi quelli a cui non viene assegnato alcun peso negli schemi di ordinamento linguistici.

Tutte le istruzioni seguenti si applicano a [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) nei confronti binari, ma non a [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)o [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia).

-   Le sequenze canonicamente equivalenti in Unicode, ad esempio LATIN SMALL LETTER A WITH RING ABOVE (U+00e5) e LATIN SMALL LETTER A + COMBINING RING ABOVE (U+0061 U+030a), non sono uguali anche se appaiono identiche ("å").
-   Le stringhe canonicamente simili in Unicode, ad esempio LATIN LETTER SMALL CAPITAL Y (U+028f) e LATIN CAPITAL LETTER Y (U+0059), che hanno un aspetto molto simile ("ʏ" e "Y") e variano solo in base ad alcuni pesi speciali delle maiuscole e minuscole nelle tabelle linguistiche, vengono considerate caratteri completamente diversi. Anche se l'applicazione imposta *bIgnoreCase* su **TRUE,** queste stringhe vengono confrontate come diverse.
-   I punti di codice definiti ma senza peso di ordinamento linguistico, ad esempio ZERO WIDTH JOINER (U+200d), vengono considerati come con i pesi dei punti di codice.
-   I punti di codice definiti nelle versioni successive di Unicode, ma che non hanno peso nelle tabelle linguistiche correnti, vengono considerati ponderi dei punti di codice.
-   I punti di codice non definiti da Unicode vengono considerati come con i relativi pesi dei punti di codice.
-   Quando l'applicazione imposta *bIgnoreCase* su **TRUE,** la funzione esegue il mapping tra maiuscole e minuscole usando la tabella maiuscola del sistema operativo anziché le informazioni nelle tabelle di ordinamento linguistiche. Il mapping è quindi indipendente dalle impostazioni locali.

Per altre informazioni sulle sequenze equivalenti canonicamente in stringhe Unicode e simili canonicamente in Unicode, vedere Uso della [normalizzazione Unicode per rappresentare stringhe](using-unicode-normalization-to-represent-strings.md).

## <a name="sort-code-points"></a>Ordinare i punti di codice

Alcuni punti di codice Unicode non hanno peso, ad esempio ZERO WIDTH NON JOINER, U+200c. Le funzioni di ordinamento valutano intenzionalmente i punti di codice senza peso come equivalenti perché non hanno peso nell'ordinamento. In Windows Vista e versioni successive, l'applicazione può ordinare questi punti di codice chiamando le funzioni di confronto delle stringhe NLS, in particolare [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal), per la valutazione di tutti i punti di codice in un valore letterale, senso binario, ad esempio nella convalida della password. Nei sistemi operativi Windows Vista, l'applicazione deve usare la funzione di runtime C **strcmp** o **wcscmp**.

Le funzioni di ordinamento ignorano i segni diacritici, ad esempio NON SPACING BREVE, U+0306, quando l'applicazione specifica il \_ flag NONSPACE hlink. Analogamente, queste funzioni ignorano i simboli, ad esempio EQUALS SIGN, U+003d , quando viene specificato il \_ flag hlink SYMBOLS. In Windows Vista e versioni successive, l'applicazione chiama [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) per la valutazione dei segni diacritici e dei punti di codice dei simboli in un senso letterale binario. Nei sistemi operativi Windows Vista, l'applicazione deve usare **strcmp** o **wcscmp**.

Alcuni punti di codice, ad esempio 0xFFFF e 0x058b, non sono attualmente assegnati in Unicode. Questi punti di codice non ricevono alcun peso nell'ordinamento e non devono mai essere passati alle funzioni di ordinamento. L'applicazione deve [**usare IsNLSDefinedString per**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) rilevare i punti di codice non Unicode in un flusso di dati.

> [!Note]  
> I risultati di [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) possono variare a seconda della versione Unicode passata se un carattere viene aggiunto a Unicode in una versione successiva e successivamente viene aggiunto alle tabelle Windows ordinamento. Per altre informazioni, vedere Usare il [controllo delle versioni dell'ordinamento.](#use-sort-versioning)

 

## <a name="sort-digits-as-numbers"></a>Ordinare le cifre come numeri

In Windows 7 e versioni successive, l'applicazione può chiamare [**CompareString,**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) [**CompareStringEx,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)o [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) usando il flag SORT \_ DIGITSASNUMBERS. Questo flag supporta l'ordinamento che considera le cifre come numeri, ad esempio l'ordinamento di "2" prima di "10".

Si noti che l'uso di questo flag non è appropriato per le cifre esadecimali come le seguenti. <dl> 01AF  
1BCD  
002A  
12FA  
AB1C  
AB02  
AB12  
</dl>

In questo caso i "numeri" sono ordinati in ordine, ma l'utente considera un elenco esadecimale ordinato in modo non corretto.

## <a name="map-strings"></a>Eseguire il mapping di stringhe

L'applicazione usa [**la funzione LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) o [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) per eseguire il mapping delle stringhe, se l'opzione LCMAP \_ SORTKEY non è specificata. Una stringa mappata ha terminazione Null se la stringa di origine ha terminazione Null.

Quando si esegue la trasformazione tra maiuscole e minuscole, la funzione non garantisce che un singolo carattere verrà mappato a un singolo carattere. Ad esempio, i flag LCMAP LOWERCASE e LCMAP UPPERCASE possono eseguire il mapping di \_ \_ German Sharp S ("") a se stesso. In alternativa, il flag LCMAP UPPERCASE può eseguire il mapping di "zioni" a "SS" e il flag LCMAP LOWERCASE può eseguire il \_ mapping di \_ "SS" a "zioni". Il comportamento dipende dalla versione NLS.

Quando si esegue la trasformazione tra maiuscole e minuscole, la funzione non è sensibile al contesto. Ad esempio, mentre il flag LCMAP UPPERCASE esegue correttamente il mapping tra il sigma minuscolo greco ("σ") e il sigma finale minuscolo greco ("ς") al sigma maiuscolo greco ("Σ"), il flag LCMAP LOWERCASE esegue sempre il mapping di "Σ" a "σ", mai a \_ \_ "ς".

Per impostazione predefinita, la funzione esegue il mapping della "i" minuscola alla "I" maiuscola, anche quando il parametro *Locale* specifica turco o azerbaigian. Per eseguire l'override di questo comportamento per il turco o l'azerbaigian, l'applicazione deve specificare LCMAP \_ LINGUISTIC \_ CASING. Se questo flag viene specificato con le impostazioni locali appropriate, " più" (I senza punto minuscolo) è la forma minuscola di "I" (I senza punto maiuscolo) e "i" (punto minuscolo I) è la forma minuscola di " PIÙ" (I punteggiata maiuscola).

Se si specifica il flag LCMAP HIRAGANA per eseguire il mapping dei caratteri katakana ai caratteri hiragana e LCMAP FULLWIDTH non è \_ \_ specificato, [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) o [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) esegue il mapping solo dei caratteri a larghezza intera all'hiragana. In questo caso, tutti i caratteri katakana a metà larghezza vengono inseriti come nella stringa di destinazione, senza mapping a hiragana. L'applicazione deve specificare LCMAP FULLWIDTH per eseguire il mapping dei caratteri katakana a metà \_ larghezza a hiragana. Il motivo di questa restrizione è che tutti i caratteri hiragana sono caratteri a larghezza intera.

Se l'applicazione deve rimuovere i caratteri dalla stringa di origine, può chiamare la funzione di mapping con i flag NORM IGNORESYMBOLS e NORM IGNORENONSPACE impostati e tutti gli altri \_ \_ flag cancellati. Se l'applicazione esegue questa operazione con una stringa di origine che non ha terminazione Null, è possibile che la funzione restituirà una stringa vuota e non restituirà un errore.

## <a name="create-sort-keys"></a>Creare chiavi di ordinamento

Quando l'applicazione specifica LCMAP \_ SORTKEY, [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) o [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) genera una chiave di ordinamento, una matrice binaria di valori byte. La chiave di ordinamento non è una stringa vera e i relativi valori rappresentano il comportamento di ordinamento della stringa di origine, ma non sono valori di visualizzazione significativi.

> [!Note]  
> La funzione ignora la kashida araba durante la generazione di una chiave di ordinamento. Se un'applicazione chiama la funzione per creare una chiave di ordinamento per una stringa contenente un kashida arabo, la funzione non crea alcun valore di chiave di ordinamento.

 

La chiave di ordinamento può contenere un numero dispari di byte. Il flag LCMAP \_ BYTEREV inverte solo un numero pari di byte. L'ultimo byte (in posizione dispari) nella chiave di ordinamento non viene invertito. Se l'0x00 byte di terminazione è un byte in posizione dispari, rimane l'ultimo byte nella chiave di ordinamento. Se l'0x00 byte di terminazione è un byte posizionato in modo uniforme, scambia le posizioni con il byte che lo precede.

Quando si genera la chiave di ordinamento, la funzione considera il trattino e l'apostrofo in modo diverso dagli altri simboli di punteggiatura, in modo che parole come "coop" e "co-op" rimangano insieme in un elenco. Tutti i simboli di punteggiatura diversi dal trattino e dall'apostrofo vengono ordinati prima dei caratteri alfanumerici. L'applicazione può modificare questo comportamento impostando il flag SORT \_ STRINGSORT, come descritto in [Funzioni di ordinamento](#sorting-functions).

Se usata in [memcmp](/cpp/c-runtime-library/reference/memcmp-wmemcmp), la chiave di ordinamento produce lo stesso ordine di quando la stringa di origine viene usata in [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) o [**CompareStringEx.**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) È consigliabile usare la funzione [memcmp](/cpp/c-runtime-library/reference/memcmp-wmemcmp) anziché [strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp), perché la chiave di ordinamento può contenere byte Null incorporati.

## <a name="use-sort-versioning"></a>Usare il controllo delle versioni dell'ordinamento

Una [tabella di](sorting.md) ordinamento include due numeri che ne identificano la versione: la versione definita e la versione NLS. Entrambi i numeri sono valori DWORD, composti da un valore principale e da un valore secondario. Il primo byte di un valore è riservato, i due byte successivi rappresentano la versione principale e l'ultimo byte rappresenta la versione secondaria. In termini esadecimali, il modello è 0xRRMMMMmm, dove R è uguale a Reserved, M è uguale a major e m è uguale a minor. Ad esempio, una versione principale di 3 con una versione secondaria di 4 è rappresentata come 0x304.

La versione definita identifica l'area dei punti di codice ed è la stessa per tutte le impostazioni locali. La versione principale viene incrementata per indicare le modifiche ai punti di codice esistenti. La versione secondaria viene incrementata per indicare che sono stati aggiunti punti di codice, ma che non sono stati modificati punti di codice esistenti in precedenza.

La versione NLS è [](locale-identifiers.md) specifica di un identificatore delle impostazioni locali o del nome delle impostazioni locali [e](locale-names.md)tiene traccia delle modifiche apportate ai pesi dei punti di codice per le impostazioni locali interessate. La versione principale viene incrementata quando vengono modificati i pesi per i punti di codice già ordinabili. La versione secondaria viene incrementata quando ai nuovi punti di codice vengono assegnati pesi, ma tutti gli altri pesi dei punti di codice ordinabili in precedenza rimangono invariati.

> [!Note]  
> Per una versione principale, uno o più punti di codice vengono modificati in modo che l'applicazione deve indicizzare nuovamente tutti i dati affinché i confronti siano validi. Per una versione secondaria, non viene spostato nulla, ma vengono aggiunti punti di codice. Per questo tipo di versione, l'applicazione deve solo indicizzare nuovamente le stringhe con valori precedentemente non ordinabili.

 

> [!IMPORTANT]
> La versione principale è stata modificata in Windows 8. I dati creati nelle versioni precedenti di Windows devono essere indicizzati nuovamente.

 

Sia la versione definita che la versione NLS si applicano ai punti di codice ordinabili recuperati usando la funzione [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) o [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) con il flag SORTKEY LCMAP e vengono usate anche dalle funzioni \_ [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)e [**FindNLSStringEx.**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) Se uno o più punti di codice in una stringa non sono ordinabili, la funzione [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) restituisce **FALSE** quando tale stringa viene passata come parametro.

L'applicazione può chiamare [**GetNLSVersion**](/windows/desktop/api/Winnls/nf-winnls-getnlsversion) o [**GetNLSVersionEx**](/windows/desktop/api/Winnls/nf-winnls-getnlsversionex) per recuperare sia la versione definita che la versione NLS per una tabella di ordinamento.

## <a name="index-the-database"></a>Indicizzare il database

Per motivi di prestazioni, l'applicazione deve seguire questa procedura durante l'indicizzazione del database.

**Per indicizzare correttamente il database**

1.  Per ogni funzione, archiviare la versione NLS, le chiavi di ordinamento di tale versione e un'indicazione dell'ordinabilità per ogni stringa indicizzata.
2.  Quando la versione secondaria viene incrementata, indicizzare nuovamente le stringhe precedentemente non ordinabili. Le stringhe interessate da questo aggiornamento devono essere limitate a quelle per cui [**IsNLSDefinedString ha**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) restituito in precedenza **FALSE.**
3.  Quando la versione principale viene incrementata, indicizzare nuovamente tutte le stringhe perché i pesi aggiornati potrebbero modificare il comportamento di qualsiasi stringa. Le versioni principali sono molto poco frequenti.

I problemi di indicizzazione del database possono verificarsi per i motivi seguenti:

-   Un sistema operativo successivo può definire punti di codice non definiti per un sistema operativo precedente, modificando così l'ordinamento.
-   I punti di codice possono avere pesi di ordinamento diversi in sistemi operativi diversi, a causa delle correzioni nel supporto della lingua.

Per ridurre al minimo la necessità di indicizzare nuovamente il database in queste circostanze, l'applicazione può usare [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) per distinguere le stringhe definite da quelle non definite in modo che l'applicazione possa rifiutare le stringhe con punti di codice non definiti. [**L'uso di GetNLSVersion**](/windows/desktop/api/Winnls/nf-winnls-getnlsversion) o [**GetNLSVersionEx**](/windows/desktop/api/Winnls/nf-winnls-getnlsversionex) consente all'applicazione di determinare se una modifica NLS influisce sulle impostazioni locali usate per una tabella di indice specifica. Se la modifica non ha alcun effetto sulle impostazioni locali, l'applicazione non deve indicizzare nuovamente la tabella.

## <a name="examples"></a>Esempio

Nella tabella seguente vengono illustrati gli effetti di alcuni flag usati con le funzioni di ordinamento. In ogni caso, la selezione dei flag determina se due caratteri diversi vengono considerati uguali ai fini dell'ordinamento.



| Carattere 1                                                        | Carattere 2                                             | Predefinito | NORM \_ IGNOREWIDTH | NORM \_ IGNOREKANA | NORM \_ IGNOREWIDTH\| NORMIGNOREKANA |
|--------------------------------------------------------------------|---------------------------------------------------------|---------|-------------------|------------------|------------------------------------|
| "あ"<br/> U+3042 HIRAGANA LETTER A<br/>                | "ガ"<br/> U+30A2 KATAKANA LETTER A<br/>     | Disuguale | Disuguale           | Uguale a            | Uguale a                              |
| "ｵ"<br/> U+FF75 HALFWIDTH KATAKANA LETTER O<br/>       | "オ"<br/> U+30AAA KATAKANA LETTER O<br/>     | Disuguale | Uguale a             | Disuguale          | Uguale a                              |
| "B"<br/> U+FF22 FULLWIDTH LATIN CAPITAL LETTER B<br/> | "B"<br/> U+0042 LATIN CAPITAL LETTER B<br/> | Disuguale | Uguale a             | Disuguale          | Uguale a                              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del supporto linguistico nazionale](using-national-language-support.md)
</dt> <dt>

[Ordinamento](sorting.md)
</dt> <dt>

[Recupero e impostazione delle informazioni sulle impostazioni locali](retrieving-and-setting-locale-information.md)
</dt> <dt>

[Uso della normalizzazione Unicode per rappresentare stringhe](using-unicode-normalization-to-represent-strings.md)
</dt> <dt>

[Considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md)
</dt> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)
</dt> <dt>

[**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal)
</dt> <dt>

[**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)
</dt> <dt>

[**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)
</dt> <dt>

[**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> <dt>

[**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex)
</dt> </dl>

 

 
