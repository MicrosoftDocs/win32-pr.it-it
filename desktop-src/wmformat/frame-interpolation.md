---
title: Interpolazione frame
description: Interpolazione frame
ms.assetid: 74dbe855-361c-42ba-b21b-322ccd1c91d0
keywords:
- Windows Media Format SDK, interpolazione frame
- codec, interpolazione frame
- interpolazione frame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c62f95322920576eec0f10f3e4d61a279fdc4cf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046310"
---
# <a name="frame-interpolation"></a>Interpolazione frame

L'interpolazione dei frame è il processo di creazione di fotogrammi video intermedi basati sui dati in due frame consecutivi di video codificato. L'interpolazione del frame aumenta in effetti la [*frequenza dei fotogrammi*](wmformat-glossary.md) del video codificato al momento della decodifica. È possibile usare l'interpolazione dei frame per migliorare la fluidità della riproduzione per i flussi video con frequenze di frame ridotte.

Poiché si tratta di una funzionalità di decodifica, non implica alcuna opzione di codifica speciale e non aggiunge alcun sovraccarico al contenuto. L'interpolazione dei frame viene specificata come impostazione di output nell'oggetto Reader.

Solo il codec Windows Media Video 9 supporta l'interpolazione dei frame.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di codec**](codec-features.md)
</dt> <dt>

[**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)
</dt> <dt>

[**Impostazioni di output**](output-settings.md)
</dt> </dl>

 

 




