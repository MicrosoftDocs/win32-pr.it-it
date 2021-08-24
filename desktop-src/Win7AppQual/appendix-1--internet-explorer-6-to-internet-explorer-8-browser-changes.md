---
description: La tabella seguente descrive le modifiche tra Microsoft Internet Explorer 6 e Windows Internet Explorer 8.
ms.assetid: 5A7DDFC4-69A4-4B5A-9C0A-6172E2142494
title: Modifiche del browser IE 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c775448d8eca55097b0121592c28ece0b2c347f4492e7a48b2d51d9ab688fa89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680291"
---
# <a name="appendix-1-internet-explorer-6-to-internet-explorer-8-browser-changes"></a>Appendice 1: Internet Explorer da 6 a Internet Explorer 8 modifiche del browser

La tabella seguente descrive le modifiche tra Microsoft Internet Explorer 6 e Windows Internet Explorer 8.



Modifiche di progettazione da Internet Explorer 6 a Internet Explorer 7

Modifiche di progettazione da Internet Explorer 7 a Internet Explorer 8

${ROWSPAN2}$Internet Explorer versioning${REMOVE}$  

Verificare la presenza di codice che non sia errato nei casi speciali relativi Internet Explorer 6, Windows Internet Explorer 7 o Internet Explorer 8 tramite analisi delle stringhe agente utente, vettori di versioni o commenti [condizionali](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85)).

-   Quando una stringa dell'agente utente (UA) lunga rileva un server che accetta solo stringhe UA più brevi, viene visualizzata una [pagina di errore](https://www.enhanceie.com/ua.aspx).

<!-- -->

-   Il Visualizzazione Compatibilità in Internet Explorer 8, che è attivato per impostazione predefinita per i siti Intranet, invia una stringa agente utente Internet Explorer 7. Per distinguere tra Internet Explorer 7 e Visualizzazione Compatibilità, cercare il nuovo [token Trident](/archive/blogs/ie/).

${ROWSPAN3}$ Aggiornamenti della conformità agli standard

-   Si applica alle [modalità documento specificate.](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85))
-   [Internet Explorer 8 Visualizzazione Compatibilità,](/archive/blogs/ie/)che è attivata per impostazione predefinita per i siti Intranet, in genere ripristina gli aggiornamenti degli [standard da Internet Explorer 7](/archive/blogs/ie/site-compatibility-and-ie8)a Internet Explorer 8 .
-   Usare l'intestazione HTTP compatibile con [X-UA EmulateIE7](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx) o l'elemento **meta** per abilitare Visualizzazione Compatibilità in siti Web o pagine Web specifiche.

${REMOVE}$  

