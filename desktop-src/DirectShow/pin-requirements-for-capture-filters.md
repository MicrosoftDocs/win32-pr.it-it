---
description: Questo argomento descrive i requisiti per l'implementazione di un pin di output in un filtro DirectShow di acquisizione.
ms.assetid: cb9cda1c-efa2-4abb-934b-21ba8cb80f30
title: Requisiti di aggiunta per i filtri di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e72c74f06970bf6124d0e5dffea458bb41bcd0a19db44acc71a51615aa2fee8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119316111"
---
# <a name="pin-requirements-for-capture-filters"></a>Requisiti di aggiunta per i filtri di acquisizione

Questo argomento descrive i requisiti per l'implementazione di un pin di output in un filtro DirectShow di acquisizione.

## <a name="pin-name"></a>Nome pin

È possibile assegnare un segnaposto a qualsiasi nome. Se il nome del pin inizia con il carattere tilde (~), Filter Graph Manager non esegue automaticamente il rendering del pin quando un'applicazione chiama [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile). Ad esempio, se il filtro ha un segnaposto di acquisizione e un segnaposto di anteprima, è possibile assegnare loro rispettivamente il nome "~Capture" e "Preview". Se un'applicazione esegue il rendering di tale filtro in un grafico, il segnaposto di anteprima si connetterà al renderer predefinito e nulla si connetterà al pin di acquisizione, che è un comportamento predefinito ragionevole. Ciò può essere applicato anche ai pin che recapitare dati in formato informativo di cui non è necessario eseguire il rendering o ai pin per cui è necessario impostare proprietà personalizzate. Si noti che i pin con il prefisso tilde (~) possono comunque essere connessi manualmente dall'applicazione.

## <a name="pin-category"></a>Aggiungi categoria

Un filtro di acquisizione ha sempre un pin di acquisizione e potrebbe avere un segnaposto di anteprima. Alcuni filtri di acquisizione potrebbero avere altri pin di output, per distribuire altri tipi di dati, ad esempio le informazioni di controllo. Ogni pin di output deve esporre [**l'interfaccia IKsPropertySet.**](ikspropertyset.md) Le applicazioni usano questa interfaccia per determinare la categoria di pin. Il pin restituisce in genere PIN \_ CATEGORY CAPTURE o PIN CATEGORY \_ \_ \_ PREVIEW. Per altre informazioni, vedere [Aggiungere un set di proprietà.](pin-property-set.md)

L'esempio seguente illustra come implementare [**IKsPropertySet**](ikspropertyset.md) per restituire la categoria del pin su un pin di acquisizione:


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

[Scrittura di filtri di acquisizione](writing-capture-filters.md)
</dt> </dl>

 

 



