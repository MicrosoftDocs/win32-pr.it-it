---
description: Il \# modello di &0034; bucket&\# 0034; è un modo per modellare i requisiti di buffering per la riproduzione uniforme.
ms.assetid: 2f7f80d6-3abb-462f-a571-b223a1d59da6
title: Modello di buffer di bucket a perdita (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5a99932fb121808f6a49323360c47c09d0acbb
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320897"
---
# <a name="the-leaky-bucket-buffer-model-microsoft-media-foundation"></a>Modello di buffer di bucket a perdita (Microsoft Media Foundation)

Quando si esegue lo streaming di file multimediali in una rete, il decodificatore riceve i dati codificati a una velocità teoricamente costante (la velocità di trasmissione). Il decodificatore utilizza questi dati per produrre output decodificato. Nel caso generale, tuttavia, il decodificatore utilizza i dati a una frequenza *variabile* , perché il codificatore può utilizzare una frequenza di codifica variabile.

Il modello "leaky bucket" è un modo per modellare i requisiti di buffering per la riproduzione senza problemi. In questo modello, il decodificatore gestisce un buffer. I dati codificati passano dalla rete al buffer e dal buffer al decodificatore. Se il buffer viene sottoposto a propagazione, significa che il decodificatore sta rimuovendo i dati dal buffer più velocemente rispetto alla distribuzione della rete. Se si verifica un overflow del buffer, significa che la rete sta distribuendo i dati più velocemente rispetto a quanto utilizzato dal decodificatore.

Questo argomento descrive il modello "leaky bucket" dei buffer per la codifica e la decodifica.

-   [Bucket a perdita](#the-leaky-bucket)
-   [Il bucket in uso](#the-bucket-in-use)
-   [Impostazione dei valori bucket a perdita per i flussi ASF](#setting-leaky-bucket-values-for-asf-streams)
-   [Valori di bucket persi nel multiplexer ASF](#leaky-bucket-values-in-the-asf-multiplexer)
-   [Aggiornamento dei valori di bucket a perdita nel sink multimediale ASF](#updating-leaky-bucket-values-in-the-asf-media-sink)
-   [Argomenti correlati](#related-topics)

## <a name="the-leaky-bucket"></a>Bucket a perdita

Per comprendere il modello di bucket a perdita, prendere in considerazione un bucket con un piccolo foro in basso. Tre parametri definiscono il bucket:

-   Capacità (B)
-   Frequenza con cui l'acqua fuoriesce dal bucket (R)
-   Completezza iniziale del bucket (F)

In questa metafora il bucket è il buffer:

![illustrazione che mostra un buffer come bucket, frequenza di input come acqua che entra nel bucket e frequenza di output come acqua che lascia un foro nel bucket](images/asf-components03.png)

Se l'acqua viene versata nel bucket alla velocità esatta *R*, il bucket rimarrà in corrispondenza di F, perché la velocità di input è uguale alla frequenza di output. Se la frequenza di input aumenta mentre *R* rimane costante, il bucket accumula acqua. Se la frequenza di input è maggiore di *R* per un periodo di tempo prolungato, si verifica un overflow del bucket. Tuttavia, la frequenza di input può variare in base a *R* senza overflow del bucket, purché la velocità media di input non superi la capacità del bucket. Maggiore è la capacità, maggiore sarà la frequenza di input che può variare in un determinato intervallo di tempo.

In ASF, il bucket di perdita è definito da tre parametri:

-   Velocità in bit media, in byte al secondo, che corrisponde alla frequenza di output (*R*)
-   La finestra del buffer, misurata in millisecondi, che corrisponde alla capacità del bucket (*B*).
-   Completezza del buffer iniziale, che in genere è impostata su zero.

La velocità in bit misura il numero medio di bit al secondo nel flusso codificato. La finestra buffer misura il numero di millisecondi di dati alla velocità in bit che possono essere inseriti nel buffer. La dimensione del buffer in bit è uguale a R \* (B/1000).

I dati del payload ASF possono entrare nel bucket di perdita a intervalli irregolari e in importi irregolari, ma devono lasciare il bucket a una velocità in bit costante positiva. A causa della finestra del buffer, esiste un possibile ritardo tra il momento in cui il payload entra nel bucket e quando viene lasciato. Il ritardo massimo che può verificarsi è *B* / *R*. I dati di payload che entrano nel bucket sono in base all'ora di presentazione e non devono mai eseguire l'overflow del bucket. Oltre al tempo di presentazione, a ogni payload è associato anche un tempo di invio, ovvero l'ora in cui i dati del payload lasciano il bucket in base alla velocità in bit. Il tempo di invio deve essere precedente all'ora di presentazione per assicurarsi che, quando il bucket si avvicina a essere pieno, ogni payload lascia il bucket prima o dopo l'ora di presentazione. A tale scopo, i tempi di presentazione vengono spostati in avanti dal valore *B* / *R* (il *preroll*) e i tempi di invio iniziano a partire da zero. L'ora di invio deve essere successiva all'ora di presentazione perché indica che il payload è stato immesso troppo tardi e non può essere incluso nell'oggetto dati. Il valore di preroll è incluso nell' [oggetto intestazione ASF](asf-file-structure.md) .

Per lo streaming senza glitch in rete, i flussi compressi all'interno del contenuto multimediale devono mantenere una velocità in bit costante per tutta la durata della riproduzione. Il modello di bucket a perdita di ASF garantisce che i dati multimediali vengano inviati attraverso la rete a una velocità in bit costante. I parametri del bucket perso sono specificati nell'oggetto proprietà del flusso esteso dell' [oggetto intestazione ASF](asf-file-structure.md). In Microsoft Media Foundation vengono impostati come attributi sul tipo di supporto che rappresenta il flusso.

I valori dei bucket persi vengono definiti sia nel sink di file ASF che nell'oggetto del multiplexer ASF sottostante e in Windows Media Encoder. Questi valori possono essere uguali o diversi. Si consideri ad esempio uno scenario di streaming, che richiede che gli esempi audio vengano recapitati in un secondo momento rispetto agli esempi video, in modo che il file possa essere trasmesso senza latenza. A tale scopo, il bucket della perdita del flusso audio nel sink multimediale può essere impostato su un valore superiore al valore impostato nel codificatore audio Windows Media.

Per impostare i valori B/R nel codificatore, l'applicazione deve impostare le proprietà [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md), [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md), [**MFPKEY \_ Rmax**](mfpkey-rmaxproperty.md)e [**MFPKEY \_ BMAX**](mfpkey-bmaxproperty.md) . Per informazioni sull'impostazione delle proprietà nel codificatore, vedere [proprietà di codifica](configuring-the-encoder.md).

## <a name="the-bucket-in-use"></a>Il bucket in uso

L'obiettivo di un codificatore è garantire che il contenuto non superi mai l'overflow del buffer. Il codificatore usa i valori della velocità in bit e della finestra del buffer come guide. Il numero effettivo di bit passati in un periodo di tempo uguale alla finestra del buffer non può mai essere maggiore del doppio delle dimensioni del buffer.

Si consideri l'esempio seguente: si ha un bucket da 3 litri con un foro al minuto, che può fluire al minuto di 1 gallone. Si posiziona il bucket sotto un perno e si apre la valvola per lasciare l'acqua a una velocità di 1 gallone al minuto. L'acqua scorre fuori dal bucket con la stessa rapidità con cui entra, senza uscire dal bucket. Si aumenta quindi il flusso dal perno a 2 litri al minuto. Ogni minuto che l'acqua scorre a questa velocità, 2 litri entrano nel bucket e 1 gallone fuoriesce, lasciando 1 gallone nel bucket. Alla fine di 3 minuti, 6 litri di acqua sono entrati nel bucket, 3 litri di perdite e il bucket è pieno.

In pratica, la velocità teorica massima dei dati su un intervallo uguale alla finestra del buffer non viene mai realizzata. Nell'esempio precedente si presuppone una velocità dati costante. Dato lo stesso bucket da 3 litri, è possibile aumentare la velocità di flusso dal perno a 6 galloni al minuto per un minuto e quindi spegnere il rubinetto per due minuti. Anche se la quantità totale di acqua inserita nel bucket rientra nel massimo teorico per la finestra del buffer, la concentrazione di tale quantità in una parte della finestra causa l'overflow del bucket. A 6 litri al minuto, i bucket da 3 litri si propagano poco dopo 30 secondi. Pertanto, la quantità effettiva massima di dati che è possibile recapitare al buffer per la durata di un intervallo uguale all'impostazione della finestra del buffer dipende dalle dimensioni dei singoli campioni e dal momento in cui vengono recapitati.

Fino a questo punto, gli esempi hanno solo illustrato il buffer usato dal decodificatore, ma il codificatore crea il contenuto compresso anche per un buffer di bucket a perdita. Il codificatore apporta tutte le modifiche necessarie agli algoritmi di compressione per tenere la velocità in bit degli esempi compressi entro i limiti descritti dalla velocità in bit e dalla finestra del buffer, supponendo che gli esempi vengano recapitati al decodificatore a una velocità costante. È possibile considerare il bucket del codificatore come il mirroring del bucket del decodificatore. Il bucket del codificatore viene riempito a una frequenza variabile determinata dalla dimensione dei singoli campioni e dalle perdite a una velocità costante uguale alla velocità in bit media.

Si consideri l'esempio seguente di un codificatore e un decodificatore connesso in rete. È possibile codificare un file video a 30 fotogrammi al secondo con una velocità in bit di 6.000 bit al secondo e una finestra del buffer di 3 secondi, ovvero una dimensione del buffer totale di 18.000 bit. Il primo campione viene codificato come fotogramma chiave e richiede 7.000 bit. Il buffer del codificatore ora contiene 7.000 bit. I 29 frame successivi sono tutti i frame Delta che rientrano in totale 3.000 bit. Quindi, il primo secondo di contenuto (30 fotogrammi) inserirebbe la completezza del buffer a 10.000 bit se non si sono verificate perdite di dati. Sappiamo che la velocità in bit del flusso è di 6.000 bit al secondo, quindi, dopo che il primo secondo del contenuto codificato viene inserito nel buffer del codificatore, la completezza scende a 4.000 bit. Nell'applicazione di decodifica questo flusso viene recapitato al buffer del decodificatore a 6.000 bit al secondo. Dopo un secondo, il buffer contiene 6.000 bit. Il primo esempio contiene 7.000 bit, quindi il buffer del decodificatore deve essere riempito di più prima che il decodificatore inizi a rimuovere gli esempi.

## <a name="setting-leaky-bucket-values-for-asf-streams"></a>Impostazione dei valori bucket a perdita per i flussi ASF

In uno scenario di codifica dei file, un'applicazione può impostare i valori dei bucket persi durante la configurazione dei flussi nel [profilo ASF](asf-profile.md).

Dopo aver creato il flusso e avere un riferimento all'interfaccia [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) del flusso, è possibile impostare i valori usando gli attributi seguenti:

-   [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) (valori di bucket a perdita media)
-   [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) (max Leaky Bucket Values)

Per informazioni sull'aggiunta di flussi e sull'acquisizione del puntatore **IMFASFStreamConfig** , vedere [aggiunta di informazioni sul flusso al sink di file ASF](adding-stream-information-to-the-asf-file-sink.md).

Questi valori contengono il set di Informazioni seguente:

-   Velocità in bit media: ottenere la velocità in bit media dal tipo di supporto di output selezionato durante la negoziazione del tipo di supporto. Usare l'attributo [**MF \_ mt \_ audio \_ Avg \_ bytes \_ al \_ secondo**](mf-mt-audio-avg-bytes-per-second-attribute.md) (per i flussi audio) o l'attributo [**MF \_ mt \_ Avg \_ bitrate**](mf-mt-avg-bitrate-attribute.md) (per i flussi video).
-   Finestra buffer: se si dispone di un'istanza del codificatore e i tipi di supporti di output negoziati, è possibile aggiornare questo valore in un secondo momento eseguendo una query sul codificatore per l'interfaccia [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) e quindi chiamando [**IWMCodecLeakyBucket:: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces. h, wmcodecdspuuid. lib). In caso contrario, usare il valore predefinito di 3000 millisecondi.
-   Dimensioni iniziali del buffer: impostare su 0.

I valori forniti dall'applicazione dipendono dal tipo di codifica e dal tipo di supporto del flusso. La codifica della [velocità in bit costante](constant-bit-rate-encoding.md) , ad esempio, richiede una frequenza a bit fissa predeterminata e una finestra del buffer. L'applicazione può specificare questi valori di bucket persione impostando la proprietà di codifica [**\_ VIDEOWINDOW di MFPKEY**](mfpkey-videowindowproperty.md) e l'attributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) nel flusso. I valori della finestra del buffer specificati vengono utilizzati per verificare che il file codificato disponga dei tempi di invio corretti contrassegnati nei pacchetti di dati e che il valore di preroll venga visualizzato nell'oggetto intestazione ASF. È sufficiente impostare **MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1** perché questi valori specificati vengono copiati nell'attributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) .

Per le modalità di codifica a 2 passaggi è necessario impostare entrambi gli attributi per specificare i valori medi e massimi.

Per la codifica VBR, l'applicazione può eseguire una query per i valori dei bucket persi utilizzati dal codificatore solo dopo il completamento del passaggio di codifica. Pertanto, durante la configurazione del sink multimediale, l'applicazione può scegliere di non impostare gli attributi o le proprietà correlate ai bucket persi. Dopo la codifica, l'applicazione deve eseguire una query sul codificatore per le proprietà [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md), [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md), [**MFPKEY \_ Rmax**](mfpkey-rmaxproperty.md)e [**MFPKEY \_**](mfpkey-bmaxproperty.md) BMAX e impostarle nel sink del supporto in modo che i valori accurati vengano riflessi nell'oggetto intestazione. Per un esempio di codice su come aggiornare i valori per la codifica VBR, vedere l'argomento relativo all'aggiornamento delle proprietà di codifica nel sink di file in [esercitazione: codifica Windows Media da 1 pass](tutorial--1-pass-windows-media-encoding.md).

Se si copia contenuto Windows Media dall'origine al sink multimediale senza codifica, è necessario impostare i valori bucket persi nel sink di supporto.

## <a name="leaky-bucket-values-in-the-asf-multiplexer"></a>Valori di bucket persi nel multiplexer ASF

In Media Foundation, i valori dei bucket persi vengono usati dal [multiplexer ASF](asf-multiplexer.md) per configurare i valori di bucket interni che usa per generare i pacchetti di dati. Il payload è contenuto all'interno di un esempio multimediale e una serie di esempi di supporti costituisce un pacchetto di dati ASF. In base ai valori dei bucket a perdita e all'ora di presentazione, il multiplexer assegna un tempo di invio per ogni esempio di supporto in modo che la velocità in bit dei pacchetti inviati attraverso la rete sia a una velocità in bit costante (*R*).

Un'applicazione non è in grado di impostare direttamente i valori dei bucket persi nel multiplexer. I valori devono essere specificati sul sink multimediale ASF, che consente di impostare i valori appropriati nel multiplexer. I valori impostati in [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) e [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) vengono usati dal multiplexer per convalidare gli esempi inviati al sink di supporto ASF vengono generati usando i valori specificati.

## <a name="updating-leaky-bucket-values-in-the-asf-media-sink"></a>Aggiornamento dei valori di bucket a perdita nel sink multimediale ASF

Un'applicazione può sovrascrivere i valori dei bucket a livello di flusso (impostati nel profilo ASF durante la creazione del flusso) impostando la proprietà [**\_ \_ \_ LEAKYBUCKET ASFSTREAMSINK con correzione MFPKEY**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) nell'archivio delle proprietà del sink multimediale. Per ottenere un riferimento all'archivio delle proprietà, usare l'oggetto ContentInfo implementato dal sink multimediale. Per ulteriori informazioni, vedere [impostazione delle proprietà nel sink di file](setting-properties-in-the-file-sink.md).

**Nota**  Questa operazione è consentita solo per i flussi audio.

Questa proprietà deve essere impostata dopo aver impostato il tipo di output nel codificatore. In base alla velocità in bit impostata nel tipo di supporto, il codificatore calcola le dimensioni del buffer per assicurarsi che gli esempi di supporti generati non superino mai il buffer. Il codificatore apporta le modifiche necessarie durante la compressione per limitare la velocità in bit degli esempi compressi entro i limiti descritti dalla velocità in bit e dalla finestra del buffer.

Analogamente agli attributi di configurazione del flusso per i bucket con perdite, impostare la velocità in bit media e la dimensione del buffer e la completezza del buffer iniziale in una matrice di valori DWORD. Per ulteriori informazioni, vedere la sezione "impostazione dei valori bucket per i flussi ASF" in questo argomento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Codec Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 
