---
description: Alcune applicazioni, ad esempio Microsoft Active Directory, Microsoft Exchange e Microsoft Access, gestiscono un database ordinabile di stringhe delle impostazioni locali e della lingua indicizzate in base al nome (stringa UTF-16) e ai relativi pesi di ordinamento.
ms.assetid: c8fc32bd-02bd-4a40-a836-d9ad9f69c209
title: Gestione dell'ordinamento nelle applicazioni
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: c0bba3d78a5219781226ecf58292ed461c902090
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885725"
---
# <a name="handling-sorting-in-your-applications"></a>Gestione dell'ordinamento nelle applicazioni

Alcune applicazioni, ad esempio Microsoft Active Directory, Microsoft Exchange e Microsoft Access, gestiscono un database ordinabile di stringhe delle impostazioni locali e della lingua indicizzate in base al nome (stringa UTF-16) e ai relativi pesi di ordinamento.

L' [ordinamento](sorting.md) è in genere intuitivo per gli utenti nelle rispettive impostazioni locali. Tuttavia, può essere non intuitivo per gli sviluppatori di applicazioni. In questo argomento vengono illustrate le considerazioni per la gestione dell'ordinamento nelle applicazioni. L'ordinamento può essere linguistico o ordinale (non linguistico).

## <a name="sorting-functions"></a>Funzioni di ordinamento

Nelle applicazioni è possibile utilizzare un'ampia gamma di funzioni di ordinamento:

-   Funzioni di confronto delle stringhe NLS. Esempi sono [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) e [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal), [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex), [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)e [**FindStringOrdinal**](/windows/desktop/api/Libloaderapi/nf-libloaderapi-findstringordinal). Vedere [considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md) per una discussione sui problemi di sicurezza correlati alle funzioni di confronto delle stringhe.
-   Funzioni wrapper che chiamano internamente le funzioni di confronto tra stringhe. Le funzioni più comuni sono [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) e [**due**](/windows/win32/api/winbase/nf-winbase-lstrcmpia), che chiamano [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw).

In genere, le funzioni di ordinamento valutano le stringhe per carattere. Tuttavia, molti linguaggi hanno elementi a più caratteri, ad esempio la coppia di due caratteri "CH" nello spagnolo tradizionale. [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) e [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) usano l'identificatore delle impostazioni locali fornito dall'applicazione o il nome per identificare gli elementi a più caratteri. Al contrario, [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)e [**due**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) usano le impostazioni locali dell'utente.

Un altro esempio è il vietnamita, che contiene molti elementi di due caratteri, ad esempio i caratteri maiuscoli, maiuscoli e minuscoli e le forme minuscole di "GI", che sono rispettivamente "GI," gi "e" gi ". Ognuno di questi moduli viene considerato come un singolo elemento di ordinamento e, se la combinazione di maiuscole e minuscole viene ignorata, viene confrontata con uguale. Tuttavia, poiché "gI" non è valido come singolo elemento, [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)e [**due**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) considerano "gi" come due elementi distinti.

Per impostazione predefinita, le funzioni [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa), [**due**](/windows/win32/api/winbase/nf-winbase-lstrcmpia), [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex), [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)e [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) usano una tecnica di tipo "Word Sort". Per questo tipo di ordinamento, tutti i segni di punteggiatura e altri caratteri non alfanumerici, ad eccezione del segno meno e dell'apostrofo, precedono qualsiasi carattere alfanumerico. Il trattino e l'apostrofo sono trattati in modo diverso rispetto agli altri caratteri non alfanumerici per garantire che parole come "Coop" e "co-op" rientrino insieme in un elenco ordinato.

Anziché un ordinamento di parole, l'applicazione può richiedere una tecnica di ordinamento delle stringhe dalle funzioni di ordinamento specificando il flag SORT \_ STRINGSORT. Un ordinamento stringa considera il trattino e l'apostrofo come qualsiasi altro carattere non alfanumerico. Le rispettive posizioni nella sequenza di ordinamento sono precedenti ai caratteri alfanumerici.

Nella tabella seguente vengono confrontati i risultati di un ordinamento di Word con i risultati di un ordinamento della stringa. 

| Ordinamento di Word | Ordinamento delle stringhe |
|-----------|-------------|
| billetta    | fattura      |
| bollette     | billetta      |
| fattura    | bollette       |
| non può    | possibile       |
| cant      | non può      |
| possibile     | cant        |
| con       | Co-op       |
| Coop      | con         |
| Co-op     | Coop        |



 

