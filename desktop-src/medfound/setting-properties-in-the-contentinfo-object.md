---
description: Durante la creazione di un file ASF, è necessario che l'oggetto ContentInfo conosca le caratteristiche del contenuto multimediale, in modo che i vari oggetti Header vengano popolati con i valori corretti.
ms.assetid: 30e3c10b-1310-4194-8b83-221dfe73b03c
title: Impostazione delle proprietà nell'oggetto ContentInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e386d5eb33dd1893b195a870425b2336ab9c316f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130474"
---
# <a name="setting-properties-in-the-contentinfo-object"></a>Impostazione delle proprietà nell'oggetto ContentInfo

Durante la creazione di un file ASF, è necessario che l'oggetto ContentInfo conosca le caratteristiche del contenuto multimediale, in modo che i vari oggetti Header vengano popolati con i valori corretti.

-   [Impostazioni correlate al contenuto nell'oggetto ContentInfo](#content-related-settings-in-the-contentinfo-object)
-   [Configurazione dell'oggetto ContentInfo con le impostazioni del codificatore](#configuring-the-contentinfo-object-with-encoder-settings)
-   [Argomenti correlati](#related-topics)

## <a name="content-related-settings-in-the-contentinfo-object"></a>Impostazioni correlate al contenuto nell'oggetto ContentInfo

Le impostazioni di configurazione del contenuto sono impostazioni di flusso, che sono contenute all'interno del profilo e specificano l'identificatore del flusso, il tipo di supporto e i parametri di bucket a perdita per il sink multimediale. Dopo che il profilo è stato impostato sull'oggetto ContentInfo chiamando [**IMFASFContentInfo:: seprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile), questi valori vengono riflessi nell'oggetto intestazione ASF che è stato generato. Per informazioni su queste impostazioni, vedere [creazione e configurazione di flussi ASF](creating-and-configuring-asf-streams.md).

## <a name="configuring-the-contentinfo-object-with-encoder-settings"></a>Configurazione dell'oggetto ContentInfo con le impostazioni del codificatore

I dati audio o video multimediali digitali sono complessi e occupano grandi quantità di memoria. Nella maggior parte dei casi, audio e video vengono compressi tramite codificatori prima di essere aggiunti a un file ASF. In Media Foundation i codificatori vengono implementati come [trasformazioni di Media Foundation](media-foundation-transforms.md) (MFTS) con un input e un output. È necessario selezionare il tipo di supporto di output in base al tipo di supporto del flusso di input e al tipo di codifica scelto per comprimere il flusso.

Prima della sessione di codifica, il codificatore deve essere configurato impostando le proprietà rilevanti a seconda del tipo di codifica.

Dopo aver configurato il codificatore, è necessario configurare l'oggetto ContentInfo con i valori del codificatore, perché il [multiplexing ASF](asf-multiplexer.md) e il sink multimediale ASF, che vengono inizializzati con l'oggetto ContentInfo popolato, usano impostazioni quali i valori dei bucket persi per generare pacchetti di dati ASF. I valori non vengono salvati nell'oggetto intestazione ASF finale. Le impostazioni di codifica sono esposte come proprietà. Per configurare l'oggetto ContentInfo con le proprietà del codificatore, eseguire le operazioni seguenti:

1.  Ottenere un puntatore all'archivio delle proprietà del codificatore eseguendo una query del codificatore (interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ) direttamente per l'interfaccia **IPropertyStore** .
2.  Chiamare [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore). Per impostare le proprietà specifiche del flusso, specificare l'identificatore del flusso nel parametro *wStreamNumber* . per le proprietà a livello di file, passare 0. Il parametro *ppIStore* riceve un puntatore all'interfaccia **IPropertyStore** . L'archivio delle proprietà ricevuto è vuoto.
3.  Chiamare **IPropertyStore:: GetValue** sul codificatore e ottenere il valore della proprietà specificando le costanti della chiave della proprietà. Per un elenco completo delle proprietà di codifica, vedere la Guida di [riferimento alla programmazione di codec](/previous-versions//aa384554(v=vs.85)).
4.  Chiamare **IPropertyStore:: SetValue** nell'oggetto ContentInfo per impostare la proprietà obbligatoria nell'archivio delle proprietà.
5.  Ripetere i passaggi 3 e 4 per ogni proprietà che si desidera impostare.

Il sink multimediale ASF può essere creato usando un oggetto Activation chiamando [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate). Il nuovo oggetto sink multimediale viene configurato in base alle impostazioni specifiche del sink multimediale che possono essere impostate nell'archivio delle proprietà dell'oggetto ContentInfo. Nella tabella seguente vengono illustrate le costanti della proprietà del sink multimediale ASF.



| Proprietà                                                                                                     | Descrizione                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFPKEY \_ ASFMEDIASINK \_ base \_ SENDTIME**](mfpkey-asfmediasink-base-sendtime-property.md)                   | Il tempo di invio indica quando verrà rilasciato il payload all'interno del bucket. Il valore di questa proprietà indica il primo tempo di invio. Il multiplexer utilizza questo valore per calcolare i tempi di invio successivi per i pacchetti generati e garantisce che i dati scorrano costantemente attraverso il bucket. |
| [**velocità in bit di MFPKEY \_ ASFMEDIASINK \_ AutoAdjust \_**](mfpkey-asfmediasink-autoadjust-bitrate-property.md)         | Questo valore **bool** indica se il multiplexer deve modificare automaticamente la velocità in bit per assicurarsi che i dati non vengano sottoposto a overflow nel bucket.                                                                                                                                              |
| [**MFPKEY \_ ASFMEDIASINK \_ DRMACTION**](mfpkey-asfmediasink-drmaction-property.md)                            | Ciò indica l'azione DRM del sink multimediale ASF per la generazione di file. In questa versione è supportata solo la transcodifica DRM.                                                                                                                                                                                   |
| [**MFPKEY \_ ASFSTREAMSINK con \_ correzione \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) | Questa proprietà deve essere impostata quando il codificatore stabilisce la finestra del buffer e la velocità in bit da usare. Per impostare questi valori, usare l'interfaccia [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) . Questa impostazione deve essere impostata per ogni flusso del file ASF.                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di un oggetto intestazione ASF per un nuovo file](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 
