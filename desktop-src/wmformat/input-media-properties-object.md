---
title: Oggetto proprietà supporti di input
description: Oggetto proprietà supporti di input
ms.assetid: e7aa6c99-b6b3-4e5b-869d-3387f70dad87
keywords:
- Windows Media Format SDK, oggetti proprietà supporti di input
- ASF (Advanced Systems Format), oggetti proprietà dei supporti di input
- ASF (formato avanzato dei sistemi), oggetti proprietà supporti di input
- oggetti, oggetti proprietà supporti di input
- oggetti proprietà supporti di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beddda23ab7be86c3cb522edb8e811978c0c9ed9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103857994"
---
# <a name="input-media-properties-object"></a>Oggetto proprietà supporti di input

Un oggetto proprietà del supporto di input creato dall'oggetto Writer supporta le interfacce seguenti. È possibile accedere a queste interfacce mediante una chiamata a **QueryInterface** su una delle interfacce dell'oggetto writer.



| Interfaccia                                        | Descrizione                                                                                                |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) | Recupera le proprietà di un flusso di input.                                                               |
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | Usato come interfaccia di base per le altre interfacce di proprietà del supporto (input, output e video).             |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | Gestisce le proprietà di un flusso video. Si tratta di un'interfaccia facoltativa, disponibile solo per i flussi video. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Oggetto writer**](writer-object.md)
</dt> </dl>

 

 




