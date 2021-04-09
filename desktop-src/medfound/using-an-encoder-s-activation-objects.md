---
description: Per la conversione di file multimediali in formato ASF, è possibile utilizzare codificatori Windows Media. Per usare questi codificatori, è necessario registrarli nel sistema.
ms.assetid: 18c26619-6047-4f7f-bb65-ca418f02e5b1
title: Uso di oggetti attivazione codificatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd44a1b97ad0f133b7215ff4474835ddfba66bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880578"
---
# <a name="using-an-encoders-activation-objects"></a>Uso di oggetti di attivazione del codificatore

Per la conversione di file multimediali in formato ASF, è possibile utilizzare codificatori Windows Media. Per usare questi codificatori, è necessario registrarli nel sistema.

Per informazioni sulla registrazione del codificatore, vedere Creazione di un' [istanza di un codificatore MFT](instantiating-the-encoder-mft.md).

-   [Uso di oggetti di attivazione del codificatore](#using-an-encoders-activation-objects)
-   [Enumerazione del codificatore in Windows 7 e versioni successive](#encoder-enumeration-in-windows-7-and-later)
-   [Argomenti correlati](#related-topics)

## <a name="using-an-encoders-activation-objects"></a>Uso di oggetti di attivazione del codificatore

In alternativa all'uso di un'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) del codificatore (descritta in [creazione di un codificatore tramite CoCreateInstance](using-an-encoder-s-imftransform--interface.md)), è possibile creare un'istanza dell'oggetto attivazione per il codificatore. Oggetti attivazione facilita la creazione del codificatore e Media Foundation fornisce le due funzioni seguenti per questo approccio:

-   [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) per la creazione di un'istanza del codificatore audio Windows Media.
-   [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) per la creazione di un'istanza del codificatore video Windows Media.

Per entrambe queste funzioni è necessario creare il tipo di supporto di destinazione e impostare le proprietà di codifica prima di chiamare queste funzioni. Se l'applicazione usa [componenti ASF a livello di pipeline](pipeline-layer-asf-components.md) per codificare un file in formato ASF ed è già stato creato e configurato il sink dei [supporti ASF](asf-media-sinks.md), è possibile ottenere questo set di informazioni dal sink dei supporti ASF.

[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) e [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) impostare il tipo di output del codificatore sul tipo di supporto specificato dall'applicazione.

**Nota**  Se si usano [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) e [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) , è possibile attivare il codificatore chiamando [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) , ma non è possibile modificare l'input e i tipi di supporti di output del codificatore, né modificare alcuna delle proprietà di codifica.

Per ulteriori informazioni sulla creazione di oggetti Media Foundation tramite oggetti Activation, vedere [oggetti Activation](activation-objects.md).

**Per ottenere il tipo di supporto di destinazione dal sink multimediale ASF**

1.  Ottenere un puntatore al puntatore [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) del sink multimediale ASF chiamando **IMFMediaSink:: QueryInterface** sul sink multimediale ASF e passando **IID \_ IMFASFContentInfo** come identificatore di interfaccia.
2.  Ottenere l'oggetto profilo ASF associato all'oggetto ContentInfo.
3.  Enumerare i flussi nel profilo per ottenere il tipo di supporto del flusso.

**Per ottenere le proprietà di codifica dal sink multimediale ASF**

1.  Se sono state configurate le [proprietà di codifica](configuring-the-encoder.md) nel sink dei supporti (descritto in [impostazione delle proprietà nel sink di file](setting-properties-in-the-file-sink.md)), è possibile un riferimento all'archivio delle proprietà del sink chiamando **IMFMediaSink:: QueryInterface** sul sink multimediale ASF e passando **IID \_ IPropertyStore** come identificatore di interfaccia.
2.  Se è presente un puntatore all'oggetto ContentInfo del sink, è possibile chiamare [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) per ottenere un riferimento all'archivio delle proprietà del sink multimediale.

    Verificare che tutte le proprietà di codifica impostate nel sink multimediale ASF siano riflesse nell'archivio delle proprietà passato a [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) e [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate). Il codificatore viene configurato automaticamente in base alle impostazioni specificate dall'applicazione.

Durante la creazione del nodo Transform nella topologia di codifica, è possibile impostare il tipo di oggetto come un puntatore [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) ricevuto in queste due chiamate. Quando la topologia viene risolta, la sessione multimediale usa l'oggetto attivazione per creare un'istanza del codificatore MFT.

## <a name="encoder-enumeration-in-windows-7-and-later"></a>Enumerazione del codificatore in Windows 7 e versioni successive

Per le applicazioni in esecuzione in Windows 7, oltre a [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) , è possibile enumerare il codificatore MFTS chiamando [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex). Questa funzione restituisce un puntatore all'oggetto Activation del codificatore MFT. La struttura della funzione è molto simile a quella descritta in precedenza, ad eccezione di **MFTEnumEx** restituisce una matrice di puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) per il codificatore MFTS che corrispondono ai **criteri di ricerca** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un'istanza di un codificatore MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Codificatori Windows Media](windows-media-encoders.md)
</dt> <dt>

[Oggetti attivazione](activation-objects.md)
</dt> </dl>

 

 



