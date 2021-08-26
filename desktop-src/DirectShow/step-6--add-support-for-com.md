---
description: Aggiunta del supporto per COM come parte della scrittura di un filtro di trasformazione. Questo è il passaggio finale di questa esercitazione.
ms.assetid: 53e4f5b7-c85d-4b44-9a0c-0ad05ca872cc
title: Passaggio 6. Aggiunta del supporto per COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 354299ed9ed2f752e0041b82af712e7a9c5411eb7bb7e16588267183442edf68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964901"
---
# <a name="step-6-add-support-for-com"></a>Passaggio 6. Aggiunta del supporto per COM

Questo è il passaggio 6 dell'esercitazione [Scrittura di filtri di trasformazione.](writing-transform-filters.md)

Il passaggio finale consiste nell'aggiungere il supporto per COM.

## <a name="reference-counting"></a>Conteggio dei riferimenti

Non è necessario implementare [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) o [**IUnknown::Release.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) Tutte le classi di filtro e pin derivano da [**CUnknown,**](cunknown.md)che gestisce il conteggio dei riferimenti.

## <a name="queryinterface"></a>QueryInterface

Tutte le classi di filtro e pin implementano [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per tutte le interfacce COM che ereditano. Ad esempio, [**CTransformFilter**](ctransformfilter.md) eredita [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (tramite [**CBaseFilter).**](cbasefilter.md) Se il filtro non espone interfacce aggiuntive, non è necessario eseguire altre operazioni.

Per esporre interfacce aggiuntive, eseguire l'override del [**metodo CUnknown::NonDelegatingQueryInterface.**](cunknown-nondelegatingqueryinterface.md) Si supponga, ad esempio, che il filtro implementi un'interfaccia personalizzata denominata IMyCustomInterface. Per esporre questa interfaccia ai client, eseguire le operazioni seguenti:

-   Derivare la classe di filtro da tale interfaccia.
-   Inserire la macro [**DECLARE \_ IUNKNOWN**](declare-iunknown.md) nella sezione della dichiarazione pubblica.
-   Eseguire [**l'override di NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) per verificare l'IID dell'interfaccia e restituire un puntatore al filtro.

Il codice seguente illustra questi passaggi:


```C++
CMyFilter : public CBaseFilter, public IMyCustomInterface
{
public:
    DECLARE_IUNKNOWN
    STDMETHODIMP NonDelegatingQueryInterface(REFIID iid, void **ppv);
};
STDMETHODIMP CMyFilter::NonDelegatingQueryInterface(REFIID iid, void **ppv)
{
    if (riid == IID_IMyCustomInterface) {
        return GetInterface(static_cast<IMyCustomInterface*>(this), ppv);
    }
    return CBaseFilter::NonDelegatingQueryInterface(riid,ppv);
}
```



Per altre informazioni, vedere [Come implementare IUnknown.](how-to-implement-iunknown.md)

## <a name="object-creation"></a>Creazione di oggetti

Se si prevede di creare un pacchetto del filtro in una DLL e renderlo disponibile ad altri client, è necessario supportare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) e altre funzioni COM correlate. La libreria di classi di base implementa la maggior parte di questo; È sufficiente fornire alcune informazioni sul filtro. Questa sezione offre una breve panoramica delle attività da eseguire. Per informazioni dettagliate, [vedere How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).

Prima di tutto, scrivere un metodo di classe statico che restituisce una nuova istanza del filtro. È possibile assegnare a questo metodo qualsiasi nome, ma la firma deve corrispondere a quella illustrata nell'esempio seguente:


```C++
CUnknown * WINAPI CRleFilter::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr)
{
    CRleFilter *pFilter = new CRleFilter();
    if (pFilter== NULL) 
    {
        *pHr = E_OUTOFMEMORY;
    }
    return pFilter;
}
```



Dichiarare quindi una matrice globale di istanze [**della classe CFactoryTemplate,**](cfactorytemplate.md) denominata *g \_ Templates.* Ogni **classe CFactoryTemplate contiene** informazioni del Registro di sistema per un filtro. Diversi filtri possono risiedere in una singola DLL. includere semplicemente voci **CFactoryTemplate** aggiuntive. È anche possibile dichiarare altri oggetti COM, ad esempio le pagine delle proprietà.


```C++
static WCHAR g_wszName[] = L"My RLE Encoder";
CFactoryTemplate g_Templates[] = 
{
  { 
    g_wszName,
    &CLSID_RLEFilter,
    CRleFilter::CreateInstance,
    NULL,
    NULL
  }
};
```



Definire un intero globale denominato *g \_ cTemplates* il cui valore è uguale alla lunghezza della *matrice \_ templates g:*


```C++
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);  
```



Infine, implementare le funzioni di registrazione dll. L'esempio seguente illustra l'implementazione minima per queste funzioni:


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}
STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



## <a name="filter-registry-entries"></a>Filtrare le voci del Registro di sistema

Negli esempi precedenti viene illustrato come registrare il CLSID di un filtro per COM. Per molti filtri, questa operazione è sufficiente. Il client deve quindi creare il filtro usando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) e aggiungerlo al grafico dei filtri chiamando [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter). In alcuni casi, tuttavia, potrebbe essere necessario fornire informazioni aggiuntive sul filtro nel Registro di sistema. Questa informazione esegue le operazioni seguenti:

-   Consente ai client di individuare il filtro usando [Filter Mapper](filter-mapper.md) o [System Device Enumerator.](system-device-enumerator.md)
-   Consente a Filter Graph Manager di individuare il filtro durante la compilazione automatica del grafo.

L'esempio seguente registra il filtro del codificatore RLE nella categoria video category. Per informazioni dettagliate, [vedere How to Register DirectShow Filters](how-to-register-directshow-filters.md). Leggere la sezione Linee guida [per la registrazione dei filtri,](guidelines-for-registering-filters.md)che descrive le procedure consigliate per la registrazione dei filtri.


```C++
// Declare media type information.
FOURCCMap fccMap = FCC('MRLE'); 
REGPINTYPES sudInputTypes = { &MEDIATYPE_Video, &GUID_NULL };
REGPINTYPES sudOutputTypes = { &MEDIATYPE_Video, (GUID*)&fccMap };

// Declare pin information.
REGFILTERPINS sudPinReg[] = {
    // Input pin.
    { 0, FALSE, // Rendered?
         FALSE, // Output?
         FALSE, // Zero?
         FALSE, // Many?
         0, 0, 
         1, &sudInputTypes  // Media types.
    },
    // Output pin.
    { 0, FALSE, // Rendered?
         TRUE, // Output?
         FALSE, // Zero?
         FALSE, // Many?
         0, 0, 
         1, &sudOutputTypes      // Media types.
    }
};
 
// Declare filter information.
REGFILTER2 rf2FilterReg = {
    1,                // Version number.
    MERIT_DO_NOT_USE, // Merit.
    2,                // Number of pins.
    sudPinReg         // Pointer to pin information.
};

STDAPI DllRegisterServer(void)
{
    HRESULT hr = AMovieDllRegisterServer2(TRUE);
    if (FAILED(hr))
    {
        return hr;
    }
    IFilterMapper2 *pFM2 = NULL;
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);
    if (SUCCEEDED(hr))
    {
        hr = pFM2->RegisterFilter(
            CLSID_RLEFilter,                // Filter CLSID. 
            g_wszName,                       // Filter name.
            NULL,                            // Device moniker. 
            &CLSID_VideoCompressorCategory,  // Video compressor category.
            g_wszName,                       // Instance data.
            &rf2FilterReg                    // Filter information.
            );
        pFM2->Release();
    }
    return hr;
}

STDAPI DllUnregisterServer()
{
    HRESULT hr = AMovieDllRegisterServer2(FALSE);
    if (FAILED(hr))
    {
        return hr;
    }
    IFilterMapper2 *pFM2 = NULL;
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);
    if (SUCCEEDED(hr))
    {
        hr = pFM2->UnregisterFilter(&CLSID_VideoCompressorCategory, 
            g_wszName, CLSID_RLEFilter);
        pFM2->Release();
    }
    return hr;
}
```



Inoltre, i filtri non devono essere in pacchetto all'interno delle DLL. In alcuni casi, è possibile scrivere un filtro specializzato progettato solo per un'applicazione specifica. In tal caso, è possibile compilare la classe di filtro direttamente nell'applicazione e crearla con l'operatore , come `new` illustrato nell'esempio seguente:


```C++
#include "MyFilter.h"  // Header file that declares the filter class.
// Compile and link MyFilter.cpp.
int main()
{
    IBaseFilter *pFilter = 0;
    {
        // Scope to hide pF.
        CMyFilter* pF = new MyFilter();
        if (!pF)
        {
            printf("Could not create MyFilter.\n");
            return 1;
        }
        pF->QueryInterface(IID_IBaseFilter, 
            reinterpret_cast<void**>(&pFilter));
    }
    
    /* Now use pFilter as normal. */
    
    pFilter->Release();  // Deletes the filter.
    return 0;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione Connessione](intelligent-connect.md)
</dt> <dt>

[Scrittura DirectShow filtri](writing-directshow-filters.md)
</dt> <dt>

[Scrittura di filtri di trasformazione](writing-transform-filters.md)
</dt> </dl>

 

 
