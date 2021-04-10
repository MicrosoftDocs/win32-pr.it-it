---
description: Filtro writer ASF WM
ms.assetid: 1b12f65f-8d77-4d38-aad9-92bb15cc0426
title: Filtro del writer ASF WM (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672996124c88632228fff3a84525c9d47f2276b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130458"
---
# <a name="wm-asf-writer-filter-directshow"></a>Filtro del writer ASF WM (DirectShow)

Il writer ASF WM è un filtro wrapper per l'oggetto writer fornito con Windows Media™ Format SDK. Il filtro accetta un numero variabile di flussi di input e crea un file ASF (Advanced Systems Format). Il filtro gestisce tutte le compressioni e il multiplexing (anche se è possibile ignorare il meccanismo di compressione). È possibile usare il writer ASF WM in diversi scenari, tra cui l'acquisizione di video digitali (DV), la ricompressione audio e la conversione di Audio-Video file multimediali con interfoliazione (AVI) o MPEG per lo streaming di rete. Questo filtro rappresenta l'unico modo per creare Microsoft® Windows Media™ file audio e Windows Media Video in Microsoft DirectShow.

Per altre informazioni, vedere [creazione di file ASF in DirectShow](creating-asf-files-in-directshow.md).



|                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter), [**IConfigAsfWriter2**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter2), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), **IPERSISTSTREAM**, **IServiceProvider**, **ISpecifyPropertyPages** inoltre, il filtro espone le seguenti interfacce SDK del formato Windows Media: **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**<br/> |
| Tipi di supporti pin di input                    | Dipende dal profilo ASF. I tipi audio e video in genere non compressi, sebbene il filtro accetti i tipi compressi se corrispondono al profilo ASF.                                                                                                                                                                                                                                                                                                                                             |
| Interfacce pin di input                     | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass), [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), **ISERVICEPROVIDER** inoltre, il pin espone la seguente interfaccia SDK di formato Windows Media: **IWMStreamConfig2** (tramite **IServiceProvider**)<br/>                                                                                                                                                                                 |
| Tipi di supporti pin di output                   | Non applicabile.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Interfacce del PIN di output                    | Non applicabile.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| CLSID filtro                             | \_WMASFWRITER CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| CLSID della pagina delle proprietà                      | \_ASFWRITERPROPERTIES CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| File eseguibile                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Merito](merit.md)                       | il merito non viene \_ \_ \_ utilizzato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Categoria filtro](filter-categories.md) | Non specificato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Commenti

Il filtro richiede Windows Media Format Software Development Kit (SDK) e le relative dipendenze sottostanti.

Numero di pin di input sul filtro che dipendono dal profilo o dall'identificatore del profilo del flusso ASF.

I pin di input supportano un metodo dell'interfaccia **IAMStreamConfig** : [**IAMStreamConfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat). Tutti gli altri metodi restituiscono E \_ NOTIMPL. Chiamare il metodo **GetFormat** per eseguire una query sul formato di compressione della destinazione del PIN, definito dal profilo ASF corrente. Usare l'interfaccia [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) per impostare il profilo.

È possibile utilizzare l'interfaccia **IServiceProvider** del filtro per ottenere un puntatore all'interfaccia **IWMWriterAdvanced2** , definita in Windows Media Format SDK. È possibile usare l'interfaccia **IWMWriterAdvanced2** per controllare il deinterlacciamento dei video quando il video di origine è interlacciato. Per impostare la modalità di deinterlacciamento, chiamare **IWMWriterAdvanced2:: SetInputSetting**. Per il parametro *dwInputNum* , usare l'indice in base zero del PIN di input video, come enumerato dall'interfaccia [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .

Nell'esempio seguente viene illustrato come eseguire una query per questa interfaccia:


```C++
// Assume that pAsfWriter is a valid IBaseFilter pointer.
IServiceProvider *pProvider = NULL;
IWMWriterAdvanced2 *pWMWA2 = NULL;

hr = pAsfWriter->QueryInterface(
    IID_IServiceProvider, 
    (void**)&pProvider
    );
if (SUCCEEDED(hr))
{
    hr = pProvider->QueryService(
        IID_IWMWriterAdvanced2,
        IID_IWMWriterAdvanced2, 
        (void**)&pWMWA2
        );
    pProvider->Release();
    if (SUCCEEDED(hr))
    {
        // Use pWMWA2. (Not shown.)
        pWMWA2->Release();
    }
}
```



Le applicazioni non devono usare alcun metodo **IWMWriterAdvanced** ereditato dall'interfaccia **IWMWriterAdvanced2** . La chiamata di questi metodi può interere con l'operazione del filtro.

L'unica modalità di scrittura di file supportata da questo filtro è la sovrascrittura del \_ file \_ . Vedere [**IFileSinkFilter2:: GetMode**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter2-getmode).

Quando il runtime di Windows Media Format SDK Invia \_ messaggi di stato WMT al filtro del writer ASF WM, il filtro li inoltra come eventi di [**\_ \_ evento WMT EC**](ec-wmt-event.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 




