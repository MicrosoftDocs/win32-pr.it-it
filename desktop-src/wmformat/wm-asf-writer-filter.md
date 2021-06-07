---
title: Filtro WRITER ASF WM (Windows Media Format 11 SDK)
description: Informazioni sul filtro WM ASF Writer.
ms.assetid: a902c92e-836d-492c-b2d2-89c216125774
keywords:
- Windows Media Format SDK,WM ASF Writer
- DirectShow, WM ASF Writer
- filtri QASF, WM ASF Writer
- WM ASF Writer,about
- Advanced Systems Format (ASF),WM ASF Writer
- ASF (Advanced Systems Format),WM ASF Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fbd6e36a8178f6ebd1943cdaac214597e0ba4e
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444702"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a>Filtro WRITER ASF WM (Windows Media Format 11 SDK)

Il filtro WM ASF Writer accetta un numero variabile di flussi di input e crea un file ASF. Il filtro gestisce tutti i tipi di compressione e multiplexing (anche se il meccanismo di compressione può essere ignorato). È possibile usare il filtro WM ASF Writer in vari scenari, tra cui l'acquisizione di video digitali (DV), la ricompressione audio e la conversione di file multimediali digitali Audio-Video interleaved (AVI) o MPEG per lo streaming di rete. Questo filtro rappresenta l'unico modo per creare file Windows Media Audio e Windows Media Video Microsoft in DirectShow.

Per altre informazioni, vedere [Creazione di file ASF in DirectShow.](creating-asf-files-in-directshow.md)

La tabella seguente contiene informazioni sul filtro WM ASF Writer, ad esempio le interfacce e i tipi di supporto supportati.



| Filtrare le informazioni                       |  Tipi                                                                                                                                                                                                                       |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro      | **IAMFilterMiscFlags,** **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2** |
| Tipi di supporti pin di input  | Dipende dal profilo. In genere tipi non compressi come MEDIATYPE Audio o MEDIATYPE Video, anche se i tipi compressi possono essere accettati \_ \_ se corrispondono al profilo                                                   |
| Interfacce pin di input   | **IPin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (tramite **IServiceProvider**)                                                                         |
| Tipi di supporti pin di output | Non applicabile                                                                                                                                                                                                          |
| Interfacce pin di output  | Non applicabile                                                                                                                                                                                                          |
| CLSID del filtro           | CLSID \_ WMAsfWriter                                                                                                                                                                                                      |
| CLSID pagina delle proprietà    | CLSID \_ WMAsfWriterProperties                                                                                                                                                                                            |
| File eseguibile             | Qasf.dll                                                                                                                                                                                                                |
| Merito                  | NON \_ \_ USARE \_                                                                                                                                                                                                     |
| Categoria filtro        | Non specificato                                                                                                                                                                                                           |



 

## <a name="remarks"></a>Commenti

Il numero di pin di input nel filtro dipende dal profilo passato al filtro. Viene creato un pin del tipo di supporto appropriato per ogni flusso definito nel profilo.

I pin di input supportano un metodo **dall'interfaccia IAMStreamConfig:** **IAMStreamConfig::GetFormat**. Tutti gli altri metodi restituiscono E \_ NOTIMPL. Chiamare il **metodo GetFormat** per eseguire una query sul formato di compressione di destinazione del pin, definito dal profilo corrente. Usare [**l'interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) per impostare il profilo.

L'interfaccia **IServiceProvider** del filtro consente alle applicazioni di recuperare [**l'interfaccia IWMWriterAdvanced2,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) definita in Windows Media Format SDK. **L'interfaccia IWMWriterAdvanced2** controlla la risoluzione deinterlacciamento video ed è utile se l'input è un'origine [*interlacciata,*](wmformat-glossary.md) ad esempio DV (video digitale). Usare i **metodi GetInputSetting** **e SetInputSetting** per controllare la deinterlacing. Non è consigliabile che i client usino uno degli altri metodi in questa interfaccia. Questa interfaccia può essere ottenuta solo dopo l'aggiunta del filtro al grafico dei filtri. Nell'esempio seguente viene illustrato come eseguire una query per questa interfaccia:


```C++
// Assume that m_pGraph is a valid IGraphBuilder interface pointer,
// and that pAsfWriter points to the IBaseFilter interface
// on the WM ASF Writer filter.

IServiceProvider *pProvider = NULL;
IWMWriterAdvanced2 *pWMWA2 = NULL;

hr = m_pGraph->AddFilter(pAsfWriter, L"WM ASF Writer");
...
hr = pAsfWriter->QueryInterface(IID_IServiceProvider, (void**)&pProvider)
if (SUCCEEDED(hr))
{
    hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
        IID_IWMWriterAdvanced2, (void**)&pWMWA2);
    pProvider->Release();
}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento su DirectShow QASF**](directshow-qasf-reference.md)
</dt> </dl>

 

 
