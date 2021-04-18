---
description: In questo argomento vengono descritti i requisiti per l'implementazione di un pin di output in un filtro di acquisizione DirectShow.
ms.assetid: cb9cda1c-efa2-4abb-934b-21ba8cb80f30
title: Requisiti PIN per i filtri di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a97d3e5c0f7fe0f5a9a341899651685df1cdd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303884"
---
# <a name="pin-requirements-for-capture-filters"></a>Requisiti PIN per i filtri di acquisizione

In questo argomento vengono descritti i requisiti per l'implementazione di un pin di output in un filtro di acquisizione DirectShow.

## <a name="pin-name"></a>Nome pin

È possibile assegnare un nome al pin. Se il nome del pin inizia con il carattere tilde (~), il gestore del grafico del filtro non esegue automaticamente il rendering del PIN quando un'applicazione chiama [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile). Se, ad esempio, il filtro ha un pin di acquisizione e un pin di anteprima, è possibile denominarli rispettivamente "~ Capture" e "Preview". Se un'applicazione esegue il rendering di tale filtro in un grafico, il pin di anteprima si connetterà al renderer predefinito e nessun elemento si connetterà al pin di acquisizione, che è un comportamento predefinito accettabile. Questo può essere applicato anche ai pin che forniscono dati informativi che non devono essere sottoposti a rendering o pin per i quali è necessario impostare proprietà personalizzate. Si noti che i pin con il prefisso tilde (~) possono comunque essere connessi manualmente dall'applicazione.

## <a name="pin-category"></a>Categoria pin

Un filtro di acquisizione ha sempre un pin di acquisizione e potrebbe avere un pin di anteprima. Alcuni filtri di acquisizione potrebbero avere altri pin di output, per fornire altri tipi di dati, ad esempio le informazioni di controllo. Ogni pin di output deve esporre l'interfaccia [**IKsPropertySet**](ikspropertyset.md) . Le applicazioni utilizzano questa interfaccia per determinare la categoria del PIN. Il pin restituisce in genere l' \_ anteprima dell'acquisizione della categoria pin \_ o della \_ categoria pin \_ . Per altre informazioni, vedere [pin set di proprietà](pin-property-set.md).

Nell'esempio seguente viene illustrato come implementare [**IKsPropertySet**](ikspropertyset.md) per restituire la categoria pin in un pin di acquisizione:


```C++
// Set: Cannot set any properties.
HRESULT CMyCapturePin::Set(REFGUID guidPropSet, DWORD dwID,
    void *pInstanceData, DWORD cbInstanceData, void *pPropData, 
    DWORD cbPropData)
{
    return E_NOTIMPL;
}

// Get: Return the pin category (our only property). 
HRESULT CMyCapturePin::Get(
    REFGUID guidPropSet,   // Which property set.
    DWORD dwPropID,        // Which property in that set.
    void *pInstanceData,   // Instance data (ignore).
    DWORD cbInstanceData,  // Size of the instance data (ignore).
    void *pPropData,       // Buffer to receive the property data.
    DWORD cbPropData,      // Size of the buffer.
    DWORD *pcbReturned     // Return the size of the property.
)
{
    if (guidPropSet != AMPROPSETID_Pin) 
        return E_PROP_SET_UNSUPPORTED;
    if (dwPropID != AMPROPERTY_PIN_CATEGORY)
        return E_PROP_ID_UNSUPPORTED;
    if (pPropData == NULL && pcbReturned == NULL)
        return E_POINTER;
    if (pcbReturned)
        *pcbReturned = sizeof(GUID);
    if (pPropData == NULL)  // Caller just wants to know the size.
        return S_OK;
    if (cbPropData < sizeof(GUID)) // The buffer is too small.
        return E_UNEXPECTED;
    *(GUID *)pPropData = PIN_CATEGORY_CAPTURE;
    return S_OK;
}

// QuerySupported: Query whether the pin supports the specified property.
HRESULT CMyCapturePin::QuerySupported(REFGUID guidPropSet, DWORD dwPropID,
    DWORD *pTypeSupport)
{
    if (guidPropSet != AMPROPSETID_Pin)
        return E_PROP_SET_UNSUPPORTED;
    if (dwPropID != AMPROPERTY_PIN_CATEGORY)
        return E_PROP_ID_UNSUPPORTED;
    if (pTypeSupport)
        // We support getting this property, but not setting it.
        *pTypeSupport = KSPROPERTY_SUPPORT_GET; 
    return S_OK;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura dei filtri di acquisizione](writing-capture-filters.md)
</dt> </dl>

 

 



