---
title: Tipi di carattere
description: Gli utenti interagiscono con testo più che con qualsiasi altro elemento in Microsoft Windows. Segoe UI (pronunciato \ 0034; VEDERE-go \ 0034;) è il tipo di carattere di sistema Windows. La dimensione del carattere standard è stata aumentata a 9 punti.
ms.assetid: 6d4f669d-d28c-4585-9bc3-ecda44de6df5
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 6c5fad1459d4ce45f2d677d4bd5864d89b125e4e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "103761224"
---
# <a name="fonts"></a>Tipi di carattere

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Gli utenti interagiscono con testo più che con qualsiasi altro elemento in Microsoft Windows. Segoe UI (pronunciato "SEE-go") è il tipo di carattere di sistema Windows. La dimensione del carattere standard è stata aumentata a 9 punti.

![illustrazione dell'alfabeto nel tipo di carattere dell'interfaccia utente Segoe ](images/vis-fonts-image1.png)

Tipo di carattere Segoe UI.

Segoe UI e Segoe non sono dello stesso tipo di carattere. Segoe UI è il tipo di carattere di Windows progettato per le stringhe di testo dell'interfaccia utente. Segoe è un tipo di carattere di personalizzazione usato da Microsoft e dai partner per produrre materiale per la stampa e la pubblicità.

Segoe UI è un carattere tipografico accessibile, aperto e descrittivo e, di conseguenza, offre una migliore leggibilità rispetto a Tahoma, Microsoft Sans Serif e Arial. Presenta le caratteristiche di un umanizzato sans serif: le diverse larghezze delle maiuscole (Narrow e e S, ad esempio, rispetto a Helvetica, in cui le larghezze sono più simili, abbastanza estese); stress e letterforms del relativo carattere minuscolo; e il suo vero corsivo, invece di un "obliquo" o un romano inclinato, come molti sans serifs di aspetto industriale. Il carattere tipografico ha lo scopo di fornire lo stesso effetto visivo sullo schermo e in stampa. Il progetto è stato progettato per essere un umanizzato sans serif senza carattere sicuro o distracting eccentricità.

Segoe UI è ottimizzato per ClearType, che è attiva per impostazione predefinita in Windows. Con ClearType abilitato, Segoe UI è un tipo di carattere elegante e leggibile. Senza ClearType abilitato, Segoe UI è solo marginalmente accettabile. Questo fattore determina quando utilizzare Segoe UI.

Segoe UI include caratteri latini, greci, cirillici e arabi. Sono disponibili nuovi tipi di carattere, ottimizzati anche per ClearType, creati per altri set di caratteri e usi. Sono inclusi Meiryo per il giapponese, Malgun Gothic per il coreano, Microsoft JhengHei per il cinese (tradizionale), Microsoft YaHei per il cinese (semplificato), Gisha per l'ebraico e Leelawadee per Thai e i tipi di carattere della raccolta ClearType progettati per l'utilizzo dei documenti.

Meiryo include caratteri latini basati su Verdana. Malgun Gothic, Microsoft JhengHei e Microsoft YaHei usano una Segoe UI personalizzata. Non è consigliabile usare versioni italiche di questi tipi di carattere. Malgun Gothic, Microsoft JhengHei e Microsoft YaHei vengono forniti solo con stili normali e in grassetto, ovvero i caratteri in corsivo vengono sintetizzati inclinando gli stili verticali. Sebbene Meiryo includa i corsivo reali e grassetto, questi stili si applicano solo ai caratteri latini i caratteri giapponesi rimangono verticali quando viene applicato lo stile corsivo.

Nell'interfaccia utente del comando [Ribbons](cmd-ribbons.md) è preferibile una variante di Meiryo, denominata Meiryo UI.

Per supportare le impostazioni locali che utilizzano questi set di caratteri, Segoe UI viene sostituito con i tipi di carattere corretti a seconda delle impostazioni locali durante il processo di [localizzazione](glossary.md) .

