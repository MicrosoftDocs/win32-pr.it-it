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
# <a name="pin-requirements-for-capture-filters"></a><span data-ttu-id="d02af-103">Requisiti PIN per i filtri di acquisizione</span><span class="sxs-lookup"><span data-stu-id="d02af-103">Pin Requirements for Capture Filters</span></span>

<span data-ttu-id="d02af-104">In questo argomento vengono descritti i requisiti per l'implementazione di un pin di output in un filtro di acquisizione DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d02af-104">This topic describes the requirements for implementing an output pin on a DirectShow capture filter.</span></span>

## <a name="pin-name"></a><span data-ttu-id="d02af-105">Nome pin</span><span class="sxs-lookup"><span data-stu-id="d02af-105">Pin Name</span></span>

<span data-ttu-id="d02af-106">È possibile assegnare un nome al pin.</span><span class="sxs-lookup"><span data-stu-id="d02af-106">You can give a pin any name.</span></span> <span data-ttu-id="d02af-107">Se il nome del pin inizia con il carattere tilde (~), il gestore del grafico del filtro non esegue automaticamente il rendering del PIN quando un'applicazione chiama [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile).</span><span class="sxs-lookup"><span data-stu-id="d02af-107">If the pin name begins with the tilde (~) character, the Filter Graph Manager does not automatically render that pin when an application calls [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile).</span></span> <span data-ttu-id="d02af-108">Se, ad esempio, il filtro ha un pin di acquisizione e un pin di anteprima, è possibile denominarli rispettivamente "~ Capture" e "Preview".</span><span class="sxs-lookup"><span data-stu-id="d02af-108">For example, if the filter has a capture pin and a preview pin, you might name them "~Capture" and "Preview," respectively.</span></span> <span data-ttu-id="d02af-109">Se un'applicazione esegue il rendering di tale filtro in un grafico, il pin di anteprima si connetterà al renderer predefinito e nessun elemento si connetterà al pin di acquisizione, che è un comportamento predefinito accettabile.</span><span class="sxs-lookup"><span data-stu-id="d02af-109">If an application renders that filter in a graph, the preview pin will connect to its default renderer, and nothing will connect to the capture pin, which is a reasonable default behavior.</span></span> <span data-ttu-id="d02af-110">Questo può essere applicato anche ai pin che forniscono dati informativi che non devono essere sottoposti a rendering o pin per i quali è necessario impostare proprietà personalizzate.</span><span class="sxs-lookup"><span data-stu-id="d02af-110">This can also apply to pins that deliver informational data that is not meant to be rendered, or pins that need custom properties set.</span></span> <span data-ttu-id="d02af-111">Si noti che i pin con il prefisso tilde (~) possono comunque essere connessi manualmente dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d02af-111">Note that pins with the tilde (~) prefix can still be connected manually by the application.</span></span>

## <a name="pin-category"></a><span data-ttu-id="d02af-112">Categoria pin</span><span class="sxs-lookup"><span data-stu-id="d02af-112">Pin Category</span></span>

<span data-ttu-id="d02af-113">Un filtro di acquisizione ha sempre un pin di acquisizione e potrebbe avere un pin di anteprima.</span><span class="sxs-lookup"><span data-stu-id="d02af-113">A capture filter always has a capture pin, and might have a preview pin.</span></span> <span data-ttu-id="d02af-114">Alcuni filtri di acquisizione potrebbero avere altri pin di output, per fornire altri tipi di dati, ad esempio le informazioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="d02af-114">Some capture filters might have other output pins, to deliver other types of data, such as control information.</span></span> <span data-ttu-id="d02af-115">Ogni pin di output deve esporre l'interfaccia [**IKsPropertySet**](ikspropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="d02af-115">Each output pin must expose the [**IKsPropertySet**](ikspropertyset.md) interface.</span></span> <span data-ttu-id="d02af-116">Le applicazioni utilizzano questa interfaccia per determinare la categoria del PIN.</span><span class="sxs-lookup"><span data-stu-id="d02af-116">Applications use this interface to determine the pin category.</span></span> <span data-ttu-id="d02af-117">Il pin restituisce in genere l' \_ anteprima dell'acquisizione della categoria pin \_ o della \_ categoria pin \_ .</span><span class="sxs-lookup"><span data-stu-id="d02af-117">The pin typically returns either PIN\_CATEGORY\_CAPTURE or PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="d02af-118">Per altre informazioni, vedere [pin set di proprietà](pin-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="d02af-118">For more information, see [Pin Property Set](pin-property-set.md).</span></span>

<span data-ttu-id="d02af-119">Nell'esempio seguente viene illustrato come implementare [**IKsPropertySet**](ikspropertyset.md) per restituire la categoria pin in un pin di acquisizione:</span><span class="sxs-lookup"><span data-stu-id="d02af-119">The following example shows how to implement [**IKsPropertySet**](ikspropertyset.md) to return the pin category on a capture pin:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d02af-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d02af-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d02af-121">Scrittura dei filtri di acquisizione</span><span class="sxs-lookup"><span data-stu-id="d02af-121">Writing Capture Filters</span></span>](writing-capture-filters.md)
</dt> </dl>

 

 



