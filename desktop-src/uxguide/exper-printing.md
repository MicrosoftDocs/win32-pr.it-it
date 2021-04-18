---
title: Stampa (nozioni di base sulla progettazione)
description: La stampa è l'esperienza utente su carta. È facile trascurarsi, ma è una parte importante dell'esperienza utente complessiva.
ms.assetid: 26f5a8dc-27b2-4c2d-a05a-f942784c3cf9
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a98bf29da1169ad43a3b1d16ab52298d62612037
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104556262"
---
# <a name="printing-design-basics"></a>Stampa (nozioni di base sulla progettazione)

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

La stampa è l'esperienza utente su carta. È facile trascurarsi, ma è una parte importante dell'esperienza utente complessiva.

In questo articolo, la *stampa* si riferisce all'esperienza utente su carta, in cui l'output viene indirizzato a carta anziché alla visualizzazione dello schermo. Il *formato descrittivo* per le stampanti si riferisce alle modifiche che il programma può effettuare per visualizzare l'output dello schermo che lo rende più adatto per l'output della carta

Nonostante la stima che il computing comporti un "ufficio senza carta", sorprendentemente si stampa ora quanto mai. Microsoft distribuisce copie complete dei deck di presentazione di Microsoft PowerPoint. gli articoli che si rilevano online, ma che desiderano eseguire ricerche con maggiore attenzione in un secondo momento, stampano importanti messaggi di posta elettronica o riprende il modulo elettronico e così via. Sebbene sia facile trascurare la stampa quando si progetta un'interfaccia utente, tenere presente che la stampa è una parte importante dell'esperienza utente complessiva.

**Nota:** Le linee guida relative alle [finestre di dialogo comuni](win-common-dlg.md) sono presentate in un articolo separato.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente corretta?

Per decidere se il programma deve supportare la stampa, prendere in considerazione le domande seguenti:

-   **Quale tipo di programma si sta progettando?** Il tipo di programma è un indicatore valido del livello di supporto di stampa appropriato. I programmi per la creazione, la visualizzazione e l'esplorazione di documenti e immagini richiedono un eccellente supporto di stampa, mentre altri tipi di programmi possono richiedere solo il supporto della stampa a un livello inferiore. Per un elenco dei tipi di programma, vedere la sezione [modelli di stampa](#printing-patterns) di questo articolo.
-   **Il programma è usato in scenari che traggono vantaggio dall'output diretto del documento?** In tal caso, è più comodo aggiungere il supporto per la stampa al programma anziché richiedere agli utenti di copiare i dati in un altro programma per la stampa.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="design-your-program-to-eliminate-unnecessary-printing"></a>Progettare il programma per eliminare la stampa non necessaria

Esistono molti motivi per cui gli utenti devono stamparne alcune, alcune delle quali sono meno efficaci. Gli utenti devono stampare perché desiderano, non perché devono. La richiesta di stampa da parte degli utenti può essere un segno di funzionalità mancanti. Ad esempio, in passato gli utenti dovevano stampare i documenti per creare commenti e suggerire revisioni, ma ora gli utenti possono eseguire queste attività direttamente all'interno di documenti di Microsoft Word. **Esaminare gli scenari del programma che comportano la stampa e, in modo ottimale, assicurarsi che la necessità di stampare sia facoltativa e non il risultato delle funzionalità mancanti.**

È anche importante ricordare che la conservazione di risorse come la carta e l'input penna è utile per l'ambiente e consente di risparmiare denaro per le organizzazioni a lungo termine.

### <a name="understand-the-differences-between-screen-display-and-print"></a>Informazioni sulle differenze tra la visualizzazione e la stampa dello schermo

Sebbene esistano molte analogie tra l'output visualizzato e la stampa, esistono anche molte differenze. Output di stampa:

