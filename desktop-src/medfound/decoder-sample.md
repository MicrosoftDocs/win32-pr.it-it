---
description: Illustra come scrivere un decodificatore per Microsoft Media Foundation.
ms.assetid: 941e5400-e679-41f4-9830-3548dc6037aa
title: Esempio di decodificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 290f8b2db32b12d535feaeef65f37b77e1a29115cd8844a8d8aad29fb7ce699a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449387"
---
# <a name="decoder-sample"></a>Esempio di decodificatore

Illustra come scrivere un decodificatore per Microsoft Media Foundation.

Questo esempio implementa un decodificatore video MPEG-1 fittizio che visualizza il time code per ogni fotogramma video. Non decodifica effettivamente il flusso di bit MPEG-1. L'immagine seguente mostra l'output video del decodificatore.

![screenshot di un fotogramma video dal decodificatore](images/decodersample.png)

> [!Note]  
> Prima dell'SDK Windows per Windows 7, questo esempio era incluso come parte dell'esempio [MPEG1Source](mpeg1source-sample.md).

 

## <a name="apis-demonstrated"></a>DIMOSTRAZIONE DELLE API

In questo esempio vengono illustrate le Media Foundation seguenti:

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nel [repository github Windows esempi classici.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/Decoder)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Media Foundation SDK](media-foundation-sdk-samples.md)
</dt> <dt>

[Media Foundation trasformazioni](media-foundation-transforms.md)
</dt> <dt>

[Scrittura di un MFT personalizzato](writing-a-custom-mft.md)
</dt> </dl>

 

 



