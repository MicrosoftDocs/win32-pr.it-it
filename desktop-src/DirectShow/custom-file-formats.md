---
description: Formati di file personalizzati
ms.assetid: 4dc77cfa-0cab-4055-9e11-f036e2d1dcca
title: Formati di file personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a478e7818701008c31d1d0c5a6e4924540ed818be19f7b50fe3ed278aa6f3ba6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998691"
---
# <a name="custom-file-formats"></a>Formati di file personalizzati

Se si dispone di un filtro mux personalizzato o writer di file che supporta il proprio formato di file, è possibile specificare il CLSID come primo parametro del [**metodo ICaptureGraphBuilder2::SetOutputFileName:**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename)


```C++
IBaseFilter *pMux = 0;
IFileSinkFilter *pSink = 0;
hr = pBuild->SetOutputFileName(&CLSID_MyCustomMuxFilter, 
    L"C:\\VidCap.avi", &pMux, &pSink);
```



Per altre informazioni su questo utilizzo, vedere [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione di video in un file](capturing-video-to-a-file.md)
</dt> </dl>

 

 



