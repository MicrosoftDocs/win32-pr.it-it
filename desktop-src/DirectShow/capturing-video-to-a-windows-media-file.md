---
description: Acquisizione di video in un file di Windows Media
ms.assetid: cc23bfce-34b9-4976-8602-e0602c7da2af
title: Acquisizione di video in un file di Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6442c1cf3751beac8d4eba751452d9573e9eede
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104234500"
---
# <a name="capturing-video-to-a-windows-media-file"></a>Acquisizione di video in un file di Windows Media

Per acquisire video e codificarlo in un file Windows Media Video (WMV), connettere il pin di acquisizione al filtro di [writer ASF WM](wm-asf-writer-filter.md) , come illustrato nella figura seguente.

![grafico di acquisizione Windows Media](images/vidcap03.png)

Il modo più semplice per creare questo grafico è specificando MEDIASUBTYPE \_ ASF nel metodo [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) :


```C++
IBaseFilter* pASFWriter = 0;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Asf,   // Create a Windows Media file.
    L"C:\\VidCap.wmv",   // File name.
    &pASFWriter,         // Receives a pointer to the filter.
    NULL);  // Receives an IFileSinkFilter interface pointer (optional).
```



Il valore MEDIASUBTYPE \_ ASF indica al generatore del grafico di acquisizione di usare il filtro del writer ASF WM come sink di file. Il generatore del grafico di acquisizione crea il filtro, lo aggiunge al grafo e chiama [**IFileSinkFilter:: myFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) per impostare il nome del file di output. Restituisce un puntatore al filtro come parametro in uscita (


```
pASFWriter
```



Nell'esempio precedente).

Usare l'interfaccia [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) nel writer ASF WM per impostare il profilo Windows Media. È necessario eseguire questa operazione prima di connettere i pin del writer ASF WM.


```C++
IConfigAsfWriter *pConfig = 0;
hr = pASFWriter->QueryInterface(IID_IConfigAsfWriter, (void**)&pConfig);
if (SUCCEEDED(hr))
{
     // Configure the ASF Writer filter.
    pConfig->Release();
}
```



Per ulteriori informazioni sull'impostazione del profilo, vedere [creazione di file ASF in DirectShow](creating-asf-files-in-directshow.md).

Chiamare [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) per connettere il filtro di acquisizione al writer ASF:


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE,   // Capture pin.
    &MEDIATYPE_Video,        // Video. Use MEDIATYPE_Audio for audio.
    pCap,                    // Pointer to the capture filter. 
    0, 
    pASFWriter);             // Pointer to the sink filter (ASF Writer).
```



Ogni pin di input nel filtro WM ASF Writer corrisponde a un flusso nel profilo Windows Media. È necessario connettere ogni pin, in modo che il contenuto del file corrisponda a quello del profilo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione di video in un file](capturing-video-to-a-file.md)
</dt> </dl>

 

 



