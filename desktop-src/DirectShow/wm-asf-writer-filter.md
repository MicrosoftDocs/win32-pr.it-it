---
description: Filtro writer ASF WM
ms.assetid: 1b12f65f-8d77-4d38-aad9-92bb15cc0426
title: Filtro writer ASF WM (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf09a99673b07e88198fd57b95a766ce821eb02
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909279"
---
# <a name="wm-asf-writer-filter-directshow"></a>Filtro writer ASF WM (DirectShow)

WM ASF Writer è un filtro wrapper per l'oggetto writer fornito con Windows Media™ Format SDK. Il filtro accetta un numero variabile di flussi di input e crea un file ASF (Advanced Systems Format). Il filtro gestisce tutta la compressione e il multiplexing (anche se il meccanismo di compressione può essere ignorato). È possibile usare WM ASF Writer in diversi scenari, tra cui acquisizione di video digitali (DV), ricompressione audio e conversione di file multimediali Audio-Video Interleaved (AVI) o MPEG per lo streaming di rete. Questo filtro offre l'unico modo per creare file audio e audio ™ Microsoft®™ windows media e Windows Media Video in Microsoft DirectShow.

Per altre informazioni, vedere [Creazione di file ASF in DirectShow.](creating-asf-files-in-directshow.md)



| Label | Valore |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMFilterMiscFlags,**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IConfigAsfWriter,**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) [**IConfigAsfWriter2,**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter2) [**IFileSinkFilter2,**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) **IPersistStream,** **IServiceProvider,** **ISpecifyPropertyPages** Inoltre, il filtro espone le interfacce di Windows Media Format SDK seguenti: **IWMIndexer2,** **IWMHeaderInfo,** **IWMWriterAdvanced2**<br/> |
| Tipi di supporti pin di input                    | Dipende dal profilo asf. In genere, i tipi audio e video non compressi, sebbene il filtro accetti i tipi compressi se corrispondono al profilo ASF.                                                                                                                                                                                                                                                                                                                                             |
| Interfacce pin di input                     | [**IAMStreamConfig,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) [**IAMWMBufferPass,**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) **IServiceProvider** Inoltre, il pin espone la seguente interfaccia di Windows Media Format SDK: **IWMStreamConfig2** (tramite **IServiceProvider**)<br/>                                                                                                                                                                                 |
| Tipi di supporti pin di output                   | Non applicabile.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Interfacce pin di output                    | Non applicabile.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Filtro CLSID                             | CLSID \_ WMAsfWriter                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| CLSID pagina delle proprietà                      | CLSID \_ AsfWriterProperties                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| File eseguibile                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Merito](merit.md)                       | NON \_ \_ USARE \_                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Categoria filtro](filter-categories.md) | Non specificato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Commenti

Il filtro richiede Windows Media Format Software Development Kit (SDK) e le relative dipendenze sottostanti.

Il numero di pin di input nel filtro dipende dall'identificatore del profilo o del profilo del flusso ASF.

I pin di input supportano un metodo **dall'interfaccia IAMStreamConfig:** [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat). Tutti gli altri metodi restituiscono E \_ NOTIMPL. Chiamare il **metodo GetFormat** per eseguire una query sul formato di compressione di destinazione del pin, definito dal profilo ASF corrente. Usare [**l'interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) per impostare il profilo.

È possibile usare l'interfaccia **IServiceProvider** del filtro per ottenere un puntatore **all'interfaccia IWMWriterAdvanced2,** definita in Windows Media Format SDK. È possibile usare **l'interfaccia IWMWriterAdvanced2** per controllare la risoluzione deinterlacciamento video quando il video di origine è interlacciato. Per impostare la modalità di dinterlacing, chiamare **IWMWriterAdvanced2::SetInputSetting**. Per il *parametro dwInputNum,* usare l'indice in base zero del pin di input video, come enumerato dall'interfaccia [**IEnumPins.**](/windows/desktop/api/Strmif/nn-strmif-ienumpins)

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



Le applicazioni non devono usare i **metodi IWMWriterAdvanced** ereditati dall'interfaccia **IWMWriterAdvanced2.** La chiamata di questi metodi potrebbe interrere con il funzionamento del filtro.

L'unica modalità di scrittura file supportata da questo filtro è AM \_ FILE \_ OVERWRITE. Vedere [**IFileSinkFilter2::GetMode**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter2-getmode).

Quando il runtime di Windows Media Format SDK invia messaggi WMT STATUS al filtro WM ASF Writer, il filtro li inoltra come \_ [**eventi EC \_ WMT \_ EVENT.**](ec-wmt-event.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 




