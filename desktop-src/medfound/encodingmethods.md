---
description: Metodi di codifica
ms.assetid: 17ab5ecc-0173-4c5c-9d65-40e506ab7e07
title: Metodi di codifica (Microsoft Media Foundation)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4366f11ea9d120d638c5600f84fc16f6c5320f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305387"
---
# <a name="encoding-methods-microsoft-media-foundation"></a>Metodi di codifica (Microsoft Media Foundation)

La maggior parte dei codec Windows Media Audio e video supporta più metodi di codifica. Sapere come e quando usare ogni metodo può essere utile per creare contenuti compressi di alta qualità.

I metodi di codifica si concentrano tutti sul buffer utilizzato dal decodificatore per gestire i dati di input compressi. Questo buffer è definito dalla velocità in bit del flusso, in bit al secondo e dalla finestra del buffer, in millisecondi. Quando si codifica, il codec si attiene ai vincoli del buffer. Per ulteriori informazioni sul buffer, vedere [il modello di buffer di bucket a perdita](the-leaky-bucket-buffer-model.md).

## <a name="constant-bit-rate-encoding"></a>Codifica della velocità in bit costante

La velocità in bit per qualsiasi flusso codificato da uno dei codec Windows Media Audio e video non è costante. La codifica della velocità in bit costante (CBR) è, pertanto, un termine alquanto fuorviante. La caratteristica distintiva di un flusso con codifica CBR è una piccola finestra del buffer, che limita la variazione delle dimensioni del campione. La codifica CBR viene utilizzata principalmente per il contenuto trasmesso in una rete alla relativa destinazione. In uno scenario di questo tipo, è importante essere in grado di basarsi sull'utilizzo coerente della larghezza di banda.

Da un punto di vista della configurazione, la codifica CBR differisce dalle altre modalità in quanto prima di iniziare la codifica, si imposta sia la velocità in bit media del contenuto di output che la finestra del buffer che si applica alla velocità in bit. In altre modalità, uno o entrambi i valori sono sconosciuti quando si configura il codificatore e viene calcolato dal codec durante la codifica. CBR è la modalità di codifica standard utilizzata da Windows Media Encoder DMOs.

## <a name="two-pass-constant-bit-rate-encoding"></a>Codifica della velocità in bit costante Two-Pass

CBR standard USA solo un singolo passaggio di codifica. Il contenuto viene fornito come esempio di input e il Codec comprime il contenuto e restituisce gli esempi di output. È anche possibile elaborare due volte gli esempi di input. Al primo passaggio, il codec esegue calcoli per ottimizzare la codifica per il contenuto. Al secondo passaggio, il codec usa i dati raccolti durante il primo passaggio per codificare il contenuto.

La codifica CBR a due passaggi presenta molti vantaggi. Spesso produce un notevole miglioramento della qualità rispetto alla codifica CBR standard senza modificare i requisiti di buffering. Questa modalità di codifica è quindi ideale per il contenuto trasmesso in rete. L'unica situazione in cui la funzionalità CBR a due passaggi non è fattibile è quando si codifica il contenuto da un'origine live e non è possibile usare un secondo passaggio.

Il tipo di supporto di output di un flusso CBR a due passaggi è identico a quello di un flusso CBR standard. è ancora necessario specificare la velocità in bit e la finestra del buffer da usare. Quando si configura DMO, è necessario impostarlo in modo da eseguire due sessioni. Al termine dell'invio degli esempi per il primo passaggio, è necessario inviare una notifica a DMO.

## <a name="quality-based-variable-bit-rate-encoding"></a>Codifica della velocità in bit della variabile Quality-Based

Poiché la codifica CBR non mantiene effettivamente una velocità in bit costante, la distinzione tra it e la codifica della velocità in bit variabile (VBR) può sembrare poco chiara. La differenza principale tra CBR e VBR è la dimensione della finestra del buffer utilizzata. I flussi con codifica VBR hanno in genere finestre di buffer di grandi dimensioni rispetto a flussi con codifica CBR. Il VBR basato sulla qualità non è un'eccezione, perché non è possibile definire né la velocità in bit né la finestra del buffer. Si imposta invece un valore qualitativo. Il codec tenta quindi di comprimere i dati in modo che la qualità del supporto codificato sia coerente per tutta la sua durata, indipendentemente dai requisiti del buffer del flusso risultante.