## <a name="sort-strings-linguistically"></a>Ordinare le stringhe linguisticamente

Le funzioni [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) e [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) verificano l'uguaglianza linguistica. Le applicazioni devono usare queste funzioni con le impostazioni locali corrette per l'ordinamento linguistico delle stringhe.

> [!Note]  
> Per compatibilità con Unicode, un'applicazione deve preferire [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) o la versione Unicode di [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw). Un altro motivo per cui si fa riferimento a [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) è che Microsoft sta eseguendo la migrazione verso l'uso di nomi di impostazioni locali anziché identificatori delle impostazioni locali per le nuove impostazioni locali, per motivi di interoperabilità. Qualsiasi applicazione eseguita solo in Windows Vista e versioni successive deve usare [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex).

 

Un altro modo per verificare l'uguaglianza linguistica consiste nell'usare [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) o [**due**](/windows/win32/api/winbase/nf-winbase-lstrcmpia), che usano sempre un ordinamento di Word. La funzione [**due**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) chiama [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) con il \_ flag ignoreCase Norm, mentre [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) lo chiama senza tale flag. Per una panoramica dell'uso delle funzioni wrapper, vedere [**stringhe**](../menurc/strings.md).

Le funzioni recuperano i risultati linguisticamente appropriati per tutte le impostazioni locali. Le aspettative dell'utente per diverse impostazioni locali possono differire significativamente nel comportamento di ordinamento, come illustrato negli esempi seguenti.

-   Molte impostazioni locali equivalgono alla legatura AE (æ) con le lettere AE. Tuttavia, islandese (Islanda) considera una lettera separata e la posiziona dopo la Z nella sequenza di ordinamento.
-   L'anello A (Å) in genere Ordina semplicemente una differenza diacritici da un oggetto. Tuttavia, svedese (Svezia) posiziona l'anello dopo la Z nella sequenza di ordinamento.

Le funzioni tentano di verificare rigorosamente che i punti di codice definiti nello standard Unicode siano canonicamente uguali a una stringa di punti di codice equivalenti. Ad esempio, il punto di codice che rappresenta un "u" minuscolo con una dieresis (ü) è canonicamente uguale a una "u" minuscola combinata con la dieresis (̈). Si noti, tuttavia, che l'equivalenza canonica non è sempre possibile.

Poiché quasi tutti i dati immessi con le tastiere di Windows e gli IME (Input Method Editor) sono conformi alla normalizzazione del formato C definita nello standard Unicode, la conversione dei dati in arrivo da altre piattaforme mediante le funzioni di normalizzazione di NLS Unicode fornisce risultati più coerenti, in particolare per le impostazioni locali che utilizzano lo script tibetano o lo script Hangul per la moderna hangul. Per ulteriori informazioni sul supporto per la normalizzazione Unicode in Windows Vista e versioni successive, vedere [utilizzo della normalizzazione Unicode per rappresentare le stringhe](using-unicode-normalization-to-represent-strings.md).

Quando il confronto tra stringhe segue la preferenza della lingua dell'utente, ad esempio quando si ordinano gli elementi per un controllo ListView ordinato, l'applicazione può eseguire una delle operazioni seguenti:

-   Chiamare [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) o [**due**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) con le impostazioni locali dell'utente.
-   Chiamare [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) o [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) per definire le impostazioni locali per il confronto, per passare flag aggiuntivi, per incorporare caratteri null o per passare lunghezze esplicite in modo che corrispondano alle parti di una stringa.

Quando i risultati del confronto devono essere coerenti indipendentemente dalle impostazioni locali, ad esempio quando si confrontano i dati recuperati con un elenco predefinito o un valore interno, l'applicazione deve usare [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) o [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) con il parametro delle *impostazioni locali* impostato su impostazioni locali \_ invarianti. Per [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), una delle chiamate seguenti corrisponderà anche se myStr è "INLAP". In questo caso, una chiamata dipendente dalle impostazioni locali a [**due**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) avrà esito negativo se le impostazioni locali correnti sono vietnamite.

In Windows XP:


```C++
int iReturn = CompareString(LOCALE_INVARIANT, NORM_IGNORECASE, mystr, -1, _T("InLap"), -1);
```