-   **Ha un valore DPI elevato.** L'output visualizzato è in genere a 96 o 120 punti per pollice (dpi), mentre l'output della stampante è in genere a 600 dpi o superiore.
-   **Dispone di tipi di carattere ottimali diversi.** Sebbene i tipi di carattere ben progettati funzionino correttamente per la visualizzazione e la stampa, i tipi di carattere Serif sono più leggibili a risoluzioni elevate per grandi quantità di testo rispetto ai tipi di carattere sans serif. Pertanto, le grandi quantità di testo destinate principalmente alla stampa devono usare un tipo di carattere serif, mentre il testo destinato principalmente alla visualizzazione deve usare un tipo di carattere sans serif. Per ulteriori informazioni, vedere [tipi di carattere](vis-fonts.md) (Segoe UI).
-   **Ha proporzioni.** La visualizzazione ha in genere una bassa [percentuale](glossary.md) di proporzioni (4:3 o 5:4), mentre la stampa usa una percentuale elevata (8.5:11 o 1:1.4142 in base alle dimensioni standard della pagina). Questo è dovuto al fatto che la stampa in [modalità verticale](glossary.md) è più comune rispetto alla [modalità orizzontale](glossary.md).
-   **Con pagine.** Di conseguenza, stampare l'output:
    -   Ha dimensioni di pagina standard. Lo standard nel Stati Uniti e in Canada è 8.5 "X11". lo standard in qualsiasi altro documento è a4.
    -   Con interruzioni di pagina.
    -   Ha margini di pagina.
    -   Contiene intestazioni e piè di pagina.
    -   Ha un output a singolo o doppio lato.
    -   Potrebbe avere più copie.
    -   Può essere stampato fuori ordine o in modo selettivo.
-   **Sono disponibili molte opzioni.** È possibile che gli utenti desiderino scegliere la stampante e il formato della carta, le opzioni di stampa, ad esempio la qualità di stampa, la stampa su due lati e la pinzatura, il numero di copie, gli intervalli di pagine, le regole di confronto e il formato di stampa.
-   **Richiede tempo e denaro.** La stampa di un documento di grandi dimensioni o di una foto di alta qualità può richiedere molto tempo e il costo della carta e dell'input penna aumenta nel tempo. Al contrario, l'output visualizzato è istantaneo ed è praticamente gratuito.
-   **Può essere nero e bianco.** Molte stampanti oggi sono nere e bianche, mentre alcune visualizzazioni sono monocromatiche.
-   **Non è interattivo.** Gli utenti non possono scorrere le pagine o i controlli per visualizzare altri contenuti. Non possono fare clic sui collegamenti o sui pulsanti o passare il mouse sui controlli. Il contenuto interattivo non ha alcun valore quando viene stampato.
-   **Può esaurire la carta, l'input penna o il toner oppure essere offline.** Di conseguenza, l'output della carta richiede più gestione degli errori e la risoluzione dei problemi.

Queste differenze possono influire sulla progettazione della stampa. La creazione di una corretta esperienza di stampa richiede un numero maggiore rispetto alla semplice indirizzamento dell'output del programma alla stampante.

### <a name="wysiwyg-and-the-evolving-requirements-of-screen-display"></a>WYSIWYG e i requisiti in evoluzione per la visualizzazione dello schermo

In passato, il principio più fondamentale per l'esperienza utente di stampa è noto come WYSIWYG ("ciò che viene visualizzato è quello che si ottiene"). Questo principio suggerisce che deve esserci una relazione forte tra ciò che viene visualizzato sullo schermo e ciò che viene stampato. Prima che WYSIWYG diventasse una procedura standard, spesso non esisteva alcuna relazione tra le versioni di visualizzazione e di stampa di un documento. Gli utenti dovevano stampare per visualizzare l'aspetto del documento in formato cartaceo. L'uso di WYSIWYG è stato un notevole miglioramento della produttività, perché la maggior parte dei programmi era progettata principalmente per la creazione e la stampa di documenti.

Attualmente, i siti Web possono essere ottimizzati per la visualizzazione e il formato descrittivo per le stampanti potrebbe essere molto diverso. Sono inoltre disponibili diversi dispositivi di elaborazione (ad esempio, smartphone e Personal Digital Assistant) che spesso richiedono un output ottimizzato per piccoli schermi. Anche se WYSIWYG è ancora l'approccio migliore per i programmi di creazione di documenti, per altri programmi spesso è più sensato ottimizzarlo per un'ampia gamma di dispositivi di destinazione. Per tali programmi, ciò che viene visualizzato in un computer può essere diverso da quello visualizzato in altri dispositivi, che può essere diverso da quello ottenuto nella pagina stampata.

