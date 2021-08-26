---
description: In questo argomento viene descritto Media Foundation trasformazioni devono gestire i timestamp.
ms.assetid: 4ab576ce-becd-4736-921e-e463c0dff841
title: Timestamp e durate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22452e8b6b8094e643126f479f13b2c447db584588f3be1c1aa6595b3e7e2bb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953201"
---
# <a name="time-stamps-and-durations"></a>Timestamp e durate

Questo argomento descrive come le [Media Foundation devono](media-foundation-transforms.md) gestire i timestamp.

Un MFT deve impostare un timestamp e una durata il più accurati possibile in tutti gli esempi di output. Per un MFT semplice che accetta un buffer di input e lo elabora completamente in un buffer di output, MFT deve semplicemente copiare il timestamp e la durata direttamente dall'esempio di input all'esempio di output. Tuttavia, molte trasformazioni sono più complesse di questa e possono richiedere calcoli più complessi del tempo di output. Tutti i MFT devono osservare le regole di base seguenti:

-   Un MFT deve provare a inserire un timestamp e una durata in tutti i campioni di output audio o video non compressi se viene specificato un timestamp accurato o una durata nei campioni di input o può essere calcolato. L'interpolazione può essere necessaria per alcuni timestamp di output, in particolare per i decodificatori.
-   I timestamp e le durate degli esempi di input devono essere mantenuti il più possibile sugli esempi di output.
-   I timestamp o le durate di output potrebbero non corrispondere all'input perché MFT trattene i dati o suddivide l'output in parti di dimensioni diverse rispetto all'input. In tal caso, MFT deve calcolare il timestamp di output dal primo esempio di input che contiene i dati usati per creare l'esempio di output. Per calcolare il timestamp di output, aggiungere il timestamp di input dell'esempio di input appropriato alla durata dei dati già trasformati da tale esempio. Il secondo esempio alla fine di questa sezione illustra questa idea.
-   Se i campioni di input hanno durata, tale durata deve essere mantenuta. Se un campione di input non ha durata, il MFT deve calcolare una durata, se possibile, dalla dimensione del buffer di output o dalla velocità dei dati specificata dal tipo di supporto.
-   Le durate calcolate devono essere troncate (arrotondate per esere arrotondate per e non arrotondate all'incremento più vicino). La pipeline ha un margine di flessibilità sufficiente per gestire durate leggermente imprecise, ma è più facile per la pipeline gestire una durata troppo breve dell'1% rispetto a una durata troppo lunga dell'1%. Detto questo, non c'è alcun motivo per abbreviare intenzionalmente le durate, se non tramite arrotondamento.

### <a name="decoders"></a>Decoder

Un decodificatore converte i pacchetti compressi in dati non compressi. Poiché l'output non è compresso, i decodificatori hanno l'obbligo speciale di ottenere i timestamp e le durate corretti. Alcuni formati compressi, in particolare MPEG-2, non hanno timestamp su tutti i pacchetti di input e spesso non hanno alcuna durata su alcun pacchetto. Per questi formati, il decodificatore è responsabile dell'inserimento di un timestamp e di una durata validi in ogni campione di output sommando le durate implicite di tutto l'output dall'ultimo esempio di input con timestamp.

Per i video, se la durata non è disponibile nel formato compresso, il decodificatore deve calcolare la durata come inversa della frequenza dei fotogrammi, convertita in unità di 100 nanosecondi e arrotondata per esere arrotondata per e per es.

Per l'audio, se la durata non è disponibile nel formato compresso, il decodificatore deve calcolare la durata come inversa della frequenza di campionamento audio moltiplicata per il numero di campioni nel buffer di output, convertita in unità da 100 nanosecondi e arrotondata per esere arrotondata per e per es.

L'unica volta che una trasformazione deve eseguire l'output di un campione senza timestamp è se mFT non ha mai ricevuto un timestamp in un campione di input o se non è possibile calcolare un timestamp di output accurato dal timestamp di input precedente.

### <a name="audio-decoders"></a>Decodificatori audio

Per i decodificatori audio, la durata di ogni campione di output viene calcolata in base alla frequenza di campionamento audio e al numero di campioni PCM per canale nel buffer di output.

Il modo corretto per calcolare i timestamp di output dipende dal fatto che i campioni di input contengano timestamp.

Se gli esempi di input contengono timestamp, il decodificatore calcola i timestamp di output dai timestamp di input, come indicato di seguito:

-   Se ogni buffer di input contiene uno o più frame compressi completi, senza fotogrammi parziali, il timestamp di output è uguale al timestamp di input, meno la latenza nota del decodificatore. Ad esempio, un decodificatore Dolby Digital (AC-3) ha una latenza di 256 campioni PCM. Ad esempio, con una frequenza di campionamento di 48 kHz, la latenza è di 5,33 millisecondi (msec). Pertanto, se il timestamp di input è 1000 msec, il timestamp di output è 1000 – 5,33 = 994,66 msec. Se il buffer di input include più di un intero frame compresso, il decodificatore produrrà un campione di output per ogni frame nell'esempio di input. Tutti gli esempi di output verranno contrassegnati correttamente in modo che non siano presenti lacune.
-   A seconda del formato di trasporto, un buffer di input potrebbe contenere frame parziali. Ad esempio, un buffer potrebbe contenere parte di un frame del buffer di input precedente, seguito da uno o più frame completi, seguiti dall'inizio del frame successivo. In questo caso, è in genere corretto presupporre che il timestamp di input corrisponda al primo frame che inizia all'interno del buffer. Ovvero, un frame parziale avviato nel buffer precedente non è incluso nel timestamp per il buffer corrente. Calcolare il timestamp di output di conseguenza.

Se gli esempi di input non contengono timestamp:

-   Il decodificatore deve generare i propri timestamp, impostando il primo timestamp di output su zero.
-   La durata del campione viene calcolata in base al numero di campioni di output nel buffer e alla frequenza di campionamento.
-   I timestamp successivi vengono calcolati dal timestamp e dalla durata precedenti: timestamp corrente + durata corrente = timestamp successivo. Non devono esserci gap nei timestamp di output.

Se il flusso di input inizialmente contiene timestamp, ma per qualche motivo passa a nessun timestamp, il decodificatore deve continuare a generare i propri timestamp di output, in modo che siano continui e non vi sia alcun gap.

Se il flusso di input contiene timestamp, ma sono presenti lacune nei tempi, il decodificatore semplicemente propaga tali lacune. In altre parole, il decodificatore non deve tentare di correggere timestamp incoerenti nel flusso di input.

### <a name="mixers"></a>Miscelatori

> [!Note]  
> In Windows Vista, la pipeline Media Foundation non supporta MFT con più di un input. I MFT a più input sono supportati in Windows 7.

 

Un mixer accetta più input e li combina in un unico output. Se i flussi di input non sono completamente bloccati o sono leggermente compensati nel tempo l'uno dall'altro, può esserci ambiguità sul momento da impostare nell'output. Di seguito sono riportate alcune linee guida, a seconda del tipo di supporto:

-   Audio. All'avvio o immediatamente dopo uno svuotamento o uno scaricamento, un mixer audio deve attendere di produrre campioni di output fino a quando non riceve un campione di input in tutti i flussi di input necessari. A questo punto, deve scegliere il timestamp meno recente degli esempi iniziali da usare come baseline per i timestamp di output. Gli altri flussi devono essere riempiti di silenzio per creare qualsiasi discrepanza temporale. Se un campione viene ricevuto in un flusso di input facoltativo, è necessario anche eseguire il factored nel calcolo. Da quel momento in poi, MFT deve cercare di produrre una catena continua e ininterrotta di timestamp di output. In generale, MFT non deve cercare di prendere in considerazione la deriva di un flusso rispetto a un altro. Deve invece calcolare i timestamp di output dal timestamp di base, dalla frequenza di output e dalle dimensioni del buffer. Quando si verifica un altro svuotamento o scaricamento, mFT deve reimpostare i timestamp di base.

-   Video. All'avvio o immediatamente dopo uno svuotamento o uno scaricamento, un mixer video deve attendere di produrre campioni di output fino a quando non riceve un campione di input in tutti i flussi di input necessari. A questo punto, deve scegliere il timestamp meno recente degli esempi iniziali da usare come baseline per i timestamp di output. In generale, deve cercare di mantenere timestamp di output continui e regolari e durate fisse, anche se l'input non è regolare, se necessario ripetendo i fotogrammi di input.

### <a name="encoders"></a>Codificatori

Un codificatore converte audio o video non compresso in pacchetti compressi. Un codificatore deve seguire queste linee guida:

-   Il codificatore deve seguire le convenzioni del formato di output. Se il formato in genere non esegue il timestamp per ogni campione, come in MPEG-2, non tutti i campioni di output devono avere un timestamp e una durata.

-   I timestamp di input devono essere mantenuti nel formato di output, se il formato include campi per i timestamp, a meno che informazioni sull'ora migliori non siano disponibili da un'altra origine, ad esempio l'applicazione stessa.

### <a name="multiplexers"></a>Multiplexer

> [!Note]  
> In Windows Vista, la pipeline Media Foundation non supporta MFT con più di un input. I MFT a più input sono supportati in Windows 7.

 

Un multiplexer combina due flussi audio o video diversi in un unico formato interleaved, ad esempio flusso di trasporto AVI o MPEG-2. Un multiplexer deve seguire queste linee guida:

-   Il multiplexer deve seguire le convenzioni del formato di output. Se il formato in genere non esegue il timestamp per ogni campione, come in MPEG-2, non tutti i campioni di output devono avere un timestamp e una durata.

-   Il timestamp deve riflettere l'ora meno recente che verrebbe inserita in qualsiasi fotogramma che inizia in tale pacchetto o l'ora del primo campione audio che verrebbe decodificato da tale pacchetto. Ignorare questa linea guida se è in conflitto con le convenzioni del formato di output.

### <a name="demultiplexers"></a>Demultiplexer

Un demultiplexer suddivide un formato interleaved, ad esempio flusso di trasporto AVI o MPEG-2, nei flussi audio e video sottostanti.

Se il formato contiene informazioni specifiche sul timestamp che possono essere usate per calcolare timestamp di output accurati in base ai timestamp di input, è necessario usare queste informazioni. Tuttavia, se il formato contiene ore in una base completamente diversa che non hanno alcuna relazione con i timestamp di input e non è possibile calcolo di un offset accurato al timestamp di input, gli orari del formato devono essere ignorati.

Se il formato non dispone di informazioni sul timestamp utilizzabili, il demultiplexer deve seguire queste regole:

-   I flussi di output non compressi devono avere timestamp e durate validi, se possibile, calcolati dal timestamp di input precedente più vicino.

-   I flussi di output compressi devono avere timestamp solo nel primo esempio di output derivato da un esempio di input con timestamp. Se l'esempio di input non ha un timestamp, nessun campione di output derivato da tale esempio di input deve avere un timestamp. Se l'esempio di input è suddiviso in più campioni di output, solo il primo esempio di output deve avere un timestamp e il resto non deve avere timestamp.

### <a name="examples"></a>Esempi

Esempio 1. Si supponga che un effetto video accetta sempre un fotogramma di input non compresso, applica l'effetto e lo copia nell'output. Non trattiene mai frame o buffer di input. Questo MFT copia semplicemente il timestamp e la durata dall'esempio di input all'esempio di output, se disponibili, e non esegue alcun calcolo dell'ora.

Esempio 2. Si supponga che un effetto audio trasformi tutti i millisecondi (ms) di ogni buffer di input, risparmiando i 10 ms aggiuntivi da combinare con il buffer successivo. Ottiene un flusso di campioni che hanno tutti una durata di 50 ms. I tempi di input sono indicati nella tabella seguente.



| Esempio | Ora di input | Durata dell'input | Ora di output | Durata dell'output |
|--------|------------|----------------|-------------|-----------------|
| 1      | 20         | 50             | 20          | 40              |
| 2      | 70         | 50             | 60          | 50              |
| 3      | 121        | 50             | 110         | 50              |
| 4      | 171        | 50             | 161         | 50              |



 

Si noti la discrepanza di 1 ms tra la durata effettiva del campione 2 e la durata implicita in base al timestamp successivo (121 ? 70 = 51).

Poiché MFT mantiene 10 ms, restituisce i primi 40 ms dell'esempio di input 1 come esempio di output 1, con un timestamp di 20 ms e una durata di 40 ms.

L'esempio di output 2 combina i 10 ms precedentemente mantenuti con 40 ms dell'esempio di input 2. A questo esempio viene assegnato un timestamp di 60 ms (il timestamp dell'esempio di input precedente, 20 ms, più la durata dei dati già elaborati da tale esempio, 40 ms). Viene data una durata di 50 ms.

Analogamente, l'esempio successivo ha un timestamp di 110 ms (70 ms + 40 ms) con una durata di 50 ms.

Il calcolo successivo è più interessante. Il timestamp implicito dell'ora e della durata di output precedenti sarebbe di 160 ms (timestamp 110 ms + durata 50 ms). Tuttavia, il timestamp di output dovrebbe essere calcolato dal timestamp di input del primo esempio di input che si sovrappone all'esempio di output nel tempo, più la lunghezza dei dati già elaborati da tale campione. L'esempio di input sovrapposto più vicino è il campione 4 (timestamp = 171), ma non è il primo. Il primo campione sovrapposto è il campione 3 (timestamp = 121). Aggiungendo i 40 ms già elaborati da tale esempio, il risultato è 161.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di un MFT personalizzato](writing-a-custom-mft.md)
</dt> </dl>

 

 



