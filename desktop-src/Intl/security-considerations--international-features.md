---
description: In questo argomento vengono fornite informazioni sulle considerazioni sulla sicurezza relative alle funzionalità di supporto internazionale.
ms.assetid: 4034f479-ad29-4c6f-82c6-977f420c4d4d
title: 'Considerazioni sulla sicurezza: funzionalità internazionali'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb9f8b849e9fb1a07f01031832449b9c9027ae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234053"
---
# <a name="security-considerations-international-features"></a>Considerazioni sulla sicurezza: funzionalità internazionali

In questo argomento vengono fornite informazioni sulle considerazioni sulla sicurezza relative alle funzionalità di supporto internazionale. È possibile usarlo come punto di partenza per visualizzare la documentazione relativa alla tecnologia internazionale di interesse per considerazioni sulla sicurezza specifiche della tecnologia.

In questo argomento sono contenute le sezioni seguenti.

-   [Considerazioni sulla sicurezza per le funzioni di conversione dei caratteri](#security-considerations-for-character-conversion-functions)
-   [Considerazioni sulla sicurezza per le funzioni di confronto](#security-considerations-for-comparison-functions)
-   [Considerazioni sulla sicurezza per i set di caratteri nei nomi di file](#security-considerations-for-character-sets-in-file-names)
-   [Considerazioni sulla sicurezza per i nomi di dominio internazionalizzati](#security-considerations-for-internationalized-domain-names)
-   [Considerazioni sulla sicurezza per le funzioni ANSI](#security-considerations-for-ansi-functions)
-   [Considerazioni sulla sicurezza per la normalizzazione Unicode](#security-considerations-for-unicode-normalization)

## <a name="security-considerations-for-character-conversion-functions"></a>Considerazioni sulla sicurezza per le funzioni di conversione dei caratteri

[**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) sono le funzioni del set di caratteri e Unicode utilizzate più di frequente per convertire i caratteri tra ANSI e Unicode. Queste funzioni hanno il rischio di causare rischi per la sicurezza in quanto contano gli elementi dei buffer di input e di output in modo diverso. Ad esempio, [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) accetta un buffer di input conteggiato in byte e inserisce i caratteri convertiti in un buffer con dimensioni in caratteri Unicode. Quando l'applicazione usa questa funzione, deve ridimensionare correttamente i buffer per evitare un sovraccarico del buffer.

Per impostazione predefinita, [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) è il mapping più appropriato per le tabelle codici, ad esempio 1252. Tuttavia, questo tipo di mapping consente più rappresentazioni della stessa stringa, lasciando l'applicazione vulnerabile agli attacchi. Ad esempio, la lettera maiuscola latina A con dieresis ("Ä") può essere mappata alla lettera maiuscola latina A ("A"); è possibile eseguire il mapping di un carattere Unicode in una lingua asiatica a una barra ("/"). \_ \_ \_ \_ Per un punto di vista della sicurezza, è preferibile usare il flag WC non adatto per i caratteri.

Alcune tabelle codici, ad esempio, le tabelle codici 5022x (ISO-2022-x), sono intrinsecamente non sicure perché consentono più rappresentazioni della stessa stringa. Il codice scritto correttamente esegue controlli di sicurezza nel formato Unicode, ma questi tipi di tabelle codici espandono la suscettibilità degli attacchi delle applicazioni e dovrebbero essere evitati, se possibile.

## <a name="security-considerations-for-comparison-functions"></a>Considerazioni sulla sicurezza per le funzioni di confronto

I confronti tra stringhe possono potenzialmente presentare problemi di sicurezza. Poiché tutte le funzioni di confronto sono leggermente diverse, una funzione potrebbe segnalare due stringhe come uguali, mentre un'altra funzione potrebbe considerarle distinte. Di seguito sono riportate alcune funzioni che possono essere utilizzate dalle applicazioni per confrontare le stringhe:

-   [due](/windows/win32/api/winbase/nf-winbase-lstrcmpia). Confronta due stringhe di caratteri in base alle regole delle impostazioni locali, senza distinzione tra maiuscole e minuscole. La funzione Confronta le stringhe controllando i primi caratteri l'una dall'altra, il secondo tra loro e così via, fino a quando non trova una disuguaglianza o raggiunge le estremità delle stringhe.
-   [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa). Confronta le stringhe usando tecniche simili a quelle di [due](/windows/win32/api/winbase/nf-winbase-lstrcmpia). L'unica differenza è che [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa) esegue un confronto tra stringhe con distinzione tra maiuscole e minuscole.
-   [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) (Windows Vista e versioni successive). Eseguire un confronto tra stringhe per le impostazioni locali fornite dall'applicazione. [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) è simile a [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), ma identifica le impostazioni locali in base al [nome](locale-names.md) delle impostazioni locali anziché all' [identificatore delle impostazioni locali](locale-identifiers.md). Queste funzioni sono simili a [due](/windows/win32/api/winbase/nf-winbase-lstrcmpia) e [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa) , ad eccezione del fatto che operano su determinate impostazioni locali invece che sulle impostazioni locali selezionate dall'utente.
-   [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) (Windows Vista e versioni successive). Confronta due stringhe Unicode per testare l'equivalenza binaria. Ad eccezione dell'opzione di non fare distinzione tra maiuscole e minuscole, questa funzione ignora tutte le equivalenze non binarie e testa tutti i punti di codice per verificarne l'uguaglianza, inclusi i punti di codice a cui non è assegnato alcun peso negli schemi di [ordinamento](sorting.md) linguistico. Si noti che le altre funzioni di confronto indicate in questo argomento non testano tutti i punti di codice per verificarne l'uguaglianza.
-   [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) (Windows Vista e versioni successive). Individuare una stringa Unicode in un'altra stringa Unicode. [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) è simile a [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), ad eccezione del fatto che identifica le impostazioni locali in base al nome delle impostazioni locali anziché all'identificatore delle impostazioni locali.
-   [**FindStringOrdinal**](/windows/desktop/api/Libloaderapi/nf-libloaderapi-findstringordinal) (Windows 7 e versioni successive). Individua una stringa Unicode in un'altra stringa Unicode. L'applicazione deve usare questa funzione anziché [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring) per tutti i confronti non linguistici.

Analogamente a [due](/windows/win32/api/winbase/nf-winbase-lstrcmpia) e [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa), [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) valuta le stringhe per carattere. Tuttavia, molti linguaggi hanno elementi a più caratteri, ad esempio l'elemento a due caratteri "CH" nello spagnolo tradizionale. Poiché [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) utilizza le impostazioni locali fornite dall'applicazione per identificare gli elementi a più caratteri e [due](/windows/win32/api/winbase/nf-winbase-lstrcmpia) e [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa) utilizzano le impostazioni locali del thread, le stringhe identiche potrebbero non essere uguali.

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) ignora i caratteri non definiti e pertanto restituisce zero (che indica stringhe uguali) per molte coppie di stringhe che sono piuttosto distinte. Una stringa può contenere valori che non eseguono il mapping a un carattere o che possono contenere caratteri con semantica all'esterno del dominio dell'applicazione, ad esempio i caratteri di controllo in un URL. Le applicazioni che utilizzano questa funzione devono fornire gestori di errori e stringhe di test per assicurarsi che siano valide prima di utilizzarle.

> [!Note]  
> Per Windows Vista e versioni successive, [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) è simile a [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw). I problemi di sicurezza sono identici per queste funzioni.

 

Problemi di sicurezza analoghi si applicano alle funzioni, ad esempio [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), che effettuano confronti impliciti. A seconda dei flag impostati, i risultati della chiamata di [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring) per la ricerca di una stringa all'interno di un'altra stringa possono variare notevolmente.

> [!Note]  
> Per Windows Vista e versioni successive, [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) è simile a [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring). I problemi di sicurezza sono identici per queste funzioni.

 

## <a name="security-considerations-for-character-sets-in-file-names"></a>Considerazioni sulla sicurezza per i set di caratteri nei nomi di file

La tabella codici di Windows e i set di caratteri OEM usati nei sistemi in lingua giapponese contengono il simbolo Yen (¥) invece di una barra rovesciata ( \\ ). Quindi, il carattere yen è un carattere non consentito per i file system NTFS e FAT. Quando si esegue il mapping di Unicode a una tabella codici in lingua giapponese, le funzioni di conversione mappano sia la barra rovesciata (U + 005C) che il normale simbolo di yen Unicode (U + 00A5) allo stesso carattere. Per motivi di sicurezza, le applicazioni non dovrebbero in genere consentire il carattere U + 00A5 in una stringa Unicode che potrebbe essere convertita per essere usata come nome file FAT.

## <a name="security-considerations-for-internationalized-domain-names"></a>Considerazioni sulla sicurezza per i nomi di dominio internazionalizzati

I nomi di dominio internazionalizzati (IDN) vengono specificati dal gruppo di lavoro di rete [RFC 3490: internazionalizzazione Domain Names in Applications (IDNA)](http://www.faqs.org/rfcs/rfc3490.html). Lo standard introduce una serie di problemi di sicurezza.

I glifi che rappresentano determinati caratteri di script diversi possono apparire simili o addirittura identici. In molti tipi di carattere, ad esempio, il cirillico minuscolo A ("a") non è distinguibile dalla minuscola latina A ("a"). Non è possibile indicare visivamente che "example.com" e "example.com" sono due nomi di dominio diversi, uno con un minuscolo latino a nel nome, l'altro con un minuscolo cirillico. Un sito host senza scrupoli può utilizzare questa ambiguità visiva per fingersi di essere un altro sito in un attacco di spoofing.

Il set di caratteri esteso che IDNA consente a IDN ha anche un potenziale di spoofing in uno script specifico. Ad esempio, esiste una somiglianza forte tra il segno meno ("-" U + 002D), il trattino ("-" U + 2010), il trattino non di rilievo ("-" U + 2011), la figura Dash ("\u2012" U + 2012), il trattino ("–" U + 2013) e il segno meno ("−" U + 2212).

Problemi simili derivano da determinate composizioni di compatibilità. Ad esempio, il singolo carattere Unicode numero TWENTY FULL STOP ("20.", U + 249B) viene convertito in "20". (U + 0032 U + 0030 U + 002E) in un passaggio profili Nameprep, prima della conversione in Punycode. In altre parole, questa composizione inserisce un punto (arresto completo). Tali composizioni hanno un potenziale di spoofing.

La combinazione di script diversi in un IDN non indica necessariamente lo spoofing o lo scopo ingannevole. [Rapporto tecnico \# 36: considerazioni sulla sicurezza Unicode](https://www.unicode.org/reports/tr36/#international_domain_names) offre diversi esempi di IDN ragionevoli che contengono una combinazione di script, ad esempio XML-Документы. com ("Документы" è il russo per "Documents").

Gli attacchi di spoofing non sono limitati a IDN. Ad esempio, "rnicrosoft.com" ha un aspetto simile a "microsoft.com", ma è un nome ASCII. Inoltre, un attacco di spoofing può essere eseguito tramite il danneggiamento di un nome. Se si aggiungono etichette aggiuntive dopo un nome di marchio noto o si include il nome del marchio nel percorso di un URL con etichetta protetta, è possibile confondere gli utenti con il novizio, indipendentemente dall'uso di IDN. Per alcune impostazioni locali, IDN sono obbligatori e il form Punycode di questi nomi non è accettabile, perché rende i nomi simili.

Per ulteriori informazioni sui problemi di sicurezza indicati qui, oltre a un numero elevato di altri problemi relativi a IDNA, vedere [Technical Report \# 36: Unicode Security Considerations](https://www.unicode.org/reports/tr36/#international_domain_names). Insieme a discussioni dettagliate sui problemi di sicurezza correlati a IDNA, questo report offre suggerimenti per la gestione dei IDN sospetti nelle applicazioni.

## <a name="security-considerations-for-ansi-functions"></a>Considerazioni sulla sicurezza per le funzioni ANSI

> [!Note]  
> È consigliabile usare Unicode nelle applicazioni globalizzate, in particolare quelle nuove, se possibile. È consigliabile utilizzare le funzioni ANSI solo se si dispone di motivi di override per non utilizzare Unicode, ad esempio la conformità a un protocollo precedente che non supporta Unicode.

 

Molte funzioni NLS (National Language Support), ad esempio [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) e [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa), presentano versioni ANSI specifiche, in questo caso, rispettivamente **GetLocaleInfoA** e **GetCalendarInfoA**. Quando l'applicazione utilizza la versione ANSI di una funzione con un sistema operativo basato su Unicode, ad esempio Windows NT, Windows 2000, Windows XP o Windows Vista, la funzione può avere esito negativo o produrre risultati non definiti. Se è necessario usare funzioni ANSI con un sistema operativo di questo tipo, assicurarsi che i dati passati dall'applicazione siano validi per ANSI.

## <a name="security-considerations-for-unicode-normalization"></a>Considerazioni sulla sicurezza per la normalizzazione Unicode

Poiché la normalizzazione Unicode può modificare il formato di una stringa, i meccanismi di sicurezza o gli algoritmi di convalida dei caratteri devono essere implementati in genere dopo la normalizzazione. Si consideri, ad esempio, un'applicazione con un'interfaccia Web che accetta un nome di file, ma non accetta un nome di percorso. Un U + FF43 U + FF1A u + FF3C u + FF57 U + FF49 u + FF4E u + FF44 u + FF4F u + FF57 u + FF53 u + 0063 u + 001A u + 003C u + 0077 u + 0069 u + 006E u + 0064 u + 006F u + 0077 u + 0073 u + u + `(c : \ w i n d o w s)` `(c:\windows)` con la NORMALIzzazione KC del modulo. Se un'applicazione verifica la presenza dei due punti e della barra rovesciata prima di implementare la normalizzazione, il risultato può essere l'accesso ai file non intenzionale.

Sebbene la normalizzazione Unicode sia un elemento per la sicurezza dei sistemi operativi, tenere presente che la normalizzazione non è una sostituzione per i criteri di sicurezza completi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Set di caratteri utilizzati nei nomi file](character-sets-used-in-file-names.md)
</dt> <dt>

[Convenzioni per prototipi di funzione](conventions-for-function-prototypes.md)
</dt> <dt>

[Gestione dell'ordinamento nelle applicazioni](handling-sorting-in-your-applications.md)
</dt> <dt>

[Gestione dei nomi di dominio internazionalizzati (IDN)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[Unicode](unicode.md)
</dt> </dl>

 

 