### <a name="optimize-for-printing"></a>Ottimizza per la stampa

I programmi che non utilizzano un'esperienza di stampa WYSIWYG rigorosa possono comunque essere ottimizzati per la stampa nei modi seguenti:

-   Riformattare il layout per le dimensioni della pagina di destinazione.
-   Fornire l'anteprima di stampa, preferibilmente con semplici opzioni di personalizzazione che consentono agli utenti di sperimentare direttamente nella finestra di dialogo di stampa, ad esempio trascinando i margini.
-   Se appropriato, fornire un'opzione di formato descrittivo per la stampante.
    -   Consolidare documenti parziali distinti in un singolo documento.
    -   Rimuovere gli sfondi e altri elementi di progettazione, ad esempio gli annunci, specialmente se non sono adatti per una stampante nera e bianca.
    -   Rimuovere gli elementi interattivi, ad esempio i controlli di navigazione e i pulsanti di comando.
    -   Assicurarsi che tutti i dati siano visibili senza barre di scorrimento o posizionati al passaggio del mouse.

        **Versione di visualizzazione:**

        ![screenshot del report ottimizzato per la schermata ](images/exper-printing-image1.png)

        **Versione per la stampa:**

        ![screenshot dello stesso report ottimizzato per la stampa ](images/exper-printing-image2.png)

        Nella versione per la stampa tutti i dati sono visibili nella pagina stampata e gli elementi interattivi vengono rimossi.

    -   Sostituire i collegamenti con il loro equivalente di testo.

        **Accettabile:**

        Per ulteriori informazioni, vedere la Guida all'UX.

        **Ottimizzato per la stampa:**

        Per ulteriori informazioni, vedere la Guida all'UX ( https://msdn.microsoft.com/windowsvista/uxguide) .

-   Converte il testo chiaro su uno sfondo scuro in testo scuro su sfondo bianco.

### <a name="include-the-right-print-options"></a>Includi le opzioni di stampa corrette

Nella finestra di dialogo Opzioni di stampa comuni sono disponibili le opzioni seguenti:

-   Selezionare la stampante e il formato della carta.
-   Impostare le proprietà della stampante.
-   Selezionare l'intervallo di pagine, il numero di copie e le regole di confronto.
-   Usare entrambi i lati del documento.

