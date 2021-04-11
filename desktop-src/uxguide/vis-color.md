---
title: Colore
description: Il colore è un elemento visivo importante della maggior parte delle interfacce utente.
ms.assetid: 30a60e9e-ebb4-40f2-8535-a9b58dc668a8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ae58ddf232a3d8311a917ea0475c7aca1bae8949
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104132131"
---
# <a name="color"></a>Colore

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Il colore è un elemento visivo importante della maggior parte delle interfacce utente. Oltre ai puri estetici, Color ha associato significati e suscita risposte emotive. Per evitare confusione nel significato, il colore deve essere utilizzato in modo coerente. Per ottenere le risposte emotive desiderate, è necessario usare il colore in modo appropriato.

Il colore è spesso considerato in termini di spazio di colore, dove RGB (Red, Green, Blue), HSL (Hue, Saturation, luminosità) e HSV (Hue, Saturation, value) sono gli spazi dei colori usati più di frequente.

![Figura di un cubo che mostra le relazioni colori ](images/vis-color-image1.png)

Lo spazio colore RGB può essere visualizzato come cubo.

Sebbene la tecnologia di visualizzazione usi valori RGB e, di conseguenza, gli sviluppatori spesso pensano ai colori in termini di RGB, lo spazio colore RGB non corrisponde al modo in cui le persone percepiscono il colore. Se, ad esempio, si aggiunge il colore rosso al ciano scuro, il risultato non viene percepito come rosso ma come cyan più chiaro.

![illustrazione dei quadratini ciano scuro e chiaro ](images/vis-color-image2.png)

In questo esempio, l'aggiunta di rosso a ciano scuro rende più chiara, non più rossa. Lo spazio colore RGB non corrisponde al modo in cui le persone percepiscono il colore.

Gli spazi dei colori HSL/HSV sono costituiti da tre componenti: tonalità, saturazione e luminosità o valore. Questi spazi dei colori vengono spesso usati al posto di RGB, perché meglio corrispondono al modo in cui le persone percepiscono il colore.

Lo spazio dei colori HSL costituisce un doppio cono che è bianco nella parte superiore, nero in basso e neutro al centro:

-   **Tonalità:** Colore di base nella rotellina dei colori, compreso tra 0 e 360 gradi, in cui i livelli 0 e 360 sono rossi.

    ![Figura di un cerchio che mostra le relazioni dei colori ](images/vis-color-image3.png)

    La rotellina del colore, dove rosso è 0 gradi, il giallo è 60 gradi, il verde è 120 gradi, cyan è 180 gradi, blu è di 240 gradi e magenta è di 300 gradi.

-   **Saturazione:** In che modo pure (vs. Dull) il colore è compreso tra 0 e 100, dove 100 è completamente saturo e 0 è grigio.
-   **Luminosità:** Quanto è chiaro il colore, compreso tra 0 e 100, in cui 100 è il più chiaro possibile (bianco, indipendentemente dalla tonalità e dalla saturazione) e 0 è il più scuro possibile (nero).

    ![figura che illustra lo spazio colore HSL ](images/vis-color-image4.png)

    Lo spazio colore HSL può essere visualizzato come un doppio cono.

Lo spazio colore HSV è simile, ad eccezione del fatto che lo spazio è costituito da un singolo cono:

-   **Tonalità:** Colore di base nella rotellina dei colori, compreso tra 0 e 360 gradi, in cui i livelli 0 e 360 sono rossi.
-   **Saturazione:** In che modo pure (vs. Dull) il colore è compreso tra 0 e 100, dove 100 è completamente saturo e 0 è grigio.
-   **Valore:** Luminosità del colore, da 0 a 100, dove 100 è il più luminoso possibile (ovvero la metà della luminosità nello spazio HSL) e 0 è il più scuro possibile (nero).

    ![figura che illustra lo spazio colore HSV ](images/vis-color-image5.png)

    Lo spazio di colore HSV può essere visualizzato come un singolo cono.

