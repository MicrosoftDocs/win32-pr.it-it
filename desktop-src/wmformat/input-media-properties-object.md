---
title: Oggetto Input Media Properties
description: Oggetto Input Media Properties
ms.assetid: e7aa6c99-b6b3-4e5b-869d-3387f70dad87
keywords:
- Windows Media Format SDK, oggetti proprietà multimediali di input
- Advanced Systems Format (ASF), oggetti proprietà multimediali di input
- ASF (Advanced Systems Format), oggetti proprietà multimediali di input
- oggetti, oggetti proprietà multimediali di input
- oggetti proprietà supporti di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf5fac14de1c0fdc6619ab0dfe61feb9fcf577acb5c22dc2243a96d943921c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809031"
---
# <a name="input-media-properties-object"></a>Oggetto Input Media Properties

Un oggetto proprietà multimediali di input creato dall'oggetto writer supporta le interfacce seguenti. Queste interfacce sono accessibili da una chiamata a **QueryInterface** su una delle interfacce dell'oggetto writer.



| Interfaccia                                        | Descrizione                                                                                                |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) | Recupera le proprietà di un flusso di input.                                                               |
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | Usato come interfaccia di base per le altre interfacce di proprietà multimediali (input, output e video).             |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | Gestisce le proprietà di un flusso video. Si tratta di un'interfaccia facoltativa, disponibile solo per i flussi video. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Oggetto writer**](writer-object.md)
</dt> </dl>

 

 




