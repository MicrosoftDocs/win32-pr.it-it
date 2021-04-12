---
description: Il sink di file ASF è un'implementazione di IMFMediaSink fornita da Media Foundation che un'applicazione può usare per archiviare i dati del supporto ASF in un file. Per informazioni sul modello a oggetti dei sink multimediali ASF e sull'utilizzo generale, vedere la pagina relativa ai sink di supporto ASF.
ms.assetid: a47caabd-23e3-4d22-b4b6-5fdb79d62ca1
title: Impostazione delle proprietà nel sink di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30af39cf13e88f6edf2a6ab68caac27c2400955a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344401"
---
# <a name="setting-properties-in-the-file-sink"></a>Impostazione delle proprietà nel sink di file

Il sink di file ASF è un'implementazione di [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fornita da Media Foundation che un'applicazione può usare per archiviare i dati del supporto ASF in un file. Per informazioni sul modello a oggetti dei sink multimediali ASF e sull'utilizzo generale, vedere la pagina relativa ai [sink di supporto ASF](asf-media-sinks.md).

Dopo aver [creato il sink di file ASF](creating-the-asf-file-sink.md), è necessario configurarlo con informazioni sui flussi nel file di output. Questa procedura è descritta in [aggiunta di informazioni sul flusso al sink di file ASF](adding-stream-information-to-the-asf-file-sink.md). È possibile impostare proprietà aggiuntive sul sink di file a seconda del tipo di codifica; Bucket persi; Proprietà generali del file. Queste impostazioni non vengono scritte nell'oggetto intestazione ASF finale. In questo argomento viene descritto il processo di aggiunta di queste proprietà nell'archivio delle proprietà del sink di file.

L'oggetto ContentInfo mantiene le proprietà del file globale e le singole proprietà del flusso per il sink di file. Per informazioni su come ottenere un riferimento all'oggetto ASF di sink di file, vedere [creazione del sink di file ASF](creating-the-asf-file-sink.md).

Per ottenere un riferimento all'archivio delle proprietà ([**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)) del sink di file, chiamare [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) sul riferimento dell'oggetto ContentInfo del sink di file.

## <a name="stream-encoding-properties"></a>Proprietà di codifica del flusso

Per codificare correttamente il contenuto, è necessario che il file conosca determinate informazioni di codifica, ad esempio il tipo di codifica e i parametri di codifica correlati. Questi valori vengono impostati nel sink di file come valori di proprietà in un archivio di proprietà gestito dall'oggetto ContentInfo ASF. Se si sta configurando il sink di file prima di creare un'istanza dei codificatori pertinenti, è possibile usare l'oggetto ContentInfo con tutte le proprietà popolate per creare i codificatori Windows Media. In questo caso, le proprietà vengono impostate automaticamente nei codificatori di cui è stata creata un'istanza. Viceversa, se si creano i codificatori prima del sink, assicurarsi che le proprietà impostate nei codificatori vengano copiate nell'archivio delle proprietà del sink di file.

Per impostare le proprietà di codifica, è necessario accedere all'archivio delle proprietà a livello di flusso del sink di file. Passare il numero del flusso nel parametro *wStreamNumber* del metodo [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) . I numeri di flusso devono corrispondere ai valori impostati durante la configurazione di ogni flusso nel profilo. I valori delle proprietà vengono impostati chiamando [**IPropertyStore:: SetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore). Nella tabella seguente vengono descritte le proprietà supportate.

Le proprietà dipendono dal tipo di codifica. Per informazioni sulle proprietà e sui rispettivi valori che è necessario impostare, vedere [Encoding Properties (proprietà di codifica](configuring-the-encoder.md)).

## <a name="leaky-bucket-property"></a>Proprietà bucket a perdita

I parametri bucket a perdita determinano la finestra del buffer effettiva utilizzata dal codificatore per il flusso. La proprietà [**MFPKEY ASFSTREAMSINK con \_ \_ correzione \_**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) del sink di file contiene i parametri del bucket di perdita, la velocità in bit, la finestra del buffer e la completezza del buffer iniziale. Questa proprietà viene impostata nell'archivio delle proprietà della proprietà a livello di flusso per il sink di file e deve essere impostata dopo la creazione e la configurazione di codificatori. Questo valore viene impostato nell'oggetto. Durante la negoziazione del tipo di supporto, il codificatore decide la finestra del buffer e la velocità in bit da usare. È possibile ottenere questi valori usando l'interfaccia **IWMCodecLeakyBucket** , definita in wmcodecifaces. h ed è necessario collegarsi a wmcodecdspuuid. lib per chiamare i relativi metodi.

I valori recuperati possono essere impostati per questa proprietà per ogni flusso nel sink di file ASF.

## <a name="global-file-sink-properties"></a>Proprietà di sink di file globali

Per ottenere l'archivio delle proprietà globali del sink di file, passare 0 nel parametro *wStreamNumber* del metodo [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) . I valori delle proprietà vengono impostati chiamando [**IPropertyStore:: SetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore). Nella tabella seguente vengono descritte le proprietà supportate.

| Proprietà a livello di file                                                                                | Descrizione                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFPKEY \_ ASFMEDIASINK \_ base \_ SENDTIME**](mfpkey-asfmediasink-base-sendtime-property.md)           | Il tempo di invio indica quando verrà rilasciato il payload all'interno del bucket. Il valore di questa proprietà indica il primo tempo di invio. Il multiplexer utilizza questo valore per calcolare i tempi di invio successivi per i pacchetti generati e garantisce che i dati scorrano costantemente attraverso il bucket. |
| [**velocità in bit di MFPKEY \_ ASFMEDIASINK \_ AutoAdjust \_**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) | Questo valore BOOL indica se il multiplexer deve modificare automaticamente la velocità in bit per assicurarsi che i dati non vengano sottoposto a overflow nel bucket.                                                                                                                                                  |
| [**MFPKEY \_ ASFMEDIASINK \_ DRMACTION**](mfpkey-asfmediasink-drmaction-property.md)                    | Ciò indica l'azione DRM del sink multimediale ASF per la generazione di file. In questa versione è supportata solo la transcodifica DRM.                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sink di supporti ASF](asf-media-sinks.md)
</dt> <dt>

[Componenti ASF a livello pipeline](pipeline-layer-asf-components.md)
</dt> <dt>

[Supporto ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