Nei sistemi operativi precedenti:


```C++
DWORD lcid = MAKELCID(MAKELANGID(LANG_ENGLISH, SUBLANG_ENGLISH_US), SORT_DEFAULT);
int iReturn = CompareString(lcid, NORM_IGNORECASE, mystr, -1, _T("InLap"), -1);
```



## <a name="sort-strings-ordinally"></a>Ordina stringhe ordinali

Per l'ordinamento ordinale (non linguistico), le applicazioni devono sempre usare la funzione [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) .

> [!Note]  
> Questa funzione è disponibile solo per Windows Vista e versioni successive.

 

[**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) Confronta due stringhe [Unicode](unicode.md) per verificare l'uguaglianza binaria, anziché l'uguaglianza linguistica. Esempi di stringhe non linguistiche sono i nomi di file NTFS, le variabili di ambiente e i nomi di mutex, Named Pipes o mailslot. Ad eccezione dell'opzione di senza distinzione tra maiuscole e minuscole, questa funzione ignora tutte le equivalenze non binarie. A differenza di altre funzioni di ordinamento, verifica l'uguaglianza di tutti i punti di codice, inclusi quelli che non hanno alcun peso negli schemi di ordinamento linguistico.

Tutte le istruzioni seguenti si applicano a [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) nei confronti binari, ma non a [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)o [**due**](/windows/win32/api/winbase/nf-winbase-lstrcmpia).

-   LE sequenze equivalenti canoniche in Unicode, ad esempio la minuscola latina A con anello sopra (U + 00e5) e la lettera latina MINUSCOLa A + anello di combinazione sopra (U + 0061 U + 030A), non sono uguali anche se appaiono identiche ("å").
-   Stringhe canonicamente simili in Unicode, ad esempio alfabeto latino SMALL CAPITAL Y (U + 028f) e LATIN CAPITAL LETTER Y (U + 0059), che hanno un aspetto molto simile ("ʏ" e "Y") e variano solo in base a un peso speciale dei casi nelle tabelle linguistiche, sono considerati caratteri completamente dissimili. Anche se l'applicazione imposta *bIgnoreCase* su **true**, queste stringhe vengono confrontate come diverse.
-   I punti di codice che sono definiti ma non hanno un peso di ordinamento linguistico, ad esempio un JOIN di larghezza ZERO (U + 200D), vengono trattati come aventi i pesi dei punti di codice.
-   I punti di codice definiti nelle versioni successive di Unicode, ma senza alcun peso nelle tabelle linguistiche correnti, vengono considerati come aventi i pesi dei punti di codice.
-   I punti di codice che non sono definiti da Unicode vengono considerati come aventi i pesi dei punti di codice.
-   Quando l'applicazione imposta *bIgnoreCase* su **true**, la funzione esegue il mapping del case utilizzando la tabella in maiuscolo del sistema operativo anziché le informazioni contenute nelle tabelle di ordinamento linguistico. Il mapping è quindi indipendente dalle impostazioni locali.

Per ulteriori informazioni sulle sequenze canonicamente equivalenti in Unicode e stringhe simili in modo canonico in Unicode, vedere [utilizzo della normalizzazione Unicode per rappresentare le stringhe](using-unicode-normalization-to-represent-strings.md).

## <a name="sort-code-points"></a>Ordina punti di codice

Alcuni punti di codice Unicode non hanno peso, ad esempio, la larghezza ZERO NON è un JOINer, U + 200C. Le funzioni di ordinamento valutano intenzionalmente i punti di codice non ponderati come equivalenti perché non hanno peso nell'ordinamento. In Windows Vista e versioni successive, l'applicazione può ordinare questi punti di codice chiamando le funzioni di confronto delle stringhe NLS, in particolare [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal), per la valutazione di tutti i punti di codice in un valore letterale, senso binario, ad esempio nella convalida della password. Nei sistemi operativi precedenti a Windows Vista, l'applicazione deve usare la funzione di runtime C **strcmp** o **wcscmp**.

Le funzioni di ordinamento ignorano i segni diacritici, ad esempio NON SPAZIatura BREVE, U + 0306, quando l'applicazione specifica il \_ flag Hlink nonspace. Analogamente, queste funzioni ignorano i simboli, ad esempio, il segno di uguale, U + 003D, quando \_ viene specificato il flag Hlink symbols. In Windows Vista e versioni successive, l'applicazione chiama [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) per la valutazione dei segni diacritici e dei punti di codice simbolo in un valore letterale, senso binario. Nei sistemi operativi precedenti a Windows Vista, l'applicazione deve usare **strcmp** o **wcscmp**.

