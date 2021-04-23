---
description: Uso di DMO in DirectShow
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: Uso di DMO in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdddc643d39798dc09807e9ecfa15c38a6e0c2cf
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908689"
---
# <a name="using-dmos-in-directshow"></a>Uso di DMO in DirectShow

Le applicazioni basate su DirectShow possono usare dmo in un grafico di filtro tramite il filtro [Wrapper DMO.](dmo-wrapper-filter.md) Questo filtro aggrega un DMO e gestisce tutti i dettagli dell'uso di DMO, ad esempio il passaggio di dati da e verso il DMO, l'allocazione di oggetti [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) e così via.

Poiché il DMO viene aggregato dal filtro, l'applicazione può eseguire una query sul filtro per qualsiasi interfaccia COM esponga L'oggetto DMO. Tuttavia, l'applicazione deve consentire al filtro di gestire tutte le operazioni di streaming nel DMO. Ad esempio, non impostare tipi di supporti, elaborare buffer, scaricare il DMO, bloccare il DMO, abilitare o disabilitare il controllo di qualità o impostare ottimizzazioni video.

Se si conosce l'identificatore di classe (CLSID) di un DMO specifico che si vuole usare, è possibile inizializzare il filtro wrapper DMO con tale DMO, come indicato di seguito:

1.  Chiamare **CoCreateInstance per** creare il filtro wrapper DMO.
2.  Eseguire una query sul filtro wrapper DMO per [**l'interfaccia IDMOWrapperFilter.**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter)
3.  Chiamare il [**metodo IDMOWrapperFilter::Init.**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) Specificare il CLSID del DMO e il GUID della categoria del DMO. Per un elenco delle categorie DMO, vedere [GUID DMO](dmo-guids.md).

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



La [**funzione DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) enumera i DMO nel Registro di sistema. Questa funzione usa un set diverso di GUID di categoria rispetto a quelli usati per i filtri DirectShow.

**Uso dell'enumeratore del dispositivo di sistema con dmo**

Anziché creare direttamente un DMO, è possibile usare [l'enumeratore](system-device-enumerator.md)dispositivo di sistema , che può enumerare qualsiasi categoria DMO supportata dal **metodo DMOEnum.** L'enumeratore del dispositivo di sistema include anche dmo quando enumera determinate categorie di filtri DirectShow. La tabella seguente illustra il mapping tra le categorie DMO e le categorie DirectShow.



| Label | Valore |
|-----------------------------|--------------------------------|
| Categoria DMO                | DirectShow equivalente          |
| CODIFICATORE AUDIO DMOCATEGORY \_ \_ | CLSID \_ AudioCompressorCategory |
| DECODIFICATORE AUDIO DMOCATEGORY \_ \_ | CLSID \_ LegacyAmFilterCategory  |
| CODIFICATORE \_ VIDEO \_ DMOCATEGORY | CLSID \_ VideoCompressorCategory |
| DECODIFICATORE VIDEO DMOCATEGORY \_ \_ | CLSID \_ LegacyAmFilterCategory  |



 

System Device Enumerator restituisce un elenco di oggetti moniker. Se il moniker rappresenta un DMO, il metodo **IMoniker::BindToObject** crea automaticamente il filtro wrapper DMO e lo inizializza con tale DMO. Di conseguenza, il fatto che sia coinvolto un DMO è trasparente per l'applicazione. Per altre informazioni sull'uso di System Device Enumerator, vedere [Using the System Device Enumerator](using-the-system-device-enumerator.md).

**Limitazioni**

Esistono alcune limitazioni quando si usano gli oggetti DMO in DirectShow:

-   Il filtro wrapper DMO non supporta gli oggetti DMO con zero input, più input o zero output.
-   Tutte le connessioni pin nel filtro wrapper DMO usano [**l'interfaccia IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)
-   DirectShow Editing Services non supporta effetti o transizioni basati su DMO.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di dmo](using-dmos.md)
</dt> </dl>

 

 



