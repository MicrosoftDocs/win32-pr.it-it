---
description: Metodi di codifica
ms.assetid: 17ab5ecc-0173-4c5c-9d65-40e506ab7e07
title: Metodi di codifica (Microsoft Media Foundation)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa11e9545aa38358e5e1c0fdb4dfc4b7a2c3ee13f24b0fa38fe76b9e8bddcc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974530"
---
# <a name="encoding-methods-microsoft-media-foundation"></a>Metodi di codifica (Microsoft Media Foundation)

La maggior parte dei Windows codec Audio e Video multimediali supporta più metodi di codifica. Sapere come e quando usare ogni metodo può essere utile per creare contenuto compresso di alta qualità.

Tutti i metodi di codifica si concentrano sul buffer usato dal decodificatore per gestire i dati di input compressi. Questo buffer è definito dalla velocità in bit del flusso, in bit al secondo, e dalla finestra del buffer, in millisecondi. Durante la codifica, il codec è abides dagli elementi del buffer. Per altre informazioni sul buffer, vedere [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).

## <a name="constant-bit-rate-encoding"></a>Codifica a velocità in bit costante

La velocità in bit per qualsiasi flusso codificato da uno dei codec audio e video Windows video non è costante. La codifica CBR (Constant Bit Rate) è quindi un termine piuttosto fuorviante. La caratteristica distintiva di un flusso con codifica CBR è una piccola finestra del buffer, che limita la variazione delle dimensioni del campione. La codifica CBR viene usata principalmente per il contenuto trasmesso in rete alla destinazione. In uno scenario di questo tipo è importante potersi basare su un utilizzo coerente della larghezza di banda.

Dal punto di vista della configurazione, la codifica CBR differisce dalle altre modalità per il fatto che prima di iniziare a codificare, si imposta sia la velocità in bit media del contenuto di output sia la finestra del buffer che si applica a tale velocità in bit. In altre modalità, uno o entrambi questi valori sono sconosciuti quando si configura il codificatore e vengono calcolati dal codec durante la codifica. CBR è la modalità di codifica standard usata dagli oggetti DMO Windows Media Encoder.

## <a name="two-pass-constant-bit-rate-encoding"></a>Two-Pass della velocità in bit costante

Il CBR standard usa un solo passaggio di codifica. Il contenuto viene fornito come esempi di input e il codec comprime il contenuto e restituisce gli esempi di output. È anche possibile elaborare due volte gli esempi di input. Al primo passaggio, il codec esegue calcoli per ottimizzare la codifica per il contenuto. Al secondo passaggio, il codec usa i dati raccolti durante il primo passaggio per codificare il contenuto.

La codifica CBR a due passi offre molti vantaggi. Spesso produce miglioramenti significativi della qualità rispetto alla codifica CBR standard senza modificare i requisiti di buffering. In questo modo questa modalità di codifica è ideale per il contenuto trasmesso in rete. L'unica situazione in cui il CBR a due passi non è fattibile è quando si codifica il contenuto da un'origine live e non è possibile usare un secondo passaggio.

Il tipo di supporto di output di un flusso CBR a due passi è identico a quello di un flusso CBR standard; È comunque possibile specificare la frequenza in bit e la finestra del buffer da usare. Quando si configura il DMO, è necessario impostarlo per eseguire due passaggi. Ed è necessario inviare una DMO al termine dell'invio di campioni per il primo passaggio.

## <a name="quality-based-variable-bit-rate-encoding"></a>Quality-Based di velocità in bit variabile

Poiché la codifica CBR non mantiene effettivamente una velocità in bit costante, la distinzione tra di essa e la codifica a velocità in bit variabile (VBR) può sembrare un po' differita. La differenza principale tra CBR e VBR è la dimensione della finestra del buffer usata. I flussi con codifica VBR hanno in genere finestre del buffer di grandi dimensioni rispetto ai flussi con codifica CBR. VbR basato sulla qualità non fa eccezione, in quanto non si definisce né la frequenza in bit né la finestra del buffer. Si imposta invece un valore di qualità. Il codec tenta quindi di comprimere i dati in modo che la qualità del supporto codificato sia coerente per tutta la durata, indipendentemente dai requisiti di buffer del flusso risultante.

