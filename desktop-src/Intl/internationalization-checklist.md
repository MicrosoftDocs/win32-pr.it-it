---
description: In questo argomento vengono fornite le azioni da intraprendere per creare codice che supporta più mercati. Prendere in considerazione queste istruzioni come guida durante la progettazione del codice e come metriche quando si valutano le compilazioni.
ms.assetid: cf2ac58e-7fc3-4635-8b82-586a0732b2a3
title: Elenco di controllo internazionalizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b18ef8cf88efa8d496d19c0b66208cd44abaf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878557"
---
# <a name="internationalization-checklist"></a>Elenco di controllo internazionalizzazione

In questo argomento vengono fornite le azioni da intraprendere per creare codice che supporta più mercati. Prendere in considerazione queste istruzioni come guida durante la progettazione del codice e come metriche quando si valutano le compilazioni.

-   Creare specifiche di programma che considerano le considerazioni internazionali dall'inizio.
    -   Progettare icone e bitmap per essere significative e non offensive nei mercati di destinazione e non contenere testo.
    -   Progettare menu e finestre di dialogo per lasciare spazio per l'espansione del testo. Ad esempio, le stringhe inglesi si espandono spesso del 40% quando vengono convertite in tedesco o olandese.
    -   Non usare riferimenti gergali o specifici per le impostazioni cultura negli elementi o nei messaggi dell'interfaccia utente.
    -   Crea combinazioni di tasti di scelta rapida accessibili dalle tastiere internazionali. Ad esempio, evitare di usare i tasti di punteggiatura come tasti di scelta rapida perché non sono sempre presenti nelle tastiere internazionali o facilmente prodotti dall'utente. Per esempi di layout della tastiera, vedere [layout di tastiera di Windows](https://msdn.microsoft.com/goglobal/bb964651.aspx).
    -   Prendere in considerazione le leggi locali che interessano la progettazione di funzionalità, ad esempio i requisiti che gli enti governativi acquistano software che supporta più lingue ufficiali.
    -   Sviluppare contratti di terze parti che supportano gli standard e le decisioni di progettazione dell'interfaccia utente internazionale dell'organizzazione.
    -   Usare la terminologia coerente nelle stringhe dell'interfaccia utente che devono essere convertite.

<!-- -->

-   Creare codice indipendente dalle impostazioni locali.
    -   Non concatenare le stringhe per formare frasi.
    -   Non usare una determinata variabile di tipo stringa in più di un contesto, ad esempio riutilizzando un frammento di frase in messaggi e prompt diversi, perché tali stringhe potrebbero non essere facili da tradurre.
    -   Stringhe di documenti che usano commenti per fornire il contesto per i traduttori e contrassegnare chiaramente le stringhe o i caratteri che non devono essere localizzati.
    -   Non usare le costanti carattere hardcoded, le costanti numeriche, le posizioni dello schermo, i nomi di file o i nomi di percorso che presuppongono una lingua specifica.
    -   Rendere i buffer sufficientemente grandi da mantenere le stringhe tradotte.
    -   Consente l'input dei dati con formati che variano in base alle impostazioni locali, ad esempio date, ore e valute.
    -   Utilizzare il formato della carta, le dimensioni della busta e altre impostazioni predefinite appropriate per le impostazioni locali specificate.
    -   Verificare che ogni edizione del linguaggio possa leggere i documenti creati dalle altre edizioni.
    -   Fornire il supporto per l'hardware specifico delle impostazioni locali, se necessario.
    -   Configurare le funzionalità che non si applicano ai mercati internazionali come opzioni di implementazione che possono essere disabilitate facilmente.

<!-- -->

-   Creazione di codice che sfrutta i vantaggi delle funzionalità internazionali offerte da Microsoft Windows.
    -   Usare le informazioni internazionali trasferite dal sistema (supporto linguistico nazionale).
    -   Usare le funzioni di sistema per l'ordinamento, la conversione dei case e il mapping delle stringhe.
    -   Utilizzare funzioni di layout di testo generico.
    -   Rispondere alle modifiche apportate alle impostazioni internazionali nel pannello di controllo.
    -   Gestire il \_ messaggio WM INPUTLANGCHANGEREQUEST.
    -   Supporto per editor del metodo di input, testo verticale e regole di suddivisione in righe nelle edizioni asiatiche orientali.

<!-- -->

-   Compila tutte le edizioni internazionali del programma da un set di file di origine.
    -   Ridurre o eliminare i meccanismi che richiedono la ricompilazione del codice per edizioni di lingue diverse.
    -   Archiviare gli elementi localizzabili, ad esempio stringhe e icone, nei file di risorse di Windows.
    -   Archiviare i documenti in tutte le edizioni della lingua usando lo stesso formato di file.

<!-- -->

-   Supportare set di caratteri diversi, non solo la tabella codici Latin 1, numero 1252.
    -   Il programma supporta gli ambienti di rete in cui i computer eseguono sistemi operativi con tabelle codici predefinite diverse.
    -   Usare GetCPInfoEx per recuperare gli intervalli di byte iniziali per le tabelle codici asiatiche orientali.
    -   Analizza i caratteri a byte doppio nelle applicazioni del linguaggio asiatico orientale, a meno che il codice non sia basato su Unicode.
    -   Supporta Unicode o la conversione tra Unicode e la tabella codici locale.
    -   Non presupporre che tutti i caratteri siano a 8 bit o a 16 bit.
    -   Usare i tipi di dati generici e i prototipi di funzione generici.
    -   Usare la proprietà charset del tipo di carattere, che chiama EnumFontFamiliesEx e la funzione della finestra di dialogo comune ChooseFont.
    -   Visualizzare e stampare testo utilizzando i tipi di carattere appropriati per le impostazioni locali.

<!-- -->

-   Testare le funzionalità internazionali del programma.
    -   Il testo tradotto deve soddisfare gli standard degli altoparlanti nativi.
    -   Le finestre di dialogo devono essere ridimensionate correttamente e il testo deve essere sillabato in modo appropriato, quando vengono visualizzate lingue diverse.
    -   Le finestre di dialogo, le barre di stato, le barre degli strumenti e i menu devono rientrare sullo schermo e leggere leggibile quando la visualizzazione è impostata su risoluzioni diverse, per tutte le lingue tradotte.
    -   Gli acceleratori del menu e della finestra di dialogo devono essere univoci.
    -   Gli utenti devono essere in grado di digitare caratteri da script non europei in documenti, finestre di dialogo e nomi file.
    -   Gli utenti devono essere in grado di tagliare, incollare, salvare e stampare caratteri da script non europei.
    -   L'ordinamento e la conversione maiuscole/minuscole devono essere accurate per diverse impostazioni locali.
    -   L'applicazione dovrebbe funzionare correttamente nelle edizioni localizzate di Windows.

 

 



