---
description: Il &\# bucket 0034;leaky&0034; è un modo per modellare i requisiti di memorizzazione nel buffer per \# la riproduzione uniforme.
ms.assetid: 2f7f80d6-3abb-462f-a571-b223a1d59da6
title: Modello di buffer bucket persa (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 848a0088a0e2b155deb6945e4a6532edb2677dc484341e50172f1bb1eb8187d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238053"
---
# <a name="the-leaky-bucket-buffer-model-microsoft-media-foundation"></a>Modello di buffer bucket persa (Microsoft Media Foundation)

Quando si esegue lo streaming dei supporti in rete, il decodificatore riceve i dati codificati a una velocità teoricamente costante (velocità di trasmissione). Il decodificatore utilizza questi dati per produrre output decodificato. Nel caso generale, tuttavia, il decodificatore utilizza i dati *a* una velocità variabile, perché il codificatore può usare una velocità di codifica variabile.

Il modello "bucket che perde" è un modo per modellare i requisiti di memorizzazione nel buffer per una riproduzione uniforme. In questo modello, il decodificatore mantiene un buffer. I dati codificati passano dalla rete al buffer e dal buffer al decodificatore. Se il sottoflusso del buffer si verifica, significa che il decodificatore rimuove i dati dal buffer più velocemente di quanto non lo sia la rete. Se il buffer si sovraccarica, significa che la rete sta fornendo i dati più velocemente di quanto il decodificatore lo usa.

Questo argomento descrive il modello di buffer "leaky bucket" per la codifica e la decodifica.

-   [Bucket di perdite](#the-leaky-bucket)
-   [Bucket in uso](#the-bucket-in-use)
-   [Impostazione dei valori del bucket di perdita per asf Flussi](#setting-leaky-bucket-values-for-asf-streams)
-   [Valori bucket persi nel multiplexer ASF](#leaky-bucket-values-in-the-asf-multiplexer)
-   [Aggiornamento dei valori dei bucket persi nel sink dei supporti asf](#updating-leaky-bucket-values-in-the-asf-media-sink)
-   [Argomenti correlati](#related-topics)

## <a name="the-leaky-bucket"></a>Bucket di perdite

Per comprendere il modello di bucket che perde, prendere in considerazione un bucket con un piccolo foro nella parte inferiore. Tre parametri definiscono il bucket:

-   Capacità (B)
-   Velocità con cui l'acqua esce dal bucket (R)
-   Completezza iniziale del bucket (F)

In questa metafora, il bucket è il buffer:

![figura che mostra un buffer come bucket, la velocità di input come acqua che entra nel bucket e la velocità di output come acqua che esce da un foro nel bucket](images/asf-components03.png)

Se l'acqua viene versata nel bucket esattamente alla velocità *R,* il bucket rimarrà a F, perché la velocità di input è uguale alla velocità di output. Se la velocità di input aumenta mentre *R* rimane costante, il bucket accumula acqua. Se la frequenza di input è maggiore *di R* per un periodo di tempo costante, alla fine il bucket si overflow. Tuttavia, la velocità di input può variare *in R* senza overflow del bucket, purché la velocità di input media non superi la capacità del bucket. Maggiore è la capacità, maggiore è la frequenza di input che può variare in un determinato intervallo di tempo.

In ASF, il bucket di perdita è definito da tre parametri:

-   Velocità in bit media, in byte al secondo, che corrisponde alla velocità di output (*R*)
-   Finestra del buffer, misurata in millisecondi, che corrisponde alla capacità del bucket (*B*).
-   Completezza iniziale del buffer, in genere impostata su zero.

La velocità in bit misura il numero medio di bit al secondo nel flusso codificato. La finestra del buffer misura il numero di millisecondi di dati alla velocità in bit che può essere adattata al buffer. La dimensione del buffer in bit è uguale a R \* (B /1000).

I dati del payload ASF possono entrare nel bucket che perde in orari irregolari e in quantità irregolari, ma devono lasciare il bucket a una velocità in bit positiva costante. A causa della finestra del buffer, esiste un possibile ritardo tra il momento in cui il payload entra nel bucket e il momento in cui esce. Il ritardo massimo che può verificarsi è *B* / *R*. I dati del payload immessi nel bucket sono in base all'ora di presentazione e non devono mai sovraccaricare il bucket. Oltre all'ora di presentazione, ogni payload ha anche un tempo di invio, ovvero l'ora in cui i dati del payload lasciano il bucket in base alla velocità in bit. L'ora di invio deve essere precedente all'ora di presentazione per garantire che, quando il bucket che perde si avvicina a essere pieno, ogni payload lascia il bucket prima o al momento della presentazione. A tale scopo, i tempi di presentazione vengono spostati in avanti dal valore / *B R* *(preroll*) e i tempi di invio ottengono un inizio iniziale a partire da zero. L'ora di invio non deve essere successiva all'ora di presentazione perché ciò indica che il payload è stato immesso nel bucket troppo tardi e non può essere incluso nell'oggetto dati. Il valore di preroll è incluso [nell'oggetto intestazione ASF.](asf-file-structure.md)

Per lo streaming senza problemi in rete, i flussi compressi all'interno del contenuto multimediale devono mantenere una velocità in bit costante per tutta la durata della riproduzione. Il modello di bucket asf leaky garantisce che i dati multimediali siano inviati in rete a una velocità in bit costante. I parametri del bucket di perdita vengono specificati nell'oggetto Proprietà flusso esteso [dell'oggetto intestazione ASF](asf-file-structure.md). In Microsoft Media Foundation, vengono impostati come attributi nel tipo di supporto che rappresenta il flusso.

I valori del bucket di perdita sono definiti sia nel sink del file ASF che nell'oggetto multiplexer ASF sottostante e nel codificatore Windows media. Questi valori possono essere uguali o diversi. Si consideri ad esempio uno scenario di streaming, che richiede che gli esempi audio siano recapitati in un secondo momento rispetto agli esempi video in modo che il file possa essere trasmesso senza latenza. A tale scopo, il bucket di perdita del flusso audio nel sink multimediale può essere impostato su un valore superiore al valore impostato nel codificatore audio Windows Media.

Per impostare i valori B/R nel codificatore, l'applicazione deve impostare le proprietà [**MFPKEY \_ RAVG,**](mfpkey-ravgproperty.md) [**MFPKEY \_ BAVG,**](mfpkey-bavgproperty.md) [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md)e [**MFPKEY \_ BMAX.**](mfpkey-bmaxproperty.md) Per informazioni sull'impostazione delle proprietà nel codificatore, vedere [Proprietà di codifica](configuring-the-encoder.md).

## <a name="the-bucket-in-use"></a>Bucket in uso

L'obiettivo di un codificatore è garantire che il contenuto non esonda mai il buffer. Il codificatore usa la velocità in bit e i valori della finestra del buffer come guide. Il numero effettivo di bit passati in qualsiasi periodo di tempo uguale alla finestra del buffer non può mai essere maggiore del doppio delle dimensioni del buffer.

Si consideri l'esempio seguente: si ha un bucket da 3 galloni con un foro attraverso il quale può scorrere 1 gallone al minuto. Si mette il bucket sotto uno spigot e si apre la valvola per far uscire l'acqua a una velocità di 1 gallone al minuto. L'acqua esce dal bucket non appena entra, senza lasciare altri elementi nel bucket. Si aumenta quindi il flusso dallo spigot a 2 galloni al minuto. Ogni minuto in cui l'acqua scorre a questa velocità, 2 galloni passano nel bucket e 1 gallone si perde, lasciando 1 gallone nel bucket. Alla fine di 3 minuti, 6 galloni di acqua sono finiti nel secchiello, 3 galloni sono fuoriusciti e il bucket è pieno.

In pratica, la velocità massima teorica dei dati in un intervallo uguale alla finestra del buffer non viene mai ottenuta. Nell'esempio precedente si presupponeva una velocità dei dati costante. Dato lo stesso bucket da 3 galloni, è possibile aumentare la velocità di flusso dallo spitore a 6 galloni al minuto per un minuto e quindi disattivare lo spigot per due minuti. Anche se la quantità totale di acqua inserita nel bucket rientra nel valore massimo teorico per la finestra del buffer, la concentrazione di tale quantità in una parte della finestra causa l'overflow del bucket. A 6 galloni al minuto, il bucket da 3 galloni trabocca poco dopo il passaggio di 30 secondi. Pertanto, la quantità massima effettiva di dati che possono essere recapitati al buffer per la durata di qualsiasi intervallo uguale all'impostazione della finestra del buffer dipende dalle dimensioni dei singoli campioni e dal momento in cui vengono recapitati.

Finora gli esempi hanno trattato solo il buffer usato dal decodificatore, ma un buffer bucket che perde viene usato anche dal codificatore che crea il contenuto compresso. Il codificatore apporta tutte le modifiche necessarie agli algoritmi di compressione per mantenere la velocità in bit dei campioni compressi entro i limiti descritti dalla velocità in bit e dalla finestra del buffer, presupponendo che i campioni verranno recapitati al decodificatore a una velocità costante. È possibile pensare al bucket del codificatore come al mirroring del bucket del decodificatore. Il bucket del codificatore viene riempito a una velocità variabile determinata dalle dimensioni dei singoli campioni e perde a una velocità costante uguale alla velocità in bit media.

Si consideri l'esempio seguente di codificatore e decodificatore connessi in rete. Codificare un file video a 30 fotogrammi al secondo con una velocità in bit di 6.000 bit al secondo e una finestra del buffer di 3 secondi (dimensioni totali del buffer di 18.000 bit). Il primo esempio è codificato come fotogramma chiave e occupa 7.000 bit. Il buffer del codificatore contiene ora 7.000 bit. I 29 fotogrammi successivi sono tutti fotogrammi differenziali per un totale di 3.000 bit. Il primo secondo del contenuto (30 fotogrammi) inserirebbe quindi la pienezza del buffer a 10.000 bit se non si verificasse alcuna perdita. Si sa che la velocità in bit del flusso è di 6.000 bit al secondo, quindi dopo che il primo secondo di contenuto codificato è stato inserito nel buffer del codificatore, la completezza scende a 4.000 bit. Nell'applicazione di decodifica questo flusso viene recapitato al buffer del decodificatore a 6.000 bit al secondo. Dopo un secondo, il buffer contiene 6.000 bit. Il primo esempio contiene 7.000 bit, quindi il buffer del decodificatore deve essere riempito di più prima che il decodificatore inizi a rimuovere i campioni.

## <a name="setting-leaky-bucket-values-for-asf-streams"></a>Impostazione dei valori del bucket di perdita per asf Flussi

In uno scenario di codifica dei file, un'applicazione può impostare i valori dei bucket persi durante la configurazione dei flussi nel [profilo ASF.](asf-profile.md)

Dopo aver creato il flusso e avere un riferimento [**all'interfaccia IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) del flusso, è possibile impostare i valori usando gli attributi seguenti:

-   [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) (valori medi dei bucket persi)
-   [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) (valori massimi del bucket di perdita)

Per informazioni sull'aggiunta di flussi e sul recupero del **puntatore IMFASFStreamConfig,** vedere Aggiunta di informazioni sul [flusso al sink di file ASF](adding-stream-information-to-the-asf-file-sink.md).

Questi valori contengono il set di informazioni seguente:

-   Velocità in bit media: ottiene la velocità in bit media dal tipo di supporto di output selezionato durante la negoziazione del tipo di supporto. Usare [**l'attributo MF \_ MT \_ AUDIO \_ AVG BYTES PER \_ \_ \_ SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) (per i flussi audio) o l'attributo [**MF MT \_ \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md) (per i flussi video).
-   Finestra buffer: se si dispone di un'istanza del codificatore e sono stati negoziati tipi di supporti di output, è possibile aggiornare questo valore in un secondo momento tramite query sul codificatore per l'interfaccia [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) e quindi chiamando [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces.h, wmcodecdspuuid.lib). In caso contrario, usare il valore predefinito di 3000 millisecondi.
-   Dimensioni iniziali del buffer: impostata su 0.

I valori forniti dall'applicazione dipendono dal tipo di codifica e dal tipo di supporto del flusso. Ad esempio, [la codifica a velocità in bit costante](constant-bit-rate-encoding.md) richiede una velocità in bit fissa predeterminata e una finestra del buffer. L'applicazione può specificare questi valori di bucket persi impostando la proprietà di codifica [**MFPKEY \_ VIDEOWINDOW**](mfpkey-videowindowproperty.md) e l'attributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) nel flusso. I valori della finestra del buffer specificati vengono usati per assicurarsi che il file codificato abbia gli orari di invio corretti contrassegnati nei pacchetti di dati e che il valore di preroll venga visualizzato nell'oggetto intestazione ASF. È sufficiente impostare **MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1** perché questi valori specificati vengono copiati nell'attributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2.**](mf-asfstreamconfig-leakybucket2-attribute.md)

Per le modalità di codifica a 2 passaggi è necessario impostare entrambi gli attributi per specificare i valori medi e massimi.

Per la codifica VBR, l'applicazione può eseguire una query per i valori di bucket persi usati dal codificatore solo dopo il completamento del passaggio di codifica. Pertanto, durante la configurazione del sink multimediale, l'applicazione può scegliere di non impostare gli attributi o le proprietà correlati ai bucket persi. Dopo la codifica, l'applicazione deve eseguire una query sul codificatore per le proprietà [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md), [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md), [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md)e [**MFPKEY \_ BMAX**](mfpkey-bmaxproperty.md) e impostarle nel sink multimediale in modo che i valori accurati si riflettano nell'oggetto intestazione. Per un esempio di codice su come aggiornare i valori per la codifica VBR, vedere "Aggiornare le proprietà di codifica nel sink di file" in [Esercitazione: 1-Pass Windows Media Encoding](tutorial--1-pass-windows-media-encoding.md).

Se si copiano Windows contenuto multimediale dall'origine al sink multimediale senza codifica, i valori di bucket persi devono essere impostati nel sink multimediale.

## <a name="leaky-bucket-values-in-the-asf-multiplexer"></a>Valori di bucket persi nel multiplexer asf

In Media Foundation, i valori di bucket persi vengono usati dal [multiplexer di ASF](asf-multiplexer.md) per configurare i valori di bucket persi interni usati per generare pacchetti di dati. Il payload è contenuto in un campione multimediale e una serie di campioni multimediali costituisce un pacchetto di dati ASF. In base ai valori di bucket persi e all'ora di presentazione, il multiplexer assegna un'ora di invio per ogni campione multimediale in modo che la velocità in bit dei pacchetti inviati in rete sia a una velocità in bit costante (*R*).

Un'applicazione non può impostare direttamente valori di bucket persi nel multiplexer. I valori devono essere specificati nel sink del supporto ASF, che imposta i valori appropriati nel multiplexer. I valori impostati in [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) e [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) vengono usati dal multiplexer per convalidare che gli esempi inviati al sink multimediale ASF vengono generati usando i valori specificati.

## <a name="updating-leaky-bucket-values-in-the-asf-media-sink"></a>Aggiornamento dei valori dei bucket persi nel sink del supporto ASF

Un'applicazione può sovrascrivere i valori del bucket di perdita a livello di flusso (impostati nel profilo ASF durante la creazione del flusso) impostando la proprietà [**MFPKEY \_ ASFSTREAMSINK \_ CORRECTED \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) nell'archivio delle proprietà del sink multimediale. Per ottenere un riferimento all'archivio delle proprietà, usare l'oggetto ContentInfo implementato dal sink multimediale. Per altre informazioni, vedere [Impostazione delle proprietà nel sink di file.](setting-properties-in-the-file-sink.md)

**Nota**  Questa operazione è consentita solo per i flussi audio.

Questa proprietà deve essere impostata dopo aver impostato il tipo di output nel codificatore. In base alla velocità in bit impostata nel tipo di supporto, il codificatore calcola le dimensioni del buffer per garantire che i campioni multimediali generati non esercitino mai il buffer. Il codificatore apporta le modifiche necessarie durante la compressione per mantenere la velocità in bit dei campioni compressi entro i limiti descritti dalla frequenza di bit e dalla finestra del buffer.

Analogamente agli attributi di configurazione del flusso per i bucket che causano perdite, impostare la velocità in bit media e le dimensioni del buffer e il livello di completezza iniziale del buffer in una matrice di DWORD. Per altre informazioni, vedere la sezione "Impostazione dei valori di bucket di perdita per asf Flussi" in questo argomento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto di ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Codec Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 