Negli spazi HSL e HSV, se la saturazione è 0, luminosità specifica una sfumatura di grigio. In Windows, gli spazi HSL e HSV vengono in genere rimappati a una scala compresa tra 0 e 240 in modo che i colori possano essere rappresentati con un valore a 32 bit.

**Nota:** Le linee guida relative ai [tipi di carattere](vis-fonts.md) e all' [accessibilità](inter-accessibility.md) sono presentate in articoli distinti.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Un utilizzo efficace dei colori può rendere più efficace l'interfaccia utente del programma. Il colore può aiutare gli utenti a comprendere a colpo d'occhio alcuni significati. Il colore può anche rendere il prodotto più gradevole e raffinato.

Sfortunatamente, è troppo semplice utilizzare il colore in modo non efficiente, soprattutto se non si è esperti di progettazione visiva. Un utilizzo scarso dei colori produce risultati in progettazioni non professionali, datate, confuse o semplicemente orribili. Un uso insufficiente del colore può essere peggiore rispetto a non usare affatto il colore.

In questa sezione vengono illustrate le informazioni necessarie per utilizzare in modo efficace il colore.

### <a name="how-color-is-used"></a>Modalità di utilizzo del colore

Il colore viene in genere usato nell'interfaccia utente per comunicare:

-   **Significato.** Il significato di un messaggio può essere riepilogato tramite il colore. Ad esempio, il colore viene spesso usato per comunicare lo stato in cui il rosso è un problema o un errore, il giallo è attenzione o avviso e il verde è positivo.
-   **Stato.** Lo stato di un oggetto può essere indicato tramite il colore. Ad esempio, Windows utilizza il colore per indicare gli Stati di selezione e di passaggio del mouse. I collegamenti all'interno di pagine Web utilizzano il blu per gli invisitati e i viola per i visitatori.
-   **Differenziazione.** Si presuppone che esista una relazione tra gli elementi dello stesso colore, quindi la codifica a colori è un modo efficace per distinguere gli oggetti. Ad esempio, in un elemento del pannello di controllo, i riquadri attività utilizzano uno sfondo verde per separarli visivamente dal contenuto principale. Microsoft Outlook consente inoltre agli utenti di assegnare flag colorati diversi ai messaggi.
-   **Enfasi.** Il colore può essere usato per attirare l'attenzione degli utenti. Ad esempio, Windows usa [le istruzioni principali](text-ui.md) blu per distinguerle dall'altro testo.

Naturalmente, il colore viene spesso usato nella grafica per motivi puramente estetici. Mentre le estetiche sono importanti, è consigliabile scegliere i colori degli elementi dell'interfaccia utente principalmente in base al significato e non al modo in cui appaiono.

### <a name="color-interpretation"></a>Interpretazione colori

**L'interpretazione dei colori degli utenti è spesso dipendente dalla cultura.** Nel Stati Uniti, ad esempio, l'Abbigliamento nuziale per la sposa è in gran parte associato al colore bianco, mentre il nero è associato a funerali. Tuttavia, molto tempo fa in Giappone, il simbolismo dei colori era solo il contrario: il bianco era il colore predominante ai funerali e il nero era considerato un colore che offre una buona fortuna per i matrimoni.

Detto questo, **l'interpretazione di rosso, giallo e verde per lo stato è coerente a livello globale.** Questa condizione è dovuta alla [convenzione di Vienna UNESCO sui segnali stradali e sui segnali](https://www.unece.org/trans/conventn/signalse.pdf), che definisce la convenzione globale per le spie di traffico (dove il colore rosso indica l'arresto, il significato verde continua e il giallo significa procedere con cautela). Questi colori di stato possono essere usati senza preoccupazioni per interpretazioni dipendenti dalle impostazioni cultura.

Oltre ai colori di stato, Windows assegna significati ai colori in base alla convenzione, come illustrato nella sezione linee guida di questo articolo. Assicurarsi che l'utilizzo dei colori del programma sia compatibile con le convenzioni dei colori.

