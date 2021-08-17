---
description: Per convertire i file multimediali in formato ASF, è possibile usare Windows codificatori multimediali. Informazioni sull'uso degli oggetti di attivazione di un codificatore.
ms.assetid: 18c26619-6047-4f7f-bb65-ca418f02e5b1
title: Uso di oggetti di attivazione dei codificatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24915020c1b888be6a1aeaca1e21af95d11cfc181a5c00a91c8359c3f780fa0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972740"
---
# <a name="using-an-encoders-activation-objects"></a>Uso degli oggetti di attivazione di un codificatore

Per convertire i file multimediali in formato ASF, è possibile usare Windows codificatori multimediali. Per usare questi codificatori, è necessario registrarli con il sistema.

Per informazioni sulla registrazione del codificatore, vedere [Creazione di un'istanza di un codificatore MFT.](instantiating-the-encoder-mft.md)

-   [Uso degli oggetti di attivazione di un codificatore](#using-an-encoders-activation-objects)
-   [Enumerazione del codificatore in Windows 7 e versioni successive](#encoder-enumeration-in-windows-7-and-later)
-   [Argomenti correlati](#related-topics)

## <a name="using-an-encoders-activation-objects"></a>Uso degli oggetti di attivazione di un codificatore

In alternativa all'uso [**dell'interfaccia IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) di un codificatore (descritta in Creazione di un codificatore tramite [CoCreateInstance),](using-an-encoder-s-imftransform--interface.md)è possibile creare un'istanza dell'oggetto attivazione per il codificatore. Gli oggetti attivazione facilitano la creazione del codificatore Media Foundation fornisce le due funzioni seguenti per questo approccio:

-   [**MFCreateWMAEncoderActivate per**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) la creazione di un'istanza Windows codificatore audio multimediale.
-   [**MFCreateWMVEncoderActivate per**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) la creazione di un'istanza Windows codificatore video multimediale.

Entrambe queste funzioni richiedono la creazione del tipo di supporto di destinazione e l'impostazione delle proprietà di codifica prima di chiamare queste funzioni. Se l'applicazione usa componenti [ASF](pipeline-layer-asf-components.md) del livello pipeline per codificare un file in formato ASF e ha già creato e configurato i sink multimediali di [ASF,](asf-media-sinks.md)è possibile ottenere questo set di informazioni dal sink multimediale di ASF.

[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) e [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) impostano il tipo di output del codificatore sul tipo di supporto specificato dall'applicazione.

**Nota**  Se si usano [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) e [**MFCreateWMVEncoderActivate,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) è possibile attivare il codificatore chiamando [**IMFActivate::ActivateObject,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) ma non è possibile modificare i tipi di input e supporti di output del codificatore né modificare le proprietà di codifica.

Per altre informazioni sulla creazione di Media Foundation di attivazione tramite oggetti di attivazione, vedere [Oggetti attivazione.](activation-objects.md)

**Per ottenere il tipo di supporto di destinazione dal sink del supporto ASF**

1.  Ottenere un puntatore al puntatore [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) del sink multimediale asf chiamando **IMFMediaSink::QueryInterface** nel sink multimediale ASF e passando **IID \_ IMFASFContentInfo** come identificatore di interfaccia.
2.  Ottiene l'oggetto profilo ASF associato all'oggetto ContentInfo.
3.  Enumerare i flussi nel profilo per ottenere il tipo di supporto del flusso.

**Per ottenere le proprietà di codifica dal sink multimediale di ASF**

1.  Se sono state [](configuring-the-encoder.md) configurate le proprietà di codifica nel sink multimediale (descritte in Impostazione delle proprietà nel [sink file](setting-properties-in-the-file-sink.md)), è possibile fare riferimento all'archivio delle proprietà del sink chiamando **IMFMediaSink::QueryInterface** nel sink multimediale ASF e passando **IID \_ IPropertyStore** come identificatore di interfaccia.
2.  Se si ha un puntatore all'oggetto ContentInfo del sink, è possibile chiamare [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) per ottenere un riferimento all'archivio delle proprietà del sink multimediale.

    Assicurarsi che tutte le proprietà di codifica impostate nel sink multimediale di ASF siano riflesse nell'archivio delle proprietà passato a [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) e [**MFCreateWMVEncoderActivate.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) Il codificatore viene configurato automaticamente in base alle impostazioni specificate dall'applicazione.

Durante la creazione del nodo di trasformazione nella topologia di codifica, è possibile impostare il tipo di oggetto come [**puntatore IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) ricevuto in queste due chiamate. Quando la topologia viene risolta, la sessione multimediale usa l'oggetto attivazione per creare un'istanza del codificatore MFT.

## <a name="encoder-enumeration-in-windows-7-and-later"></a>Enumerazione del codificatore in Windows 7 e versioni successive

Per le applicazioni in esecuzione in Windows 7, oltre a [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) è possibile enumerare i MFT del codificatore chiamando [**MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) Questa funzione restituisce un puntatore all'oggetto attivazione del codificatore MFT. La struttura della funzione è molto simile a **MFTEnum** descritta in precedenza, ad eccezione del fatto che **MFTEnumEx** restituisce una matrice di puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) per i MFT del codificatore che corrispondono ai criteri di ricerca.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un'istanza di un codificatore MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Codificatori multimediali](windows-media-encoders.md)
</dt> <dt>

[Oggetti di attivazione](activation-objects.md)
</dt> </dl>

 

 



