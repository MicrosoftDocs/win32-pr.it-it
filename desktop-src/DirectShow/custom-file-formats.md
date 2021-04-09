---
description: Formati di file personalizzati
ms.assetid: 4dc77cfa-0cab-4055-9e11-f036e2d1dcca
title: Formati di file personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 361dca97fcd34b30e3c29d6ba189ad26968d4fbb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965695"
---
# <a name="custom-file-formats"></a>Formati di file personalizzati

Se si dispone di un filtro MUX o di un file writer personalizzato che supporta il proprio formato di file, è possibile specificare il CLSID come primo parametro del metodo [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) :


```C++
IBaseFilter *pMux = 0;
IFileSinkFilter *pSink = 0;
hr = pBuild->SetOutputFileName(&CLSID_MyCustomMuxFilter, 
    L"C:\\VidCap.avi", &pMux, &pSink);
```



Per ulteriori informazioni su questo utilizzo, vedere [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione di video in un file](capturing-video-to-a-file.md)
</dt> </dl>

 

 