### <a name="color-accessibility"></a>Accessibilità colori

L'uso del colore influiscono sull'accessibilità del software al più ampio pubblico possibile. Gli utenti con ipovisione o ipovisione potrebbero non essere in grado di visualizzare i colori. Circa l'8% dei maschi adulti ha una forma di confusione dei colori (spesso definita in modo non corretto come "daltonismo"), di cui la confusione dei colori rosso-verde è la più comune.

![figura che mostra i colori primari come visualizzato normalmente ](images/vis-color-image6.png)

Colori primari, come illustrato con la normale visione del colore.

![figura che Mostra gli stessi colori visualizzati con protanopia ](images/vis-color-image7.png)

Colori primari visualizzati con protanopia (1% di popolamento maschile).

![figura che Mostra gli stessi colori visualizzati con Deuteranopia ](images/vis-color-image8.png)

I colori primari visualizzati con Deuteranopia (6% del popolamento maschile).

![figura che Mostra gli stessi colori visualizzati con tritanopia ](images/vis-color-image9.png)

Colori primari visualizzati con Tritanopia (1% di popolamento maschile).

Per ulteriori informazioni, vedere [Color-Blind gli utenti possono visualizzare il sito?](/previous-versions/windows/internet-explorer/ie-developer/)

### <a name="use-color-to-reinforce-visually"></a>Usare il colore per rafforzare visivamente

La soluzione migliore per l'interpretazione dei colori e i problemi di accessibilità consiste nell'usare il colore per rafforzare visivamente il significato di uno di questi metodi di comunicazione principali:

-   **Testo** Il testo conciso è in genere la comunicazione principale più efficace direttamente nell'interfaccia utente o tramite una descrizione comando.

![Screenshot di una piccola icona rossa con descrizione comando ](images/vis-color-image10.png)

In questo esempio viene usato il testo della descrizione comando per comunicare il significato di un'icona.

-   **Design.** Le icone sono facilmente distinguibili dalle progettazioni, soprattutto dalla relativa forma di struttura.

![screenshot delle icone con sfumature di grigio (scala di grigi) ](images/vis-color-image11.png)

In questo esempio, le icone standard sono facilmente distinguibili in base alle rispettive progettazioni.

-   **Percorso.** È anche possibile usare la posizione relativa, ma questo approccio è più debole rispetto alle alternative. Per essere efficace, il percorso deve essere standard e ben noto, come per i semafori.

Mentre color è l'attributo più ovvio di molti progetti, deve sempre essere ridondante.

### <a name="designing-with-color"></a>Progettazione con colore

Ironicamente, il modo migliore per progettare il colore è iniziare progettando senza colore, usando [wireframe](glossary.md) o monocromatico, quindi aggiungere il colore in un secondo momento. In questo modo si garantisce che le informazioni non vengano comunicate solo con il colore. Consente inoltre di verificare che le stampe risultino ottimali sulle stampanti monocromatiche.

### <a name="use-theme-or-system-colors"></a>USA tema o colori di sistema

Sebbene esistano molti fattori complessi nell'utilizzo efficace dei colori, nell'interfaccia utente di Windows la scelta del colore spesso si riduce per scegliere semplicemente il colore del [tema](glossary.md) appropriato o il [colore di sistema](glossary.md) secondo alcune semplici regole. Gli utenti possono quindi selezionare e personalizzare queste combinazioni di colori come scelgono.

In questo modo, non solo si è in grado di soddisfare le preferenze di colore di tutti gli utenti, ma si elimina il carico di scelta della combinazione di colori perfetta che funziona per tutti i gusti, gli stili e le impostazioni cultura (che, ovviamente, è altrimenti impossibile).

**Se si esegue una sola operazione...**

Scegliere colori selezionando il colore del tema appropriato o il colore di sistema. Non usare mai il colore come metodo principale di comunicazione, ma come metodo secondario per rinforzare il significato visivamente. Progettare utilizzando wireframe o monocromatico per garantire che il colore sia secondario.

