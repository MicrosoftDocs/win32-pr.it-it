---
description: In questo argomento vengono fornite informazioni sulle considerazioni sulla sicurezza correlate alle funzionalità di supporto internazionale.
ms.assetid: 4034f479-ad29-4c6f-82c6-977f420c4d4d
title: 'Considerazioni sulla sicurezza: funzionalità internazionali'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2e61566fdf51b80a76e5c8997018f35ce421dee6dd0e1b9e290888d96576249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147044"
---
# <a name="security-considerations-international-features"></a>Considerazioni sulla sicurezza: funzionalità internazionali

In questo argomento vengono fornite informazioni sulle considerazioni sulla sicurezza correlate alle funzionalità di supporto internazionale. È possibile usarlo come punto di partenza e quindi vedere la documentazione relativa alla tecnologia internazionale di interesse per considerazioni sulla sicurezza specifiche della tecnologia.

In questo argomento sono contenute le sezioni seguenti.

-   [Considerazioni sulla sicurezza per le funzioni di conversione dei caratteri](#security-considerations-for-character-conversion-functions)
-   [Considerazioni sulla sicurezza per le funzioni di confronto](#security-considerations-for-comparison-functions)
-   [Considerazioni sulla sicurezza per i set di caratteri nei nomi file](#security-considerations-for-character-sets-in-file-names)
-   [Considerazioni sulla sicurezza per i nomi di dominio internazionalizzati](#security-considerations-for-internationalized-domain-names)
-   [Considerazioni sulla sicurezza per le funzioni ANSI](#security-considerations-for-ansi-functions)
-   [Considerazioni sulla sicurezza per la normalizzazione Unicode](#security-considerations-for-unicode-normalization)

## <a name="security-considerations-for-character-conversion-functions"></a>Considerazioni sulla sicurezza per le funzioni di conversione dei caratteri

[**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) sono le funzioni Unicode e dei set di caratteri più comunemente usate per convertire i caratteri tra ANSI e Unicode. Queste funzioni possono causare rischi per la sicurezza perché contano gli elementi dei buffer di input e output in modo diverso. Ad esempio, [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) accetta un buffer di input conteggiato in byte e inserisce i caratteri convertiti in un buffer ridimensionato in caratteri Unicode. Quando l'applicazione usa questa funzione, deve ridimensionare correttamente i buffer per evitare un sovraccarico del buffer.

[**Per impostazione predefinita, WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) è il mapping "più adatto" per le pagine di codice, ad esempio 1252. Tuttavia, questo tipo di mapping consente più rappresentazioni della stessa stringa, lasciando potenzialmente l'applicazione vulnerabile agli attacchi. Ad esempio, la lettera maiuscola a caratteri latini A con dieresi (" I") potrebbe essere mappata alla lettera maiuscola latino A ("A"); un carattere Unicode in una lingua asiatica potrebbe essere mappato a una barra ("/"). L'uso del flag WC \_ NO \_ BEST FIT \_ \_ CHARS è preferibile dal punto di vista della sicurezza.

Alcune pagine codici, ad esempio le code pages 5022x (iso-2022-x), sono intrinsecamente non sicure perché consentono più rappresentazioni della stessa stringa. Il codice scritto correttamente esegue controlli di sicurezza in formato Unicode, ma questi tipi di tabella codici espandono la vulnerabilità di attacco delle applicazioni e, se possibile, devono essere evitati.

## <a name="security-considerations-for-comparison-functions"></a>Considerazioni sulla sicurezza per le funzioni di confronto

I confronti di stringhe possono presentare potenzialmente problemi di sicurezza. Poiché tutte le funzioni di confronto sono leggermente diverse, una funzione potrebbe segnalare due stringhe come uguali, mentre un'altra funzione potrebbe considerarle distinte. Di seguito sono riportate diverse funzioni che le applicazioni possono usare per confrontare le stringhe:

-   [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia). Confronta due stringhe di caratteri in base alle regole delle impostazioni locali, senza distinzione tra maiuscole e minuscole. La funzione confronta le stringhe controllando i primi caratteri l'uno con l'altro, i secondi caratteri l'uno rispetto all'altro e così via, fino a quando non trova una disuguaglianza o raggiunge le estremità delle stringhe.
-   [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa). Confronta le stringhe usando tecniche simili a quelle di [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia). L'unica differenza è che [lstrcmp esegue un](/windows/win32/api/winbase/nf-winbase-lstrcmpa) confronto tra stringhe con distinzione tra maiuscole e minuscole.
-   [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) (Windows Vista e versioni successive). Eseguire un confronto tra stringhe in base alle impostazioni locali fornite dall'applicazione. [**CompareStringEx è**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) simile a [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), ma identifica le impostazioni locali in base al nome delle impostazioni [locali](locale-names.md) anziché all'identificatore delle impostazioni [locali](locale-identifiers.md). Queste funzioni sono simili a [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia) e [lstrcmp,](/windows/win32/api/winbase/nf-winbase-lstrcmpa) ad eccezione del fatto che operano su impostazioni locali specifiche anziché su impostazioni locali selezionate dall'utente.
-   [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) (Windows Vista e versioni successive). Confronta due stringhe Unicode per verificare l'equivalenza binaria. Fatta eccezione per la possibilità di non fare distinzione tra maiuscole e minuscole, questa funzione ignora tutte le equivalenze non binarie e verifica l'uguaglianza di tutti i punti di codice, inclusi i punti di codice che non hanno alcun peso negli schemi di ordinamento [linguistico.](sorting.md) Si noti che le altre funzioni di confronto citate in questo argomento non verificano l'uguaglianza di tutti i punti di codice.
-   [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) (Windows Vista e versioni successive). Individuare una stringa Unicode in un'altra stringa Unicode. [**FindNLSStringEx è**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) simile a [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), ad eccezione del fatto che identifica le impostazioni locali in base al nome delle impostazioni locali anziché all'identificatore delle impostazioni locali.
-   [**FindStringOrdinal**](/windows/desktop/api/Libloaderapi/nf-libloaderapi-findstringordinal) (Windows 7 e versioni successive). Individua una stringa Unicode in un'altra stringa Unicode. L'applicazione deve usare questa funzione invece [**di FindNLSString per**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring) tutti i confronti non linguistici.

Come [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia) e [lstrcmp,](/windows/win32/api/winbase/nf-winbase-lstrcmpa) [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) valuta le stringhe carattere per carattere. Tuttavia, molte lingue hanno elementi a più caratteri, ad esempio l'elemento a due caratteri "CH" nello spagnolo tradizionale. Poiché [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) usa le impostazioni locali fornite dall'applicazione per identificare gli elementi a più caratteri e [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia) [e lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa) usano le impostazioni locali del thread, le stringhe identiche potrebbero non essere uguali.

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) ignora i caratteri non definiti e quindi restituisce zero (che indica stringhe uguali) per molte coppie di stringhe piuttosto distinte. Una stringa può contenere valori non mappati ad alcun carattere o caratteri con semantica esterna al dominio dell'applicazione, ad esempio caratteri di controllo in un URL. Le applicazioni che usano questa funzione devono fornire gestori di errori e stringhe di test per assicurarsi che siano valide prima di usarle.

> [!Note]  
> Per Windows Vista e versioni successive, [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) è simile a [**CompareString.**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) I problemi di sicurezza sono identici per queste funzioni.

 

Problemi di sicurezza simili si applicano alle funzioni, ad [**esempio FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), che ese trovano confronti impliciti. A seconda dei flag impostati, i risultati della chiamata a [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring) per cercare una stringa all'interno di un'altra stringa possono variare notevolmente.

> [!Note]  
> Per Windows Vista e versioni successive, [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) è simile a [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring). I problemi di sicurezza sono identici per queste funzioni.

 

## <a name="security-considerations-for-character-sets-in-file-names"></a>Considerazioni sulla sicurezza per i set di caratteri nei nomi file

Windows tabella codici e i set di caratteri OEM usati nei sistemi in lingua giapponese contengono il simbolo Della Lingua (¥) anziché una barra rovesciata ( \\ ). Di conseguenza, il carattere Unicode è un carattere non consentito per i file system NTFS e FAT. Quando si esegue il mapping di Unicode a una tabella codici in lingua giapponese, le funzioni di conversione eseguano il mapping tra la barra rovesciata (U+005C) e il normale simbolo Unicode Unicode (U+00A5) a questo stesso carattere. Per motivi di sicurezza, le applicazioni non devono in genere consentire il carattere U+00A5 in una stringa Unicode che potrebbe essere convertita per l'uso come nome file FAT.

## <a name="security-considerations-for-internationalized-domain-names"></a>Considerazioni sulla sicurezza per i nomi di dominio internazionalizzati

I nomi IDN (Internationalized Domain Names) vengono specificati da Network Working Group [RFC 3490: Internationalizing Domain Names in Applications (IDNA).](http://www.faqs.org/rfcs/rfc3490.html) Lo standard introduce una serie di problemi di sicurezza.

I glifi che rappresentano determinati caratteri di script diversi potrebbero apparire simili o addirittura identici. In molti tipi di carattere, ad esempio, la lettera A minuscola cirillica ("a") non è distinguibile dalla lettera A minuscola latina ("a"). Non è possibile indicare visivamente che "example.com" e "example.com" sono due nomi di dominio diversi, uno con una A minuscola in latino nel nome, l'altro con una A minuscola cirillica. Un sito host senza scrupoli può usare questa ambiguità visiva per fingere di essere un altro sito in un attacco di spoofing.

Il set di caratteri esteso che IDNA consente per i nomi IDN ha anche un potenziale di spoofing all'interno di uno script specifico. Ad esempio, esiste una forte somiglianza tra il trattino meno ("-" U+002D), il trattino ("—" U+2010), il trattino unificatore ("-" U+2011), il trattino della figura ("\u2012" U+2012), il trattino ("-" U+2013) e il segno meno ("=" U+2212).

Problemi simili derivano da determinate composizione di compatibilità. Ad esempio, il singolo carattere Unicode NUMBER TWENTY FULL STOP ("20.", U+249B) viene convertito in "20". (U+0032 U+0030 U+002E) in un passaggio NamePrep, prima della conversione in Punycode. In altre parole, questa composizione inserisce un punto (arresto completo). Tali composizione hanno un potenziale di spoofing.

La combinazione di script diversi in un IDN non indica necessariamente lo spoofing o la finalità indotta. [Technical Report \# 36: Unicode Security Considerations](https://www.unicode.org/reports/tr36/#international_domain_names) (Report tecnico 36: Considerazioni sulla sicurezza Unicode) offre diversi esempi di IDN ragionevoli che contengono una combinazione di script, ad esempio XML-Документы.com ("Документы" è russo per "documenti").

Gli attacchi di spoofing non sono limitati ai nomi IDN. Ad esempio, "rnicrosoft.com" è simile a "microsoft.com", ma è un nome ASCII. Inoltre, un attacco di spoofing può essere effettuato tramite danneggiamento di un nome. L'aggiunta di etichette aggiuntive dopo un nome di marchio noto o l'inclusione del nome del marchio nel percorso di un URL etichettato come sicuro può confondere gli utenti non esperti, indipendentemente dall'uso dell'IDN. Per alcune impostazioni locali, i nomi IDN sono obbligatori e il formato Punycode di questi nomi non è accettabile, perché rende i nomi incompleti.

Per altre informazioni sui problemi di sicurezza indicati qui, oltre a un numero elevato di altri problemi relativi a IDNA, vedere Technical Report 36: Unicode Security Considerations ( Report tecnico [ \# 36: Considerazioni sulla sicurezza Unicode).](https://www.unicode.org/reports/tr36/#international_domain_names) Oltre a discussioni dettagliate sui problemi di sicurezza correlati a IDNA, questo report offre suggerimenti per la gestione dei nomi IDN sospetti nelle applicazioni.

## <a name="security-considerations-for-ansi-functions"></a>Considerazioni sulla sicurezza per le funzioni ANSI

> [!Note]  
> È consigliabile usare Unicode nelle applicazioni globalizzate, in particolare quelle nuove, se possibile. È consigliabile usare le funzioni ANSI solo se si dispone di motivi di override per non usare Unicode, ad esempio la conformità a un protocollo precedente che non supporta Unicode.

 

Molte funzioni NLS (National Language Support), ad esempio [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) e [**GetCalendarInfo,**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)hanno versioni ANSI specifiche, in questo caso **GetLocaleInfoA** e **GetCalendarInfoA,** rispettivamente. Quando l'applicazione usa la versione ANSI di una funzione con un sistema operativo basato su Unicode, ad esempio Windows NT, Windows 2000, Windows XP o Windows Vista, la funzione può avere esito negativo o produrre risultati non definiti. Se si ha un motivo interessante per usare le funzioni ANSI con un sistema operativo di questo tipo, assicurarsi che i dati passati dall'applicazione siano validi per ANSI.

## <a name="security-considerations-for-unicode-normalization"></a>Considerazioni sulla sicurezza per la normalizzazione Unicode

Poiché la normalizzazione Unicode può modificare la forma di una stringa, i meccanismi di sicurezza o gli algoritmi di convalida dei caratteri devono in genere essere implementati dopo la normalizzazione. Si consideri ad esempio un'applicazione con un'interfaccia Web che accetta un nome di file, ma non un nome di percorso. U+FF43 U+FF1A U+FF3C U+FF57 U+FF49 U+FF4E U+FF44 U+FF4F U+FF57 U+FF53 cambia `(c : \ w i n d o w s)` in U+0063 U+001A U+003C U+0077 U+0069 U+006E U+0064 U+006F U+0077 U+0073 con `(c:\windows)` normalizzazione KC. Se un'applicazione verifica la presenza dei due punti e della barra rovesciata prima di implementare la normalizzazione, il risultato può essere l'accesso non intenzionale ai file.

Sebbene la normalizzazione Unicode sia un elemento per rendere sicuri i sistemi operativi, tenere presente che la normalizzazione non è una sostituzione per un criterio di sicurezza completo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Set di caratteri usati nei nomi di file](character-sets-used-in-file-names.md)
</dt> <dt>

[Convenzioni per prototipi di funzione](conventions-for-function-prototypes.md)
</dt> <dt>

[Gestione dell'ordinamento nelle applicazioni](handling-sorting-in-your-applications.md)
</dt> <dt>

[Gestione dei nomi di dominio internazionalizzati (IDN)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[Unicode](unicode.md)
</dt> </dl>

 

 
