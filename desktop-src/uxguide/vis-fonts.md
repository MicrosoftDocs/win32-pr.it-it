---
title: Tipi di carattere
description: Gli utenti interagiscono con il testo più di qualsiasi altro elemento in Microsoft Windows. Segoe UI (pronunciato \ 0034; SEE-go \ 0034;) è il tipo Windows di sistema. La dimensione del carattere standard è stata aumentata a 9 punti.
ms.assetid: 6d4f669d-d28c-4585-9bc3-ecda44de6df5
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 7ac9f725349433f1cd5f2070b0c80d86acb9d8b3f4d9537cc14375d977283620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119816549"
---
# <a name="fonts"></a>Tipi di carattere

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Gli utenti interagiscono con il testo più di qualsiasi altro elemento in Microsoft Windows. Segoe UI (pronunciato "SEE-go") è il Windows di sistema. La dimensione del carattere standard è stata aumentata a 9 punti.

![Illustrazione dell'alfabeto nel tipo di carattere segoe ui ](images/vis-fonts-image1.png)

Tipo Segoe UI carattere.

Segoe UI e Segoe non sono dello stesso tipo di carattere. Segoe UI è il tipo di carattere Windows destinato alle stringhe di testo dell'interfaccia utente. Segoe è un tipo di carattere di personalizzazione usato da Microsoft e dai partner per produrre materiale per la stampa e la pubblicità.

Segoe UI è un carattere tipografico disponibile, aperto e descrittivo e di conseguenza ha una migliore leggibilità rispetto a Tahoma, Microsoft Sans Serif e Arial. Ha le caratteristiche di un sans serif umanista: le diverse larghezze delle sue maiuscole (E e S, ad esempio, stretta, rispetto a Helvetica, dove le larghezze sono più simili, piuttosto larghe); stress e letterforms della relativa lettera minuscola; e il vero corsivo (anziché un "obliquo" o un romano obliquo, come molti sans serifs dall'aspetto industriale). Il carattere tipografico ha lo stesso effetto visivo sullo schermo e sulla stampa. È stato progettato per essere un sans serif umanista senza carattere forte o distrazione.

Segoe UI è ottimizzato per ClearType, che è on per impostazione predefinita in Windows. Con ClearType abilitato, Segoe UI è un tipo di carattere elegante e leggibile. Senza ClearType abilitato, Segoe UI è solo marginalmente accettabile. Questo fattore determina quando usare Segoe UI.

Segoe UI caratteri latini, greco, cirillico e arabo. Sono disponibili nuovi tipi di carattere, ottimizzati anche per ClearType, creati per altri set di caratteri e utilizzi. Questi includono Meiryo per il giapponese, Malgun Hebrew per il coreano, Microsoft JhengHei per il cinese (tradizionale), Microsoft YaHei per il cinese (semplificato), Gisha per l'ebraico e Leelawadee per il tailandese e i tipi di carattere della raccolta ClearType progettati per l'uso dei documenti.

Meiryo include caratteri latini basati su Verdana. Malgun Gothic, Microsoft JhengHei e Microsoft YaHei usano un Segoe UI. L'uso di versioni in corsivo di questi tipi di carattere non è consigliato. Malgun Gothic, Microsoft JhengHei e Microsoft YaHei vengono forniti solo con stili regolari e in grassetto, vale a dire che i caratteri corsivi vengono sintetizzati mediante la diffusione degli stili eretta. Anche se Meiryo include il corsivo vero e il corsivo grassetto, questi stili si applicano solo ai caratteri latini che i caratteri giapponesi rimangono in posizione verticale quando viene applicato lo stile corsivo.

Una variante di Meiryo, denominata Interfaccia utente di Meiryo, è preferibile nell'interfaccia utente dei [comandi](cmd-ribbons.md) delle barre multifunzione.

Per supportare le impostazioni locali che usano questi set di caratteri, Segoe UI vengono sostituiti con i tipi di carattere corretti a seconda delle impostazioni locali durante il [processo di localizzazione.](glossary.md)

Per ottenere la Segoe UI e altri tipi di carattere Microsoft per la distribuzione con un programma Windows, contattare [Monotype.](https://www.monotype.com/)

**Nota:** Le linee guida relative [allo stile e al tono](text-style-tone.md) e al testo [dell'interfaccia](text-ui.md) utente sono presentate in articoli separati.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="fonts-typefaces-point-sizes-and-attributes"></a>Tipi di carattere, caratteri tipografici, dimensioni dei punti e attributi

Nella tipografia tradizionale, un tipo di carattere descrive una combinazione di un carattere tipografico, una dimensione in punti e attributi. Un carattere tipografico è l'aspetto del tipo di carattere. Segoe UI, Tahoma, Verdana e Arial sono tutti caratteri tipografici. La dimensione in punti si riferisce alla dimensione del carattere, misurata dalla parte superiore degli ascendenti alla parte inferiore dei discendenti, meno la spaziatura interna (detta interlinea). Un punto è circa 1/72 pollice. Infine, un tipo di carattere può avere attributi in grassetto o corsivo.

In modo informale, gli utenti usano spesso il tipo di carattere al posto del carattere tipografico come fatto in questo articolo, ma Segoe UI è un carattere tipografico, non un tipo di carattere. Ogni combinazione di attributi è un tipo di carattere univoco(ad esempio, 9 punti Segoe UI normale, 10 punti Segoe UI grassetto e così via).

### <a name="serif-and-sans-serif"></a>Serif e sans serif

I caratteri tipografici sono serif o sans serif. Serif si riferisce a piccole curve che spesso completano i tratti delle lettere in un tipo di carattere. Un carattere tipografico sans serif non ha serifs.

I lettori preferiscono in genere i tipi di carattere serif usati come corpo del testo all'interno di un documento. I serif offrono un senso di formalità ed eleganza per un documento. Per il testo dell'interfaccia utente, la necessità di un aspetto pulito e la risoluzione inferiore dei monitor del computer rendono i caratteri sans serif la scelta migliore.

### <a name="contrast"></a>Si confronti

Il testo è più semplice da leggere quando esiste una grande differenza tra la luminanza del testo e lo sfondo. Il testo nero su sfondo bianco offre anche il contrasto più elevato di testo scuro su uno sfondo molto chiaro. Questa combinazione è ideale per le superfici principali dell'interfaccia utente.

Il testo chiaro su sfondo scuro offre un buon contrasto, ma non è così buono come il testo scuro su uno sfondo chiaro. Questa combinazione è valida per le superfici secondarie dell'interfaccia utente, ad esempio i riquadri attività di Esplora risorse, che si vuole de-evidenziare rispetto alle superfici principali dell'interfaccia utente.

**Per assicurarsi che gli utenti leggono il testo, usare testo scuro su uno sfondo chiaro.**

### <a name="affordances"></a>Affordances

Il testo può usare [le opzioni seguenti](glossary.md) per indicare come viene usato:

-   **Puntatore.** Il puntatore I-bar ("text select") indica che il testo è selezionabile, mentre il puntatore freccia verso sinistra ("selezione normale") indica che il testo non lo è.
-   **Cursore.** Quando il testo ha lo stato attivo per l'input, il cursore è la barra verticale lampeggiante che indica il punto di inserimento/selezione nel testo selezionabile o modificabile.
-   **Casella.** Casella intorno al testo che indica che è modificabile. Per ridurre il peso della presentazione, la casella può essere visualizzata dinamicamente solo quando è selezionato il testo modificabile.
-   **Colore primo piano.** Grigio chiaro indica che il testo è disabilitato. I colori non grigi, in particolare blu e viola, indicano che il testo è un collegamento.
-   **Colore di sfondo.** Uno sfondo grigio chiaro suggerisce debolmente che il testo è di sola lettura, ma in pratica il testo di sola lettura può avere qualsiasi sfondo a colori.

Questi affordance vengono combinati per i significati seguenti:

-   **Modificabile.** Testo visualizzato in una casella, con un puntatore di selezione del testo, un cursore (sullo stato attivo per l'input) e in genere su uno sfondo bianco.
-   **Sola lettura e selezionabile.** Testo con un puntatore di selezione e un cursore (sullo stato attivo per l'input).
-   **Sola lettura, non selezionabile.** Testo con un puntatore a forma di freccia.
-   **Disabilitati.** Testo grigio chiaro con un puntatore a forma di freccia, talvolta su uno sfondo grigio.

Il testo di sola lettura ha in genere uno sfondo grigio, ma non è necessario uno sfondo grigio. In realtà, uno sfondo grigio può essere indesiderato, soprattutto per blocchi di testo di grandi dimensioni, perché suggerisce che il testo è disabilitato e sconsiglia la lettura.

### <a name="accessibility-and-the-system-font-sizes-and-colors"></a>Accessibilità e tipo di carattere, dimensioni e colori del sistema

Le linee guida per rendere il testo accessibile agli utenti con disabilità o disabilità possono essere ridotte a una semplice regola: Rispettare le impostazioni dell'utente usando sempre il tipo di carattere, le dimensioni e i colori del sistema.

**Se si fa una sola cosa...**

Rispettare le impostazioni dell'utente usando sempre il tipo di carattere, le dimensioni e i colori del sistema.

**Sviluppatori:** Dal codice è possibile determinare le proprietà del carattere di sistema (incluse le dimensioni) usando la funzione API GetThemeFont. È possibile determinare i colori di sistema usando la funzione dell'API GetThemeSysColor.

Poiché non è possibile fare ipotesi sulle impostazioni del tema di sistema degli utenti, è necessario:

-   Basare sempre i colori e gli sfondi dei caratteri nei colori del tema di sistema. Non creare mai colori personalizzati in base a valori RGB fissi (rosso, verde, blu).
-   Abbinare sempre i colori del testo di sistema ai colori di sfondo corrispondenti. Ad esempio, se si sceglie COLOR STATICTEXT come colore del testo, è necessario scegliere \_ ANCHE COLOR STATIC come colore di \_ sfondo.
-   Creare sempre nuovi tipi di carattere in base alle variazioni delle dimensioni proporzionali del tipo di carattere di sistema. Date le metriche dei caratteri di sistema, è possibile creare variazioni grassetto, corsivo, più grandi e più piccole.

**Un modo semplice per garantire che il programma rispetti le impostazioni degli utenti è testare usando una dimensione del carattere diversa e una combinazione di colori a contrasto elevato.** Tutto il testo deve essere ridimensionato e visualizzato correttamente nella combinazione di colori scelta.

## <a name="usage-patterns"></a>Modelli di utilizzo

Il testo ha diversi modelli di utilizzo:



|    Utilizzo                                         |    Descrizione                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Testo per la barra del titolo**<br/> Testo sulla barra del titolo che identifica la finestra.<br/>                                                                                                                                                                | ![Esempio di tipo di carattere per il testo della barra del titolo ](images/vis-fonts-image2.png)<br/>                                                                            |
| **Istruzioni principali**<br/> Testo che illustra le operazione da eseguire in una pagina, una finestra o una finestra di dialogo. <br/>                                                                                                                                              | ![esempio di carattere di testo main-instructions ](images/vis-fonts-image3.png)<br/>                                                                    |
| **Istruzioni secondarie**<br/> Testo supplementare che spiega cosa fare in una pagina, una finestra o una finestra di dialogo. <br/>                                                                                                                            | ![esempio di tipo di carattere testo per istruzioni secondarie ](images/vis-fonts-image4.png)<br/>                                                               |
| **Testo normale**<br/> Testo normale (di sola lettura) visualizzato in un'interfaccia utente. <br/>                                                                                                                                                           | ![Esempio di tipo di carattere normale ](images/vis-fonts-image5.png)<br/>                                                                               |
| **Testo evidenziato**<br/> Il testo in grassetto viene usato per semplificare l'analisi del testo e per attirare l'attenzione sul testo che gli utenti devono leggere. il testo in corsivo viene usato per fare riferimento al testo letteralmente (anziché alle virgolette) e per evidenziare parole specifiche. <br/> | ![Esempio di tipo di carattere del testo evidenziato ](images/vis-fonts-image6.png)<br/>                                                                           |
| **Testo modificabile**<br/> Il testo che gli utenti possono modificare viene visualizzato in una casella. Per ridurre lo spessore della presentazione, la casella può essere visualizzata solo quando è selezionato il testo modificabile. <br/>                                                          | ![esempio di tipo di carattere di testo modificabile ](images/vis-fonts-image7.png)<br/>                                                                             |
| **Testo disabilitato**<br/> Testo che non si applica al contesto corrente, ad esempio le etichette per i controlli disabilitati. il testo disabilitato indica che gli utenti (in genere) non devono leggere il testo. <br/>                                           | ![Esempio di tipo di carattere di testo disabilitato ](images/vis-fonts-image8.png)<br/>                                                                             |
| **Collegamenti**<br/> Testo usato per passare a un'altra pagina, finestra o argomento della Guida oppure per avviare un comando. <br/>                                                                                                                                     | ![Esempio di tipo di carattere del testo del collegamento ](images/vis-fonts-image9.png)<br/> ![esempio di tipo di carattere di testo collegamenti (passaggio del mouse) ](images/vis-fonts-image10.png)<br/> |
| **Intestazione del gruppo**<br/> Testo utilizzato per raggruppare gli elementi in una visualizzazione elenco. <br/>                                                                                                                                                                          | ![Esempio di tipo di carattere di testo intestazione gruppo ](images/vis-fonts-image11.png)<br/>                                                                        |
| **Nome file**<br/> Testo del nome file (solo nella visualizzazione contenuto). <br/>                                                                                                                                                                               | ![esempio di tipo di carattere di testo per il nome del file (nella visualizzazione contenuto) ](images/vis-fonts-image12.png)<br/>                                                         |
| **Testo del documento**<br/> Testo usato nei documenti (a differenza del testo dell'interfaccia utente). <br/>                                                                                                                                                                  | ![esempio di tipo di carattere del testo del documento ](images/vis-fonts-image13.png)<br/>                                                                            |
| **Intestazioni di documento**<br/> Testo utilizzato come intestazione all'interno di un documento. <br/>                                                                                                                                                                    | ![Esempio di carattere di testo delle intestazioni di documento ](images/vis-fonts-image14.png)<br/>                                                                   |



 

## <a name="guidelines"></a>Indicazioni

### <a name="fonts-and-colors"></a>Tipi di carattere e colori

-   **I tipi di carattere e i colori seguenti sono i valori predefiniti Windows Vista e Windows 7.**



| Modello | Simbolo del tema | Tipo di carattere, Colore |
|-----------------------------------------------------------------------------------------------|-----------------------------|------------------------------------------------------------|
| ![Esempio di tipo di carattere per il testo della barra del titolo ](images/vis-fonts-image2.png)<br/>                    | CaptionFont<br/>      | 9 pt. black ( \# 000000) Segoe UI<br/>                 |
| ![esempio di carattere di testo main-instructions ](images/vis-fonts-image3.png)<br/>            | MainInstruction<br/>  | 12 pt. blu \# (003399) Segoe UI<br/>                 |
| ![esempio di tipo di carattere testo per istruzioni secondarie ](images/vis-fonts-image4.png)<br/>       | Istruzione<br/>      | 9 pt. black ( \# 000000) Segoe UI<br/>                 |
| ![Esempio di tipo di carattere normale ](images/vis-fonts-image5.png)<br/>                       | BodyText<br/>         | 9 pt. black ( \# 000000) Segoe UI<br/>                 |
| ![Esempio di tipo di carattere del testo evidenziato ](images/vis-fonts-image6.png)<br/>                   | BodyText<br/>         | 9 pt. nero ( \# 000000) Segoe UI, grassetto o corsivo<br/> |
| ![esempio di tipo di carattere di testo modificabile ](images/vis-fonts-image7.png)<br/>                     | BodyText<br/>         | 9 pt. nero ( \# 000000) Segoe UI, in una casella<br/>       |
| ![Esempio di tipo di carattere di testo disabilitato ](images/vis-fonts-image8.png)<br/>                     | Disabled<br/>         | 9 pt. grigio scuro \# (323232) Segoe UI<br/>             |
| ![Esempio di tipo di carattere del testo del collegamento ](images/vis-fonts-image9.png)<br/>                         | HyperLinkText<br/>    | 9 pt. blue ( \# 0066CC) Segoe UI<br/>                  |
| ![esempio di tipo di carattere di testo collegamenti (passaggio del mouse) ](images/vis-fonts-image10.png)<br/>               | Accesso frequente<br/>              | 9 pt. blu chiaro \# (3399FF) Segoe UI<br/>            |
| ![Esempio di tipo di carattere di testo intestazione gruppo ](images/vis-fonts-image11.png)<br/>                |                             | 11 pt. blu \# (003399) Segoe UI<br/>                 |
| ![esempio di tipo di carattere di testo per il nome del file (nella visualizzazione contenuto) ](images/vis-fonts-image12.png)<br/> |                             | 11 pt. black ( \# 000000) Segoe UI<br/>                |
| ![esempio di tipo di carattere del testo del documento ](images/vis-fonts-image13.png)<br/>                    | (nessuna)<br/>           | 9 pt. black ( \# 000000) Calibri<br/>                  |
| ![Esempio di carattere di testo delle intestazioni di documento ](images/vis-fonts-image14.png)<br/>           | (nessuna)<br/>           | 17 pt. black ( \# 000000) Calibri<br/>                 |



 

-   **Scegliere i tipi di carattere e ottimizzare i layout delle finestre in base alla tecnologia dell'interfaccia utente e alla versione di destinazione Windows:**



| Tecnologia dell'interfaccia utente | Versione Windows destinazione | Tipi di carattere da usare e ottimizzare |
|--------------------------------------------|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Presentation Foundation<br/> | Tutti<br/>                                        | Usare parti del tema WPF.<br/>                                                                                                                                                                                                                                                                                                                                  |
| Win32 o WinForms<br/>               | Windows Vista o versioni successive<br/>                     | Usare il tipo di Segoe UI appropriato.<br/>                                                                                                                                                                                                                                                                                                                    |
|                                            | Componenti estendibili o pre-Windows Vista<br/> | Per impostare come destinazione Windows XP e Windows 2000, usare lo pseudo carattere MS Shell Dlg 2 a 8 punti, mappato a Tahoma.<br/> Per le versioni precedenti di Windows, usare lo pseudo carattere MS Shell Dlg a 8 punti, mappato a Tahoma in Windows 2000 e Windows XP e a MS Sans Serif in Windows 95, Windows 98, Windows Millennium Edition e Windows NT 4.0.<br/> |



 

-   **Gli sviluppatori:**
    -   Per gli elementi che usano un layout fisso (ad esempio Windows di dialogo e WinForms), imposta come hard code il tipo di carattere appropriato della tabella precedente.
    -   Per gli elementi che usano il layout dinamico (ad esempio Windows Presentation Foundation), usare i tipi di carattere del tema. Usare API del tema come DrawThemeText per disegnare testo in base al simbolo del tema. Assicurarsi di avere un'alternativa basata sulle metriche di sistema nel caso in cui il servizio del tema non sia in esecuzione.
-   **Per Segoe UI, usare una dimensione del carattere di 9 punti o superiore.** Il Segoe UI tipo di carattere è ottimizzato per queste dimensioni, quindi evitare di usare dimensioni più piccole.
-   **Abbinare sempre i colori del testo di sistema ai colori di sfondo corrispondenti.** Ad esempio, se si sceglie COLOR STATICTEXT come colore del testo, è necessario scegliere \_ anche COLOR STATIC come colore di \_ sfondo.
-   **Creare sempre nuovi tipi di carattere in base a variazioni di dimensioni proporzionali del tipo di carattere di sistema.** Data la metrica del tipo di carattere di sistema, è possibile creare varianti grassetto, corsivo, più grande e più piccolo.
-   Visualizzare blocchi di testo di sola lettura di grandi dimensioni,ad esempio le condizioni di licenza, su uno sfondo chiaro anziché su uno sfondo grigio. Gli sfondi grigi suggeriscono che il testo è disabilitato e sconsiglia la lettura.
-   **Prendere in considerazione una lunghezza massima di riga di 65 caratteri** per semplificare la lettura del testo. I caratteri includono lettere, punteggiatura e spazi.

### <a name="attributes"></a>Attributi

-   La maggior parte del testo dell'interfaccia utente deve essere normale senza attributi. Gli attributi possono essere usati come segue:
    -   **Grassetto.** Usare nelle etichette dei controlli per semplificare l'analisi del testo. Usare con parsimonio per attirare l'attenzione sul testo che gli utenti devono leggere. L'uso di un formato troppo grassetto ne ne ha meno effetto.
    -   **Corsivo.** Usare per fare riferimento al testo letteralmente anziché virgolette. Usare con parsimonio per evidenziare parole specifiche. Usare per [le richieste nelle](glossary.md) [caselle di testo](ctrl-text-boxes.md) e negli elenchi a discesa [modificabili](/windows/desktop/uxguide/ctrl-drop).
    -   **Corsivo grassetto.** Non usare.
    -   **Sottolineare.** Non usare ad eccezione dei collegamenti. Usare invece il corsivo per l'enfasi.
-   Non tutti i tipi di carattere supportano il grassetto e il corsivo, quindi non dovrebbero mai essere fondamentali per comprendere il testo.