### <a name="use-theme-or-system-colors-correctly"></a>Usare i colori del tema o del sistema correttamente

Si supponga che gli utenti scelgano i colori del tema o del sistema in base alle esigenze personali e che i colori del tema o del sistema siano costruiti in modo appropriato. In base a questo presupposto, se si scelgono sempre i colori del tema o del sistema in base allo scopo previsto e si abbinano i primi primi a quelli associati, i colori sono sicuramente leggibili e rispettano i desideri degli utenti in tutte le modalità video, inclusa la [modalità a contrasto elevato](glossary.md). Il colore di sistema del testo della finestra, ad esempio, è sicuramente leggibile rispetto al colore del sistema di sfondo della finestra.

In particolare, sempre:

-   **Scegliere i colori in base al loro scopo.** Non scegliere i colori in base all'aspetto corrente perché l'aspetto può essere modificato dall'utente o dalle versioni future di Windows.
-   **Corrisponde ai colori di primo piano con i colori di sfondo associati.** I colori di primo piano sono sicuramente leggibili solo per i colori di sfondo associati. Non combinare e abbinare i colori di primo piano con altri colori di sfondo o ancora peggiori, altri colori di primo piano.
-   **Non combinare tipi di colori.** Ovvero, sempre corrispondono ai colori del tema con i colori del tema associati, i colori di sistema con i colori di sistema associati e i colori cablati con altri colori cablati. Ad esempio, non è garantito che il colore del testo del tema sia leggibile rispetto a uno sfondo cablato.
-   **Se è necessario hardwire i colori, gestire la modalità a contrasto elevato come caso speciale.**

**Se si esegue una sola operazione...**

Scegliere sempre i colori del tema o del sistema in base allo scopo designato e abbinare i primili ai propri sfondi associati.

### <a name="using-other-colors"></a>Uso di altri colori

Mentre il tema di Windows definisce un set completo di parti del tema, è possibile che il programma richieda colori che non sono definiti nel file di tema. Sebbene sia possibile hardwire tali colori, un approccio migliore consiste nel derivare i colori dal tema o dai colori di sistema. L'uso strategico di questo approccio offre tutti i vantaggi derivanti dall'uso dei colori del tema e del sistema, ma con una maggiore flessibilità.

Si supponga, ad esempio, che sia necessario uno sfondo della finestra più scuro del colore di sfondo della finestra del tema. Nello spazio dei colori HSL, un colore più scuro indica un colore con una luminosità inferiore. Pertanto, è possibile derivare un colore di sfondo della finestra più scura usando i passaggi seguenti:

-   Ottenere il colore RGB del tema dello sfondo della finestra.
-   Converte l'oggetto RGB nel relativo valore HSL.
-   Ridurre il valore di luminosità (per, ad indicare, 20%).
-   Eseguire di nuovo la conversione in valori RGB.

Con questo approccio, il colore derivato viene sicuramente percepito come una sfumatura più scura del colore originale (a meno che il colore originale non fosse molto scuro per iniziare).

![illustrazione che Mostra gli effetti della luminosità ridotta ](images/vis-color-image12.png)

In questo esempio, il colore di sfondo di una finestra più scura deriva dal colore del tema.

### <a name="testing-colors"></a>Test di colori

Per determinare se l'uso del colore del programma è accessibile e non usato come metodo di comunicazione principale, è consigliabile usare le utilità [Fujitsu ColorDoctor](https://www.fujitsu.com/global/about/businesspolicy/tech/design/) o [Vischeck](https://www.vischeck.com/) per verificare quanto segue:

-   Dipendenza complessiva dal colore con il filtro della scala di grigi.
-   Problemi di confusione dei colori specifici con i filtri protanopia, deuteranopia e tritanopia.

Per determinare se l'uso del colore del programma è stato programmato correttamente, testare il programma nelle modalità seguenti:

