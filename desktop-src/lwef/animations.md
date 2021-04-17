---
title: Animazioni
description: Animazioni
ms.assetid: 8bd9ac94-3f86-4168-bf33-7a2c8d11907d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf1b9f5e8daa320390f5c19c3c4c27cb8195a8fe
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104558682"
---
# <a name="animations"></a>Animazioni

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Le animazioni di un carattere riflettono il sesso, l'età, la personalità e il comportamento. Il numero e i tipi di animazioni creati per un carattere dipendono da ciò che fa il carattere e da come risponde a situazioni diverse.

Analogamente alle animazioni tradizionali, le animazioni digitali comportano la creazione di una serie di immagini leggermente diverse che, quando vengono visualizzate in sequenza, offrono l'illusione dell'azione. La creazione di immagini di animazione di alta qualità può richiedere un animatore esperto, ma lo stile e la presentazione del carattere creato influiscono anche sulla qualità. I caratteri bidimensionali con forme e funzionalità semplici possono a volte essere efficaci come (o più effettivi) caratteri con rendering elevato. Non è necessario creare un'immagine realistica per rappresentare un carattere effettivo. Molti dei cartoni animati più diffusi non sono realistici nella presentazione, ma sono efficaci perché l'animatore capisce come dare un'azione ed emozioni. L'appendice fornisce informazioni generali sui principi di progettazione dell'animazione di base.

### <a name="frames"></a>Frame

Ogni animazione creata per un carattere Microsoft Agent è costituita da una sequenza di frame temporizzata. Ogni frame nell'animazione è costituito da una o più immagini bitmap. Le immagini possono essere minime quanto necessario o grandi dimensioni del frame stesso.

È possibile includere come immagini aggiuntive per il frame i dettagli relativi all'animazione, ad esempio l'occhio o il movimento del dito. È possibile sovrapporre diverse immagini per creare un oggetto composito e variare la loro posizione nei livelli. Questa tecnica consente di riutilizzare le immagini in più frame e di variare i dettagli che cambiano. Ad esempio, se si desidera disporre di un carattere Wave, per ogni fotogramma è possibile utilizzare un'immagine di base con tutti gli elementi, tranne la mano, e sovrapporre l'immagine di base a un'immagine della mano diversa. Analogamente, se si desidera far lampeggiare il carattere, è possibile sovrapporre un diverso set di occhi su un'immagine di base per ogni fotogramma. Le immagini possono anche essere sfalsate dall'immagine di base. Verrà tuttavia visualizzata solo la parte dell'immagine presente nelle dimensioni del frame.

In un'animazione possono essere presenti tutti i frame desiderati; Tuttavia, un'animazione tipica media circa 14 frame, in modo che riproduca per non più di sei secondi. Questo periodo di tempo modesto garantisce che il carattere appaia reattivo per l'input dell'utente. Inoltre, maggiore è il numero di frame, più grande è il file di animazione. Per i caratteri scaricati basati sul Web, mantenere le dimensioni del file di animazione il più piccolo possibile, pur continuando a fornire un set di frame ragionevolmente dimensionato, in modo che l'animazione del carattere non venga compensata.

### <a name="image-design"></a>Progettazione immagine

È possibile utilizzare qualsiasi strumento di grafica o animazione per creare immagini per i frame di animazione, purché vengano archiviate le immagini finali nella bitmap di Windows (. Formato BMP). Quando le immagini vengono create, utilizzare l'editor dei caratteri di Microsoft Agent (disponibile in [scaricabile](https://www.microsoft.com/download/en/details.aspx?id=14765)) per assemblare, sequenziare e ora le immagini, fornire altre informazioni sui caratteri e compilare tutte le informazioni in un file di caratteri finale.

Le immagini di caratteri devono essere progettate in una tavolozza di colori 256, mantenendo i 20 colori di sistema Windows standard nella posizione standard della tavolozza (le prime 10 e ultime 10 posizioni). Ciò significa che la tavolozza dei colori del carattere può utilizzare i colori di sistema standard e fino a 236 altri colori. Quando si definisce la tavolozza, includere qualsiasi oggetto utilizzato dal carattere nell'animazione. Se la tavolozza del carattere posiziona i colori nelle posizioni dei colori del sistema, i colori dei caratteri verranno sovrascritti con i colori di sistema quando Microsoft Agent creerà la tavolozza.