Il programma potrebbe richiedere opzioni aggiuntive, ad esempio le opzioni di contenuto del documento (contenuto da stampare), le opzioni di formattazione (come stampare, incluse la qualità di stampa, le dimensioni delle immagini, l'adattamento al frame) e le opzioni relative ai colori. Se è necessario fornire opzioni aggiuntive, eseguire questa operazione estendendo la finestra di dialogo Opzioni di stampa comuni. Non creare una finestra di dialogo di stampa personalizzata.

Quando si progettano le opzioni di stampa, considerare l'esperienza durante la stampa di più documenti. È probabile che il successivo processo di stampa sarà molto simile all'ultimo processo di stampa. Ottimizzando le impostazioni predefinite per le ristampe e i processi di stampa simili non è necessario che gli utenti ripartano completamente ogni volta.

### <a name="design-print-preview-for-performance-and-usability"></a>Progettare un'anteprima di stampa per le prestazioni e l'usabilità

**Un processo di stampa errato spreca tempo e denaro. Per i programmi di creazione dei documenti, gli utenti devono essere in grado di valutare i risultati prima di eseguire la stampa effettiva.** Un'anteprima di stampa deve consentire agli utenti di:

-   Valutare i margini, le interruzioni di pagina, l'orientamento della pagina, le intestazioni e i piè di pagina.
-   Sfogliare tutte le pagine.
-   Stampa direttamente dall'anteprima di stampa.

Il rendering di alcuni documenti complessi, ad esempio i \[ disegni CAD di progettazione computerizzata \] , può richiedere molto tempo. Le prestazioni dell'anteprima sono importanti perché un'anteprima di stampa può diventare piuttosto noiosa se è necessario eseguire il rendering di ogni pagina. **Di conseguenza, è preferibile avere un'anteprima di stampa che esegue rapidamente il rendering ed è sufficientemente accurata da consentire agli utenti di valutare i risultati della stampa rispetto a un'anteprima completamente accurata che esegue il rendering lentamente.**

Quando si progetta l'anteprima di stampa, prendere in considerazione l'intera attività di preparazione alla stampa. Cosa si intende per gli utenti? Quali modifiche verranno modificate? I programmi per la creazione di documenti devono fornire un'anteprima di stampa interattiva, in modo che gli utenti possano modificare le impostazioni modificate di frequente, come i margini e le interruzioni di riga

Tuttavia, nella maggior parte dei casi, il programma deve eseguire l'operazione corretta per impostazione predefinita. Quando necessario, avvisare in caso di situazioni di stampa che è improbabile che siano quelle previste dall'utente. Non fare affidamento sugli utenti che trovano problemi usando l'anteprima di stampa. Si supponga, ad esempio, che un foglio di calcolo includa un numero eccessivo di colonne da stampare in una singola pagina in modalità verticale. Sebbene il programma possa presentare una finestra di dialogo di conferma, una soluzione migliore consiste nel stampare automaticamente in modalità orizzontale.

**Se si eseguono solo cinque operazioni...**

1.  Progettare un'esperienza di stampa appropriata per il tipo di programma.
2.  Esaminare gli scenari del programma che comportano la stampa e la massima portata possibile, in modo da richiedere la stampa facoltativa.
3.  Fornire utili estensioni di stampa personalizzando la finestra di dialogo Stampa comune. Non creare una finestra di dialogo di stampa personalizzata per questo scopo.
4.  Ottimizzare le opzioni di stampa per ristampe e processi di stampa simili.
5.  Fornire una funzionalità di anteprima quando appropriato.

## <a name="printing-patterns"></a>Modelli di stampa

Il tipo di programma è l'indicatore principale dell'esperienza di stampa appropriata:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Creazione di documenti avanzati</strong><br/> Utilizzato per creare, visualizzare e stampare documenti di fascia alta. La possibilità di creare stampe di alta qualità è uno dei motivi principali per cui il programma esiste. Destinata a utenti esperti. <br/></td>
<td><strong>Obiettivi utente:</strong> Risultati perfetti controllo dettagliato sull'output di stampa.<br/> <strong>Esempio:</strong> Microsoft Word<br/> <strong>Esperienza di stampa consigliata:</strong><br/>
<ul>
<li>Output ottimizzato per la stampa (WYSIWYG).</li>
<li>Funzionalità avanzate di formattazione dei documenti con opzioni per la stampa di oggetti di grandi dimensioni.</li>
<li>Opzioni di stampa avanzate, incluse le intestazioni e i piè di pagina. Le opzioni di stampa correlate ai documenti vengono salvate all'interno del documento stesso.</li>
<li>Anteprime di stampa veloci, accurate e potenti.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Creazione di documenti intermedi</strong><br/> Utilizzato per creare e visualizzare documenti più complessi. La possibilità di creare stampe di qualità elevata è importante, ma non necessariamente uno dei motivi principali per cui il programma esiste. Destinati a utenti intermedi. <br/></td>
<td><strong>Obiettivi utente:</strong> Risultati soddisfacenti con il minimo sforzo. Un controllo sull'output di stampa.<br/> <strong>Esempi:</strong> La maggior parte dei programmi di Microsoft Office, ad esempio Outlook ed Excel.<br/> <strong>Esperienza di stampa consigliata:</strong><br/>
<ul>
<li>Output ottimizzato per la stampa (WYSIWYG).</li>
<li>Alcune funzionalità di formattazione dei documenti, con la possibilità di stampare oggetti di grandi dimensioni senza troncamento.</li>
<li>Alcune opzioni di stampa personalizzate, incluse le intestazioni e i piè di pagina.</li>
<li>Anteprime di stampa accurate e facili da usare.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Creazione di un documento semplice</strong><br/> Utilizzato per creare e visualizzare documenti semplici. Destinato a tutti gli utenti. <br/></td>
<td><strong>Obiettivi utente:</strong> Supporto di stampa di base con le opzioni di stampa standard. Gli utenti si aspettano risultati validi senza alcuna modifica.<br/> <strong>Esempi:</strong> WordPad, Paint.<br/> <strong>Esperienza di stampa consigliata:</strong><br/>
<ul>
<li>L'output può essere ottimizzato per la stampa (WYSIWYG), ma questa operazione non è obbligatoria.</li>
<li>Alcune funzionalità di formattazione dei documenti, con la possibilità di stampare oggetti di grandi dimensioni senza troncamento.</li>
<li>Opzioni di stampa standard; le opzioni di stampa personalizzate sono facoltative.</li>
<li>Anteprime semplici o senza stampa.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Visualizzatori documenti</strong><br/> Utilizzato per visualizzare i documenti. Gli utenti non possono modificare il contenuto o il formato del documento. <br/></td>
<td><strong>Obiettivi utente:</strong> Supporto di stampa di base con le opzioni di stampa standard. Gli utenti si aspettano risultati validi senza alcuna modifica. I problemi di stampa vengono gestiti automaticamente perché gli utenti non possono modificare il documento.<br/> <strong>Esempio:</strong> Windows Internet Explorer<br/> <strong>Esperienza di stampa consigliata:</strong><br/>
<ul>
<li>L'output può essere ottimizzato per la stampa (WYSIWYG), ma questa operazione non è obbligatoria.</li>
<li>Il programma gestisce automaticamente le interruzioni di pagina, Elimina le pagine vuote, gestisce oggetti di grandi dimensioni e rimuove gli sfondi e altri elementi di progettazione.</li>
<li>Opzioni di stampa standard; le opzioni di stampa personalizzate sono facoltative.</li>
<li>Anteprime semplici o senza stampa.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Utilità o applicazioni line-of-business</strong><br/> Utilizzato per eseguire attività semplici e specifiche. Destinato a tutti gli utenti. <br/></td>
<td><strong>Obiettivi utente:</strong> Possibilità di esportare i dati selezionati in modo efficiente. Gli utenti si aspettano risultati validi senza alcuna modifica. Spesso, per tali programmi, gli utenti sono piacevolmente sorpresi a trovare qualsiasi supporto per la stampa.<br/> <strong>Esperienza di stampa consigliata:</strong><br/>
<ul>
<li>Il supporto di stampa è facoltativo a seconda degli scenari supportati.</li>
<li>L'output può essere ottimizzato per la stampa (WYSIWYG), ma questa operazione non è obbligatoria.</li>
<li>Alcune funzionalità di formattazione dei documenti. Potrebbe essere accettabile se gli oggetti di grandi dimensioni vengono troncati.</li>
<li>Opzioni di stampa standard.</li>
<li>Anteprima di stampa facoltativa.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Non stampare pagine o pagine vuote con solo intestazioni e piè di pagina.** Tuttavia, stampare le pagine vuote se le intestazioni o i piè di pagina contengono numeri di pagina e i numeri di pagina potrebbero farvi riferimento altrove.
-   **Eseguire lo spooling completo di tutti i processi di stampa in sospeso prima di arrestare un programma.**

### <a name="formatting-pages"></a>Formattazione di pagine

-   **Riformattare il layout del testo in base alle dimensioni della pagina di destinazione.** Non troncare mai il testo.
-   Se gli utenti non controllano il formato del documento:
    -   **Gestione automatica di oggetti di grandi dimensioni mediante scalabilità, rotazione o suddivisione tra pagine.** Per altre linee guida sulla stampa di oggetti di grandi dimensioni, vedere [oggetti di dimensioni](#oversized-objects)eccessive.
    -   **Ottimizzare le interruzioni di pagina per eliminare le pagine vuote e quasi vuote.**
    -   **Converte il testo chiaro su uno sfondo scuro in testo scuro su sfondo bianco.**
    -   **Rimuovere gli sfondi e altri elementi di progettazione,** soprattutto se non sono adatti a una stampante nera e bianca.
-   **Se il programma presenta documenti parziali distinti, fornire un'opzione di formato descrittivo per la stampa per consolidarli in un singolo documento per la stampa.**
-   **Rimuovi elementi interattivi:**
    -   Rimuovere i controlli di spostamento e i pulsanti di comando.
    -   Assicurarsi che tutti i dati siano visibili senza barre di scorrimento.
    -   Sostituire i collegamenti con il loro equivalente di testo.

        **Accettabile:**

        Per ulteriori informazioni, vedere la Guida all'UX.

        **Ottimizzato per la stampa:**

        Per ulteriori informazioni, vedere la Guida all'UX ( https://msdn.microsoft.com/windowsvista/uxguide) .

        In questo esempio, il collegamento viene sostituito con il testo equivalente tra parentesi.

    -   Spostare le informazioni utili visualizzate al passaggio del mouse su inline.

### <a name="oversized-objects"></a>Oggetti sovradimensionati

La gestione di oggetti di grandi dimensioni, ad esempio fogli di calcolo, grafica e foto, rappresenta un problema univoco alla stampa. Scegliere uno degli approcci seguenti:

-   **Ridimensionare l'oggetto per adattarlo alla pagina.** Questo approccio funziona bene se la stampa dell'oggetto è solo leggermente troppo grande, il mantenimento dell'oggetto in una singola pagina è importante e l'oggetto è ancora leggibile se ridimensionato.

    ![screenshot della foto ridimensionato alla metà di una pagina ](images/exper-printing-image3.png)

    In questo esempio, l'immagine di grandi dimensioni viene ridimensionata per adattarsi alla pagina.

-   **Ruotare la pagina.** Questo approccio funziona bene quando alcune pagine stampano meglio in modalità orizzontale in modalità verticale (e viceversa).

    ![screenshot della foto orizzontale ruotata in verticale ](images/exper-printing-image4.png)

    In questo esempio, l'immagine di grandi dimensioni viene ruotata per adattarsi meglio alla pagina.

-   **Stampare l'oggetto in diverse pagine.** L'approccio funziona bene quando l'oggetto non può essere ridimensionato o non deve essere ridimensionato e la rotazione della pagina non è utile o non è necessaria. Se l'oggetto dispone di limiti interni (ad esempio, i separatori di colonna e di riga in un foglio di calcolo), suddividere le pagine su questi limiti anziché all'interno del contenuto. Inoltre, ripetere tutti gli elementi necessari per comprendere la pagina, ad esempio legende o intestazioni di colonna. Quando si suddivide un oggetto in più pagine, assegnare i numeri di pagina in ordine di lettura (da sinistra a destra, dall'alto verso il basso).

    ![screenshot delle intestazioni di colonna ripetute nella pagina successiva ](images/exper-printing-image5.png)

    In questo esempio, la tabella di grandi dimensioni viene stampata in due pagine. Le intestazioni di colonna vengono mantenute da pagina a pagina per facilitare la comprensione rapida.

-   **Troncare l'oggetto** (stampa solo la parte dell'oggetto ancora visibile dopo il troncamento). Questo approccio è la soluzione più semplice da implementare, ma probabilmente è il meno accettabile. Si noti inoltre che il troncamento non è mai accettabile per il testo.

    ![screenshot della metà della foto nella pagina verticale ](images/exper-printing-image6.png)

    In questo esempio, l'immagine di grandi dimensioni viene troncata.

