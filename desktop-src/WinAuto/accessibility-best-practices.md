---
title: Procedure consigliate per l'accesso facilitato
description: L'implementazione delle procedure consigliate descritte in questa sezione consente di garantire che l'applicazione sia accessibile agli utenti che usano assistive technology prodotti.
ms.assetid: ef694361-49b7-424c-a583-1eadc2519db7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f596378c55b5f99af5b24fa60a23d980407392298fe2ad656579730fbab709
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327871"
---
# <a name="accessibility-best-practices"></a>Procedure consigliate per l'accesso facilitato

L'implementazione delle procedure consigliate descritte in questa sezione consente di garantire che l'applicazione sia accessibile agli utenti che usano assistive technology prodotti. Molte di queste procedure consigliate sono incentrate su una buona progettazione dell'interfaccia utente. Ogni procedura consigliata include informazioni sull'implementazione per controlli o applicazioni. In molti casi, gran parte del lavoro per soddisfare queste procedure consigliate è già inclusa nei controlli.

In questo argomento sono contenute le sezioni seguenti.

-   [Accesso a livello di codice](#programmatic-access)
    -   [Abilitare l'accesso a livello di codice a tutti gli elementi dell'interfaccia utente e al testo](#enable-programmatic-access-to-all-ui-elements-and-text)
    -   [Inserire nomi, titoli e descrizioni in oggetti di interfaccia utente, frame e pagine](#place-names-titles-and-descriptions-on-ui-objects-frames-and-pages)
    -   [Verificare che gli eventi a livello di codice siano attivati da tutte le attività dell'interfaccia utente](#ensure-programmatic-events-are-triggered-by-all-ui-activities)
-   [Impostazioni utente](#user-settings)
    -   [Rispettare tutte le impostazioni a livello di sistema e non interferire con le funzioni di accesso facilitato](#respect-all-system-wide-settings-and-do-not-interfere-with-accessibility-functions)
-   [Progettazione dell'interfaccia utente visiva](#visual-ui-design)
    -   [Non Hard-Code colori](#do-not-hard-code-colors)
    -   [Supportare il contrasto elevato e tutti gli attributi di visualizzazione del sistema](#support-high-contrast-and-all-system-display-attributes)
    -   [Verificare che tutti gli elementi dell'interfaccia utente siano ridimensionati correttamente in base alle impostazioni DPI](#ensure-all-ui-correctly-scales-by-any-dpi-setting)
-   [Navigazione tramite tastiera](#keyboard-navigation)
    -   [Fornire l'interfaccia della tastiera per tutti gli elementi dell'interfaccia utente](#provide-keyboard-interface-for-all-ui-elements)
    -   [Mostrare lo stato attivo della tastiera](#show-the-keyboard-focus)
    -   [Supportare gli standard di esplorazione e schemi di navigazione potenti](#support-navigation-standards-and-powerful-navigation-schemes)
    -   [Non consentire alla posizione del mouse di interferire con la navigazione da tastiera](#do-not-let-mouse-location-interfere-with-keyboard-navigation)
-   [Interfaccia multimodale](#multi-modal-interface)
    -   [Fornire equivalenti selezionabili dall'utente per gli elementi non di testo](#provide-user-selectable-equivalents-for-non-text-elements)
    -   [Usare il colore, ma fornire anche alternative al colore](#use-color-but-also-provide-alternatives-to-color)
    -   [Usare le API di input standard con chiamate indipendenti dal dispositivo](#use-standard-input-apis-with-device-independent-calls)
-   [Argomenti correlati](#related-topics)

## <a name="programmatic-access"></a>Accesso a livello di codice

Le procedure consigliate in questa sezione si apprendono che assistive technology prodotti hanno un accesso a livello di codice adeguato alle informazioni e alle funzionalità dell'interfaccia utente.

### <a name="enable-programmatic-access-to-all-ui-elements-and-text"></a>Abilitare l'accesso a livello di codice a tutti gli elementi dell'interfaccia utente e al testo

Gli elementi dell'interfaccia utente dell'applicazione devono essere accessibili a livello assistive technology prodotti. Tutti gli elementi dell'interfaccia utente devono avere etichette, devono esporre tutti i valori delle proprietà e devono generare tutti gli eventi appropriati. Per i controlli Windows standard, la maggior parte di queste operazioni è già stata eseguita tramite gli oggetti proxy Automazione interfaccia utente e Microsoft Active Accessibility Microsoft. I controlli personalizzati, tuttavia, richiedono lavoro aggiuntivo per assicurarsi che siano completamente esposti in modo che i fornitori di assistive technology possano identificare e modificare gli elementi dell'interfaccia utente dell'applicazione.

Seguendo questa procedura consigliata, assistive technology fornitori di identificare e modificare gli elementi dell'interfaccia utente del prodotto.

### <a name="place-names-titles-and-descriptions-on-ui-objects-frames-and-pages"></a>Inserire nomi, titoli e descrizioni in oggetti di interfaccia utente, frame e pagine

Poiché assistive technology, in particolare le utilità per la lettura dello schermo, usano i titoli per comprendere la posizione di un frame, un oggetto o una pagina nello schema di navigazione, i titoli devono essere molto descrittivi. I titoli descrittivi di qualità consentono assistive technology prodotti di identificare e modificare gli elementi dell'interfaccia utente in controlli e applicazioni. Ad esempio, un titolo di pagina Web "Pagina Web Microsoft" è inutile se l'utente si è inserito in un'area specifica. Un titolo descrittivo è fondamentale per gli utenti non vedenti che dipendono dalle utilità per la lettura dello schermo.

Seguendo questa procedura consigliata, i assistive technology di identificare e modificare l'interfaccia utente in applicazioni e controlli di esempio.

### <a name="ensure-programmatic-events-are-triggered-by-all-ui-activities"></a>Verificare che gli eventi a livello di codice siano attivati da tutte le attività dell'interfaccia utente

L'applicazione deve generare eventi ogni volta che si verificano modifiche nello stato o nell'aspetto di un elemento dell'interfaccia utente.

Seguendo questa procedura consigliata, i assistive technology possono restare in ascolto delle modifiche nell'interfaccia utente e notificare tali modifiche all'utente.

## <a name="user-settings"></a>Impostazioni utente

La procedura consigliata in questa sezione garantisce che i controlli o le applicazioni non eseguono l'override delle impostazioni utente.

### <a name="respect-all-system-wide-settings-and-do-not-interfere-with-accessibility-functions"></a>Rispettare tutte le impostazioni a livello di sistema e non interferire con le funzioni di accesso facilitato

Gli utenti possono usare Pannello di controllo per impostare alcuni flag a livello di sistema; Altri flag possono essere impostati a livello di codice. Queste impostazioni non devono essere modificate da controlli o applicazioni. Inoltre, le applicazioni devono supportare le impostazioni di accessibilità del sistema operativo host.

Seguendo questa procedura consigliata gli utenti potranno configurare le impostazioni di accessibilità e sapere che queste non verranno modificate dalle applicazioni.

## <a name="visual-ui-design"></a>Progettazione dell'interfaccia utente visiva

Le procedure consigliate in questa sezione assicurano che i controlli o le applicazioni usino i colori e le immagini in modo efficace e possano essere usati assistive technology prodotti.

### <a name="do-not-hard-code-colors"></a>Non Hard-Code colori

È possibile che le persone daltoniche, con ipovisione o che usano uno schermo in bianco e nero non possano usare applicazioni con colori hardcoded.

Seguendo questa procedura consigliata gli utenti potranno modificare le combinazioni di colori in base alle proprie esigenze.

### <a name="support-high-contrast-and-all-system-display-attributes"></a>Supportare il contrasto elevato e tutti gli attributi di visualizzazione del sistema

Le applicazioni non devono interrompere o disabilitare le impostazioni di contrasto, le selezioni dei colori o altre impostazioni e attributi di visualizzazione a livello di sistema selezionati dall'utente. Le impostazioni a livello di sistema adottate da un utente migliorano l'accessibilità delle applicazioni, pertanto non deve essere disabilitate o ignorate dalle applicazioni. I colori devono essere usati nella loro corretta combinazione di colore di primo piano e di sfondo per fornire un contrasto appropriato. I colori non correlati non devono essere combinati e i colori non devono essere invertiti.

Molti utenti richiedono specifiche combinazioni di contrasto elevato, ad esempio testo bianco su sfondo nero. L'inversione dei colori, usando testo nero su sfondo bianco, provoca la smarginatura del colore di sfondo sul colore di primo piano, rendendo difficile la lettura per alcuni utenti.

### <a name="ensure-all-ui-correctly-scales-by-any-dpi-setting"></a>Verificare che tutti gli elementi dell'interfaccia utente siano ridimensionati correttamente in base alle impostazioni DPI

Assicurarsi che tutti gli elementi dell'interfaccia utente possano essere ridimensionati correttamente in base a qualsiasi impostazione di punti per pollice (dpi). Assicurarsi anche che gli elementi dell'interfaccia utente si adattino a uno schermo di 1024 x 768 con 120 punti per pollice (dpi).

## <a name="keyboard-navigation"></a>Navigazione tramite tastiera

Le procedure consigliate in questa sezione assicurano che tutte le funzionalità dell'applicazione siano accessibili agli utenti che si basano sulla tastiera.

### <a name="provide-keyboard-interface-for-all-ui-elements"></a>Fornire l'interfaccia della tastiera per tutti gli elementi dell'interfaccia utente

Le tabulazioni, soprattutto se pianificate con attenzione, offrono agli utenti un altro modo per spostarsi nell'interfaccia utente.

Le applicazioni devono fornire le interfacce di tastiera seguenti:

-   Tabulazioni per tutti i controlli con cui l'utente può interagire, ad esempio pulsanti, collegamenti o caselle di riepilogo.
-   Ordine di tabulazione logico.

### <a name="show-the-keyboard-focus"></a>Mostrare lo stato attivo della tastiera

Gli utenti devono sapere quale oggetto ha lo stato attivo in modo da poter prevedere l'effetto delle pressioni dei tasti. Per evidenziare lo stato attivo, usare colori, tipi di carattere o grafiche quali rettangoli o l'ingrandimento. Per evidenziare lo stato attivo a livello acustico, modificare il volume, il passo o la qualità tonale.

Per evitare confusione, le applicazioni devono nascondere tutti gli indicatori visivi dello stato attivo e disattivare le selezioni che si trovano in finestre (o riquadri) non attive.

Le applicazioni devono eseguire le operazioni seguenti con lo stato attivo:

-   Un elemento deve sempre avere lo stato attivo della tastiera.
-   Lo stato attivo della tastiera deve essere visibile e ovvio.
-   Le selezioni e/o gli elementi con stato attivo devono essere evidenziati visivamente.

### <a name="support-navigation-standards-and-powerful-navigation-schemes"></a>Supportare gli standard di esplorazione e schemi di navigazione potenti

Diversi aspetti dello spostamento tramite tastiera offrono agli utenti diversi modi per spostarsi nell'interfaccia utente.

Le applicazioni devono fornire le interfacce di tastiera seguenti:

-   Tasti di scelta rapida e tasti di scelta sottolineati per tutti i comandi, i menu e i controlli.
-   Tasti di scelta rapida per collegamenti importanti.
-   Tutte le voci di menu hanno una chiave di accesso. tutti i pulsanti hanno tasti di scelta rapida, tutti i comandi hanno un tasto di scelta rapida.

### <a name="do-not-let-mouse-location-interfere-with-keyboard-navigation"></a>Non consentire alla posizione del mouse di interferire con la navigazione da tastiera

La posizione del mouse non dovrebbe interferire con la navigazione da tastiera. Ad esempio, se il mouse è posizionato in un punto e l'utente si sposta con la tastiera, un clic del mouse non dovrebbe verificarsi a meno che non avviato dall'utente.

## <a name="multi-modal-interface"></a>Interfaccia multimodale

La procedura consigliata in questa sezione garantisce che l'interfaccia utente dell'applicazione includa alternative per gli elementi visivi.

### <a name="provide-user-selectable-equivalents-for-non-text-elements"></a>Fornire equivalenti selezionabili dall'utente per gli elementi non di testo

Per ogni elemento non di testo, fornire un equivalente selezionabile dall'utente per testo, trascrizioni o descrizioni audio, ad esempio testo alternativo, didascalie o commenti visivi.

Gli elementi non di testo coprono un'ampia gamma di elementi dell'interfaccia utente, tra cui immagini, aree mappa immagine, animazioni, applet, frame, script, pulsanti grafici, suoni, file audio e video autonomi. Gli elementi non di testo sono importanti quando contengono informazioni visive, voce o informazioni audio generali a cui l'utente deve accedere per comprendere il contenuto dell'interfaccia utente.

### <a name="use-color-but-also-provide-alternatives-to-color"></a>Usare il colore, ma fornire anche alternative al colore

Usare il colore per migliorare, evidenziare o avvalorare le informazioni visualizzate in altri modi, ma che non comunicano informazioni con i soli colori. Gli utenti daltonici o che usano uno schermo monocromatico necessitano di alternative ai colori.

### <a name="use-standard-input-apis-with-device-independent-calls"></a>Usare le API di input standard con chiamate indipendenti dal dispositivo

Le chiamate indipendenti dal dispositivo assicurano che tutti i dispositivi di input siano trattati allo stesso modo, fornendo assistive technology prodotti con le informazioni necessarie sull'interfaccia utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Panoramica dell'API di Automazione](windows-automation-api-overview.md)
</dt> </dl>

 

 




