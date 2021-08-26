---
description: Uso di dmo in DirectShow
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: Uso di dmo in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d056d22e5e9b42795cbe95ce676ac293605453200e0a691d4f0d00374e94cee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078651"
---
# <a name="using-dmos-in-directshow"></a>Uso di dmo in DirectShow

Le applicazioni basate DirectShow possono usare gli oggetti DMO in un grafico di filtro, tramite il [DMO wrapper.](dmo-wrapper-filter.md) Questo filtro aggrega un DMO e gestisce tutti i dettagli dell'uso del DMO, ad esempio il passaggio di dati da e verso il DMO, l'allocazione di oggetti [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) e così via.

Poiché il DMO viene aggregato in base al filtro, l'applicazione può eseguire una query sul filtro per qualsiasi interfaccia COM esponga DMO'applicazione. Tuttavia, l'applicazione deve consentire al filtro di gestire tutte le operazioni di streaming nel DMO. Ad esempio, non impostare tipi di supporti, elaborare buffer, scaricare il DMO, bloccare il DMO, abilitare o disabilitare il controllo qualità o impostare ottimizzazioni video.

Se si conosce l'identificatore di classe (CLSID) di un DMO specifico che si vuole usare, è possibile inizializzare il filtro wrapper DMO con tale DMO, come indicato di seguito:

1.  Chiamare **CoCreateInstance per** creare il filtro DMO wrapper.
2.  Eseguire una query DMO filtro wrapper per [**l'interfaccia IDMOWrapperFilter.**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter)
3.  Chiamare il [**metodo IDMOWrapperFilter::Init.**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) Specificare il CLSID del DMO e il GUID della DMO della categoria. Per un elenco delle DMO, vedere DMO [GUID](dmo-guids.md).

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



La [**funzione DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) enumera gli oggetti DMO nel Registro di sistema. Questa funzione usa un set diverso di GUID di categoria da quelli usati per DirectShow filtri.

**Uso dell'enumeratore del dispositivo di sistema con gli oggetti DMO**

Anziché creare direttamente un DMO, è possibile usare System [Device Enumerator,](system-device-enumerator.md)che può enumerare qualsiasi categoria DMO supportata dal **metodo DMOEnum.** L'enumeratore del dispositivo di sistema include anche gli oggetti DMO quando enumera DirectShow di filtro. Nella tabella seguente viene illustrato il mapping tra DMO categorie e DirectShow categorie.



| Etichetta | Valore |
|-----------------------------|--------------------------------|
| DMO Categoria                | DirectShow Equivalente          |
| CODIFICATORE AUDIO DMOCATEGORY \_ \_ | CLSID \_ AudioCompressorCategory |
| DECODIFICATORE AUDIO DMOCATEGORY \_ \_ | CLSID \_ LegacyAmFilterCategory  |
| CODIFICATORE \_ VIDEO \_ DMOCATEGORY | CLSID \_ VideoCompressorCategory |
| DECODIFICATORE VIDEO DMOCATEGORY \_ \_ | CLSID \_ LegacyAmFilterCategory  |



 

System Device Enumerator restituisce un elenco di oggetti moniker. Se il moniker rappresenta un DMO, il metodo **IMoniker::BindToObject** crea automaticamente il filtro wrapper DMO e lo inizializza con tale DMO. Di conseguenza, il fatto che un DMO sia coinvolto è trasparente per l'applicazione. Per altre informazioni sull'uso di System Device Enumerator, vedere [Using the System Device Enumerator](using-the-system-device-enumerator.md).

**Limitazioni**

Esistono alcune limitazioni quando si usano gli oggetti DMO in DirectShow:

-   Il DMO wrapper non supporta gli oggetti DMO con zero input, più input o zero output.
-   Tutte le connessioni pin nel filtro wrapper DMO usano [**l'interfaccia IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)
-   DirectShow I servizi di modifica non supportano DMO effetti o transizioni basati su criteri.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di dmo](using-dmos.md)
</dt> </dl>

 

 