### <a name="headers-and-footers"></a>Intestazioni e piè di pagina

-   **Fornire intestazioni e piè di pagina per i programmi avanzati e intermedi per la creazione di documenti.** Valutare la possibilità di fornire intestazioni e piè di pagina per altri tipi di programmi se usati per documenti a più pagine.
-   **Rendere personalizzabili le intestazioni e i piè di pagina.** Consente agli utenti di definire le parti sinistra, centrale e destra.
    -   Per le intestazioni, inserire il nome del documento sul lato sinistro per impostazione predefinita.
    -   Per i piè di pagina, inserire il copyright o l'origine del documento sul lato sinistro e il numero di pagina sul lato destro, per impostazione predefinita.
-   **Utilizzare URL e percorso di file descrittivi.** Visualizza spazi come spazi, non "%20".

### <a name="print-commands"></a>Stampa comandi

-   **Per le barre dei menu e i menu di scelta rapida, utilizzare il comando stampa per visualizzare la finestra di dialogo Opzioni di stampa comuni.** Utilizzare i puntini di sospensione per indicare che sono necessarie informazioni aggiuntive.

    ![screenshot del menu file, comando stampa selezionato ](images/exper-printing-image7.png)

    In questo esempio, il comando Print presenta i puntini di sospensione per indicare che verrà visualizzata la finestra di dialogo Opzioni di stampa comuni per ottenere ulteriori informazioni.