Il formato VBR basato sulla qualità usa un singolo passaggio di codifica e tende a creare flussi compressi di grandi dimensioni. Al termine della codifica, il codec imposta i requisiti del buffer in modo che il decodificatore possa decomprimere i dati. Il flusso VBR codificato non è adatto per lo streaming in rete, quindi è consigliabile usare VBR basato sulla qualità solo per gli scenari di riproduzione locali (o per il download e la riproduzione).

## <a name="unconstrained-variable-bit-rate-encoding"></a>Codifica della velocità in bit variabile non vincolata

Diversamente da VBR basato sulla qualità, il VBR non vincolato non viene codificato in un livello di qualità specifico. Codifica invece il contenuto con la massima qualità possibile mantenendo una velocità in bit specificata. Il VBR non vincolato usa due passaggi di codifica ed è simile a un CBR a due passaggi, con la differenza che non viene specificata un'impostazione della finestra del buffer per il flusso. Ciò significa che non esiste alcun limite per le dimensioni dei singoli campioni nel flusso, purché la velocità in bit media sia minore o uguale al valore impostato.

Il formato VBR non vincolato è di uso limitato, perché esistono pochi scenari di riproduzione che hanno requisiti in base ai requisiti del buffer. Il codec può impostare la finestra del buffer su qualsiasi valore necessario dopo la codifica, senza alcun controllo sulle dimensioni del buffer. Nella maggior parte dei casi, se non si è interessati alla dimensione del buffer o alla coerenza di utilizzo della larghezza di banda, è consigliabile usare un VBR basato sulla qualità.

## <a name="peak-constrained-variable-bit-rate-encoding"></a>Codifica della velocità in bit della variabile Peak-Constrained

La modalità di codifica finale è un VBR con vincoli di picco. Analogamente a VBR non vincolato, questa modalità usa due sessioni di codifica e codifica a una velocità in bit specificata. Tuttavia, con il picco di VBR vincolato è possibile configurare anche il valore di picco per la codifica. I valori di picco sono simili ai normali valori di configurazione del buffer: la velocità in bit massima e una finestra del buffer di picco. Il file è codificato in modo da essere conforme a un buffer descritto dai valori di picco, con la condizione che la velocità di bit media complessiva del flusso sia uguale o inferiore al valore di velocità in bit medio specificato.

Un VBR vincolato può essere di difficile concettualizzazione. Ecco il modo più semplice per pensare al modello di buffer usato. Si supponga che il flusso sia un flusso CBR con la velocità in bit massima e la finestra del buffer di picco utilizzata per definire il buffer. In genere, la velocità in bit di picco è piuttosto elevata. Il codificatore garantisce che il valore della velocità media in bit previsto venga mantenuto per la durata del flusso. In un determinato punto del flusso, la velocità in bit media è garantita maggiore della dimensione del flusso totale in bit divisa per la durata del flusso in secondi).

Si consideri l'esempio seguente: si configura un flusso con una velocità in bit media di 16.000 bit al secondo, una velocità in bit di picco di 48.000 bit al secondo e una finestra buffer di picco di 3.000 (3 secondi). Le dimensioni del buffer utilizzato per il flusso sono di 144.000 bit (48.000 bit al secondo x 3 secondi) come determinato dai valori di picco. Il codificatore comprime i dati in modo che siano conformi a tale buffer. Inoltre, la velocità in bit media del flusso deve essere inferiore a 16.000. Se il codificatore deve eseguire alcuni esempi di dimensioni molto elevate per gestire un segmento complesso di contenuto, può sfruttare le dimensioni del buffer di grandi dimensioni. Tuttavia, altre parti del flusso devono essere codificate a una velocità in bit più bassa per abbassare la media fino al livello specificato.

La codifica VBR con vincoli di picco è utile per riprodurre i dispositivi con una capacità di buffer finita e alcuni vincoli di velocità dati. Un esempio comune è la codifica utilizzata per i DVD.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della codifica VBR](usingvbrencoding.md)
</dt> <dt>

[Codec Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