Maggiore è il numero di colori usati nella tavolozza dei colori di un carattere, maggiore è la possibilità che parte dei colori del carattere venga rimappata per i sistemi configurati in un'impostazione di colore a 8 bit (256). Prendere in considerazione anche l'utilizzo della tavolozza dell'applicazione in cui verrà utilizzato il carattere. È preferibile evitare di rimappare i caratteri dei colori dell'applicazione host e viceversa. Analogamente, se si prevede di supportare più caratteri visualizzati contemporaneamente, è probabile che si desideri mantenere una tavolozza coerente per tali caratteri. È possibile considerare l'uso dei soli colori di sistema standard nel carattere se gli utenti hanno come destinazione una configurazione dei colori a 8 bit. Tuttavia, questo potrebbe non impedire la modifica del mapping del colore del carattere se un'altra applicazione ridefinisce estensivamente la tavolozza dei colori. Nei sistemi impostati su risoluzioni di colore più elevate, la rimappatura della tavolozza dei colori non dovrebbe essere un problema perché il sistema gestisce automaticamente le tavolozze dei colori.

L'uso di un numero maggiore di colori in un'immagine può aumentare anche la dimensione complessiva del file di animazione. Il numero di colori e la frequenza di variazione possono determinare il grado di compressione del file di caratteri. Ad esempio, un carattere bidimensionale che usa solo pochi colori comprimerà meglio di un carattere ombreggiato tridimensionale.

È necessario usare la stessa tavolozza dei colori per l'intero file di caratteri. Non è possibile modificare la tavolozza per animazioni diverse. Se si tenta di supportare le configurazioni dei colori a 8 bit, è consigliabile utilizzare la stessa tavolozza per l'applicazione e qualsiasi altro carattere che si intende supportare.

La posizione<sup>11</sup> nella tavolozza è definita per impostazione predefinita come colore di trasparenza (o alfa), sebbene sia anche possibile impostare il colore utilizzando l'editor dei caratteri di Microsoft Agent. I servizi di animazione di Microsoft Agent eseguono il rendering trasparente di qualsiasi pixel in questo colore, quindi utilizzare il colore nelle immagini solo quando si desidera la trasparenza.

Valutare con attenzione la forma del carattere, perché può influire sulle prestazioni dell'animazione. Per visualizzare il carattere, i servizi animazione creano una finestra area in base all'immagine complessiva. Piccole aree irregolari spesso richiedono più dati dell'area e possono ridurre le prestazioni di animazione del carattere. Pertanto, quando possibile, evitare gap o elementi a singolo pixel e dettagli.

Evitare l'anti-aliasing del bordo esterno del carattere. Sebbene l'anti-aliasing sia una tecnica efficace per ridurre i bordi frastagliati, si basa su colori adiacenti. Poiché il carattere può essere visualizzato sopra una varietà di colori, l'anti-aliasing del perimetro esterno può rendere il carattere non corretto rispetto ad altri sfondi. Tuttavia, è possibile usare l'anti-aliasing nei dettagli interni del carattere senza riscontrare questo problema.

### <a name="frame-size"></a>Dimensioni frame

Le dimensioni del frame non devono essere in genere maggiori di 128 x 128 pixel. Anche se i caratteri possono essere più grandi o più piccoli in una delle due dimensioni, l'editor dei caratteri di Microsoft Agent utilizza questo valore come dimensione di visualizzazione e ridimensiona le immagini dei caratteri se si definisce una dimensione del fotogramma maggiore. La dimensione del fotogramma 128 x 128 costituisce un compromesso ragionevole con lo spazio che il carattere occuperà sullo schermo. L'applicazione può ridimensionare un carattere in fase di esecuzione.

### <a name="frame-duration"></a>Durata frame

È possibile utilizzare l'editor dei caratteri di Microsoft Agent per impostare la durata di visualizzazione di ogni frame di animazione prima del passaggio al frame successivo. Impostare la durata di ogni fotogramma su almeno 10 centesimi di secondo (10 fotogrammi al secondo): qualsiasi valore inferiore potrebbe non essere percettibile in alcuni sistemi. È anche possibile impostare la durata più a lungo, ma evitare pause non naturali nell'azione.

