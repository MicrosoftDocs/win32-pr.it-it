---
description: '\_Esempio di AUDIODELAY MFT'
ms.assetid: 08f119f9-cacd-4000-96b6-60c8c0055e9c
title: Esempio MFT_AudioDelay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d382ce7d1c5e9475bef85f11ef9754345e123b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309084"
---
# <a name="mft_audiodelay-sample"></a>\_Esempio di AUDIODELAY MFT

Viene illustrato come implementare un effetto audio come una trasformazione di Media Foundation (MFT). Il ritardo audio MFT accetta audio PCM come input, applica un effetto delay (ECHO) e restituisce i dati audio modificati.

## <a name="apis-demonstrated"></a>API illustrate

In questo esempio vengono illustrate le interfacce Microsoft Media Foundation seguenti:

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a>Utilizzo

L' \_ esempio MFT AudioDelay compila una dll che è un server com per MFT. Prima di usare il file MFT, è necessario registrare la DLL. È possibile usare lo strumento TopoEdit per compilare una topologia che include il ritardo audio MFT. Per ulteriori informazioni su TopoEdit, vedere [TopoEdit](topoedit.md). È anche possibile modificare l' [esempio PlaybackFX](/previous-versions//bb970336(v=vs.85)) per usare il MFT. Sarà necessario modificare la funzione AddBranchToPartialTopology in Player. cpp. Modificare la riga seguente da:

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, GUID_NULL);
}
```

Con:

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, CLSID_DelayMFT);
}
```

Il valore CLSID \_ DelayMFT è dichiarato nel file di intestazione AudioDelayUuids. h nella cartella di \_ esempio MFT AudioDelay.

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Media Foundation SDK](media-foundation-sdk-samples.md)
</dt> <dt>

[Trasformazioni Media Foundation](media-foundation-transforms.md)
</dt> <dt>

[\_Esempio di scala di grigi MFT](mft-grayscale-sample.md)
</dt> <dt>

[Scrittura di un MFT personalizzato](writing-a-custom-mft.md)
</dt> </dl>

 

 