Alcuni punti di codice, ad esempio 0xFFFF e 0x058B, non sono attualmente assegnati in Unicode. Questi punti di codice non ricevono alcun peso nell'ordinamento e non devono mai essere passati alle funzioni di ordinamento. L'applicazione deve usare [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) per rilevare i punti di codice non Unicode in un flusso di dati.

> [!Note]  
> I risultati di [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) possono variare a seconda della versione Unicode passata se un carattere viene aggiunto a Unicode in una versione successiva e viene successivamente aggiunto alle tabelle di ordinamento di Windows. Per ulteriori informazioni, vedere [utilizzo del controllo delle versioni di ordinamento](#use-sort-versioning).

 

## <a name="sort-digits-as-numbers"></a>Ordina cifre come numeri

In Windows 7 e versioni successive, l'applicazione può chiamare [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)o [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) usando il \_ flag Sort DIGITSASNUMBERS. Questo flag supporta l'ordinamento che considera le cifre come numeri, ad esempio l'ordinamento di "2" prima di "10".

Si noti che l'utilizzo di questo flag non è appropriato per cifre esadecimali come la seguente. <dl> 01AF  
1BCD  
002A  
12FA  
AB1C  
AB02  
AB12  
</dl>

In questo caso i "numeri" sono ordinati in ordine, ma l'utente percepisce un elenco esadecimale non ordinato.

## <a name="map-strings"></a>Stringhe mappa

L'applicazione usa la funzione [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) o [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) per eseguire il mapping delle stringhe, se \_ non è specificato LCMAP SORTKEY. Una stringa mappata è con terminazione null se la stringa di origine è con terminazione null.

Quando si esegue la trasformazione tra lettere maiuscole e minuscole, la funzione non garantisce che un singolo carattere venga mappato a un singolo carattere. Ad esempio, i \_ flag LCMAP minuscole e LCMAP \_ maiuscoli possono eseguire il mapping della lingua tedesca Sharp S ("ß") a se stessa. In alternativa, il \_ flag LCMAP maiuscolo può mappare "ß" a "SS" e il \_ flag LCMAP minuscole può eseguire il mapping di "SS" a "ß". Il comportamento dipende dalla versione NLS.

Quando si trasformano tra maiuscole e minuscole, la funzione non è sensibile al contesto. Se, ad esempio, il \_ flag LCMAP maiuscolo esegue correttamente il mapping di un Sigma minuscolo greco ("σ") e del Sigma minuscolo finale Sigma ("σ") a Sigma maiuscolo ("σ"), il \_ flag minuscolo LCMAP esegue sempre il mapping di "σ" a "σ", mai a "σ".

Per impostazione predefinita, la funzione esegue il mapping dei caratteri "i" minuscoli alla "I" maiuscola, anche quando il parametro delle *impostazioni locali* specifica turco o azero. Per eseguire l'override di questo comportamento per turco o Azero, l'applicazione deve specificare la LCMAP \_ linguistica \_ . Se questo flag viene specificato con le impostazioni locali appropriate, "ı" (dotless minuscolo i) è la forma minuscola di "I" (maiuscolo DOTLESS I) e "i" (punteggiato minuscolo I) è la forma minuscola di "i" (maiuscola punteggiata).

Se \_ viene specificato il flag hiragana LCMAP per eseguire il mapping dei caratteri Katakana a caratteri Hiragana e LCMAP \_ fullwidth non è specificato, [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) o [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) esegue solo il mapping di caratteri a larghezza intera a hiragana. In questo caso, qualsiasi carattere katakana a metà larghezza viene inserito come nella stringa di destinazione, senza mapping a hiragana. L'applicazione deve specificare LCMAP \_ fullwidth per eseguire il mapping dei caratteri Katakana a metà larghezza all'hiragana. Il motivo di questa restrizione è che tutti i caratteri hiragana sono caratteri a larghezza intera.

Se l'applicazione deve rimuovere i caratteri dalla stringa di origine, può chiamare la funzione di mapping con i \_ flag Norm IGNORESYMBOLS e Norm \_ IGNORENONSPACE impostati e tutti gli altri flag deselezionati. Se l'applicazione esegue questa operazione con una stringa di origine con terminazione null, è possibile che la funzione restituisca una stringa vuota e non restituisca un errore.

## <a name="create-sort-keys"></a>Creazione di chiavi di ordinamento

Quando l'applicazione specifica LCMAP \_ SORTKEY, [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) o [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) genera una chiave di ordinamento, una matrice binaria di valori di byte. La chiave di ordinamento non è una stringa vera e i relativi valori rappresentano il comportamento di ordinamento della stringa di origine, ma non sono valori di visualizzazione significativi.

> [!Note]  
> La funzione ignora il Kashida arabo durante la generazione di una chiave di ordinamento. Se un'applicazione chiama la funzione per creare una chiave di ordinamento per una stringa contenente una Kashida araba, la funzione non crea alcun valore della chiave di ordinamento.

 

La chiave di ordinamento può contenere un numero dispari di byte. Il \_ flag BYTEREV di LCMAP inverte solo un numero pari di byte. L'ultimo byte (con posizione dispari) nella chiave di ordinamento non viene invertito. Se il byte di terminazione 0x00 è un byte con posizione dispari, rimane l'ultimo byte della chiave di ordinamento. Se il byte di chiusura 0x00 è un byte posizionato in modo uniforme, scambia le posizioni con il byte che la precede.

Quando si genera la chiave di ordinamento, la funzione considera il trattino e l'apostrofo in modo diverso rispetto ad altri simboli di punteggiatura, in modo che le parole come "Coop" e "co-op" restino insieme in un elenco. Tutti i simboli di punteggiatura diversi dal trattino e dal tipo di apostrofo prima dei caratteri alfanumerici. L'applicazione può modificare questo comportamento impostando il \_ flag Sort STRINGSORT, come descritto in [funzioni di ordinamento](#sorting-functions).

Quando viene usato in [memcmp](/cpp/c-runtime-library/reference/memcmp-wmemcmp), la chiave di ordinamento produce lo stesso ordine in cui viene usata la stringa di origine in [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) o [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex). È necessario utilizzare la funzione [memcmp](/cpp/c-runtime-library/reference/memcmp-wmemcmp) anziché [strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp), perché la chiave di ordinamento può includere byte null incorporati.

## <a name="use-sort-versioning"></a>Usa controllo delle versioni di ordinamento

Una tabella di [ordinamento](sorting.md) presenta due numeri che ne identificano la versione, ovvero la versione definita e la versione NLS. Entrambi i numeri sono valori DWORD, composti da un valore principale e da un valore secondario. Il primo byte di un valore è riservato, i due byte successivi rappresentano la versione principale e l'ultimo byte rappresenta la versione secondaria. In termini esadecimali, il modello è 0xRRMMMMmm, dove R è uguale a reserved, M è uguale a Major e m è uguale a minor. Ad esempio, una versione principale di 3 con una versione secondaria di 4 viene rappresentata come 0x304.

La versione definita identifica il repertorio dei punti di codice ed è la stessa per tutte le impostazioni locali. La versione principale incrementa per indicare le modifiche ai punti di codice esistenti. La versione secondaria incrementa per indicare che i punti di codice sono stati aggiunti, ma che non sono stati modificati punti di codice precedentemente esistenti.

La versione NLS è specifica di un [identificatore delle impostazioni locali](locale-identifiers.md) o di un [nome delle impostazioni locali](locale-names.md)e tiene traccia delle modifiche apportate ai pesi dei punti di codice per le impostazioni locali interessate. La versione principale viene incrementata quando vengono modificati i pesi per i punti di codice già ordinabili. La versione secondaria viene incrementata quando vengono assegnati pesi ai nuovi punti di codice, ma tutti gli altri pesi dei punti di codice ordinati in precedenza rimangono invariati.

> [!Note]  
> Per una versione principale, uno o più punti di codice vengono modificati in modo che l'applicazione debba indicizzare nuovamente tutti i dati affinché i confronti siano validi. Per una versione secondaria, nessun elemento viene spostato, ma vengono aggiunti punti di codice. Per questo tipo di versione, l'applicazione deve solo reindicizzare le stringhe con valori precedentemente non ordinabili.

 

> [!IMPORTANT]
> La versione principale è stata modificata in Windows 8. È necessario reindicizzare i dati creati con versioni precedenti di Windows.

 

Entrambe le versioni NLS e definite si applicano ai punti di codice ordinabili recuperati tramite la funzione [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) o [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) con il flag di LCMAP \_ SORTKEY e usati anche dalle funzioni [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)e [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) . Se uno o più punti di codice in una stringa non sono ordinabili, la funzione [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) restituisce **false** quando tale stringa viene passata come parametro.

L'applicazione può chiamare [**GetNLSVersion**](/windows/desktop/api/Winnls/nf-winnls-getnlsversion) o [**GetNLSVersionEx**](/windows/desktop/api/Winnls/nf-winnls-getnlsversionex) per recuperare sia la versione definita che la versione NLS per una tabella di ordinamento.

## <a name="index-the-database"></a>Indicizzare il database

Per motivi di prestazioni, l'applicazione deve seguire questa procedura durante l'indicizzazione del database.

**Per indicizzare correttamente il database**

1.  Per ogni funzione, archiviare la versione NLS, le chiavi di ordinamento della versione e un'indicazione di ordinabilità per ogni stringa indicizzata.
2.  Quando viene incrementata la versione secondaria, indicizzare nuovamente le stringhe precedentemente non ordinate. Le stringhe interessate da questo aggiornamento devono essere confinate a quelle per cui [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) ha restituito in precedenza **false**.
3.  Quando la versione principale viene incrementata, indicizzare nuovamente tutte le stringhe perché i pesi aggiornati potrebbero modificare il comportamento di qualsiasi stringa. Le versioni principali sono molto rare.

È possibile che si verifichino problemi di indicizzazione del database per i motivi seguenti:

-   Un sistema operativo successivo può definire punti di codice non definiti per un sistema operativo precedente, modificando quindi l'ordinamento.
-   I punti di codice possono avere pesi di ordinamento diversi in sistemi operativi diversi, a causa di correzioni del supporto per le lingue.

Per ridurre al minimo la necessità di reindicizzare il database in queste circostanze, l'applicazione può utilizzare [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) per distinguere tra stringhe non definite, in modo che l'applicazione possa rifiutare stringhe con punti di codice non definiti. L'utilizzo di [**GetNLSVersion**](/windows/desktop/api/Winnls/nf-winnls-getnlsversion) o [**GetNLSVersionEx**](/windows/desktop/api/Winnls/nf-winnls-getnlsversionex) consente all'applicazione di determinare se una modifica NLS influisca sulle impostazioni locali utilizzate per una determinata tabella dell'indice. Se la modifica non ha alcun effetto sulle impostazioni locali, l'applicazione non deve reindicizzare la tabella.

## <a name="examples"></a>Esempio

Nella tabella seguente vengono illustrati gli effetti di determinati flag utilizzati con le funzioni di ordinamento. In ogni caso, la selezione dei flag determina se due caratteri diversi sono considerati uguali ai fini dell'ordinamento.



| Carattere 1                                                        | Carattere 2                                             | Predefinito | \_IGNOREWIDTH Norm | \_IGNOREKANA Norm | \_IGNOREWIDTH Norm \| NORMIGNOREKANA |
|--------------------------------------------------------------------|---------------------------------------------------------|---------|-------------------|------------------|------------------------------------|
| あ<br/> U + 3042 HIRAGANA LETTERA A<br/>                | "ガ"<br/> U + 30A2-LETTERA KATAKANA A<br/>     | Diversi | Diversi           | Uguale a            | Uguale a                              |
| "ｵ"<br/> U + FF75 CARATTERE KATAKANA LETTER O<br/>       | "オ"<br/> U + 30AA O LETTERA KATAKANA<br/>     | Diversi | Uguale a             | Diversi          | Uguale a                              |
| B<br/> U + FF22 FULLWIDTH LATIN CAPITAL LETTERA B<br/> | "B"<br/> U + 0042 LATIN CAPITAL LETTERA B<br/> | Diversi | Uguale a             | Diversi          | Uguale a                              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del supporto per le lingue nazionali](using-national-language-support.md)
</dt> <dt>

[Ordinamento](sorting.md)
</dt> <dt>

[Recupero e impostazione delle informazioni sulle impostazioni locali](retrieving-and-setting-locale-information.md)
</dt> <dt>

[Uso della normalizzazione Unicode per rappresentare le stringhe](using-unicode-normalization-to-represent-strings.md)
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

 

 