Per concedere in licenza Segoe UI e altri tipi di carattere Microsoft per la distribuzione con un programma basato su Windows, contattare [Monotype](https://www.monotype.com/).

**Nota:** Le linee guida correlate allo [stile e](text-style-tone.md) al [testo dell'interfaccia utente](text-ui.md) sono presentate in articoli distinti.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="fonts-typefaces-point-sizes-and-attributes"></a>Tipi di carattere, caratteri tipografici, dimensioni punti e attributi

Nella tipografia tradizionale un tipo di carattere descrive una combinazione di caratteri tipografici, dimensioni di punti e attributi. Un carattere tipografico è l'aspetto del tipo di carattere. Segoe UI, Tahoma, Verdana e Arial sono tutti caratteri tipografici. Le dimensioni del punto si riferiscono alla dimensione del tipo di carattere, misurata dalla parte superiore del valore ascendente alla parte inferiore dei discendenti, meno la spaziatura interna (denominata iniziale). Un punto è approssimativamente di 1/72 pollice. Infine, un tipo di carattere può avere attributi di grassetto o corsivo.

In modo informale, le persone usano spesso il carattere al posto del carattere tipografico come fatto in questo articolo, ma tecnicamente Segoe UI è un carattere tipografico, non un tipo di carattere. Ogni combinazione di attributi è un tipo di carattere univoco, ad esempio 9 punti Segoe UI regolari, 10 punti Segoe UI grassetto e così via.

### <a name="serif-and-sans-serif"></a>Serif e Sans Serif

I caratteri tipografici sono Serif o sans serif. Serif si riferisce a piccoli ritocchi che spesso terminano i tratti di lettere in un tipo di carattere. Un carattere tipografico Sans Serif non ha Serif.

I lettori preferiscono in genere i caratteri serif usati come testo del corpo in un documento. I Serif forniscono una sensazione di formalità ed eleganza a un documento. Per il testo dell'interfaccia utente, la necessità di un aspetto pulito e la risoluzione inferiore dei monitoraggi computer rendono i caratteri tipografici sans serif la scelta migliore.

### <a name="contrast"></a>Si confronti

Il testo è più semplice da leggere quando esiste una grande differenza tra la luminosità del testo e lo sfondo. Il testo nero su uno sfondo bianco fornisce il testo scuro a contrasto più elevato su uno sfondo molto chiaro può offrire un contrasto elevato. Questa combinazione è ottimale per le superfici primarie dell'interfaccia utente.

Il testo chiaro su uno sfondo scuro offre un contrasto positivo, ma non un testo scuro su uno sfondo chiaro. Questa combinazione è ottimale per le superfici dell'interfaccia utente secondaria, ad esempio i riquadri attività di Esplora risorse, che si vuole deaccentuare in relazione alle superfici dell'interfaccia utente primaria.

**Per assicurarsi che gli utenti leggano il testo, usare un testo scuro in uno sfondo chiaro.**

### <a name="affordances"></a>Affordances

Il testo può usare il [affordances](glossary.md) seguente per indicare come viene usato:

-   **Puntatore.** Il puntatore i-barra ("Text Select") indica che il testo è selezionabile, mentre il puntatore a sinistra ("Normal Select") indica che il testo non è.
-   **Cursore.** Quando il testo ha lo stato attivo per l'input, il cursore è la barra verticale intermittente che indica il punto di inserimento/selezione nel testo selezionabile o modificabile.
-   **Dialogo.** Casella intorno al testo che indica che è modificabile. Per ridurre il peso della presentazione, è possibile che la casella venga visualizzata dinamicamente solo quando viene selezionato il testo modificabile.
-   **Colore primo piano.** Il grigio chiaro indica che il testo è disabilitato. I colori non grigio, in particolare blu e viola, indicano che il testo è un collegamento.
-   **Colore di sfondo.** Uno sfondo grigio chiaro suggerisce che il testo è di sola lettura, ma in pratica il testo di sola lettura può avere qualsiasi sfondo dei colori.

Questi affordances vengono combinati per i significati seguenti:

-   **Modificabile.** Testo visualizzato in una casella, con un puntatore di selezione del testo, un accento circonflesso (sullo stato attivo per l'input) e in genere su uno sfondo bianco.
-   **Di sola lettura, selezionabile.** Testo con un puntatore Select e un accento circonflesso (sullo stato attivo per l'input).
-   **Sola lettura, non selezionabile.** Testo con un puntatore a freccia.
-   **Disabilitati.** Testo grigio chiaro con un puntatore a freccia, a volte su uno sfondo grigio.

Il testo di sola lettura ha tradizionalmente uno sfondo grigio, ma non è necessario uno sfondo grigio. In realtà, uno sfondo grigio può essere indesiderato, specialmente per grandi blocchi di testo, perché suggerisce che il testo è disabilitato e sconsiglia la lettura.

### <a name="accessibility-and-the-system-font-sizes-and-colors"></a>Accessibilità e il tipo di carattere, le dimensioni e i colori del sistema

Le linee guida per rendere il testo accessibile agli utenti con disabilità o problemi possono essere ridotte a una semplice regola: rispettare le impostazioni dell'utente usando sempre il tipo di carattere, le dimensioni e i colori del sistema.

**Se si esegue una sola operazione...**

Rispettare le impostazioni dell'utente usando sempre il tipo di carattere, le dimensioni e i colori del sistema.

**Sviluppatori:** Dal codice è possibile determinare le proprietà del tipo di carattere del sistema, incluse le relative dimensioni, usando la funzione API GetThemeFont. È possibile determinare i colori di sistema utilizzando la funzione API GetThemeSysColor.

Poiché non è possibile creare presupposti sulle impostazioni del tema di sistema degli utenti, è necessario:

-   Basare sempre i colori e gli sfondi dei tipi di carattere dai colori del tema del sistema. Non creare mai colori personalizzati in base ai valori RGB fissi (rosso, verde, blu).
-   Corrisponde sempre ai colori del testo del sistema con i colori di sfondo corrispondenti. Se ad esempio si sceglie COLOR \_ STATICTEXT per il colore del testo, è inoltre necessario scegliere \_ static Color per il colore di sfondo.
-   Creare sempre nuovi tipi di carattere in base alle varianti proporzionali del tipo di carattere del sistema. Date le metriche dei tipi di carattere di sistema, è possibile creare variazioni in grassetto, corsivo, dimensioni maggiori e minori.

**Un modo semplice per verificare che il programma rispetti le impostazioni degli utenti consiste nel testare usando una dimensione del carattere diversa e una combinazione di colori a contrasto elevato.** Tutto il testo deve essere ridimensionato e visualizzato correttamente nella combinazione di colori scelta.

## <a name="usage-patterns"></a>Modelli di utilizzo

Il testo presenta diversi modelli di utilizzo:



|                                                                                                                                                                                                                                                           |                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Testo per la barra del titolo**<br/> Testo sulla barra del titolo che identifica la finestra.<br/>                                                                                                                                                                | ![esempio di tipo di carattere testo barra del titolo ](images/vis-fonts-image2.png)<br/>                                                                            |
| **Istruzioni principali**<br/> Testo che illustra le operazioni da eseguire in una pagina, una finestra o una finestra di dialogo. <br/>                                                                                                                                              | ![esempio di tipo di carattere testo istruzioni principali ](images/vis-fonts-image3.png)<br/>                                                                    |
| **Istruzioni secondarie**<br/> Testo supplementare che illustra le operazioni da eseguire in una pagina, una finestra o una finestra di dialogo. <br/>                                                                                                                            | ![esempio di tipo di carattere del testo istruzioni secondarie ](images/vis-fonts-image4.png)<br/>                                                               |
| **Testo normale**<br/> Testo ordinario (di sola lettura) visualizzato in un'interfaccia utente. <br/>                                                                                                                                                           | ![esempio di tipo di carattere testo normale ](images/vis-fonts-image5.png)<br/>                                                                               |
| **Testo enfatizzato**<br/> Il testo in grassetto viene usato per semplificare l'analisi del testo e per attirare l'attenzione sul testo che gli utenti devono leggere. il testo in corsivo viene usato per fare riferimento letteralmente al testo (anziché alle virgolette) e per evidenziare parole specifiche. <br/> | ![esempio di tipo di carattere del testo enfatizzato ](images/vis-fonts-image6.png)<br/>                                                                           |
| **Testo modificabile**<br/> Il testo che gli utenti possono modificare viene visualizzato in una casella. per ridurre il peso della presentazione, è possibile che la casella venga visualizzata solo quando è selezionato il testo modificabile. <br/>                                                          | ![esempio di tipo di carattere testo modificabile ](images/vis-fonts-image7.png)<br/>                                                                             |
| **Testo disabilitato**<br/> Testo che non si applica al contesto corrente, ad esempio le etichette per i controlli disabilitati. il testo disabilitato indica che gli utenti (normalmente) non devono preoccuparsi di leggere il testo. <br/>                                           | ![esempio di tipo di carattere testo disabilitato ](images/vis-fonts-image8.png)<br/>                                                                             |
| **Collegamenti**<br/> Testo utilizzato per passare a un'altra pagina, a una finestra o a un argomento della Guida oppure avviare un comando. <br/>                                                                                                                                     | ![esempio di tipo di carattere del testo del collegamento ](images/vis-fonts-image9.png)<br/> ![esempio di tipo di carattere del testo dei collegamenti (hover) ](images/vis-fonts-image10.png)<br/> |
| **Intestazione gruppo**<br/> Testo utilizzato per raggruppare gli elementi in una visualizzazione elenco. <br/>                                                                                                                                                                          | ![esempio di tipo di carattere testo intestazione gruppo ](images/vis-fonts-image11.png)<br/>                                                                        |
| **Nome file**<br/> Testo del nome file (solo nella visualizzazione contenuto). <br/>                                                                                                                                                                               | ![esempio di tipo di carattere del testo del nome file (in visualizzazione contenuto) ](images/vis-fonts-image12.png)<br/>                                                         |
| **Testo del documento**<br/> Testo usato nei documenti (in contrapposizione al testo dell'interfaccia utente). <br/>                                                                                                                                                                  | ![esempio di tipo di carattere del testo del documento ](images/vis-fonts-image13.png)<br/>                                                                            |
| **Intestazioni di documento**<br/> Testo utilizzato come intestazione all'interno di un documento. <br/>                                                                                                                                                                    | ![esempio di tipo di carattere testo intestazioni documento ](images/vis-fonts-image14.png)<br/>                                                                   |



 

## <a name="guidelines"></a>Indicazioni

### <a name="fonts-and-colors"></a>Tipi di carattere e colori

-   **I tipi di carattere e i colori seguenti sono predefiniti per Windows Vista e Windows 7.**



|                                                                                               |                             |                                                            |
|-----------------------------------------------------------------------------------------------|-----------------------------|------------------------------------------------------------|
| **Modello**<br/>                                                                        | **Simbolo del tema**<br/> | **Tipo di carattere, colore**<br/>                                 |
| ![esempio di tipo di carattere testo barra del titolo ](images/vis-fonts-image2.png)<br/>                    | CaptionFont<br/>      | 9 PT. nero ( \# 000000) Segoe UI<br/>                 |
| ![esempio di tipo di carattere testo istruzioni principali ](images/vis-fonts-image3.png)<br/>            | MainInstruction<br/>  | 12 PT. blu ( \# 003399) Segoe UI<br/>                 |
| ![esempio di tipo di carattere del testo istruzioni secondarie ](images/vis-fonts-image4.png)<br/>       | Istruzione<br/>      | 9 PT. nero ( \# 000000) Segoe UI<br/>                 |
| ![esempio di tipo di carattere testo normale ](images/vis-fonts-image5.png)<br/>                       | BodyText<br/>         | 9 PT. nero ( \# 000000) Segoe UI<br/>                 |
| ![esempio di tipo di carattere del testo enfatizzato ](images/vis-fonts-image6.png)<br/>                   | BodyText<br/>         | 9 PT. Segoe UI nero ( \# 000000), grassetto o corsivo<br/> |
| ![esempio di tipo di carattere testo modificabile ](images/vis-fonts-image7.png)<br/>                     | BodyText<br/>         | 9 PT. Segoe UI nero ( \# 000000), in una casella<br/>       |
| ![esempio di tipo di carattere testo disabilitato ](images/vis-fonts-image8.png)<br/>                     | Disabled<br/>         | 9 PT. grigio scuro ( \# 323232) Segoe UI<br/>             |
| ![esempio di tipo di carattere del testo del collegamento ](images/vis-fonts-image9.png)<br/>                         | HyperLinkText<br/>    | 9 PT. blu ( \# 0066CC) Segoe UI<br/>                  |
| ![esempio di tipo di carattere del testo dei collegamenti (hover) ](images/vis-fonts-image10.png)<br/>               | Accesso frequente<br/>              | 9 PT. blu chiaro ( \# 3399FF) Segoe UI<br/>            |
| ![esempio di tipo di carattere testo intestazione gruppo ](images/vis-fonts-image11.png)<br/>                |                             | 11 PT. blu ( \# 003399) Segoe UI<br/>                 |
| ![esempio di tipo di carattere del testo del nome file (in visualizzazione contenuto) ](images/vis-fonts-image12.png)<br/> |                             | 11 PT. nero ( \# 000000) Segoe UI<br/>                |
| ![esempio di tipo di carattere del testo del documento ](images/vis-fonts-image13.png)<br/>                    | (nessuna)<br/>           | 9 PT. nero ( \# 000000) calibri<br/>                  |
| ![esempio di tipo di carattere testo intestazioni documento ](images/vis-fonts-image14.png)<br/>           | (nessuna)<br/>           | 17 PT. nero ( \# 000000) calibri<br/>                 |



 

-   **Scegliere tipi di carattere e ottimizzare il layout delle finestre in base alla tecnologia dell'interfaccia utente e alla versione di destinazione di Windows:**



|                                            |                                                       |                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tecnologia dell'interfaccia utente**<br/>               | **Versione di destinazione di Windows**<br/>                 | **Tipi di carattere da usare e ottimizzare per**<br/>                                                                                                                                                                                                                                                                                                                     |
| Windows Presentation Foundation<br/> | Tutti<br/>                                        | Usare parti del tema WPF.<br/>                                                                                                                                                                                                                                                                                                                                  |
| Win32 o WinForms<br/>               | Windows Vista o versioni successive<br/>                     | Utilizzare il tipo di carattere Segoe UI appropriato.<br/>                                                                                                                                                                                                                                                                                                                    |
|                                            | Componenti estendibili o precedenti a Windows Vista<br/> | Per fare riferimento a Windows XP e Windows 2000, usare il tipo di carattere pseudo per MS Shell Dlg 2 a 8 punti, che esegue il mapping a Tahoma.<br/> Per fare riferimento a versioni precedenti di Windows, usare lo pseudo-carattere di 8 punti MS Shell Dlg, che esegue il mapping a Tahoma in Windows 2000 e Windows XP e a MS Sans Serif in Windows 95, Windows 98, Windows Millennium Edition e Windows NT 4,0.<br/> |



 

-   **Gli sviluppatori**
    -   Per gli elementi che usano il layout fisso, ad esempio i modelli di finestra di dialogo di Windows e WinForms, il codice rigido è il tipo di carattere appropriato della tabella precedente.
    -   Per gli elementi che usano il layout dinamico (ad esempio Windows Presentation Foundation), usare i tipi di carattere del tema. Usare API del tema come DrawThemeText per creare il testo in base al simbolo del tema. Assicurarsi di disporre di un'alternativa basata sulle metriche di sistema nel caso in cui il servizio tema non sia in esecuzione.
-   **Per Segoe UI, utilizzare una dimensione del carattere a 9 punti o superiore.** Il tipo di carattere Segoe UI è ottimizzato per queste dimensioni, quindi evitare di utilizzare dimensioni inferiori.
-   **Corrisponde sempre ai colori del testo del sistema con i colori di sfondo corrispondenti.** Se ad esempio si sceglie COLOR \_ STATICTEXT per il colore del testo, è inoltre necessario scegliere \_ static Color per il colore di sfondo.
-   **Creare sempre nuovi tipi di carattere in base alle varianti proporzionali del tipo di carattere del sistema.** Date le metriche dei tipi di carattere di sistema, è possibile creare variazioni in grassetto, corsivo, dimensioni maggiori e minori.
-   Visualizzazione di grandi blocchi di testo di sola lettura (ad esempio termini di licenza) su uno sfondo chiaro anziché su uno sfondo grigio. Gli sfondi grigi suggeriscono che il testo è disabilitato e sconsiglia la lettura.
-   Prendere in **considerazione una lunghezza di riga massima di 65 caratteri** per semplificare la lettura del testo. I caratteri includono lettere, punteggiatura e spazi.

### <a name="attributes"></a>Attributi

-   La maggior parte del testo dell'interfaccia utente deve essere normale senza attributi. Gli attributi possono essere usati come indicato di seguito:
    -   **Grassetto.** Utilizzare nelle etichette dei controlli per semplificare l'analisi del testo. Per attirare l'attenzione sul testo, gli utenti devono leggere. L'uso di una quantità eccessiva di grassetto ne diminuisce l'effetto.
    -   **Corsivo.** Utilizzare per fare riferimento letteralmente al testo anziché alle virgolette. Usare sporadicamente per evidenziare parole specifiche. Usare per le [richieste](glossary.md) nelle [caselle di testo](ctrl-text-boxes.md) e negli elenchi a [discesa modificabili](/windows/desktop/uxguide/ctrl-drop).
    -   **Corsivo in grassetto.** Non usare.
    -   **Sottolineare.** Non usare ad eccezione dei collegamenti. Usare corsivo invece per l'enfasi.
-   Non tutti i tipi di carattere supportano grassetto e corsivo, quindi non dovrebbero mai essere cruciali per comprendere il testo.

