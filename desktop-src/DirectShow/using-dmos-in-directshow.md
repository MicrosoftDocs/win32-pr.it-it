---
description: Uso di DMOs in DirectShow
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: Uso di DMOs in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c90513649756a49067e523390292d4b44e1eac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131886"
---
# <a name="using-dmos-in-directshow"></a>Uso di DMOs in DirectShow

Le applicazioni basate su DirectShow possono usare DMOs in un grafico di filtro, tramite il filtro del [wrapper DMO](dmo-wrapper-filter.md) . Questo filtro aggrega un DMO e gestisce tutti i dettagli dell'uso di DMO, ad esempio il passaggio di dati da e verso DMO, l'allocazione di oggetti [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) e così via.

Poiché il DMO è aggregato dal filtro, l'applicazione può eseguire una query sul filtro per qualsiasi interfaccia COM esposta da DMO. Tuttavia, l'applicazione deve consentire al filtro di gestire tutte le operazioni di streaming sul DMO. Ad esempio, non impostare i tipi di supporto, elaborare i buffer, scaricare il DMO, bloccare il DMO, abilitare o disabilitare il controllo qualità o impostare le ottimizzazioni video.

Se si conosce l'identificatore di classe (CLSID) di un DMO specifico che si vuole usare, è possibile inizializzare il filtro del wrapper DMO con tale DMO, come indicato di seguito:

1.  Chiamare **CoCreateInstance** per creare il filtro del wrapper DMO.
2.  Eseguire una query sul filtro del wrapper DMO per l'interfaccia [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) .
3.  Chiamare il metodo [**IDMOWrapperFilter:: init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) . Specificare il CLSID di DMO e il GUID della categoria DMO. Per un elenco di categorie DMO, vedere [GUID DMO](dmo-guids.md).

Il codice seguente illustra questi passaggi:


```C++
// Create the DMO Wrapper filter.
IBaseFilter *pFilter;
HRESULT hr = CoCreateInstance(CLSID_DMOWrapperFilter, NULL, 
    CLSCTX_INPROC_SERVER, IID_IBaseFilter, 
    reinterpret_cast<void**>(&pFilter));

if (SUCCEEDED(hr)) 
{
    // Query for IDMOWrapperFilter.
    IDMOWrapperFilter *pDmoWrapper;
    hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, 
        reinterpret_cast<void**>(&pDmoWrapper));

    if (SUCCEEDED(hr)) 
    {     
        // Initialize the filter.
        hr = pDmoWrapper->Init(CLSID_MyDMO, DMOCATEGORY_VIDEO_EFFECT); 
        pDmoWrapper->Release();

        if (SUCCEEDED(hr)) 
        {
            // Add the filter to the graph.
            hr = pGraph->AddFilter(pFilter, L"My DMO");
        }
    }
    pFilter->Release();
}
```



La funzione [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) enumera DMOS nel registro di sistema. Questa funzione usa un set di GUID di categoria diverso da quelli usati per i filtri DirectShow.

**Uso di System Device Enumerator con DMOs**

Anziché creare direttamente un DMO, è possibile usare l' [enumeratore del dispositivo di sistema](system-device-enumerator.md), che può enumerare qualsiasi categoria DMO supportata dal metodo **DMOEnum** . L'enumeratore di dispositivo di sistema include anche DMOs quando enumera determinate categorie di filtro DirectShow. La tabella seguente illustra il mapping tra le categorie DMO e le categorie DirectShow.



|                             |                                |
|-----------------------------|--------------------------------|
| Categoria DMO                | Equivalente DirectShow          |
| \_ \_ codificatore audio DMOCATEGORY | \_AUDIOCOMPRESSORCATEGORY CLSID |
| \_decodificatore audio DMOCATEGORY \_ | \_LEGACYAMFILTERCATEGORY CLSID  |
| \_ \_ codificatore video DMOCATEGORY | \_VIDEOCOMPRESSORCATEGORY CLSID |
| \_decodificatore video DMOCATEGORY \_ | \_LEGACYAMFILTERCATEGORY CLSID  |



 

L'enumeratore System Device restituisce un elenco di oggetti moniker. Se il moniker rappresenta un DMO, il metodo **IMoniker:: BindToObject** crea automaticamente il filtro del wrapper DMO e lo inizializza con tale DMO. Pertanto, il fatto che un DMO sia presente è trasparente per l'applicazione. Per ulteriori informazioni sull'utilizzo di System Device Enumerator, vedere [using the System Device Enumerator](using-the-system-device-enumerator.md).

**Limitazioni**

L'uso di DMOs in DirectShow presenta alcune limitazioni:

-   Il filtro del wrapper DMO non supporta DMOs con zero input, più input o zero output.
-   Tutte le connessioni pin sul filtro del wrapper DMO usano l'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .
-   I servizi di modifica DirectShow non supportano gli effetti o le transizioni basati su DMO.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di DMOs](using-dmos.md)
</dt> </dl>

 

 