L'editor dei caratteri di Microsoft Agent supporta inoltre la diramazione da un frame in un'animazione a un'altra, in base alle percentuali di probabilità fornite. Per qualsiasi frame specifico, è possibile definire fino a tre rami diversi. La creazione di rami consente di creare animazioni che variano quando vengono riprodotte e animazioni che eseguono il ciclo. Tuttavia, prestare attenzione quando si usa la diramazione perché potrebbe creare problemi quando si tenta di riprodurre un'animazione dopo l'altra. Se, ad esempio, si esegue un'animazione di ciclo o di branching, è possibile continuare per un tempo illimitato a meno che non si usi un metodo [**Stop**](stop-method.md) . In caso di dubbi, evitare la diramazione.

I frame che non hanno immagini e sono impostati su zero Duration non vengono visualizzati quando sono inclusi in un'animazione. È possibile usare questa funzionalità per creare frame che supportano la diramazione senza essere visibili. Tuttavia, verrà visualizzato un frame che non ha ancora immagini con una durata maggiore di zero. Evitare pertanto di includere frame vuoti nell'animazione, perché l'utente potrebbe non essere in grado di distinguere un frame vuoto da quando il carattere è nascosto.

### <a name="frame-transition"></a>Transizione del frame

Quando si progetta un'animazione, valutare la modalità di transizione graduale da e verso l'animazione. Se, ad esempio, si crea un'animazione in cui il carattere si trova a destra e un altro oggetto in cui vengono lasciati i movimenti di carattere, si desidera che il carattere venga animato in modo uniforme da una posizione all'altra. Sebbene sia possibile compilarlo in una delle due animazioni, una soluzione migliore consiste nel definire una posizione neutra o transitoria dalla quale inizia e restituisce il carattere. L'animazione alla posizione neutra può essere incorporata come parte di ogni animazione o come animazione separata. Nell'editor dei caratteri di Microsoft Agent è possibile specificare un'animazione **restituita** complementare per ogni animazione per il carattere. L'animazione **restituita** non deve essere in genere costituita da più di 2-4 frame, quindi il carattere può passare rapidamente alla posizione neutra.

Ad esempio, se si usa lo scenario "gestuale a destra, quindi gestuale a sinistra", è possibile creare un'animazione **GestureRight** , a partire da un frame in cui il carattere viene visualizzato in una posizione neutra e aggiungere frame con immagini che estendono la mano del carattere a destra. Creare quindi la relativa animazione **restituita** : un'animazione complementare con immagini che restituiscono il carattere alla relativa posizione neutra. È possibile assegnare questo oggetto come animazione di ritorno per l'animazione **GestureRight** . Successivamente, creare l'animazione **GestureLeft** che inizia dalla posizione neutra e estende il braccio del carattere a sinistra. Infine, creare un'animazione di **ritorno** complementare anche per questa animazione. Un'animazione **restituita** inizia in genere con un'immagine che segue l'ultima immagine dell'animazione precedente.

L'avvio e la restituzione alla stessa posizione neutra, all'interno di un'animazione o tramite un'animazione return, consentono di riprodurre qualsiasi animazione in qualsiasi ordine. I servizi di animazione Microsoft Agent riproducono automaticamente l'animazione return designata in molte situazioni. Ad esempio, i servizi giocano l'animazione **restituita** designata prima di riprodurre le animazioni di stato minimo del carattere. È consigliabile definire e assegnare animazioni **restituite** se le animazioni non terminano già nella posizione neutra.

Se si desidera fornire transizioni personalizzate tra animazioni specifiche; Poiché, ad esempio, vengono sempre riprodotte in un ordine ben definito, è possibile evitare di definire animazioni di **ritorno** . Tuttavia, è comunque consigliabile iniziare e terminare la sequenza di animazioni dalla posizione neutra.

### <a name="speaking-animation"></a>Animazione vocale

