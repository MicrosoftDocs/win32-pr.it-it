---
description: Viene illustrato come implementare un effetto video come una trasformazione Media Foundation (MFT).
ms.assetid: ad7d20bc-5eab-4390-a48b-5ea8e97ead7d
title: Esempio MFT_Grayscale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273c562eb5985d0a329c434a8e4aa44119744496
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130510"
---
# <a name="mft_grayscale-sample"></a>\_Esempio di scala di grigi MFT

Viene illustrato come implementare un effetto video come una trasformazione Media Foundation (MFT). La MFT in scala di grigi converte il video YUV in scala di grigi impostando i valori croma nel video su neutro. Il MFT accetta video non compressi nei formati UYVY, YUY2 o NV12.

## <a name="apis-demonstrated"></a>API illustrate

In questo esempio vengono illustrate le interfacce Microsoft Media Foundation seguenti:

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a>Utilizzo

L' \_ esempio relativo alle gradazioni di grigio per MFT compila una dll che è un server com per MFT. Prima di usare il file MFT, è necessario registrare la DLL.

Per visualizzare la MFT in scala di grigi in uso, eseguire l' [esempio PlaybackFX](/previous-versions//bb970336(v=vs.85)). È anche possibile usare lo strumento TopoEdit per compilare una topologia che include la MFT in scala di grigi. Per ulteriori informazioni su TopoEdit, vedere [TopoEdit](topoedit.md).

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_grayscale).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video su YUV](about-yuv-video.md)
</dt> <dt>

[Esempi di Media Foundation SDK](media-foundation-sdk-samples.md)
</dt> <dt>

[Trasformazioni Media Foundation](media-foundation-transforms.md)
</dt> <dt>

[\_Esempio di AUDIODELAY MFT](mft-audiodelay-sample.md)
</dt> <dt>

[Scrittura di un MFT personalizzato](writing-a-custom-mft.md)
</dt> </dl>

 

 
