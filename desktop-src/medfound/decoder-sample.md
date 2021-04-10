---
description: Viene illustrato come scrivere un decodificatore per Microsoft Media Foundation.
ms.assetid: 941e5400-e679-41f4-9830-3548dc6037aa
title: Esempio di decodificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd7586534876cfa7f530e675b0342a92bf46b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966401"
---
# <a name="decoder-sample"></a>Esempio di decodificatore

Viene illustrato come scrivere un decodificatore per Microsoft Media Foundation.

Questo esempio implementa un decodificatore video MPEG-1 fittizio che Visualizza il codice temporale per ogni fotogramma video. Non decodifica effettivamente il Bitstream MPEG-1. La figura seguente mostra l'output video del decodificatore.

![Screenshot di un frame video dal decodificatore](images/decodersample.png)

> [!Note]  
> Prima del Windows SDK per Windows 7, questo esempio era incluso nell' [esempio MPEG1Source](mpeg1source-sample.md).

 

## <a name="apis-demonstrated"></a>API illustrate

In questo esempio vengono illustrate le interfacce Media Foundation seguenti:

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/Decoder).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Media Foundation SDK](media-foundation-sdk-samples.md)
</dt> <dt>

[Trasformazioni Media Foundation](media-foundation-transforms.md)
</dt> <dt>

[Scrittura di un MFT personalizzato](writing-a-custom-mft.md)
</dt> </dl>

 

 