-   Temi abilitati con il tema predefinito di Windows.
-   Il tema è abilitato utilizzando un tema non predefinito.
-   Tema disabilitato ("stile classico di Windows" nelle impostazioni del tema nell'elemento del pannello di controllo della personalizzazione).
-   Contrasto elevato nero (testo bianco su sfondo nero).
-   Contrasto elevato bianco (testo nero in uno sfondo bianco).

Tutti gli elementi della schermata devono essere leggibili e vengono visualizzati come previsto, anche immediatamente dopo la modifica della modalità.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Non usare mai il colore come metodo principale di comunicazione,** ma come metodo secondario per rinforzare il significato visivamente.

### <a name="using-theme-and-system-colors"></a>Uso del tema e colori di sistema

-   Quando possibile, **scegliere colori selezionando il colore del tema appropriato o il colore di sistema.** In questo modo, è sempre possibile rispettare le preferenze di colore degli utenti.
-   **Scegliere tema e colori di sistema in base al loro scopo.** Non scegliere i colori in base all'aspetto corrente, in quanto tale aspetto può essere modificato dall'utente o dalle versioni future di Windows.
-   **Corrisponde ai colori di primo piano con i colori di sfondo associati.** I colori di primo piano sono sicuramente leggibili solo per i colori di sfondo associati. Non combinare e abbinare i colori di primo piano con altri colori di sfondo o ancora peggiori, altri colori di primo piano.
-   **Non combinare tipi di colori.** Ovvero, sempre corrispondono ai colori del tema con i colori del tema associati, i colori di sistema con i colori di sistema associati e i colori cablati con altri colori cablati. Ad esempio, non è garantito che il colore del testo del tema sia leggibile rispetto a uno sfondo cablato.
-   **Se è necessario usare un colore che non sia un tema o un colore di sistema:**
    -   **Preferisce derivare il colore da un tema o da un colore di sistema su cablatura il relativo valore.** Usare il processo descritto in precedenza in questo articolo, in uso di altri colori.
    -   **Gestire la modalità a contrasto elevato come caso speciale.**
-   **Gestire le modifiche del tema.** Le modifiche del tema vengono gestite automaticamente da Windows con frame e controlli comuni della finestra standard. Windows con frame di finestra personalizzati, controlli personalizzati o di personalizzazione del proprietario e altro uso del colore devono gestire le modifiche del tema in modo esplicito.
    -   **Sviluppatori:** È possibile rispondere agli eventi di modifica del tema gestendo il \_ messaggio WM THEMECHANGED.

### <a name="color-meaning"></a>Significato colore

-   Anche se è consigliabile usare i colori del tema e del sistema (o i colori derivati) ogni volta che è possibile, assicurarsi che qualsiasi altro uso di colore sia compatibile con l'uso del colore seguente all'interno di Windows.



|                                      |                                                                               |                                                                                                                                                                 |
|--------------------------------------|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hue**<br/>                   | **Significato**<br/>                                                        | **Utilizzo in Windows**<br/>                                                                                                                                   |
| blu/verde<br/>                | Marchio Windows<br/>                                                      | Background: personalizzazione di Windows.<br/>                                                                                                                        |
| Glass, black, Gray, White<br/> | neutrale<br/>                                                            | Background: frame della finestra standard, menu Start, barra delle applicazioni, barra laterale.<br/> Foreground: testo normale.<br/>                                                |
| blue<br/>                      | avvio, commit<br/>                                                      | Background: pulsanti di comando predefiniti, ricerca, accesso.<br/> Icone: informazioni, guida.<br/> Primo piano: istruzioni principali, collegamenti.<br/>           |
| rosso<br/>                       | errore, arresto, vulnerabile, critico, attenzione immediata, con restrizioni<br/> | Background: stato, stato interrotto (indicatori di stato).<br/> Icone: errore, arresto, chiusura della finestra, eliminazione, input obbligatorio, mancante, non disponibile.<br/>     |
| yellow<br/>                    | avviso, attenzione, discutibile<br/>                                     | Background: stato, stato in pausa (indicatori di stato).<br/> Icone: avviso<br/>                                                                       |
| green<br/>                     | Go, procedere, avanzamento, sicuro<br/>                                        | Background: stato, stato normale (indicatori di stato).<br/> Icone: go, done, Refresh.<br/> Foreground: percorsi e URL (nei risultati della ricerca).<br/> |
| purple<br/>                    | visitato<br/>                                                            | Primo piano: collegamenti visitati (per i collegamenti all'interno di Windows Internet Explorer e documenti).<br/>                                                                |



 

-   **Per evitare di comunicare i significati precedenti, scegliere i colori hanno una saturazione elevata a metà e bassa e luminosità alta o bassa.** Gli utenti associano i significati precedenti a colori con saturazione completa o elevata e luminosità di livello intermedio, quindi è possibile evitare queste associazioni scegliendo diverse sfumature.

![figura che illustra l'effetto della luminosità sul colore ](images/vis-color-image13.png)

In questo esempio, sono disponibili tre diverse gradazioni di colore giallo, ma solo la tonalità di luminosità di livello intermedio e a elevata saturazione comunica un avviso. L'icona della cartella gialla non sembra essere un avviso.

### <a name="using-color-with-data"></a>Uso del colore con i dati

-   Se utile, **assegnare il colore ai dati per consentire agli utenti di differenziarlo.** Si noti che gli utenti presumeranno che i dati con colori simili abbiano significati simili.
-   **Per impostazione predefinita, assegnare colori facili da distinguere.** In genere, i colori sono semplici da distinguere se sono lontani tra loro negli spazi dei colori HSL/HSV, mantenendo al contempo un contrasto elevato con lo sfondo:
    -   Quando si scelgono i colori, preferire le armonie Triad o le tonalità complementari, ma non le tonalità adiacenti.

        ![figura che illustra come scegliere colori a contrasto ](images/vis-color-image14.png)

        In questo esempio, se la prima assegnazione di colore è rossa, il colore successivo deve essere blu, verde o ciano, ma non magenta, viola, arancione o giallo.

    -   I colori presentano un contrasto elevato se c'è una grande differenza nella tonalità, saturazione o luminosità.

        ![figura che mostra un colore in background diversi ](images/vis-color-image15.png)

        In questo esempio, il colore di base blu chiaro è in contrasto con gli sfondi con grandi differenze di tonalità, saturazione o luminosità.

    -   L'uso di uno sfondo bianco o molto chiaro rende più semplice distinguere i colori di primo piano.

        ![figura che illustra un contrasto positivo e scarso ](images/vis-color-image16.png)

        In questo esempio, i colori di sfondo bianco e chiaro rendono più semplice distinguere il colore di primo piano.

-   **Consente agli utenti di personalizzare queste assegnazioni di colori** perché la scelta dei colori è soggettiva e una preferenza personale. Se sono presenti molti colori coordinati, consentire agli utenti di modificarli come gruppo utilizzando combinazioni di colori.
-   **Consente agli utenti di etichettare queste assegnazioni di colori.** Questo consente di semplificare l'identificazione e la ricerca.
-   **A differenza dei colori dell'interfaccia utente, i dati non devono essere modificati quando cambiano i colori di sistema.**

## <a name="documentation"></a>Documentazione

-   **Fare riferimento agli elementi dell'interfaccia utente in base ai relativi nomi, non in base ai relativi colori.** Tali riferimenti non sono accessibili e i colori del sistema possono cambiare. Se il nome di un elemento dell'interfaccia utente non è noto o non è sufficientemente descrittivo, visualizzare uno screenshot da chiarire.

**Corretto:**

![screenshot del messaggio contenente la barra informazioni ](images/vis-color-image17.png)

**Non corretto:**

![screenshot del messaggio contenente ' Gold Bar ' ](images/vis-color-image18.png)

Nell'esempio errato, il messaggio fa riferimento alla barra informazioni di Windows Internet Explorer in base al relativo colore anziché al nome.

