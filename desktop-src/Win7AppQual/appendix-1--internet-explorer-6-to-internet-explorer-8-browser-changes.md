---
description: Nella tabella seguente vengono descritte le modifiche apportate tra Microsoft Internet Explorer 6 e Windows Internet Explorer 8.
ms.assetid: 5A7DDFC4-69A4-4B5A-9C0A-6172E2142494
title: Modifiche del browser IE 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7abf978d2211a03b59a78847a66efc21f3213c41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882001"
---
# <a name="appendix-1-internet-explorer-6-to-internet-explorer-8-browser-changes"></a>Appendice 1: modifiche del browser da Internet Explorer 6 a Internet Explorer 8

Nella tabella seguente vengono descritte le modifiche apportate tra Microsoft Internet Explorer 6 e Windows Internet Explorer 8.



Modifiche di progettazione da Internet Explorer 6 a Internet Explorer 7

Modifiche di progettazione da Internet Explorer 7 a Internet Explorer 8

$ {ROWSPAN2} $Internet Esplora risorse $ {REMOVE} $  

Verificare la presenza di codice che in modo non corretto in Internet Explorer 6, Windows Internet Explorer 7 o Internet Explorer 8 venga [utilizzato per lo sniffing di stringhe dell'agente utente, i vettori di versioni o i commenti condizionali](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85)).

-   Quando una stringa agente utente lungo rileva un server che accetta solo stringhe UA più brevi, gli utenti visualizzano [una pagina di errore](https://www.enhanceie.com/ua.aspx).

<!-- -->

-   La visualizzazione compatibilità di Internet Explorer 8, attivata per impostazione predefinita per i siti Intranet, invia una stringa agente utente di Internet Explorer 7. Per distinguere tra Internet Explorer 7 e visualizzazione compatibilità, cercare il nuovo [token Trident](/archive/blogs/ie/).

Aggiornamenti per la conformità agli standard di $ {ROWSPAN3} $

-   Si applica alle [modalità documento specificate](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)).
-   La [modalità di visualizzazione compatibilità di Internet Explorer 8](/archive/blogs/ie/), che è attiva per impostazione predefinita per i siti Intranet, in genere [Ripristina gli aggiornamenti degli standard da Internet Explorer 7 a Internet Explorer 8](/archive/blogs/ie/site-compatibility-and-ie8).
-   Usare l'intestazione HTTP [EmulateIE7 X-UA-Compatible](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx) o **meta** per abilitare la visualizzazione della compatibilità nei siti Web o in pagine Web specifiche.

$ {REMOVE} $  

Eccezione della modalità non standard: non è necessario apportare modifiche di conformità agli standard per le pagine Web che specificano il DOCTYPE della modalità non standard, impostando l'opzione DOCTYPE "standards-compliance" su "off".

Si applicano alla modalità "Strict" o degli standard di Internet Explorer 7 e superiori:

-   I [Prolog XML](/previous-versions/windows/internet-explorer/ie-developer/) nella prima riga del codice sorgente non causano più la mancata riuscita delle dichiarazioni DOCTYPE.
-   Il contenuto di overflow del [modello box](/previous-versions/windows/internet-explorer/ie-developer/) interseca il riquadro e non aumenta più automaticamente il div della casella per adattarlo al contenuto.
-   [Alcuni filtri CSS](/previous-versions/windows/internet-explorer/ie-developer/) (ad esempio, \* HTML, carattere di \_ sottolineatura e/ \* \* /commento) non sono supportati.
-   Viene creata un'istanza [solo dell'elemento oggetto più esterno negli oggetti annidati](/previous-versions/windows/internet-explorer/ie-developer/) .
-   Le [applicazioni che si basano sull'elemento SELECT](/previous-versions/windows/internet-explorer/ie-developer/) per ottenere un HWND da usare con le API Microsoft Win32 potrebbero interrompersi perché l' [elemento SELECT](/archive/blogs/ie/) è ora un controllo senza finestra.
-   Il [formato CDF (Channel Definition Format)](/previous-versions/aa740486(v=msdn.10)) non è supportato, a favore dei feed RSS.
-   [XBM](/previous-versions/aa740486(v=msdn.10)), un formato di imaging progettato per sistemi basati su X, non è supportato.
-   I [tag di base](/previous-versions/aa740486(v=msdn.10)) all'esterno del documento Head non sono consentiti.

Si applicano alla modalità degli standard di Internet Explorer 8 e superiori:

-   [Gli elementi P senza chiusura](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx) vengono chiusi automaticamente quando sono seguiti da elementi [**Table**](https://msdn.microsoft.com/library/ms535901(v=VS.85).aspx), [**form**](https://msdn.microsoft.com/library/ms535249(v=VS.85).aspx), [**noframes**](https://msdn.microsoft.com/library/ms535857(v=VS.85).aspx)o [**noscript**](https://msdn.microsoft.com/library/ms535858(v=VS.85).aspx) .
-   Il formato [HTML](/archive/blogs/ie/site-compatibility-and-ie8) non valido non è supportato, a favore del markup valido valido.
-   La sintassi dell' [attributo "NomeClasse"](/archive/blogs/ie/site-compatibility-and-ie8) non è supportata, a favore della sintassi "class".
-   [La raccolta Attributes](/archive/blogs/ie/site-compatibility-and-ie8) non contiene tutti i possibili attributi riconosciuti da Windows Internet Explorer.
-   L'ordinamento degli attributi [è stato modificato](/archive/blogs/ie/site-compatibility-and-ie8), influisce sulla raccolta di attributi, innerHTML e outerHTML.
-   [GetElementById](/archive/blogs/ie/site-compatibility-and-ie8) distingue tra maiuscole e minuscole e non cerca gli attributi del nome.
-   I [selettori di prefisso CSS generici](/archive/blogs/ie/site-compatibility-and-ie8) (ovvero la \\ sintassi v: \* ) non sono supportati, a favore dei nomi di tag espliciti.
-   Le [espressioni CSS](/archive/blogs/ie/site-compatibility-and-ie8) non sono supportate, a favore del supporto CSS migliorato o della logica DHTML.
-   Il codice destinato ai metodi oggetto JSON personalizzati potrebbe essere in conflitto con il [nuovo oggetto JSON nativo](/archive/blogs/ie/site-compatibility-and-ie8) in Internet Explorer 8.
-   [Annulla le proprietà iniziali](/archive/blogs/ie/site-compatibility-and-ie8) nell'oggetto currentStyle per restituire il valore iniziale.
-   [I valori delle proprietà non specificate](/archive/blogs/ie/site-compatibility-and-ie8) nell'oggetto di tipo oggetto currentStyle restituiscono una stringa vuota. ad esempio, vedere il post di Blog relativo al [menu ASP.NET e al rendering di IE8 per il rendering bianco](/archive/blogs/giorgio/) .

<!-- -->

-   Per i siti e le applicazioni in cui l'accessibilità costituisce un problema, aggiornare la [sintassi aria per tutte le modalità di rendering di Internet Explorer](/archive/blogs/ie/).
-   Controllare l' [elenco completo di aggiornamenti CSS da Internet Explorer 6 a Internet Explorer 8](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx).

Miglioramenti della sicurezza

-   Applicare indipendentemente dalla modalità documento.
-   È possibile disattivare le funzionalità di sicurezza utilizzando [criteri di gruppo](https://www.microsoft.com/p/group-policy/9wzdncrfjtm4?activetab=pivot:overviewtab).

<!-- -->

-   Il bypass [Window. opener](/previous-versions/aa740486(v=msdn.10)) alla finestra. la richiesta di chiusura non è consentita.
-   La [protezione della memorizzazione degli oggetti nella cache](/previous-versions/windows/internet-explorer/ie-developer/) è abilitata per impostazione predefinita, che blocca l'accesso ai riferimenti di oggetti quando gli utenti accedono a un nuovo dominio (si applica a Internet Explorer 6 e versioni successive in Windows XP con Service Pack 2 (SP2) e versioni successive).
-   I [gli scriptlet DHTML](/previous-versions/windows/internet-explorer/ie-developer/) sono disabilitati per impostazione predefinita.
-   [Gli script che scrivono sulla barra di stato](/previous-versions/windows/internet-explorer/ie-developer/) vengono bloccati.
-   La [creazione di URL potrebbe non riuscire](/previous-versions/windows/internet-explorer/ie-developer/) se gli URL non soddisfano le linee guida RFC.
-   [Pagine HTTPS visualizzano una pagina di errore](/previous-versions/windows/internet-explorer/ie-developer/) se il sito è configurato solo per SSLv2 o se il certificato di sicurezza del sito è obsoleto o non valido, contiene errori o ha crittografie deboli.
-   Sono supportati solo [nomi di dominio internazionali con codifica "punycode"](/previous-versions/windows/internet-explorer/ie-developer/) . Sono bloccati altri formati, ad esempio ANSI e UTF-8.
-   Gli [URL di script tra domini](/previous-versions/windows/internet-explorer/ie-developer/), la navigazione reindirizzata negli oggetti DOM e le navigazioni con frame sono bloccati.
-   Le [finestre di dialogo modali o non modali](/previous-versions/aa740486(v=msdn.10)) create da script potrebbero sembrare [leggermente più grandi](/archive/blogs/ie/).
-   I [protocolli non sicuri](/previous-versions/aa740486(v=msdn.10)) visualizzano source, Gopher (a livello di WinInet) e Telnet non funzionano.

<!-- -->

-   Il [filtro XSS](/archive/blogs/ie/) è attivo per impostazione predefinita, che blocca i modelli di script che più spesso assomigliano ad attacchi XSS di tipo 1, a meno che non vengano disabilitati tramite un'intestazione HTTP X-XSS-Protection.
-   Gli hacker di comunicazione tra più domini, ad esempio gli [script src](/archive/blogs/jscript/) , non sono supportati, a favore delle funzionalità più sicure di [XDM e XDR Ajax](/archive/blogs/ie/).
-   I siti abilitati per AJAX che [manipolano manualmente l'hash dell'URL](/previous-versions//cc891506(v=vs.85)) potrebbero essere interrotti dalla nuova proprietà di navigazione Window. location. hash.
-   Le [nuove funzionalità AJAX](https://msdn.microsoft.com/library/Gg598940(v=VS.85).aspx) come [xdm](/archive/blogs/ie/) hanno [**proprietà native**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc288548(v=vs.85)) che potrebbero essere in conflitto con le proprietà personalizzate esistenti.
-   Il [controllo di caricamento file](/archive/blogs/ie/) invia al server solo il percorso del file, non il percorso completo.
-   L'esecuzione del codice HTML o dello script fornito con un [ \* tipo MIME "image/"](/archive/blogs/ie/) è bloccata.
-   Se si [Sposta un frame di primo livello](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565638(v=vs.85)) in un sito in un contesto di sicurezza diverso, viene aperta una nuova finestra o una nuova scheda anziché spostarsi all'interno del frame esistente.
-   [Lo script con codifica UTF-7](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565635(v=vs.85)) è forzato nella codifica Windows-1252, che potrebbe causare il rendering del testo normale.
-   Le [pagine "modalità mista" http/https](/archive/blogs/askie/mixed-content-and-internet-explorer-8-0) visualizzano una finestra di dialogo che consente di visualizzare automaticamente solo gli elementi protetti (rispetto al precedente valore predefinito non protetto). È possibile che gli utenti [scelgano erroneamente di bloccare gli elementi http, ad](/archive/blogs/askie/mixed-content-and-internet-explorer-8-0)esempio le immagini chiave.
-   [DEP/NX è attivo per impostazione predefinita](https://www.microsoft.com/windows/internet-explorer/readiness/developers-existing.aspx#depnx), che blocca determinati componenti aggiuntivi (ovvero, controlli ActiveX e oggetti com) compilati utilizzando versioni precedenti di ATL dall'esecuzione del codice contrassegnato come "non eseguibile" in memoria.
-   Il [contenuto restituito da un proxy Web](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565641(v=vs.85)) viene bloccato se non viene stabilito un tunnel SSL in risposta a una richiesta di connessione al server originale.

Modifiche dell'architettura

-   Applicare indipendentemente dalla modalità di compatibilità o documento.

<!-- -->

-   La [modalità protetta](/previous-versions/windows/internet-explorer/ie-developer/) è abilitata per impostazione predefinita per [le zone Internet, Intranet e siti con restrizioni](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537187(v=vs.85)). Questa modalità consente di [bloccare le estensioni del browser che potrebbero](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565645(v=vs.85)) comportare un rischio di sicurezza dall'esecuzione e dalle applicazioni con [privilegi inferiori per l'accesso a processi con privilegi più elevati](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565646(v=vs.85)), come il menu Start, il pannello di controllo e il registro di sistema di Microsoft Windows (si applica a Internet Explorer 7 e versioni successive in Windows Vista e versioni successive).

<!-- -->

-   [Aggiornamento in modalità protetta](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565648(v=vs.85)): per impostazione predefinita viene eseguito il livello di integrità medio (anziché basso) per la Intranet.
-   [Internet Explorer](https://www.microsoft.com/windows/internet-explorer/readiness/developers-existing.aspx#lcie) a regime di controllo libero potrebbe bloccare i componenti aggiuntivi (ovvero, controlli ActiveX e oggetti com) che eseguono una delle operazioni seguenti:
    -   Usare le tecniche di gerarchia di Windows per individuare le finestre cornice e tabulazione dell'interfaccia utente (che ora vengono eseguite in processi distinti a livelli di integrità diversi).
    -   Creare una sottoclasse del frame dell'interfaccia utente, ora a livello di integrità medio, da un processo di tabulazione con basso livello di integrità.
    -   Usare tecniche di messaggistica non supportate tra frame e schede dell'interfaccia utente.



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione della compatibilità delle applicazioni durante la migrazione a Internet Explorer 8](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 
