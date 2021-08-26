---
description: Esempio \_ audioDelay MFT
ms.assetid: 08f119f9-cacd-4000-96b6-60c8c0055e9c
title: MFT_AudioDelay esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4af3d89c7dda4a67a2fece09ff9e6d3bc0a63927e94b259df40334fd9ba29b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012671"
---
# <a name="mft_audiodelay-sample"></a>Esempio \_ audioDelay MFT

Illustra come implementare un effetto audio come Media Foundation transform (MFT). Il ritardo audio MFT accetta l'audio PCM come input, applica un effetto di ritardo (echo) e restituisce i dati audio modificati.

## <a name="apis-demonstrated"></a>DIMOSTRAZIONE DELLE API

In questo esempio vengono illustrate le Microsoft Media Foundation seguenti:

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a>Utilizzo

L'esempio \_ AudioDelay MFT compila una DLL che è un server COM per MFT. Prima di usare MFT, è necessario registrare la DLL. È possibile usare lo strumento TopoEdit per creare una topologia che includa il ritardo audio MFT. Per altre informazioni su TopoEdit, vedere [TopoEdit.](topoedit.md) È anche possibile modificare [l'esempio PlaybackFX per](/previous-versions//bb970336(v=vs.85)) usare MFT. Sarà necessario modificare la funzione AddBranchToPartialTopology in Player.cpp. Modificare la riga seguente da:

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

Il valore CLSID DelayMFT viene dichiarato nel file di intestazione \_ AudioDelayUuids.h nella cartella di esempio \_ AudioDelay MFT.

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nel [repository github Windows esempi classici.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Media Foundation SDK](media-foundation-sdk-samples.md)
</dt> <dt>

[Media Foundation trasformazioni](media-foundation-transforms.md)
</dt> <dt>

[Esempio di scala di grigi MFT \_](mft-grayscale-sample.md)
</dt> <dt>

[Scrittura di un MFT personalizzato](writing-a-custom-mft.md)
</dt> </dl>

 

 
