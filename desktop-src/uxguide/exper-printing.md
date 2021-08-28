---
title: Stampa (nozioni di base sulla progettazione)
description: La stampa è l'esperienza utente su carta. È facile da ignorare, ma è una parte importante dell'esperienza utente complessiva.
ms.assetid: 26f5a8dc-27b2-4c2d-a05a-f942784c3cf9
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 125c0eab965597c3e359f323f43b8881ff50b754
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482157"
---
# <a name="printing-design-basics"></a>Stampa (nozioni di base sulla progettazione)

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

La stampa è l'esperienza utente su carta. È facile da ignorare, ma è una parte importante dell'esperienza utente complessiva.

In questo articolo la stampa *si* riferisce all'esperienza utente su carta, in cui l'output viene indirizzato alla carta anziché allo schermo. *Il formato adatto alla stampante* si riferisce alle modifiche che il programma può apportare all'output dello schermo che lo rendono più adatto per l'output su carta.

Nonostante la previsione che il calcolo possa comportare l'"ufficio senza carta", è sorprendentemente sufficiente stampare ora più che mai. Le copie cartacee dei mazzi di presentazione di Microsoft PowerPoint vengono distribuite, vengono stampati articoli individuati online ma si vuole eseguire ricerche più attentamente in un secondo momento, stampare messaggi di posta elettronica o curriculum importanti ricevuti in formato elettronico e così via. Anche se è facile ignorare la stampa durante la progettazione di un'interfaccia utente, tenere presente che la stampa è una parte importante dell'esperienza utente complessiva.

**Nota:** Le linee guida relative [ai dialoghe comuni](win-common-dlg.md) sono presentate in un articolo separato.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente giusta?

Per decidere se il programma deve supportare la stampa, considerare queste domande:

-   **Quale tipo di programma si sta progettando?** Il tipo di programma è un buon indicatore del livello appropriato di supporto per la stampa. I programmi di creazione, visualizzazione ed esplorazione di documenti e immagini necessitano di un eccellente supporto per la stampa, mentre altri tipi di programmi possono richiedere solo un supporto di stampa inferiore. Per un elenco dei tipi di programma, vedere la [sezione Modelli di](#printing-patterns) stampa di questo articolo.
-   **Il programma viene usato in scenari che traggono vantaggio dall'output cartaceo diretto?** In tal caso, è più utile aggiungere il supporto per la stampa al programma anziché richiedere agli utenti di copiare i dati in un altro programma per la stampa.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="design-your-program-to-eliminate-unnecessary-printing"></a>Progettare il programma per eliminare la stampa non necessaria

Esistono molti motivi per cui gli utenti devono stampare alcuni elementi che sono buoni, altri meno. Gli utenti devono stampare perché vogliono, non perché devono. Richiedere agli utenti di stampare può essere un segno di funzionalità mancanti. In passato, ad esempio, gli utenti dovevano stampare documenti per inserire commenti e suggerire revisioni, ma ora gli utenti possono eseguire queste attività direttamente all'interno Microsoft Word documenti. **Esaminare gli scenari del programma che comportano la stampa e, nella misura migliore possibile, assicurarsi che la necessità di stampare sia facoltativa e non il risultato di funzionalità mancanti.**

Vale anche la pena ricordare che la conservazione di risorse come la carta e l'input penna è utile a livello ambientale e consente alle organizzazioni di risparmiare denaro a lungo termine.

### <a name="understand-the-differences-between-screen-display-and-print"></a>Informazioni sulle differenze tra la visualizzazione dello schermo e la stampa

Anche se esistono molte analogie tra l'output di visualizzazione e la stampa, esistono anche molte differenze. Output di stampa:

-   **Ha un valore dpi elevato.** L'output dello schermo è in genere di 96 o 120 punti per pollice (dpi), mentre l'output della stampante è in genere a 600 dpi o superiore.
-   **Ha tipi di carattere ottimali diversi.** Anche se i tipi di carattere ben progettati funzionano bene sia per la visualizzazione che per la stampa, i tipi di carattere serif sono più leggibili a risoluzioni elevate per grandi quantità di testo rispetto ai tipi di carattere sans serif. Pertanto, grandi quantità di testo destinate principalmente alla stampa devono usare un tipo di carattere serif, mentre il testo destinato principalmente alla visualizzazione deve usare un tipo di carattere sans serif. Per altre informazioni, vedere [Tipi di](vis-fonts.md) carattere (Segoe UI).
-   **Ha proporzioni.** La visualizzazione ha [](glossary.md) in genere proporzioni basse (4:3 o 5:4), mentre la stampa usa proporzioni elevate (8,5:11 o 1:1,4142 in base alle dimensioni standard della pagina). Ciò è dovuto al [fatto che la](glossary.md) stampa in modalità verticale è più comune della modalità [orizzontale.](glossary.md)
-   **Contiene pagine.** Di conseguenza, stampare l'output:
    -   Ha dimensioni di pagina standard. Lo standard in Stati Uniti e Canada è 8,5"x11". lo standard ovunque si trovi è il documento A4.
    -   Contiene interruzioni di pagina.
    -   Ha margini di pagina.
    -   Contiene intestazioni e piè di pagina.
    -   Ha un output a lato singolo o doppio.
    -   Può avere più copie.
    -   Può essere stampato in ordine o in modo selettivo.
-   **Ha molte opzioni.** Gli utenti possono scegliere una stampante e un formato carta, opzioni della stampante (ad esempio qualità di stampa, stampa fronte/retro e graffatura), numero di copie, intervalli di pagine, regole di confronto e formato di stampa.
-   **Richiede tempo e denaro.** La stampa di un documento di grandi dimensioni o di una foto di alta qualità può richiedere molto tempo e il costo della carta e dell'input penna aumenta nel tempo. Al contrario, l'output visualizzato è istantaneo e essenzialmente gratuito.
-   **Può essere in bianco e nero.** Molte stampanti sono attualmente in bianco e nero, mentre pochi display sono monocromatici.
-   **Non è interattivo.** Gli utenti non possono scorrere pagine o controlli per visualizzare altro contenuto. Non possono fare clic su collegamenti o pulsanti o passare il puntatore del mouse sui controlli. Il contenuto interattivo non ha alcun valore quando viene stampato.
-   **La carta, l'input penna o il toner possono essere eseguiti o offline.** Di conseguenza, l'output cartaceo richiede una maggiore gestione e risoluzione degli errori.

Queste differenze possono influire sulla progettazione della stampa. La creazione di un'esperienza di stampa ottimale non richiede solo l'indirizzamento dell'output del programma alla stampante.

### <a name="wysiwyg-and-the-evolving-requirements-of-screen-display"></a>WYSIWYG e i requisiti in evoluzione dello schermo

In teoria, il principio più fondamentale per l'esperienza utente di stampa è noto come WYSIWYG ("what you see is what you get"). Questo principio suggerisce che deve esserci una forte relazione tra ciò che viene visualizzato sul display e ciò che viene stampato. Prima che WYSIWYG diventasse una pratica standard, spesso non esisteva alcuna relazione tra le versioni di visualizzazione e di stampa di un documento. Gli utenti dovevano stampare per vedere l'aspetto del documento su carta. L'uso di WYSIWYG è stato un ottimo miglioramento della produttività perché la maggior parte dei programmi al momento era progettata principalmente per la creazione e la stampa di documenti.

Attualmente, per i siti Web è comune ottimizzare per la visualizzazione e il formato descrittivo della stampante può risultare molto diverso. Inoltre, sono disponibili diversi dispositivi di calcolo (ad esempio, smartphone e assistenti digitali personali) che spesso necessitano di output ottimizzato per schermi di piccole dimensioni. Sebbene WYSIWYG sia ancora l'approccio migliore per i programmi di creazione di documenti, per altri programmi è spesso più opportuno ottimizzare per un'ampia gamma di dispositivi di destinazione. Per questi programmi, ciò che si vede su un display del PC potrebbe essere diverso da quello visualizzato su altri display del dispositivo, che potrebbe essere diverso da quello visualizzato nella pagina stampata.

### <a name="optimize-for-printing"></a>Ottimizzare per la stampa

I programmi che non utilizzano una rigorosa esperienza di stampa WYSIWYG possono comunque ottimizzare la stampa nei modi seguenti:

-   Riformattare il layout per le dimensioni della pagina di destinazione.
-   Fornire l'anteprima di stampa, preferibilmente con semplici opzioni di personalizzazione che consentono agli utenti di sperimentare direttamente nella finestra di dialogo di stampa , ad esempio trascinando i margini.
-   Se appropriato, specificare un'opzione di formato adatta alla stampante.
    -   Consolidare documenti parziali separati in un singolo documento.
    -   Rimuovere gli sfondi e altri elementi di progettazione, ad esempio gli annunci, soprattutto se non sono adatti per una stampante in bianco e nero.
    -   Rimuovere gli elementi interattivi, ad esempio i controlli di spostamento e i pulsanti di comando.
    -   Assicurarsi che tutti i dati siano visibili senza barre di scorrimento o al passaggio del mouse.

        **Versione di visualizzazione:**

        ![Screenshot del report ottimizzato per lo schermo ](images/exper-printing-image1.png)

        **Versione semplice da usare per la stampante:**

        ![Screenshot dello stesso report ottimizzato per la stampa ](images/exper-printing-image2.png)

        Nella versione di tipo stampante tutti i dati sono visibili nella pagina stampata e gli elementi interattivi vengono rimossi.

    -   Sostituire i collegamenti con l'equivalente di testo.

        **Accettabile:**

        Per altre informazioni, vedere Guida all'esperienza utente.

        **Ottimizzato per la stampa:**

        Per altre informazioni, vedere Guida all'esperienza utente ( https://msdn.microsoft.com/windowsvista/uxguide) .

-   Convertire testo chiaro su sfondo scuro in testo scuro su sfondo bianco.

### <a name="include-the-right-print-options"></a>Includere le opzioni di stampa giuste

La finestra di dialogo comune Opzioni di stampa offre le opzioni seguenti:

-   Selezionare la stampante e il formato della carta.
-   Impostare le proprietà della stampante.
-   Selezionare l'intervallo di pagine, il numero di copie e le regole di confronto.
-   Usare entrambi i lati della carta.

Il programma può richiedere opzioni aggiuntive, ad esempio opzioni per il contenuto del documento (contenuto da stampare), opzioni di formattazione (come stampare, tra cui qualità di stampa, dimensioni delle immagini, adattamento alla cornice) e opzioni di colore. Se è necessario fornire opzioni aggiuntive, eseguire questa operazione estendendo la finestra di dialogo comune Opzioni di stampa. Non creare una finestra di dialogo Stampa personalizzata.

Quando si progettano le opzioni di stampa, è consigliabile considerare l'esperienza di stampa di più documenti. È probabile che il processo di stampa successivo sia molto simile all'ultimo processo di stampa. Ottimizzare le impostazioni predefinite per le ristampe e processi di stampa simili non fanno in modo che gli utenti inizino completamente ogni volta.

### <a name="design-print-preview-for-performance-and-usability"></a>Progettare l'anteprima di stampa per prestazioni e usabilità

**Un processo di stampa non corretto spreca tempo e denaro. Per i programmi di creazione di documenti, gli utenti devono essere in grado di valutare i risultati prima di eseguire la stampa effettiva.** Un'anteprima di stampa deve consentire agli utenti di:

-   Valutare margini, interruzioni di pagina, orientamento della pagina, intestazioni e piè di pagina.
-   Esplorare tutte le pagine.
-   Stampare direttamente dall'anteprima di stampa.

Il rendering di alcuni documenti complessi, ad esempio disegni CAD di progettazione con supporto informatico, può richiedere \[ \] molto tempo. Le prestazioni dell'anteprima sono importanti perché un'anteprima di stampa può diventare piuttosto noiosa se il rendering di ogni pagina richiede un po' di tempo. **Di conseguenza, è meglio avere un'anteprima di stampa che esegue il rendering rapidamente ed è sufficientemente accurata da consentire agli utenti di valutare i risultati di stampa piuttosto che avere un'anteprima completamente accurata che esegue il rendering lentamente.**

Quando si progetta l'anteprima di stampa, considerare l'intera attività di preparazione per la stampa. Cosa stanno cercando gli utenti? Cosa cambieranno? I programmi di creazione di documenti devono offrire un'anteprima di stampa interattiva in modo che gli utenti possano modificare le impostazioni modificate di frequente, ad esempio margini e interruzioni di riga all'interno dell'anteprima.

Tuttavia, nella misura migliore possibile, il programma deve eseguire la cosa giusta per impostazione predefinita. Quando necessario, avvisare in caso di situazioni di stampa che è improbabile che l'utente intendeva. Non affidarsi alla ricerca di problemi con l'anteprima di stampa da parte degli utenti. Si supponga, ad esempio, che un foglio di calcolo abbia troppe colonne da stampare su una singola pagina in modalità verticale. Sebbene il programma possa presentare una finestra di dialogo di conferma, una soluzione migliore consiste nel stampare automaticamente in modalità orizzontale.

**Se si eservino solo cinque operazioni...**

1.  Progettare un'esperienza di stampa appropriata per il tipo di programma.
2.  Esaminare gli scenari del programma che comportano la stampa e nel migliore dei modi, rendere facoltativa la necessità di stampare.
3.  Fornire estensioni di stampa utili personalizzando la finestra di dialogo Stampa comune. Non creare una finestra di dialogo Stampa personalizzata a questo scopo.
4.  Ottimizzare le opzioni di stampa per ristampe e processi di stampa simili.
5.  Fornire una funzionalità di anteprima quando appropriato.

## <a name="printing-patterns"></a>Modelli di stampa

Il tipo di programma è l'indicatore principale dell'esperienza di stampa appropriata:




| | | <strong>Creazione avanzata di documenti</strong><br /> Usato per creare, visualizzare e stampare documenti di fascia alta. La possibilità di creare stampe di alta qualità è uno dei motivi principali per cui il programma esiste. Destinate a utenti esperti. <br /> | <strong>Obiettivi dell'utente:</strong> Controllo dettagliato dei risultati perfetto sull'output di stampa.<br /><strong>Esempio:</strong> Microsoft Word<br /><strong>Esperienza di stampa consigliata:</strong><br /><ul><li>Output ottimizzato per la stampa (WYSIWYG).</li><li>Funzionalità avanzate di formattazione dei documenti, con opzioni per stampare oggetti di grandi dimensioni.</li><li>Opzioni di stampa avanzate, incluse intestazioni e piè di pagina. Le opzioni di stampa correlate al documento vengono salvate all'interno del documento stesso.</li><li>Anteprime di stampa veloci, accurate e potenti.</li></ul> | | <strong>Creazione di documenti intermedi</strong><br /> Usato per creare e visualizzare documenti più complessi. La possibilità di creare stampe di buona qualità è importante, ma non necessariamente uno dei motivi principali per cui il programma esiste. Destinato agli utenti intermedi. <br /> | <strong>Obiettivi dell'utente:</strong> Risultati ottimali con un impegno minimo. Controllo sull'output di stampa.<br /><strong>Esempi:</strong> La maggior Microsoft Office, ad esempio Outlook e Excel.<br /><strong>Esperienza di stampa consigliata:</strong><br /><ul><li>Output ottimizzato per la stampa (WYSIWYG).</li><li>Alcune funzionalità di formattazione dei documenti, con la possibilità di stampare oggetti di grandi dimensioni senza troncamento.</li><li>Alcune opzioni di stampa personalizzate, incluse intestazioni e piè di pagina.</li><li>Anteprime di stampa accurate e facili da usare.</li></ul> | | <strong>Creazione semplice di documenti</strong><br /> Usato per creare e visualizzare documenti semplici. Destinato a tutti gli utenti. <br /> | <strong>Obiettivi dell'utente:</strong> Supporto di stampa di base con opzioni di stampa standard. Gli utenti si aspettano buoni risultati senza alcuna modifica.<br /><strong>Esempi:</strong> WordPad, Paint.<br /><strong>Esperienza di stampa consigliata:</strong><br /><ul><li>L'output può essere ottimizzato per la stampa (WYSIWYG), ma non è obbligatorio.</li><li>Alcune funzionalità di formattazione dei documenti, con la possibilità di stampare oggetti di grandi dimensioni senza troncamento.</li><li>Opzioni di stampa standard; Le opzioni di stampa personalizzate sono facoltative.</li><li>Anteprime di stampa semplici o non disponibili.</li></ul> | | <strong>Visualizzatori di documenti</strong><br /> Usato per visualizzare i documenti. Gli utenti non possono modificare il contenuto o il formato del documento. <br /> | <strong>Obiettivi dell'utente:</strong> Supporto di stampa di base con opzioni di stampa standard. Gli utenti si aspettano buoni risultati senza alcuna modifica. I problemi di stampa vengono gestiti automaticamente perché gli utenti non possono modificare il documento.<br /><strong>Esempio:</strong> Windows Internet Explorer<br /><strong>Esperienza di stampa consigliata:</strong><br /><ul><li>L'output può essere ottimizzato per la stampa (WYSIWYG), ma non è obbligatorio.</li><li>Il programma gestisce automaticamente le interruzioni di pagina, elimina le pagine vuote, gestisce oggetti di grandi dimensioni e rimuove gli sfondi e altri elementi di progettazione.</li><li>Opzioni di stampa standard; Le opzioni di stampa personalizzate sono facoltative.</li><li>Anteprime di stampa semplici o non disponibili.</li></ul> | | <strong>Utilità o applicazioni line-of-business</strong><br /> Usato per eseguire attività semplici e specifiche. Destinato a tutti gli utenti. <br /> | <strong>Obiettivi dell'utente:</strong> Possibilità di esportare i dati selezionati in modo efficiente. Gli utenti si aspettano buoni risultati senza alcuna modifica. Spesso per questi programmi, gli utenti sono piacevolmente sorprendeti nel trovare qualsiasi supporto per la stampa.<br /><strong>Esperienza di stampa consigliata:</strong><br /><ul><li>Il supporto per la stampa è facoltativo a seconda degli scenari supportati.</li><li>L'output può essere ottimizzato per la stampa (WYSIWYG), ma non è obbligatorio.</li><li>Alcune funzionalità di formattazione dei documenti. Potrebbe essere accettabile se gli oggetti di grandi dimensioni vengono troncati.</li><li>Opzioni di stampa standard.</li><li>Anteprime di stampa facoltative.</li></ul> | 




 

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Non stampare pagine vuote o pagine con solo intestazioni e piè di pagina.** Tuttavia, stampare pagine vuote se le intestazioni o i piè di pagina contengono numeri di pagina e tali numeri di pagina potrebbero fare riferimento altrove.
-   **Eseguire lo spooling completo di tutti i processi di stampa in sospeso prima di arrestare un programma.**

### <a name="formatting-pages"></a>Formattazione delle pagine

-   **Riformatta il layout del testo per adattarlo alle dimensioni della pagina di destinazione.** Non troncare mai il testo.
-   Se gli utenti non controllano il formato del documento:
    -   **Gestire automaticamente oggetti di grandi dimensioni ridimensionando, ruotando o suddividendo le pagine.** Per altre linee guida sulla stampa di oggetti di grandi dimensioni, vedere [Oggetti di grandi dimensioni.](#oversized-objects)
    -   **Ottimizzare le interruzioni di pagina per eliminare le pagine vuote e quasi vuote.**
    -   **Converte testo chiaro su sfondo scuro in testo scuro su sfondo bianco.**
    -   **Rimuovere sfondi e altri elementi di progettazione,** soprattutto se non sono adatti per una stampante in bianco e nero.
-   **Se il programma presenta documenti parziali separati, fornire un'opzione di formato di tipo stampante per consolidarli in un singolo documento per la stampa.**
-   **Rimuovere gli elementi interattivi:**
    -   Rimuovere i controlli di spostamento e i pulsanti di comando.
    -   Assicurarsi che tutti i dati siano visibili senza barre di scorrimento.
    -   Sostituire i collegamenti con il testo equivalente.

        **Accettabile:**

        Per altre informazioni, vedere Guida all'esperienza utente.

        **Ottimizzato per la stampa:**

        Per altre informazioni, vedere Guida all'esperienza utente ( https://msdn.microsoft.com/windowsvista/uxguide) .

        In questo esempio il collegamento viene sostituito con il testo equivalente tra parentesi.

    -   Sposta le informazioni utili visualizzate al passaggio del mouse su inline.

### <a name="oversized-objects"></a>Oggetti di oversized

La gestione di oggetti di grandi dimensioni, ad esempio fogli di calcolo, grafica e foto, è un problema specifico della stampa. Scegliere uno degli approcci seguenti:

-   **Ridimensionare l'oggetto per adattarlo alla pagina.** Questo approccio funziona bene se l'oggetto è solo leggermente troppo grande per la stampa, mantenere l'oggetto su una singola pagina è importante e l'oggetto è ancora leggibile quando viene ridimensionato.

    ![screenshot della foto ridimensionata a metà di una pagina ](images/exper-printing-image3.png)

    In questo esempio, l'immagine di grandi dimensioni viene ridimensionata per adattarsi alla pagina.

-   **Ruotare la pagina.** Questo approccio funziona bene quando alcune pagine vengono stampate meglio in modalità orizzontale in modalità verticale (e viceversa).

    ![Screenshot della foto orizzontale ruotata in verticale ](images/exper-printing-image4.png)

    In questo esempio l'immagine grande viene ruotata per adattarsi meglio alla pagina.

-   **Stampare l'oggetto su più pagine.** L'approccio funziona bene quando l'oggetto non può essere ridimensionato o non deve essere ridimensionato e la rotazione della pagina non è utile o non è consigliabile. Se l'oggetto ha limiti interni, ad esempio i divisori di riga e di colonna in un foglio di calcolo, interrompere le pagine in questi limiti anziché all'interno del contenuto. Ripetere anche tutti gli elementi necessari per comprendere la pagina, ad esempio legende o intestazioni di colonna. Quando si divide un oggetto in più pagine, assegnare i numeri di pagina in ordine di lettura (da sinistra a destra, dall'alto verso il basso).

    ![screenshot delle testine di colonna ripetute nella pagina successiva ](images/exper-printing-image5.png)

    In questo esempio la tabella di grandi dimensioni viene stampata su due pagine. Le intestazioni di colonna vengono mantenute da una pagina all'altra per facilitare la comprensione rapida.

-   **Tronca l'oggetto** (stampando solo la parte dell'oggetto ancora visibile dopo il troncamento). Questo approccio è la soluzione più semplice da implementare, ma probabilmente è il meno accettabile. Si noti anche che il troncamento non è mai accettabile per il testo.

    ![Screenshot della metà di una foto grande nella pagina verticale ](images/exper-printing-image6.png)

    In questo esempio l'immagine grande viene troncata.