-   **Per le barre degli strumenti utilizzate con una barra dei menu, utilizzare un comando di stampa immediato.** Facendo clic sul pulsante viene stampata una sola copia del documento sulla stampante predefinita. Tali comandi della barra degli strumenti devono essere immediati. Per indicare che il comando è immediato, inserire la stampante predefinita nella descrizione comando. Gli utenti possono accedere al comando stampa completa dalla barra dei menu.

    ![screenshot dell'icona della stampante e della relativa descrizione comando ](images/exper-printing-image8.png)

    In questo esempio il comando stampa di una barra degli strumenti viene stampato immediatamente anziché visualizzare la finestra di dialogo delle opzioni di stampa comune. L'inserimento della stampante predefinita nella descrizione comando fornisce un rinforzo testuale che l'utente ignora la finestra di dialogo.

-   **Per le barre degli strumenti utilizzate senza una barra dei menu, utilizzare un pulsante stampa Split.** Facendo clic sul pulsante viene stampata una sola copia del documento sulla stampante predefinita. Facendo clic sulla freccia del pulsante viene visualizzato un menu con i comandi di stampa completa, anteprima di stampa e imposta pagina.

    ![screenshot dell'icona della stampante sul pulsante di divisione ](images/exper-printing-image9.png)

    In questo esempio, la barra degli strumenti di Windows Internet Explorer utilizza un pulsante di comando combinato per fornire tutti i comandi di stampa.

-   **Per l'interfaccia utente del comando della barra multifunzione, inserire il comando stampa nel menu dell'applicazione.**

    ![screenshot dei comandi posizionati verticalmente a sinistra ](images/exper-printing-image10.png)

    Per le barre multifunzione, è possibile accedere al comando stampa tramite il menu applicazione.

### <a name="print-options"></a>Opzioni di stampa

-   **Non creare una finestra di dialogo Opzioni di stampa personalizzate.** Se è necessario fornire opzioni aggiuntive, estendere la finestra di dialogo comuni opzioni di stampa. Non usare una finestra di dialogo separata per altre opzioni di stampa.

**Non corretto:**

![screenshot della finestra di dialogo Opzioni di stampa personalizzate ](images/exper-printing-image11.png)

In questo esempio Fabrikam USA erroneamente una finestra di dialogo separata per altre opzioni di stampa.

**Sviluppatori:** Per informazioni su come estendere la finestra di dialogo Stampa comune, vedere [struttura PRINTDLGEX](/windows/win32/api/commdlg/ns-commdlg-printdlgexa).

-   **Quando si estende la finestra di dialogo Opzioni di stampa comuni, non duplicare le funzionalità già fornite.**
-   **Se gli utenti hanno la possibilità di mantenere le impostazioni da un processo di stampa a quello successivo, rendere le impostazioni predefinite.** Per il primo processo di stampa dopo l'avvio del programma, utilizzare i valori predefiniti standard, inclusa la stampante predefinita. Per i processi di stampa successivi nell' [istanza](glossary.md)del programma, mantenere le ultime dimensioni della stampante e della carta selezionate. Non mantenere il numero di copie o intervalli di pagine, perché è molto meno probabile che vengano riselezionate in un secondo momento.
-   **Ottimizzare le impostazioni rimuovendo le opzioni attualmente non applicabili.** Rimuovere le opzioni non coerenti con le funzionalità della stampante o delle caratteristiche selezionate del documento corrente. Ad esempio, un'applicazione di stampa fotografica può limitare le combinazioni di formato carta, tipo di carta e qualità di stampa per ottenere risultati ottimali, quindi la scelta di un'opzione di carta patinata potrebbe rimuovere buste dai formati di carta. Se per qualsiasi motivo gli utenti desiderano visualizzare tutte le opzioni, è possibile fornire questa possibilità tramite un controllo, ad esempio una casella di controllo.

**Sviluppatori:** Per informazioni su come determinare le funzionalità della stampante selezionata, vedere [Print Schema](../printdocs/print-schema.md).

-   **Per i programmi avanzati per la creazione di documenti, salvare le opzioni di stampa relative ai documenti all'interno del documento stesso.** Per questi programmi, le opzioni di stampa sono parte integrante del documento.
-   **Per altri tipi di programmi, salvare le impostazioni per ogni singolo utente.**
-   **Valutare la possibilità di selezionare una stampante non predefinita per la stampa specializzata.** Ad esempio, un'applicazione di stampa fotografica può sempre selezionare la stampante utilizzata per l'ultima volta dal programma, indipendentemente dalla stampante predefinita del sistema. In questo modo si presuppone che la stampante predefinita del sistema non sia una stampante foto. Tali programmi devono salvare l'impostazione per l'ultima stampante selezionata.
-   **Non bloccare il programma durante il rilevamento delle funzionalità della stampante.** In questo modo si presenta un'esperienza utente insufficiente. In alternativa, eseguire una delle operazioni seguenti:
    -   Eseguire il rilevamento delle funzionalità della stampante in un thread separato.
    -   Timeout dopo 10 secondi.
    -   Consente di specificare una finestra di dialogo per consentire agli utenti di annullare.

![screenshot della finestra di dialogo ' connessione a' ](images/exper-printing-image12.png)

In questo esempio, la finestra di dialogo rende più semplice annullare il rilevamento della funzionalità della stampante se l'utente decide che l'attività sta richiedendo troppo tempo.

### <a name="print-previews"></a>Anteprime di stampa

-   **Fornire una funzionalità di anteprima di stampa quando appropriato.** Tutti i programmi di creazione di documenti traggono vantaggio dalle anteprime di stampa, ma gli utenti non si aspettano in semplici programmi di creazione di documenti. Per i programmi avanzati per la creazione di documenti, provare a usare l'anteprima di stampa direttamente nella finestra principale del programma.

![screenshot della pagina visualizzata nell'anteprima di stampa ](images/exper-printing-image13.png)

In questo esempio Word dispone del supporto per l'anteprima di stampa all'interno della finestra principale del programma.

-   Fornire funzionalità di anteprima di stampa che consentono agli utenti di:
    -   Valutare i margini, le interruzioni di pagina, l'orientamento della pagina, le intestazioni e i piè di pagina.
    -   Sfogliare tutte le pagine.
    -   Stampa direttamente dall'anteprima di stampa.

È consigliabile fornire un'anteprima di stampa interattiva, in modo che gli utenti possano regolare le impostazioni modificate di frequente, come i margini e le interruzioni di riga direttamente nell'anteprima.

-   **Il rendering delle pagine dell'anteprima di stampa viene eseguito entro un secondo.** È preferibile avere un'anteprima di stampa che viene visualizzata rapidamente e sufficientemente accurata da consentire agli utenti di valutare i risultati della stampa rispetto a un'anteprima completamente accurata che esegue il rendering lentamente.
-   **Per i programmi avanzati per la creazione di documenti, provare a estendere la finestra di dialogo stampa standard incorporando la funzionalità di anteprima direttamente al suo interno,** anziché creare una finestra di dialogo separata.
-   **Fornire un pulsante ovvio per la chiusura della modalità di anteprima.**

![screenshot dell'icona di chiusura e dell'etichetta di anteprima di stampa ](images/exper-printing-image14.png)

Per la modalità anteprima di stampa in Word è presente un comando di chiusura anteprima ovvio.

### <a name="printing-errors"></a>Errori di stampa

**Nota:** Una volta eseguito lo spooling del processo di stampa alla stampante, Windows è responsabile di eventuali errori successivi. Il programma deve gestire solo gli errori che si verificano prima dello spooling del processo di stampa.

-   **Prima di eseguire lo spooling di un processo di stampa, verificare la presenza di potenziali problemi di stampa che l'utente può risolvere.** Presentare una conferma chiara e concisa prima di continuare con la stampa. Laddove possibile, offrire per risolvere automaticamente il problema. Questa operazione può impedire un dispendio di tempo e denaro.

## <a name="text"></a>Testo

-   Per l'opzione di stampa su entrambi i lati del documento, etichettare l'opzione stampa a doppio lato. Non usare la frase duplex manuale.

## <a name="documentation"></a>Documentazione

-   Utilizzare stampa, non stampa, come verbo.
-   È accettabile usare la stampa per fare riferimento al risultato di un processo di stampa.
-   Utilizzare coda di stampa, non coda stampanti.