VbR basato sulla qualità usa un singolo passaggio di codifica e tende a creare flussi compressi di grandi dimensioni. Al termine della codifica, il codec imposta i requisiti del buffer in modo che il decodificatore possa decomprimere i dati. Il flusso VBR codificato non è adatto per lo streaming in rete, quindi la funzione VBR basata sulla qualità deve essere usata solo per scenari di riproduzione locali (o download e riproduzione).

## <a name="unconstrained-variable-bit-rate-encoding"></a>Codifica a velocità in bit variabile non vincolata

A differenza di VBR basato sulla qualità, la funzione VBR non vincolata non viene codificata a un livello di qualità specifico. Al contrario, codifica il contenuto alla massima qualità possibile mantenendo al tempo stesso una velocità in bit specificata. VbR senza vincoli usa due passaggi di codifica ed è simile a CBR a due passaggi, ad eccezione del fatto che non si specifica un'impostazione della finestra del buffer per il flusso. Ciò significa che non esiste alcun limite alla dimensione dei singoli campioni nel flusso, purché la velocità in bit media sia minore o uguale al valore impostato.

VbR senza vincoli è di uso limitato, perché esistono pochi scenari di riproduzione che hanno requisiti in linea con i requisiti del buffer. Il codec può impostare la finestra del buffer su qualsiasi valore richiesto dopo la codifica, senza alcun controllo sulle dimensioni del buffer. Nella maggior parte dei casi, se non si è interessati alle dimensioni del buffer o alla coerenza dell'utilizzo della larghezza di banda, è consigliabile usare la funzionalità vbr basata sulla qualità.

## <a name="peak-constrained-variable-bit-rate-encoding"></a>Peak-Constrained di velocità in bit variabile

La modalità di codifica finale è vbr con vincoli di picco. Come vbr non vincolato, questa modalità usa due passaggi di codifica e codifica a una velocità in bit specificata. Tuttavia, con il limite massimo di vbr vincolato si configura anche il valore di picco per la codifica. I valori di picco sono simili ai normali valori di configurazione del buffer: è presente una velocità in bit di picco e una finestra del buffer di picco. Il file viene codificato in modo da essere conforme a un buffer descritto dai valori di picco, con la condizione che la velocità in bit media complessiva del flusso sia uguale o inferiore al valore di velocità in bit media specificato.

La rappresentazione vbr vincolata può essere difficile da concettualizzare. Ecco il modo più semplice per pensare al modello di buffering usato. Si supponga che il flusso sia un flusso CBR con la velocità in bit massima e la finestra del buffer di picco usata per definire il buffer. In genere, la velocità in bit massima è piuttosto elevata. Il codificatore garantisce che il valore di velocità in bit media previsto indicato venga mantenuto per la durata del flusso. In qualsiasi punto specifico del flusso, la velocità in bit media è garantita come maggiore della dimensione totale del flusso in bit divisa per la durata del flusso in secondi).

Si consideri l'esempio seguente: si configura un flusso con una velocità in bit media di 16.000 bit al secondo, una velocità in bit massima di 48.000 bit al secondo e una finestra di picco del buffer di 3.000 (3 secondi). La dimensione del buffer usato per il flusso è di 144.000 bit (48.000 bit al secondo x 3 secondi) come determinato dai valori di picco. Il codificatore comprime i dati in modo che siano conformi a tale buffer. Inoltre, la velocità in bit media del flusso deve essere 16.000 o inferiore. Se il codificatore deve creare campioni di dimensioni molto grandi per gestire un segmento complesso di contenuto, può sfruttare le dimensioni del buffer di grandi dimensioni. Tuttavia, altre parti del flusso devono essere codificate a una velocità in bit inferiore per portare la media al livello specificato.

La codifica VBR con limiti di picco è utile per i dispositivi di riproduzione con una capacità di buffer limitata e alcuni vincoli di velocità dei dati. Un esempio comune è la codifica usata per i DVD.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della codifica VBR](usingvbrencoding.md)
</dt> <dt>

[Codec Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