### <a name="headers-and-footers"></a>Intestazioni e piè di pagina

-   **Specificare intestazioni e piè di pagina per programmi di creazione di documenti avanzati e intermedi.** È consigliabile specificare intestazioni e piè di pagina per altri tipi di programmi se vengono usati per documenti a più pagine.
-   **Rendere personalizzabili intestazioni e piè di pagina.** Consente agli utenti di definire le parti a sinistra, al centro e a destra.
    -   Per le intestazioni, inserire il nome del documento a sinistra per impostazione predefinita.
    -   Per i piè di pagina, inserire il copyright o l'origine del documento sul lato sinistro e il numero di pagina sul lato destro, per impostazione predefinita.
-   **Usare url e percorsi di file descrittivi.** Visualizza gli spazi come spazi, non "%20".

### <a name="print-commands"></a>Comandi di stampa

-   **Per le barre dei menu e i menu di scelta rapida, usare il comando Stampa che visualizza la finestra di dialogo comune Opzioni di stampa.** Usare i puntini di sospensione per indicare che sono necessarie informazioni aggiuntive.

    ![screenshot del menu File, comando stampa selezionato ](images/exper-printing-image7.png)

    In questo esempio il comando Stampa include i puntini di sospensione per indicare che verrà visualizzata la finestra di dialogo comune Opzioni di stampa per ottenere altre informazioni.