Eccezione della modalità Quirks: non è necessario apportare modifiche di conformità agli standard per le pagine Web che specificano la modalità quirks DOCTYPE (impostando l'opzione DOCTYPE "standards-compliance" su "off").

Si applicano alla modalità "Strict" o degli standard di Internet Explorer 7 e superiori:

-   [I proloscamenti XML](/previous-versions/windows/internet-explorer/ie-developer/) nella prima riga del codice sorgente non causano più errori nelle dichiarazioni DOCTYPE.
-   [Box model](/previous-versions/windows/internet-explorer/ie-developer/) overflow content intersects box and no longer automatically -grows the box div to fit the content.
-   [Alcuni filtri CSS](/previous-versions/windows/internet-explorer/ie-developer/) (ad \* esempio, HTML, carattere di sottolineatura e \_ \* \* ///comment) non sono supportati.
-   [Viene creata un'istanza solo dell'elemento OBJECT](/previous-versions/windows/internet-explorer/ie-developer/) più esterno negli oggetti annidati.
-   [Le applicazioni che si](/previous-versions/windows/internet-explorer/ie-developer/) basano sull'elemento SELECT per ottenere un oggetto HWND da usare con le API Microsoft Win32 potrebbero interrompersi perché l'elemento [SELECT](/archive/blogs/ie/) è ora un controllo senza finestra.
-   [Il formato CDF (Channel Definition Format)](/previous-versions/aa740486(v=msdn.10)) non è supportato, a favore dei feed RSS.
-   [XBM,](/previous-versions/aa740486(v=msdn.10))un formato di creazione dell'immagine progettato per sistemi basati su X, non è supportato.
-   [I tag BASE](/previous-versions/aa740486(v=msdn.10)) all'esterno del documento HEAD non sono consentiti.

Si applicano alla modalità degli standard di Internet Explorer 8 e superiori:

-   [Gli elementi P non](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx) chiusi vengono chiusi automaticamente quando sono seguiti dagli elementi [**TABLE,**](https://msdn.microsoft.com/library/ms535901(v=VS.85).aspx) [**FORM,**](https://msdn.microsoft.com/library/ms535249(v=VS.85).aspx) [**NOFRAMES**](https://msdn.microsoft.com/library/ms535857(v=VS.85).aspx) [**o NOSCRIPT.**](https://msdn.microsoft.com/library/ms535858(v=VS.85).aspx)
-   [Il formato HTML non](/archive/blogs/ie/site-compatibility-and-ie8) valido non è supportato, a favore di markup valido ben formato.
-   La [sintassi dell'attributo "className"](/archive/blogs/ie/site-compatibility-and-ie8) non è supportata, a favore della sintassi "class".
-   [La raccolta di](/archive/blogs/ie/site-compatibility-and-ie8) attributi non contiene tutti i possibili attributi che Windows Internet Explorer riconosce.
-   [L'ordinamento degli attributi è stato](/archive/blogs/ie/site-compatibility-and-ie8)modificato, con effetti sulla raccolta di attributi, innerHTML e outerHTML.
-   [GetElementById fa distinzione](/archive/blogs/ie/site-compatibility-and-ie8) tra maiuscole e minuscole e non esegue la ricerca degli attributi del nome.
-   [I selettori di prefisso CSS generici](/archive/blogs/ie/site-compatibility-and-ie8) (ovvero la sintassi v : ) non sono \\ \* supportati, a favore dei nomi di tag espliciti.
-   [Le espressioni CSS](/archive/blogs/ie/site-compatibility-and-ie8) non sono supportate, a favore del supporto CSS migliorato o della logica DHTML.
-   Il codice destinato ai metodi dell'oggetto JSON personalizzato potrebbe essere in conflitto con il nuovo oggetto [JSON](/archive/blogs/ie/site-compatibility-and-ie8) nativo in Internet Explorer 8.
-   [Le proprietà iniziali non impostate](/archive/blogs/ie/site-compatibility-and-ie8) sull'oggetto currentStyle restituiscono il valore iniziale.
-   [I valori delle](/archive/blogs/ie/site-compatibility-and-ie8) proprietà non specificati nell'oggetto stile dell'oggetto currentStyle restituiscono una stringa vuota(ad esempio, vedere il post di blog relativo al problema di rendering bianco di ASP.NET Menu e [IE8).](/archive/blogs/giorgio/)

<!-- -->

-   Per i siti e le applicazioni in cui l'accessibilità rappresenta un problema, aggiornare la sintassi ARIA in tutte le [Internet Explorer di rendering.](/archive/blogs/ie/)
-   Controllare [l'elenco completo degli aggiornamenti CSS da Internet Explorer 6 a Internet Explorer 8](https://msdn.microsoft.com/library/Cc843977(v=VS.85).aspx).

Miglioramenti della sicurezza

-   Applicare indipendentemente dalla modalità documento.
-   È possibile disattivare le funzionalità di sicurezza [usando Criteri di gruppo](https://www.microsoft.com/p/group-policy/9wzdncrfjtm4?activetab=pivot:overviewtab).

<!-- -->

-   Il [bypass di window.opener](/previous-versions/aa740486(v=msdn.10)) al prompt window.close non è consentito.
-   [](/previous-versions/windows/internet-explorer/ie-developer/) La protezione della memorizzazione nella cache degli oggetti è abilitata per impostazione predefinita, che blocca l'accesso ai riferimenti degli oggetti quando gli utenti passano a un nuovo dominio (si applica a Internet Explorer 6 e versioni successive in Windows XP con Service Pack 2 (SP2) e versioni successive).
-   [Gli scriptlet DHTML sono](/previous-versions/windows/internet-explorer/ie-developer/) disabilitati per impostazione predefinita.
-   [Gli script che scrivono nella barra di stato](/previous-versions/windows/internet-explorer/ie-developer/) sono bloccati.
-   [La creazione di URL potrebbe non](/previous-versions/windows/internet-explorer/ie-developer/) riuscire se gli URL non soddisfano le linee guida RFC.
-   [Le pagine HTTPS](/previous-versions/windows/internet-explorer/ie-developer/) visualizzano una pagina di errore se il sito è configurato solo per SSLv2 o se il certificato di sicurezza del sito è obsoleto o non valido, contiene errori o ha una crittografia debole.
-   Sono supportati solo i nomi di dominio [internazionalizzati con codifica "Punycode".](/previous-versions/windows/internet-explorer/ie-developer/) Altri formati, ad esempio ANSI e UTF-8, sono bloccati.
-   [Gli URL degli script tra domini,](/previous-versions/windows/internet-explorer/ie-developer/)la navigazione reindirizzata negli oggetti DOM e gli spostamenti tra frame sono bloccati.
-   [Le finestre di dialogo modali o non modali](/previous-versions/aa740486(v=msdn.10)) create dallo script potrebbero sembrare [leggermente più grandi.](/archive/blogs/ie/)
-   [I protocolli non](/previous-versions/aa740486(v=msdn.10)) sicuri view-source, Gopher (a livello WinINET) e Telnet non funzionano.

<!-- -->

-   Il filtro [XSS](/archive/blogs/ie/) è attivata per impostazione predefinita, che blocca i modelli di script più simili agli attacchi XSS di tipo 1, a meno che non vengano disabilitati tramite un'intestazione HTTP X-XSS-Protection.
-   Gli attacchi di comunicazione tra domini e documenti come [SCRIPT SRC](/archive/blogs/jscript/) non sono supportati, a favore di funzionalità [AJAX XDM e XDR più sicure.](/archive/blogs/ie/)
-   I siti abilitati per AJAX [che modificano manualmente l'hash dell'URL](/previous-versions//cc891506(v=vs.85)) potrebbero essere interrotti dalla nuova proprietà di navigazione window.location.hash.
-   [Le nuove funzionalità AJAX](https://msdn.microsoft.com/library/Gg598940(v=VS.85).aspx) come [XDM](/archive/blogs/ie/) hanno [**proprietà native**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc288548(v=vs.85)) che potrebbero essere in conflitto con le proprietà personalizzate esistenti.
-   [Il controllo caricamento](/archive/blogs/ie/) file invia al server solo il percorso del file, non il percorso completo.
-   L'esecuzione di codice o script HTML recapitato con [un tipo MIME "image/ \* "](/archive/blogs/ie/) è bloccata.
-   [L'esplorazione di un frame di livello superiore](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565638(v=vs.85)) in un sito in un contesto di sicurezza diverso apre una nuova finestra o scheda invece di spostarsi all'interno del frame esistente.
-   [Lo script con codifica UTF-7](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565635(v=vs.85)) viene forzato Windows codifica 1252, che potrebbe causare il rendering del testo normale.
-   [Le pagine HTTP/HTTPS in "modalità mista"](/archive/blogs/askie/mixed-content-and-internet-explorer-8-0) visualizzano una finestra di dialogo che per impostazione predefinita visualizza solo gli elementi protetti (rispetto all'impostazione predefinita precedente non protetta). Gli utenti potrebbero scegliere erroneamente [di bloccare gli elementi HTTP,](/archive/blogs/askie/mixed-content-and-internet-explorer-8-0)ad esempio le immagini chiave.
-   [DEP/NX](https://www.microsoft.com/windows/internet-explorer/readiness/developers-existing.aspx#depnx)è on per impostazione predefinita, che blocca l'esecuzione di codice contrassegnato come "non eseguibile" in memoria da parte di determinati componenti aggiuntivi, ovvero controlli ActiveX e oggetti COM, compilati usando versioni precedenti di ATL.
-   [Il contenuto restituito da un proxy Web](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565641(v=vs.85)) viene bloccato se non viene stabilito un tunnel SSL in risposta a una richiesta CONNECT al server originale.

Modifiche dell'architettura

-   Applicare indipendentemente dal documento o dalla modalità di compatibilità.

<!-- -->

-   [La modalità protetta](/previous-versions/windows/internet-explorer/ie-developer/) è abilitata per impostazione [predefinita per le aree Internet, Intranet e Siti con restrizioni](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537187(v=vs.85)). Questa modalità impedisce alle estensioni del [browser](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565645(v=vs.85)) [](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565646(v=vs.85))che potrebbero comportare un rischio per la sicurezza dall'esecuzione di applicazioni con privilegi più bassi dall'accesso a processi con privilegi più elevati, ad esempio menu Start, Pannello di controllo e il Registro di sistema di Microsoft Windows (si applica a Internet Explorer 7 e versioni successive in Windows Vista e versioni successive).

<!-- -->

-   [Aggiornamento in modalità protetta:](/previous-versions/windows/internet-explorer/ie-developer/compatibility/dd565648(v=vs.85))la rete Intranet viene eseguita con un livello di integrità medio (anziché basso) per impostazione predefinita.
-   [I componenti Internet Explorer](https://www.microsoft.com/windows/internet-explorer/readiness/developers-existing.aspx#lcie) a coppia libera potrebbero bloccare i componenti aggiuntivi,ovvero ActiveX controlli e oggetti COM, che esercitino una delle operazioni seguenti:
    -   Usare tecniche di gerarchia di Windows per individuare le finestre cornice e scheda dell'interfaccia utente (che ora vengono eseguite in processi separati a livelli di integrità diversi).
    -   Creare una sottoclasse del frame dell'interfaccia utente (ora a livello di integrità media) da un processo scheda a bassa integrità.
    -   Usare tecniche di messaggistica non supportate tra schede e frame dell'interfaccia utente.



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione della compatibilità delle applicazioni durante la migrazione a Internet Explorer 8](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 
