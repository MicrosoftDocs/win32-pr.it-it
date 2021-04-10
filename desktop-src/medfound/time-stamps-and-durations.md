---
description: In questo argomento viene descritto il modo in cui Media Foundation le trasformazioni devono gestire i timestamp.
ms.assetid: 4ab576ce-becd-4736-921e-e463c0dff841
title: Timestamp e durate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2323c11fa0e3ec2b2b2d5ba1cefe4f5d5fa80c5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130466"
---
# <a name="time-stamps-and-durations"></a>Timestamp e durate

In questo argomento viene descritto il modo in cui [Media Foundation le trasformazioni](media-foundation-transforms.md) devono gestire i timestamp.

Per tutti gli esempi di output, una MFT deve impostare un timestamp accurato e una durata più lunga possibile. Per una semplice MFT che accetta un buffer di input e lo elabora completamente in un buffer di output, il MFT dovrebbe semplicemente copiare il timestamp e la durata direttamente dall'esempio di input all'esempio di output. Tuttavia, molte trasformazioni sono più complesse di questo e possono richiedere calcoli più complessi del tempo di output. Tutti MFTs devono rispettare le regole di base seguenti:

-   Una MFT dovrebbe provare a inserire un timestamp e una durata su tutti i campioni di output video o audio non compressi se viene fornita una durata o un timestamp accurato per gli esempi di input oppure può essere calcolato. L'interpolazione potrebbe essere necessaria per alcuni timestamp di output, specialmente per i decodificatori.
-   Gli indicatori temporali e le durate degli esempi di input devono essere conservati per quanto possibile negli esempi di output.
-   Gli indicatori temporali o le durate di output potrebbero non corrispondere all'input perché il MFT trattiene i dati o suddivide l'output in parti di dimensioni diverse rispetto all'input. In tal caso, la MFT dovrebbe calcolare il timestamp di output del primo esempio di input che contiene i dati usati per creare l'esempio di output. Per calcolare il timestamp di output, aggiungere il timestamp di input dell'esempio di input appropriato alla durata dei dati che sono già stati trasformati dall'esempio. Nel secondo esempio alla fine di questa sezione viene illustrato questo concetto.
-   Se gli esempi di input hanno una durata, tale durata deve essere mantenuta. Se un esempio di input non ha durata, il file MFT deve calcolare una durata, se possibile, a partire dalla dimensione del buffer di output o dalla velocità dati fornita dal tipo di supporto.
-   Le durate calcolate devono essere troncate (arrotondate per difetto), non arrotondate all'incremento più vicino. La pipeline è sufficientemente lenta per gestire le durate leggermente inesatte, ma è più facile per la pipeline gestire una durata pari a 1% troppo breve rispetto a una durata pari all'1% troppo lunga. Detto questo, non esiste alcun motivo per abbreviare deliberatamente le durate, a parte l'arrotondamento.

### <a name="decoders"></a>Decodificatori

Un decodificatore converte i pacchetti compressi in dati non compressi. Poiché l'output non è compresso, i decodificatori hanno un obbligo speciale di ottenere i timestamp e le durate corrette. Alcuni formati compressi, in particolare MPEG-2, non hanno timestamp su tutti i pacchetti di input e spesso non hanno durata in alcun pacchetto. Per questi formati, il decodificatore è responsabile dell'inserimento di un timestamp e di una durata validi per ogni esempio di output, sommando le durate implicite di tutti gli output dall'ultimo campione di input con timestamp.

Per video, se la durata non è disponibile nel formato compresso, il decodificatore deve calcolare la durata come inverso della frequenza dei fotogrammi, convertita in unità di 100 nanosecondi e arrotondata per difetto.

Per audio, se la durata non è disponibile nel formato compresso, il decodificatore deve calcolare la durata come l'inverso della frequenza di campionamento audio moltiplicata per il numero di campioni nel buffer di output, convertita in unità di 100 nanosecondi e arrotondato per difetto.

L'unico momento in cui una trasformazione deve restituire un campione senza un timestamp è se il MFT non ha mai ricevuto un timestamp per un esempio di input o se non è possibile calcolare un timestamp di output accurato dal timestamp di input precedente.

### <a name="audio-decoders"></a>Decodificatori audio

Per i decodificatori audio, la durata di ogni campione di output viene calcolata in base alla frequenza di campionamento audio e al numero di campioni PCM per canale nel buffer di output.

Il modo corretto per calcolare i timestamp di output varia a seconda che gli esempi di input contengano timestamp.

Se gli esempi di input contengono timestamp, il decodificatore calcola i timestamp di output dagli indicatori temporali di input, come indicato di seguito:

-   Se ogni buffer di input contiene uno o più frame compressi completi, senza frame parziali, il timestamp di output è uguale al timestamp di input, meno la latenza nota del decodificatore. Un decodificatore Dolby Digital (AC-3), ad esempio, ha una latenza di 256 campioni PCM. Ad esempio, alla frequenza di campionamento 48-kHz, la latenza è 5,33 millisecondi (msec). Se pertanto il timestamp di input è 1000 msec, il timestamp di output è 1000 – 5,33 = 994,66 msec. Se il buffer di input include più di un intero frame compresso, il decodificatore produrrà un esempio di output per ogni frame nell'esempio di input. Tutti gli esempi di output avranno un timestamp corretto in modo che non vi siano Gap.
-   A seconda del formato di trasporto, un buffer di input può contenere frame parziali. Un buffer, ad esempio, può contenere parte di un frame dal buffer di input precedente, seguito da uno o più frame completi, seguiti dall'inizio del frame successivo. In questo caso, in genere è corretto presumere che il timestamp di input corrisponda al primo frame che inizia all'interno del buffer. Ovvero, un frame parziale avviato nel buffer precedente non è incluso nel timestamp per il buffer corrente. Calcolare di conseguenza il timestamp di output.

Se gli esempi di input non contengono alcun timestamp:

-   Il decodificatore deve generare i propri timestamp, impostando il primo timestamp di output su zero.
-   La durata del campione viene calcolata in base al numero di campioni di output nel buffer e alla frequenza di campionamento.
-   I timestamp successivi vengono calcolati dal timestamp e dalla durata precedenti: timestamp corrente + durata corrente = timestamp successivo. Non devono esserci Gap negli indicatori temporali di output.

Se il flusso di input contiene inizialmente timestamp, ma per qualche motivo passa a nessun timestamp, il decodificatore deve continuare a generare i propri timestamp di output, in modo che siano continui e che non si verifichino Gap.

Se il flusso di input contiene timestamp, ma sono presenti gap negli orari, il decodificatore propagherà semplicemente tali gap. In altre parole, il decodificatore non deve tentare di correggere indicatori temporali incoerenti nel flusso di input.

### <a name="mixers"></a>Miscelatori

> [!Note]  
> In Windows Vista, la pipeline Media Foundation non supporta MFTs con più di un input. I MFTs con più input sono supportati in Windows 7.

 

Un mixer accetta più input e li combina in un unico output. Se i flussi di input non sono completamente bloccati o se sono leggermente sfalsati tra loro, è possibile che si verifichino ambiguità sul tempo da impostare nell'output. Di seguito sono riportate alcune linee guida, a seconda del tipo di supporto:

-   Audio. All'avvio o immediatamente dopo lo svuotamento o lo svuotamento, un mixer audio deve attendere la generazione di esempi di output fino a quando non riceve un esempio di input in tutti i flussi di input necessari. A questo punto, deve scegliere il timestamp meno recente degli esempi iniziali da usare come base per i timestamp di output. Gli altri flussi devono essere riempiti con il silenzio per comportare eventuali discrepanze temporali. Se un campione viene ricevuto su un flusso di input facoltativo, è necessario fattorizzarlo anche nel calcolo. Da quel punto in poi, il MFT dovrebbe sforzarsi di produrre una catena continua e non interruppe di timestamp di output. In generale, il MFT non deve tentare di tenere conto di un flusso in modo non conforme rispetto a un altro. Al contrario, è necessario calcolare i timestamp di output dal timestamp di base, la velocità di output e le dimensioni del buffer. Quando si verifica un altro svuotamento o scaricamento, il MFT deve reimpostare i timestamp di base.

-   Video. All'avvio o immediatamente dopo uno svuotamento o uno scaricamento, un mixer video deve attendere per produrre esempi di output fino a quando non riceve un esempio di input in tutti i flussi di input necessari. A questo punto, deve scegliere il timestamp meno recente degli esempi iniziali da usare come base per i timestamp di output. In generale, si consiglia di tenere traccia dei timestamp di output continui e regolari e di durate fisse, anche se l'input non è regolare, se necessario, ripetendo i frame di input.

### <a name="encoders"></a>Codificatori

Un codificatore converte audio o video non compressi in pacchetti compressi. Un codificatore deve attenersi alle linee guida seguenti:

-   Il codificatore deve seguire le convenzioni del formato di output. Se il formato non è in genere il timestamp di ogni esempio, come in MPEG-2, non tutti i campioni di output devono avere un timestamp e una durata.

-   Gli indicatori temporali di input devono essere conservati nel formato di output, se il formato contiene campi per i timestamp, a meno che le informazioni sul tempo migliori siano disponibili da un'altra origine, ad esempio l'applicazione stessa.

### <a name="multiplexers"></a>Multiplexer