-   **Per le barre degli strumenti usate con una barra dei menu, usare un comando Stampa immediato.** Facendo clic sul pulsante viene stampata una singola copia del documento sulla stampante predefinita. Tali comandi della barra degli strumenti devono essere immediati. Per indicare che il comando è immediato, inserire la stampante predefinita nella descrizione comando. Gli utenti possono accedere al comando Stampa completo dalla barra dei menu.

    ![screenshot dell'icona della stampante e della relativa descrizione comando ](images/exper-printing-image8.png)

    In questo esempio il comando Stampa in una barra degli strumenti viene stampato immediatamente anziché visualizzare la finestra di dialogo comune Opzioni di stampa. L'inserimento della stampante predefinita nella descrizione comando fornisce un rinforzo testuale che indica che l'utente sta ignorando la finestra di dialogo.

-   **Per le barre degli strumenti usate senza una barra dei menu, usare un pulsante di menu suddiviso Stampa.** Facendo clic sul pulsante viene stampata una singola copia del documento sulla stampante predefinita. Facendo clic sulla parte freccia del pulsante viene visualizzato un menu con i comandi Stampa, Anteprima di stampa e Imposta pagina completi.

    ![Screenshot dell'icona della stampante sul pulsante di menu suddiviso ](images/exper-printing-image9.png)

    In questo esempio, la barra Windows Internet Explorer barra degli strumenti usa un controllo pulsante di menu suddiviso per fornire tutti i comandi di stampa.

-   **Per l'interfaccia utente dei comandi della barra multifunzione, inserire il comando Stampa nel menu dell'applicazione.**

    ![Screenshot dei comandi posizionati verticalmente a sinistra ](images/exper-printing-image10.png)

    Per le barre multifunzione, è possibile accedere al comando Stampa usando il menu dell'applicazione.

### <a name="print-options"></a>Opzioni di stampa

-   **Non creare una finestra di dialogo Opzioni di stampa personalizzata.** Se è necessario fornire opzioni aggiuntive, estendere la finestra di dialogo comune Opzioni di stampa. Non usare una finestra di dialogo separata per opzioni di stampa aggiuntive.

**Non corretto:**

![Screenshot della finestra di dialogo opzioni di stampa personalizzate ](images/exper-printing-image11.png)

In questo esempio Fabrikam usa erroneamente una finestra di dialogo separata per opzioni di stampa aggiuntive.

**Sviluppatori:** Per informazioni su come estendere la finestra di dialogo comune Stampa, vedere [Struttura PRINTDLGEX.](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)

-   **Quando si estende la finestra di dialogo comune Opzioni di stampa, non duplicare le funzionalità già fornite.**
-   **Se è probabile che gli utenti mantengano le impostazioni da un processo di stampa a quello successivo, impostare tali impostazioni come impostazioni predefinite.** Per il primo processo di stampa dopo l'avvio del programma, usare i valori predefiniti standard, inclusa la stampante predefinita. Per i processi di stampa successivi [nell'istanza del programma](glossary.md), mantenere l'ultima stampante e il formato della carta selezionati. Non mantenere il numero di copie o intervalli di pagine, perché è molto meno probabile che questi elementi verranno selezionati di nuovo in un secondo momento.
-   **Ottimizzare le impostazioni rimuovendo le opzioni attualmente non applicabili.** Rimuovere le opzioni non coerenti con le funzionalità della stampante o delle caratteristiche selezionate del documento corrente. Ad esempio, un'applicazione per la stampa di foto potrebbe limitare le combinazioni di formato carta, tipo di carta e qualità di stampa che offrono risultati ottimali, pertanto la scelta di un'opzione di carta glossario potrebbe rimuovere le buste dai formati di carta. Se per qualsiasi motivo gli utenti vogliono visualizzare tutte le opzioni, è possibile fornire questa possibilità tramite un controllo, ad esempio una casella di controllo.

**Sviluppatori:** Per informazioni su come determinare le funzionalità della stampante selezionata, vedere [Schema di stampa.](../printdocs/print-schema.md)

-   **Per i programmi di creazione di documenti avanzati, salvare le opzioni di stampa correlate ai documenti all'interno del documento stesso.** Per questi programmi, le opzioni di stampa sono parte integrante del documento.
-   **Per altri tipi di programmi, salvare le impostazioni in base all'utente.**
-   **È consigliabile selezionare una stampante non predefinita per la stampa specializzata.** Ad esempio, un'applicazione di stampa di foto può sempre selezionare l'ultima stampante usata dal programma, indipendentemente dalla stampante predefinita del sistema. In questo modo si presuppone che la stampante predefinita del sistema non sia probabilmente una stampante foto. Tali programmi devono salvare l'impostazione per l'ultima stampante selezionata.
-   **Non bloccare il programma durante il rilevamento delle funzionalità della stampante.** Questa operazione presenta un'esperienza utente scadente. In alternativa, è possibile:
    -   Eseguire il rilevamento delle funzionalità della stampante in un thread separato.
    -   Timeout dopo 10 secondi.
    -   Specificare una finestra di dialogo per consentire agli utenti di annullare l'operazione.

![Screenshot della finestra di dialogo "Connessione a" ](images/exper-printing-image12.png)

In questo esempio, la finestra di dialogo semplifica l'annullamento del rilevamento delle funzionalità della stampante se l'utente decide che l'attività sta prendendo troppo tempo.

### <a name="print-previews"></a>Anteprime di stampa

-   **Fornire una funzionalità di anteprima di stampa quando appropriato.** Tutti i programmi di creazione di documenti traggono vantaggio dalle anteprime di stampa, ma gli utenti non li prevedono in semplici programmi di creazione di documenti. Per i programmi avanzati di creazione di documenti, è consigliabile avere il supporto dell'anteprima di stampa direttamente nella finestra principale del programma.

![Screenshot della pagina visualizzata nell'anteprima di stampa ](images/exper-printing-image13.png)

In questo esempio, Word ha il supporto dell'anteprima di stampa all'interno della finestra principale del programma.

-   Fornire funzionalità di anteprima di stampa che consentono agli utenti di:
    -   Valutare margini, interruzioni di pagina, orientamento della pagina, intestazioni e piè di pagina.
    -   Esplorare tutte le pagine.
    -   Stampare direttamente dall'anteprima di stampa.

È consigliabile fornire un'anteprima di stampa interattiva in modo che gli utenti possano modificare le impostazioni modificate di frequente, ad esempio margini e interruzioni di riga direttamente all'interno dell'anteprima.

-   **Fare in modo che il rendering delle pagine di anteprima di stampa sia eseguito entro un secondo.** È meglio avere un'anteprima di stampa che esegue il rendering rapidamente ed è sufficientemente accurata da consentire agli utenti di valutare i risultati della stampa piuttosto che avere un'anteprima completamente accurata che viene visualizzata lentamente.
-   **Per i programmi avanzati di** creazione di documenti, è consigliabile estendere la finestra di dialogo Stampa standard incorporando la funzionalità di anteprima direttamente al suo interno, anziché creare una finestra di dialogo separata.
-   **Fornire un pulsante ovvio per la chiusura della modalità di anteprima.**

![Screenshot dell'icona di chiusura dell'anteprima di stampa e dell'etichetta ](images/exper-printing-image14.png)

La modalità Anteprima di stampa in Word include un comando di chiusura dell'anteprima ovvio.

### <a name="printing-errors"></a>Errori di stampa

**Nota:** Dopo che il processo di stampa è stato spoolato alla stampante, Windows è responsabile di eventuali errori successivi. Il programma deve gestire solo gli errori che si verificano prima dello spooling del processo di stampa.

-   **Prima di eseguire lo spooling di un processo di stampa, verificare la presenza di potenziali problemi di stampa che l'utente può risolvere.** Prima di continuare a stampare, presentare una conferma chiara e concisa. Quando possibile, offrire di risolvere automaticamente il problema. In questo modo è possibile evitare uno spreco di tempo e denaro.

## <a name="text"></a>Testo

-   Per stampare su entrambi i lati del foglio, etichettare l'opzione Stampa fronte/retro. Non usare la frase Manual Duplex.

## <a name="documentation"></a>Documentazione

-   Usare print, not print out, come verbo.
-   È accettabile usare printout per fare riferimento al risultato di un processo di stampa.
-   Usare la coda di stampa, non la coda della stampante.