Fornire le immagini della bocca per ogni animazione durante la quale si vuole che il carattere sia in grado di pronunciare, a meno che la progettazione del carattere non abbia una bocca animata o un'indicazione dell'output parlato. In generale, il movimento della bocca è molto importante. Un carattere può sembrare meno intelligente, simpatico o onesto se il suo movimento della bocca non è ragionevolmente sincronizzato con il riconoscimento vocale. Le immagini mouth consentono al carattere di sincronizzare il labbro con l'output parlato. Si definiscono le immagini mouth separatamente e come file bitmap di Windows. Devono corrispondere alla stessa tavolozza dei colori delle altre immagini nell'animazione.

I servizi di animazione dell'agente Microsoft visualizzano i frame di animazione della bocca sopra l'ultimo frame di un'animazione, detto anche *frame di pronuncia* dell'animazione. Ad esempio, quando il carattere parla nell'animazione **GestureRight** , i servizi animazione sovrapposti ai frame di animazione mouth sull'ultimo frame di **GestureRight**. Un carattere non può parlare durante l'animazione, quindi si forniscono solo le immagini della bocca solo per l'ultimo frame di un'animazione. Inoltre, il frame di conversazione deve essere il frame finale di un'animazione, quindi un carattere non può parlare in un'animazione di ciclo.

In genere, è necessario fornire le immagini mouth con le stesse dimensioni del frame e dell'immagine di base, ma includere solo l'area che aggiunge un'animazione come parte del movimento della bocca ed eseguire il rendering del resto dell'immagine nel colore trasparente. Progettare l'immagine in modo che corrisponda all'immagine nel frame di pronuncia quando sovrapposta. Per ottenere una corrispondenza corretta, è probabile che sia necessario creare un set separato di immagini mouth per ogni animazione in cui il carattere parla.

Un'immagine in bocca può includere più di una bocca, ad esempio il mento o altre parti del corpo del carattere mentre parla. Tuttavia, se si sposta una mano o una zampa, si noti che potrebbe sembrare spostata in modo casuale perché la sovrapposizione della bocca visualizzata sarà basata sul fonema corrente di una frase pronunciata. Inoltre, il server Ritaglia l'immagine della bocca al contorno dell'immagine del frame di pronuncia. Progettare l'immagine della sovrapposizione della bocca in modo che rimanga all'interno della struttura dell'immagine del frame di base, perché il server usa l'immagine di base per creare il limite della finestra per il carattere.

L'editor di caratteri Microsoft Agent consente di definire sette posizioni di base per la bocca che corrispondono alle forme della bocca dei fonemi comuni illustrate nella tabella seguente:

**Immagini di animazione mouth**



| Posizione bocca | Immagine di esempio                       | Rappresentazione                                                                                                                     |
|----------------|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| Chiusa         | :::image type="icon" source="images/g07ci01.gif":::<br/> | Forma normale della bocca chiusa. Usato anche per fonemi come "m" come in "mom", "b" come in "Bob", "f" come in "Fife".<br/>           |
| Aperto 1    | :::image type="icon" source="images/g07ci02.gif":::<br/> | La bocca è leggermente aperta, a larghezza intera. Usato per fonemi come "g" come in "bavaglio", "l" come in "pausa", "orecchio" come in "ascolta".<br/> |
| Open-Wide 2    | :::image type="icon" source="images/g07ci03.gif":::<br/> | Mouth è parzialmente aperto, a larghezza intera. Usato per fonemi come "n" come in "Nun", "d" come in "Dad", "t" come in "tot".<br/>    |
| Open-Wide 3    | :::image type="icon" source="images/g07ci04.gif":::<br/> | Mouth è aperto, a larghezza intera. Usato per fonemi come "u" come in "Hut", "EA" come in "Head", "Your" come in "Hurt".<br/>          |
| Open-Wide 4    | :::image type="icon" source="images/g07ci05.gif":::<br/> | Mouth è completamente aperto, a larghezza intera. Usato per fonemi come "a" come in "Hat", "ow" come in "how".<br/>                   |
| Aperto-medio    | :::image type="icon" source="images/g07ci06.gif":::<br/> | La bocca è aperta a metà larghezza. Usato per fonemi come "Oy" come in "Ahoy", "o" come in "Hot".<br/>                              |
| Apertura-stretta    | :::image type="icon" source="images/g07ci07.gif":::<br/> | Mouth è aperto a larghezza ristretta. Usato per fonemi come "o" come in "Hoop", "o" come in "Hope", "w" come in "Wet".<br/>           |



 

 

 





