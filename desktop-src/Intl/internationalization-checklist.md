---
description: In questo argomento vengono illustrate le azioni da eseguire per creare codice che supporta più mercati. Prendere in considerazione queste istruzioni come guida durante la progettazione del codice e come metriche quando si valutano le compilazioni.
ms.assetid: cf2ac58e-7fc3-4635-8b82-586a0732b2a3
title: Elenco di controllo per l'internazionalizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4650f7bd1111f35c911d6efe12bfbec4b537f2cdabdc50160965b5e602708b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147514"
---
# <a name="internationalization-checklist"></a>Elenco di controllo per l'internazionalizzazione

In questo argomento vengono illustrate le azioni da eseguire per creare codice che supporta più mercati. Prendere in considerazione queste istruzioni come guida durante la progettazione del codice e come metriche quando si valutano le compilazioni.

-   Creare fin dall'inizio specifiche del programma che contino per considerazioni internazionali.
    -   Progettare icone e bitmap in modo che siano significative e non offensive nei mercati di destinazione e non contengano testo.
    -   Progettare menu e finestre di dialogo per lasciare spazio all'espansione del testo. Ad esempio, le stringhe in inglese spesso si espandono del 40% quando vengono tradotte in tedesco o olandese.
    -   Non usare riferimenti slang o culturalmente specifici negli elementi o nei messaggi dell'interfaccia utente.
    -   Creare combinazioni di tasti di scelta rapida accessibili nelle tastiere internazionali. Ad esempio, evitare di usare i tasti di punteggiatura come tasti di scelta rapida perché non vengono sempre trovati su tastiere internazionali o prodotti facilmente dall'utente. Per esempi di layout di tastiera, vedere Windows [layout di tastiera](https://msdn.microsoft.com/goglobal/bb964651.aspx).
    -   Prendere in considerazione le leggi locali che interessano le progettazioni di funzionalità, ad esempio i requisiti che le entità governative acquistano software che supporta più lingue ufficiali.
    -   Sviluppare contratti di terze parti che supportano gli standard e le decisioni di progettazione internazionali dell'interfaccia utente dell'organizzazione.
    -   Usare una terminologia coerente nelle stringhe dell'interfaccia utente che devono essere convertite.

<!-- -->

-   Creare codice indipendente dalle impostazioni locali.
    -   Non concatenare stringhe per formare frasi.
    -   Non usare una determinata variabile di stringa in più contesti, ad esempio il riutilizzo di un frammento di frase in messaggi e richieste diversi, perché tali stringhe potrebbero non essere facili da tradurre.
    -   Documentare le stringhe usando i commenti per fornire il contesto per i traduttori e contrassegnare chiaramente stringhe o caratteri che non devono essere localizzati.
    -   Non usare costanti carattere hard-coded, costanti numeriche, posizioni dello schermo, nomi di file o nomi di percorso che presupsumeno una lingua specifica.
    -   Rendere i buffer sufficientemente grandi da contenere stringhe tradotte.
    -   Consente l'input di dati con formati che variano in base alle impostazioni locali, ad esempio date, ore e valute.
    -   Usare le dimensioni della carta, le dimensioni della busta e altre impostazioni predefinite appropriate per le impostazioni locali specificate.
    -   Assicurarsi che ogni edizione linguistica sia in grado di leggere i documenti creati dalle altre edizioni.
    -   Fornire il supporto per hardware specifico delle impostazioni locali, se necessario.
    -   Configurare funzionalità che non si applicano ai mercati internazionali come opzioni di implementazione che possono essere disabilitate facilmente.

<!-- -->

-   Creare codice che sfrutta le funzionalità internazionali offerte da Microsoft Windows.
    -   Usare le informazioni internazionali trasportate dal sistema (Supporto linguistico nazionale).
    -   Usare le funzioni di sistema per l'ordinamento, la conversione di maiuscole e minuscole e il mapping di stringhe.
    -   Usare funzioni di layout di testo generiche.
    -   Rispondere alle modifiche alle impostazioni internazionali in Pannello di controllo.
    -   Gestire il messaggio WM \_ INPUTLANGCHANGEREQUEST.
    -   Supporto di editor di metodi di input, testo verticale e regole di interruzione di riga nelle edizioni dell'Asia orientale.

<!-- -->

-   Compilare tutte le edizioni internazionali del programma da un unico set di file di origine.
    -   Ridurre al minimo o eliminare i meccanismi che richiedono la ricompilazione del codice per diverse edizioni del linguaggio.
    -   Archiviare elementi localizzabili, ad esempio stringhe e icone, Windows file di risorse.
    -   Archiviare i documenti in tutte le edizioni linguistiche usando lo stesso formato di file.

<!-- -->

-   Supporta set di caratteri diversi, non solo la tabella codici Latin 1, numero 1252.
    -   Il programma supporta ambienti di rete in cui i computer eseguono sistemi operativi con diverse code pages predefinite.
    -   Usare GetCPInfoEx per recuperare gli intervalli di byte di lead per le code pages dell'Asia orientale.
    -   Analizzare i caratteri a byte doppio nelle applicazioni in lingue dell'Asia orientale, a meno che il codice non sia basato su Unicode.
    -   Supporta Unicode o la conversione tra Unicode e la tabella codici locale.
    -   Non presupporre che tutti i caratteri siano a 8 bit o a 16 bit.
    -   Usare tipi di dati generici e prototipi di funzioni generiche.
    -   Usare la proprietà charset del tipo di carattere, che chiama EnumFontFamiliesEx e la funzione della finestra di dialogo comune ChooseFont.
    -   Visualizzare e stampare il testo usando i tipi di carattere appropriati per le impostazioni locali.

<!-- -->

-   Testare le funzionalità internazionali del programma.
    -   Il testo tradotto deve soddisfare gli standard dei parlanti nativi.
    -   Le finestre di dialogo devono essere ridimensionate correttamente e il testo deve essere sillabato in modo appropriato quando vengono visualizzate lingue diverse.
    -   Le finestre di dialogo, le barre di stato, le barre degli strumenti e i menu devono adattarsi allo schermo e leggere in modo leggibile quando la visualizzazione è impostata su risoluzioni diverse, per tutte le lingue tradotte.
    -   I tasti di scelta rapida di menu e finestre di dialogo devono essere univoci.
    -   Gli utenti devono essere in grado di digitare caratteri da script non europei in documenti, finestre di dialogo e nomi di file.
    -   Gli utenti devono essere in grado di tagliare, incollare, salvare e stampare correttamente caratteri da script non europei.
    -   L'ordinamento e la conversione di maiuscole e minuscole devono essere accurati per impostazioni locali diverse.
    -   L'applicazione deve funzionare correttamente nelle edizioni localizzate di Windows.

 

 



