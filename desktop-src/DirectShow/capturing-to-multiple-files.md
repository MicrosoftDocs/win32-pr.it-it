---
description: Acquisizione in più file
ms.assetid: 6073a891-e9f5-442d-a2d9-3a7b97f7f735
title: Acquisizione in più file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79ce7a1b4b91a0f78031a661e2c2e10895b4a21b1cfb068ca505429468a3af1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017579"
---
# <a name="capturing-to-multiple-files"></a>Acquisizione in più file

Dopo aver acquisito un video in un file, è possibile passare a un nuovo file arrestando il grafo e impostando il nome del file nel [filtro Writer file.](file-writer-filter.md) Chiamare il [**metodo IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) nel writer di file. È possibile ottenere un puntatore [**all'interfaccia IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) quando si compila il grafo, tramite il *parametro pSink* del metodo SetOutputFileName. Nel codice seguente viene illustrato come eseguire questa operazione:


```C++
IBaseFilter *pMux;
IFileSinkFilter *pSink
hr = pBuild->SetOutputFileName(&MEDIASUBTYPE_Avi, L"C:\\YourFileName.avi", 
    &pMux, &pSink);
if (SUCCEEDED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, 
        pCap, NULL, pMux);

    if (SUCCEEDED(hr))
    {
        pControl->Run();
        /* Wait awhile, then stop the graph. */
        pControl->Stop();
        // Change the file name and run the graph again.
        pSink->SetFileName(L"YourFileName02.avi", 0);
        pControl->Run();
    }
    pMux->Release();
    pSink->Release();
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione di video in un file](capturing-video-to-a-file.md)
</dt> </dl>

 

 