> [!Note]  
> In Windows Vista, la pipeline Media Foundation non supporta MFTs con più di un input. I MFTs con più input sono supportati in Windows 7.

 

Un multiplexer combina due flussi audio o video diversi in un formato con interfoliazione, ad esempio il flusso di trasporto AVI o MPEG-2. Un multiplexer deve attenersi alle linee guida seguenti:

-   Il multiplexer deve seguire le convenzioni del formato di output. Se il formato non è in genere il timestamp di ogni esempio, come in MPEG-2, non tutti i campioni di output devono avere un timestamp e una durata.

-   Il timestamp deve riflettere la prima ora che verrebbe posizionata in qualsiasi frame che inizia con tale pacchetto o l'ora del primo campione audio che verrebbe decodificato da tale pacchetto. Ignorare questa linea guida se è in conflitto con le convenzioni del formato di output.

### <a name="demultiplexers"></a>Demultiplexer

Un Demultiplexer suddivide un formato con interfoliazione, ad esempio un flusso di trasporto AVI o MPEG-2, nei flussi audio e video sottostanti.

Se il formato contiene informazioni specifiche sul timestamp che possono essere usate per calcolare indicatori temporali di output accurati in base ai timestamp di input, tali informazioni devono essere usate. Tuttavia, se il formato contiene tempi in una base completamente diversa che non presentano relazioni con i timestamp di input e non è possibile calcolare un offset accurato al timestamp di input, le ore del formato devono essere ignorate.

Se il formato non dispone di informazioni sul timestamp utilizzabili, il Demultiplexer deve attenersi alle regole seguenti:

-   I flussi di output non compressi devono avere timestamp e durate validi, se possibile, calcolati dal timestamp di input precedente più vicino.

-   I flussi di output compressi devono avere timestamp solo sul primo campione di output derivato da un campione di input con un timestamp. Se l'esempio di input non dispone di un timestamp, nessun campione di output derivato dall'esempio di input deve avere un timestamp. Se l'esempio di input è suddiviso in più esempi di output, solo il primo campione di output deve avere un timestamp e il resto non deve avere timestamp.

### <a name="examples"></a>Esempi

Esempio 1. Si supponga che un effetto video accetti sempre un frame di input non compresso, applica l'effetto e lo copia nell'output. Non viene mai eseguito alcun frame o buffer di input. Questa MFT copia semplicemente il timestamp e la durata dall'esempio di input nell'esempio di output, se disponibili, e non esegue alcun calcolo temporale.

Esempio 2. Si supponga che un effetto audio trasformi tutti i 10 millisecondi (MS) di ogni buffer di input, salvando i 10 ms aggiuntivi per combinarli con il buffer successivo. Ottiene un flusso di campioni che hanno tutti una durata di 50 ms. Gli orari di input sono riportati nella tabella seguente.



| Esempio | Tempo di input | Durata input | Ora output | Durata dell'output |
|--------|------------|----------------|-------------|-----------------|
| 1      | 20         | 50             | 20          | 40              |
| 2      | 70         | 50             | 60          | 50              |
| 3      | 121        | 50             | 110         | 50              |
| 4      | 171        | 50             | 161         | 50              |



 

Si noti la discrepanza di 1 ms tra la durata effettiva del campione 2 e la durata implicita in base al timestamp successivo (121? 70 = 51).

Poiché il MFT include 10 ms, viene restituito il primo 40 ms di input sample 1 come output sample 1, con un timestamp di 20 ms e una durata di 40 ms.

Output Sample 2 combina i 10 ms precedentemente mantenuti con 40 ms di input Sample 2. A questo esempio viene assegnato un timestamp di 60 ms (il timestamp dell'esempio precedente di input, 20ms, oltre alla durata dei dati già elaborati dall'esempio, 40ms). Viene fornita una durata di 50 ms.

Analogamente, l'esempio successivo ha un timestamp di 110ms (70ms + 40ms) con una durata di 50 ms.

Il calcolo successivo è più interessante. Il timestamp implicito del tempo di output e della durata precedenti è 160 ms (timestamp 110 ms + Duration 50 ms). Tuttavia, il timestamp di output dovrebbe essere calcolato dal timestamp di input dell'esempio di input più recente che si sovrappone all'esempio di output nel tempo, oltre alla lunghezza dei dati già elaborati dall'esempio. L'esempio di input sovrapposto più vicino è l'esempio 4 (timestamp = 171), ma questo non è il primo. Il primo esempio sovrapposto è il campione 3 (timestamp = 121). Aggiungendo il 40ms che è già stato elaborato dall'esempio, il risultato è 161.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di un MFT personalizzato](writing-a-custom-mft.md)
</dt> </dl>

 

 



