---
title: Filtro per writer ASF WM (Windows Media Format 11 SDK)
description: Filtro writer ASF WM
ms.assetid: a902c92e-836d-492c-b2d2-89c216125774
keywords:
- Windows Media Format SDK, WM ASF Writer
- DirectShow, WM-writer ASF
- Filtri QASF, writer ASF WM
- Writer ASF WM, informazioni
- ASF (Advanced Systems Format), writer ASF WM
- ASF (formato avanzato dei sistemi), writer ASF WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0de34bcf4b4047673f832d78f40377f98e94d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300787"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a>Filtro per writer ASF WM (Windows Media Format 11 SDK)

Il filtro del writer ASF WM accetta un numero variabile di flussi di input e crea un file ASF. Il filtro gestisce tutte le compressioni e il multiplexing (anche se è possibile ignorare il meccanismo di compressione). È possibile usare il filtro WM ASF Writer in diversi scenari, tra cui l'acquisizione di video digitali (DV), la ricompressione audio e la conversione di Audio-Video file multimediali con interfoliazione (AVI) o MPEG digitali per lo streaming di rete. Questo filtro rappresenta l'unico modo per creare i file di Microsoft Windows Media Audio e Windows Media Video in DirectShow.

Per altre informazioni, vedere [creazione di file ASF in DirectShow](creating-asf-files-in-directshow.md).

La tabella seguente contiene informazioni sul filtro del writer ASF WM, ad esempio le interfacce e i tipi di supporto supportati.



|                        |                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro      | **IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2** |
| Tipi di supporti pin di input  | Dipendente dal profilo. Tipi generalmente non compressi, ad esempio MEDIATYPE \_ audio o MEDIATYPE \_ video, sebbene i tipi compressi possano essere accettati se corrispondono al profilo                                                   |
| Interfacce pin di input   | **Ipin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (tramite **IServiceProvider**)                                                                         |
| Tipi di supporti pin di output | Non applicabile                                                                                                                                                                                                          |
| Interfacce del PIN di output  | Non applicabile                                                                                                                                                                                                          |
| CLSID filtro           | \_WMASFWRITER CLSID                                                                                                                                                                                                      |
| CLSID della pagina delle proprietà    | \_WMASFWRITERPROPERTIES CLSID                                                                                                                                                                                            |
| File eseguibile             | Qasf.dll                                                                                                                                                                                                                |
| Merito                  | il merito non viene \_ \_ \_ utilizzato                                                                                                                                                                                                     |
| Categoria filtro        | Non specificato                                                                                                                                                                                                           |



 

## <a name="remarks"></a>Commenti

Il numero di pin di input sul filtro dipende dal profilo passato al filtro. Viene creato un pin del tipo di supporto appropriato per ogni flusso definito nel profilo.

I pin di input supportano un metodo dell'interfaccia **IAMStreamConfig** : **IAMStreamConfig:: GetFormat**. Tutti gli altri metodi restituiscono E \_ NOTIMPL. Chiamare il metodo **GetFormat** per eseguire una query sul formato di compressione della destinazione del PIN, definito dal profilo corrente. Usare l'interfaccia [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) per impostare il profilo.

L'interfaccia **IServiceProvider** del filtro consente alle applicazioni di recuperare l'interfaccia [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) , definita in Windows Media Format SDK. L'interfaccia **IWMWriterAdvanced2** controlla la deinterlacciamento dei video ed è utile se l'input è un'origine [*interlacciata*](wmformat-glossary.md) , ad esempio DV (video digitale). Usare i metodi **GetInputSetting** e **SetInputSetting** per controllare la deinterlacciamento. Non è consigliabile che i client usino uno degli altri metodi su questa interfaccia. Questa interfaccia può essere ottenuta solo dopo che il filtro è stato aggiunto al grafico di filtro. Nell'esempio seguente viene illustrato come eseguire una query per questa interfaccia:


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

 

 
