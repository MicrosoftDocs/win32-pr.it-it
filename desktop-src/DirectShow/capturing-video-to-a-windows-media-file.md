---
description: Acquisizione di video in un Windows multimediale
ms.assetid: cc23bfce-34b9-4976-8602-e0602c7da2af
title: Acquisizione di video in un Windows multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3268d3a3df4a24c5836dba81f7ef4cf0b872907f09367d3212d27c38c0dd4414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158706"
---
# <a name="capturing-video-to-a-windows-media-file"></a>Acquisizione di video in un Windows multimediale

Per acquisire video e codificarlo in un file di Windows Media Video (WMV), connettere il pin di acquisizione al filtro [WM ASF Writer,](wm-asf-writer-filter.md) come illustrato nel diagramma seguente.

![Grafico di Windows Media Capture](images/vidcap03.png)

Il modo più semplice per creare questo grafo è specificare MEDIASUBTYPE \_ Asf nel [**metodo ICaptureGraphBuilder2::SetOutputFileName:**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename)


```C++
IBaseFilter* pASFWriter = 0;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Asf,   // Create a Windows Media file.
    L"C:\\VidCap.wmv",   // File name.
    &pASFWriter,         // Receives a pointer to the filter.
    NULL);  // Receives an IFileSinkFilter interface pointer (optional).
```



Il valore MEDIASUBTYPE Asf indica a Capture Graph Builder di usare il filtro \_ WM ASF Writer come sink del file. Capture Graph Builder crea il filtro, lo aggiunge al grafo e chiama [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) per impostare il nome del file di output. Restituisce un puntatore al filtro come parametro in uscita (


```
pASFWriter
```



nell'esempio precedente).

Usare [**l'interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) in WM ASF Writer per impostare il Windows media. È necessario eseguire questa operazione prima di connettere eventuali segnaposto in WM ASF Writer.


```C++
IConfigAsfWriter *pConfig = 0;
hr = pASFWriter->QueryInterface(IID_IConfigAsfWriter, (void**)&pConfig);
if (SUCCEEDED(hr))
{
     // Configure the ASF Writer filter.
    pConfig->Release();
}
```



Per altre informazioni sull'impostazione del profilo, vedere [Creazione di file ASF in DirectShow](creating-asf-files-in-directshow.md).

Chiamare [**ICaptureGraphBuilder2::RenderStream per**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) connettere il filtro di acquisizione al writer ASF:


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE,   // Capture pin.
    &MEDIATYPE_Video,        // Video. Use MEDIATYPE_Audio for audio.
    pCap,                    // Pointer to the capture filter. 
    0, 
    pASFWriter);             // Pointer to the sink filter (ASF Writer).
```



Ogni pin di input nel filtro DI WM ASF Writer corrisponde a un flusso nel Windows media. È necessario connettere ogni pin, in modo che il contenuto del file corrisponda al profilo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione di video in un file](capturing-video-to-a-file.md)
</dt> </dl>

 

 



