---
description: Un attributo è una coppia chiave/valore, dove la chiave è un GUID e il valore è un PROPVARIANT. Gli attributi vengono utilizzati in tutti i Microsoft Media Foundation per configurare gli oggetti, descrivere i formati multimediali, le proprietà degli oggetti query e altri scopi.
ms.assetid: 44af5e03-5f0a-4564-b9d6-b8c935df35b2
title: Attributi in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e7893586aa1e966b95c1af5d04246bbb0c82ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749383"
---
# <a name="attributes-in-media-foundation"></a><span data-ttu-id="40ff1-104">Attributi in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="40ff1-104">Attributes in Media Foundation</span></span>

<span data-ttu-id="40ff1-105">Un attributo è una coppia chiave/valore, dove la chiave è un GUID e il valore è un **PROPVARIANT**.</span><span class="sxs-lookup"><span data-stu-id="40ff1-105">An attribute is a key/value pair, where the key is a GUID and the value is a **PROPVARIANT**.</span></span> <span data-ttu-id="40ff1-106">Gli attributi vengono utilizzati in tutti i Microsoft Media Foundation per configurare gli oggetti, descrivere i formati multimediali, le proprietà degli oggetti query e altri scopi.</span><span class="sxs-lookup"><span data-stu-id="40ff1-106">Attributes are used throughout Microsoft Media Foundation to configure objects, describe media formats, query object properties, and other purposes.</span></span>

<span data-ttu-id="40ff1-107">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="40ff1-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="40ff1-108">Informazioni sugli attributi</span><span class="sxs-lookup"><span data-stu-id="40ff1-108">About Attributes</span></span>](#about-attributes)
-   [<span data-ttu-id="40ff1-109">Serializzazione degli attributi</span><span class="sxs-lookup"><span data-stu-id="40ff1-109">Serializing Attributes</span></span>](#serializing-attributes)
-   [<span data-ttu-id="40ff1-110">Implementazione di IMFAttributes</span><span class="sxs-lookup"><span data-stu-id="40ff1-110">Implementing IMFAttributes</span></span>](#implementing-imfattributes)
-   [<span data-ttu-id="40ff1-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="40ff1-111">Related topics</span></span>](#related-topics)

## <a name="about-attributes"></a><span data-ttu-id="40ff1-112">Informazioni sugli attributi</span><span class="sxs-lookup"><span data-stu-id="40ff1-112">About Attributes</span></span>

<span data-ttu-id="40ff1-113">Un attributo è una coppia chiave/valore, dove la chiave è un GUID e il valore è un **PROPVARIANT**.</span><span class="sxs-lookup"><span data-stu-id="40ff1-113">An attribute is a key/value pair, where the key is a GUID and the value is a **PROPVARIANT**.</span></span> <span data-ttu-id="40ff1-114">I valori degli attributi sono limitati ai tipi di dati seguenti:</span><span class="sxs-lookup"><span data-stu-id="40ff1-114">Attribute values are restricted to the following data types:</span></span>

-   <span data-ttu-id="40ff1-115">Intero senza segno a 32 bit (**UInt32**).</span><span class="sxs-lookup"><span data-stu-id="40ff1-115">Unsigned 32-bit integer (**UINT32**).</span></span>
-   <span data-ttu-id="40ff1-116">Intero senza segno a 64 bit (**UInt64**).</span><span class="sxs-lookup"><span data-stu-id="40ff1-116">Unsigned 64-bit integer (**UINT64**).</span></span>
-   <span data-ttu-id="40ff1-117">numero a virgola mobile a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="40ff1-117">64-bit floating-point number.</span></span>
-   <span data-ttu-id="40ff1-118">GUID.</span><span class="sxs-lookup"><span data-stu-id="40ff1-118">GUID.</span></span>
-   <span data-ttu-id="40ff1-119">Stringa di caratteri "wide" con terminazione Null.</span><span class="sxs-lookup"><span data-stu-id="40ff1-119">Null-terminated wide-character string.</span></span>
-   <span data-ttu-id="40ff1-120">Matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="40ff1-120">Byte array.</span></span>
-   <span data-ttu-id="40ff1-121">Puntatore **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="40ff1-121">**IUnknown** pointer.</span></span>

<span data-ttu-id="40ff1-122">Questi tipi sono definiti nell'enumerazione [**del \_ \_ tipo di attributo MF**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_type) .</span><span class="sxs-lookup"><span data-stu-id="40ff1-122">These types are defined in the [**MF\_ATTRIBUTE\_TYPE**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_type) enumeration.</span></span> <span data-ttu-id="40ff1-123">Per impostare o recuperare i valori di attributo, utilizzare l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="40ff1-123">To set or retrieve attribute values, use the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="40ff1-124">Questa interfaccia contiene metodi indipendenti dai tipi per ottenere e impostare i valori in base al tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="40ff1-124">This interface contains type-safe methods to get and set values by data type.</span></span> <span data-ttu-id="40ff1-125">Ad esempio, per impostare un intero a 32 bit, chiamare [**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="40ff1-125">For example, to set a 32-bit integer, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span> <span data-ttu-id="40ff1-126">Le chiavi di attributo sono univoche all'interno di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="40ff1-126">Attribute keys are unique within an object.</span></span> <span data-ttu-id="40ff1-127">Se si impostano due valori diversi con la stessa chiave, il secondo valore sovrascrive il primo.</span><span class="sxs-lookup"><span data-stu-id="40ff1-127">If you set two different values with the same key, the second value overwrites the first.</span></span>

<span data-ttu-id="40ff1-128">Diverse interfacce di Media Foundation ereditano l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="40ff1-128">Several Media Foundation interfaces inherit the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="40ff1-129">Gli oggetti che espongono questa interfaccia hanno attributi facoltativi o obbligatori che l'applicazione deve impostare sull'oggetto o che possono recuperare gli attributi che l'applicazione può recuperare.</span><span class="sxs-lookup"><span data-stu-id="40ff1-129">Objects that expose this interface have optional or mandatory attributes that the application should set on the object, or have attributes that the application can retrieve.</span></span> <span data-ttu-id="40ff1-130">Inoltre, alcuni metodi e funzioni accettano un puntatore **IMFAttributes** come parametro, che consente all'applicazione di impostare le informazioni di configurazione.</span><span class="sxs-lookup"><span data-stu-id="40ff1-130">Also, some methods and functions take an **IMFAttributes** pointer as a parameter, which enables the application to set configuration information.</span></span> <span data-ttu-id="40ff1-131">L'applicazione deve creare un archivio di attributi per contenere gli attributi di configurazione.</span><span class="sxs-lookup"><span data-stu-id="40ff1-131">The application must create an attribute store to hold the configuration attributes.</span></span> <span data-ttu-id="40ff1-132">Per creare un archivio attributi vuoto, chiamare [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span><span class="sxs-lookup"><span data-stu-id="40ff1-132">To create an empty attribute store, call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>

<span data-ttu-id="40ff1-133">Il codice seguente illustra due funzioni.</span><span class="sxs-lookup"><span data-stu-id="40ff1-133">The following code shows two functions.</span></span> <span data-ttu-id="40ff1-134">Il primo crea un nuovo archivio di attributi e imposta un ipotetico attributo denominato MY \_ Attribute con un valore stringa.</span><span class="sxs-lookup"><span data-stu-id="40ff1-134">The first creates a new attribute store and sets a hypothetical attribute named MY\_ATTRIBUTE with a string value.</span></span> <span data-ttu-id="40ff1-135">La seconda funzione recupera il valore di questo attributo.</span><span class="sxs-lookup"><span data-stu-id="40ff1-135">The second function retrieves the value of this attribute.</span></span>


```C++
extern const GUID MY_ATTRIBUTE;

HRESULT ShowCreateAttributeStore(IMFAttributes **ppAttributes)
{
    IMFAttributes *pAttributes = NULL;
    const UINT32 cElements = 10;  // Starting size.

    // Create the empty attribute store.
    HRESULT hr = MFCreateAttributes(&pAttributes, cElements);

    // Set the MY_ATTRIBUTE attribute with a string value.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MY_ATTRIBUTE,
            L"This is a string value"
            );
    }

    // Return the IMFAttributes pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }

    SAFE_RELEASE(pAttributes);

    return hr;
}

HRESULT ShowGetAttributes()
{
    IMFAttributes *pAttributes = NULL;
    WCHAR *pwszValue = NULL;
    UINT32 cchLength = 0;

    // Create the attribute store.
    HRESULT hr = ShowCreateAttributeStore(&pAttributes);

    // Get the attribute.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->GetAllocatedString(
            MY_ATTRIBUTE,
            &pwszValue,
            &cchLength
            );
    }

    CoTaskMemFree(pwszValue);
    SAFE_RELEASE(pAttributes);

    return hr;
}
```



<span data-ttu-id="40ff1-136">Per un elenco completo degli attributi di Media Foundation, vedere [Media Foundation attributi](media-foundation-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="40ff1-136">For a complete list of Media Foundation attributes, see [Media Foundation Attributes](media-foundation-attributes.md).</span></span> <span data-ttu-id="40ff1-137">Il tipo di dati previsto per ogni attributo è documentato in questa posizione.</span><span class="sxs-lookup"><span data-stu-id="40ff1-137">The expected data type for each attribute is documented there.</span></span>

## <a name="serializing-attributes"></a><span data-ttu-id="40ff1-138">Serializzazione degli attributi</span><span class="sxs-lookup"><span data-stu-id="40ff1-138">Serializing Attributes</span></span>

<span data-ttu-id="40ff1-139">Media Foundation dispone di due funzioni per la serializzazione degli archivi di attributi.</span><span class="sxs-lookup"><span data-stu-id="40ff1-139">Media Foundation has two functions for serializing attribute stores.</span></span> <span data-ttu-id="40ff1-140">Uno scrive gli attributi in una matrice di byte, l'altro li scrive in un flusso che supporta l'interfaccia **IStream** .</span><span class="sxs-lookup"><span data-stu-id="40ff1-140">One writes the attributes to a byte array, the other writes them to a stream that supports the **IStream** interface.</span></span> <span data-ttu-id="40ff1-141">Ogni funzione ha una funzione corrispondente che carica i dati.</span><span class="sxs-lookup"><span data-stu-id="40ff1-141">Each function has a corresponding function that loads the data.</span></span>



| <span data-ttu-id="40ff1-142">Operazione</span><span class="sxs-lookup"><span data-stu-id="40ff1-142">Operation</span></span> | <span data-ttu-id="40ff1-143">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="40ff1-143">Byte Array</span></span>                                                   | <span data-ttu-id="40ff1-144">IStream</span><span class="sxs-lookup"><span data-stu-id="40ff1-144">IStream</span></span>                                                                        |
|-----------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="40ff1-145">Salva</span><span class="sxs-lookup"><span data-stu-id="40ff1-145">Save</span></span>      | [<span data-ttu-id="40ff1-146">**MFGetAttributesAsBlob**</span><span class="sxs-lookup"><span data-stu-id="40ff1-146">**MFGetAttributesAsBlob**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesasblob)       | [<span data-ttu-id="40ff1-147">**MFSerializeAttributesToStream**</span><span class="sxs-lookup"><span data-stu-id="40ff1-147">**MFSerializeAttributesToStream**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-mfserializeattributestostream)         |
| <span data-ttu-id="40ff1-148">Caricamento</span><span class="sxs-lookup"><span data-stu-id="40ff1-148">Load</span></span>      | [<span data-ttu-id="40ff1-149">**MFInitAttributesFromBlob**</span><span class="sxs-lookup"><span data-stu-id="40ff1-149">**MFInitAttributesFromBlob**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfinitattributesfromblob) | [<span data-ttu-id="40ff1-150">**MFDeserializeAttributesFromStream**</span><span class="sxs-lookup"><span data-stu-id="40ff1-150">**MFDeserializeAttributesFromStream**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-mfdeserializeattributesfromstream) |



 

<span data-ttu-id="40ff1-151">Per scrivere il contenuto di un archivio di attributi in una matrice di byte, chiamare [**MFGetAttributesAsBlob**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesasblob).</span><span class="sxs-lookup"><span data-stu-id="40ff1-151">To write the contents of an attribute store into a byte array, call [**MFGetAttributesAsBlob**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesasblob).</span></span> <span data-ttu-id="40ff1-152">Gli attributi con valori di puntatore **IUnknown** vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="40ff1-152">Attributes with **IUnknown** pointer values are ignored.</span></span> <span data-ttu-id="40ff1-153">Per caricare di nuovo gli attributi in un archivio di attributi, chiamare [**MFInitAttributesFromBlob**](/windows/desktop/api/mfapi/nf-mfapi-mfinitattributesfromblob).</span><span class="sxs-lookup"><span data-stu-id="40ff1-153">To load the attributes back into an attribute store, call [**MFInitAttributesFromBlob**](/windows/desktop/api/mfapi/nf-mfapi-mfinitattributesfromblob).</span></span>

<span data-ttu-id="40ff1-154">Per scrivere un archivio di attributi in un flusso, chiamare [**MFSerializeAttributesToStream**](/windows/desktop/api/mfobjects/nf-mfobjects-mfserializeattributestostream).</span><span class="sxs-lookup"><span data-stu-id="40ff1-154">To write an attribute store to a stream, call [**MFSerializeAttributesToStream**](/windows/desktop/api/mfobjects/nf-mfobjects-mfserializeattributestostream).</span></span> <span data-ttu-id="40ff1-155">Questa funzione può effettuare il marshalling dei valori del puntatore **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="40ff1-155">This function can marshal **IUnknown** pointer values.</span></span> <span data-ttu-id="40ff1-156">Il chiamante deve fornire un oggetto flusso che implementi l'interfaccia **IStream** .</span><span class="sxs-lookup"><span data-stu-id="40ff1-156">The caller must provide a stream object that implements the **IStream** interface.</span></span> <span data-ttu-id="40ff1-157">Per caricare un archivio di attributi da un flusso, chiamare [**MFDeserializeAttributesFromStream**](/windows/desktop/api/mfobjects/nf-mfobjects-mfdeserializeattributesfromstream).</span><span class="sxs-lookup"><span data-stu-id="40ff1-157">To load an attribute store from a stream, call [**MFDeserializeAttributesFromStream**](/windows/desktop/api/mfobjects/nf-mfobjects-mfdeserializeattributesfromstream).</span></span>

## <a name="implementing-imfattributes"></a><span data-ttu-id="40ff1-158">Implementazione di IMFAttributes</span><span class="sxs-lookup"><span data-stu-id="40ff1-158">Implementing IMFAttributes</span></span>

<span data-ttu-id="40ff1-159">Media Foundation fornisce un'implementazione predefinita di [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), ottenuta chiamando la funzione [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) .</span><span class="sxs-lookup"><span data-stu-id="40ff1-159">Media Foundation provides a stock implementation of [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), which is obtained by calling the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function.</span></span> <span data-ttu-id="40ff1-160">Nella maggior parte dei casi, è consigliabile usare questa implementazione e non fornire un'implementazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="40ff1-160">In most situations, you should use this implementation, and not provide your own custom implementation.</span></span>

<span data-ttu-id="40ff1-161">È possibile che si verifichi una situazione in cui è necessario implementare l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) : se si implementa una seconda interfaccia che eredita **IMFAttributes**.</span><span class="sxs-lookup"><span data-stu-id="40ff1-161">There is one situation when you might need to implement the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface: If you implement a second interface that inherits **IMFAttributes**.</span></span> <span data-ttu-id="40ff1-162">In tal caso, è necessario fornire le implementazioni per i metodi **IMFAttributes** ereditati dalla seconda interfaccia.</span><span class="sxs-lookup"><span data-stu-id="40ff1-162">In that case, you must provide implementations for the **IMFAttributes** methods inherited by the second interface.</span></span>

<span data-ttu-id="40ff1-163">In questa situazione, è consigliabile eseguire il wrapping dell'implementazione di Media Foundation esistente di [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span><span class="sxs-lookup"><span data-stu-id="40ff1-163">In this situation, it is recommended to wrap the existing Media Foundation implementation of [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span></span> <span data-ttu-id="40ff1-164">Il codice seguente illustra un modello di classe che contiene un puntatore **IMFAttributes** ed esegue il wrapping di ogni metodo **IMFAttributes** , ad eccezione dei metodi **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="40ff1-164">The following code shows a class template that holds an **IMFAttributes** pointer and wraps every **IMFAttributes** method, except for the **IUnknown** methods.</span></span>


```C++
#include <assert.h>

// Helper class to implement IMFAttributes. 

// This is an abstract class; the derived class must implement the IUnknown 
// methods. This class is a wrapper for the standard attribute store provided 
// in Media Foundation.

// template parameter: 
// The interface you are implementing, either IMFAttributes or an interface 
// that inherits IMFAttributes, such as IMFActivate

template <class IFACE=IMFAttributes>
class CBaseAttributes : public IFACE
{
protected:
    IMFAttributes *m_pAttributes;

    // This version of the constructor does not initialize the 
    // attribute store. The derived class must call Initialize() in 
    // its own constructor.
    CBaseAttributes() : m_pAttributes(NULL)
    {
    }

    // This version of the constructor initializes the attribute 
    // store, but the derived class must pass an HRESULT parameter 
    // to the constructor.

    CBaseAttributes(HRESULT& hr, UINT32 cInitialSize = 0) : m_pAttributes(NULL)
    {
        hr = Initialize(cInitialSize);
    }

    // The next version of the constructor uses a caller-provided 
    // implementation of IMFAttributes.

    // (Sometimes you want to delegate IMFAttributes calls to some 
    // other object that implements IMFAttributes, rather than using 
    // MFCreateAttributes.)

    CBaseAttributes(HRESULT& hr, IUnknown *pUnk)
    {
        hr = Initialize(pUnk);
    }

    virtual ~CBaseAttributes()
    {
        if (m_pAttributes)
        {
            m_pAttributes->Release();
        }
    }

    // Initializes the object by creating the standard Media Foundation attribute store.
    HRESULT Initialize(UINT32 cInitialSize = 0)
    {
        if (m_pAttributes == NULL)
        {
            return MFCreateAttributes(&m_pAttributes, cInitialSize); 
        }
        else
        {
            return S_OK;
        }
    }

    // Initializes this object from a caller-provided attribute store.
    // pUnk: Pointer to an object that exposes IMFAttributes.
    HRESULT Initialize(IUnknown *pUnk)
    {
        if (m_pAttributes)
        {
            m_pAttributes->Release();
            m_pAttributes = NULL;
        }


        return pUnk->QueryInterface(IID_PPV_ARGS(&m_pAttributes));
    }

public:

    // IMFAttributes methods

    STDMETHODIMP GetItem(REFGUID guidKey, PROPVARIANT* pValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetItem(guidKey, pValue);
    }

    STDMETHODIMP GetItemType(REFGUID guidKey, MF_ATTRIBUTE_TYPE* pType)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetItemType(guidKey, pType);
    }

    STDMETHODIMP CompareItem(REFGUID guidKey, REFPROPVARIANT Value, BOOL* pbResult)
    {
        assert(m_pAttributes);
        return m_pAttributes->CompareItem(guidKey, Value, pbResult);
    }

    STDMETHODIMP Compare(
        IMFAttributes* pTheirs, 
        MF_ATTRIBUTES_MATCH_TYPE MatchType, 
        BOOL* pbResult
        )
    {
        assert(m_pAttributes);
        return m_pAttributes->Compare(pTheirs, MatchType, pbResult);
    }

    STDMETHODIMP GetUINT32(REFGUID guidKey, UINT32* punValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetUINT32(guidKey, punValue);
    }

    STDMETHODIMP GetUINT64(REFGUID guidKey, UINT64* punValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetUINT64(guidKey, punValue);
    }

    STDMETHODIMP GetDouble(REFGUID guidKey, double* pfValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetDouble(guidKey, pfValue);
    }

    STDMETHODIMP GetGUID(REFGUID guidKey, GUID* pguidValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetGUID(guidKey, pguidValue);
    }

    STDMETHODIMP GetStringLength(REFGUID guidKey, UINT32* pcchLength)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetStringLength(guidKey, pcchLength);
    }

    STDMETHODIMP GetString(REFGUID guidKey, LPWSTR pwszValue, UINT32 cchBufSize, UINT32* pcchLength)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetString(guidKey, pwszValue, cchBufSize, pcchLength);
    }

    STDMETHODIMP GetAllocatedString(REFGUID guidKey, LPWSTR* ppwszValue, UINT32* pcchLength)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetAllocatedString(guidKey, ppwszValue, pcchLength);
    }

    STDMETHODIMP GetBlobSize(REFGUID guidKey, UINT32* pcbBlobSize)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetBlobSize(guidKey, pcbBlobSize);
    }

    STDMETHODIMP GetBlob(REFGUID guidKey, UINT8* pBuf, UINT32 cbBufSize, UINT32* pcbBlobSize)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetBlob(guidKey, pBuf, cbBufSize, pcbBlobSize);
    }

    STDMETHODIMP GetAllocatedBlob(REFGUID guidKey, UINT8** ppBuf, UINT32* pcbSize)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetAllocatedBlob(guidKey, ppBuf, pcbSize);
    }

    STDMETHODIMP GetUnknown(REFGUID guidKey, REFIID riid, LPVOID* ppv)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetUnknown(guidKey, riid, ppv);
    }

    STDMETHODIMP SetItem(REFGUID guidKey, REFPROPVARIANT Value)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetItem(guidKey, Value);
    }

    STDMETHODIMP DeleteItem(REFGUID guidKey)
    {
        assert(m_pAttributes);
        return m_pAttributes->DeleteItem(guidKey);
    }

    STDMETHODIMP DeleteAllItems()
    {
        assert(m_pAttributes);
        return m_pAttributes->DeleteAllItems();
    }

    STDMETHODIMP SetUINT32(REFGUID guidKey, UINT32 unValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetUINT32(guidKey, unValue);
    }

    STDMETHODIMP SetUINT64(REFGUID guidKey,UINT64 unValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetUINT64(guidKey, unValue);
    }

    STDMETHODIMP SetDouble(REFGUID guidKey, double fValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetDouble(guidKey, fValue);
    }

    STDMETHODIMP SetGUID(REFGUID guidKey, REFGUID guidValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetGUID(guidKey, guidValue);
    }

    STDMETHODIMP SetString(REFGUID guidKey, LPCWSTR wszValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetString(guidKey, wszValue);
    }

    STDMETHODIMP SetBlob(REFGUID guidKey, const UINT8* pBuf, UINT32 cbBufSize)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetBlob(guidKey, pBuf, cbBufSize);
    }

    STDMETHODIMP SetUnknown(REFGUID guidKey, IUnknown* pUnknown)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetUnknown(guidKey, pUnknown);
    }

    STDMETHODIMP LockStore()
    {
        assert(m_pAttributes);
        return m_pAttributes->LockStore();
    }

    STDMETHODIMP UnlockStore()
    {
        assert(m_pAttributes);
        return m_pAttributes->UnlockStore();
    }

    STDMETHODIMP GetCount(UINT32* pcItems)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetCount(pcItems);
    }

    STDMETHODIMP GetItemByIndex(UINT32 unIndex, GUID* pguidKey, PROPVARIANT* pValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetItemByIndex(unIndex, pguidKey, pValue);
    }

    STDMETHODIMP CopyAllItems(IMFAttributes* pDest)
    {
        assert(m_pAttributes);
        return m_pAttributes->CopyAllItems(pDest);
    }

    // Helper functions
    
    HRESULT SerializeToStream(DWORD dwOptions, IStream* pStm)      
        // dwOptions: Flags from MF_ATTRIBUTE_SERIALIZE_OPTIONS
    {
        assert(m_pAttributes);
        return MFSerializeAttributesToStream(m_pAttributes, dwOptions, pStm);
    }

    HRESULT DeserializeFromStream(DWORD dwOptions, IStream* pStm)
    {
        assert(m_pAttributes);
        return MFDeserializeAttributesFromStream(m_pAttributes, dwOptions, pStm);
    }

    // SerializeToBlob: Stores the attributes in a byte array. 
    // 
    // ppBuf: Receives a pointer to the byte array. 
    // pcbSize: Receives the size of the byte array.
    //
    // The caller must free the array using CoTaskMemFree.
    HRESULT SerializeToBlob(UINT8 **ppBuffer, UINT32 *pcbSize)
    {
        assert(m_pAttributes);

        if (ppBuffer == NULL)
        {
            return E_POINTER;
        }
        if (pcbSize == NULL)
        {
            return E_POINTER;
        }

        *ppBuffer = NULL;
        *pcbSize = 0;

        UINT32 cbSize = 0;
        BYTE *pBuffer = NULL;

        HRESULT hr = MFGetAttributesAsBlobSize(m_pAttributes, &cbSize);

        if (FAILED(hr))
        {
            return hr;
        }

        pBuffer = (BYTE*)CoTaskMemAlloc(cbSize);
        if (pBuffer == NULL)
        {
            return E_OUTOFMEMORY;
        }

        hr = MFGetAttributesAsBlob(m_pAttributes, pBuffer, cbSize);

        if (SUCCEEDED(hr))
        {
            *ppBuffer = pBuffer;
            *pcbSize = cbSize;
        }
        else
        {
            CoTaskMemFree(pBuffer);
        }
        return hr;
    }
    
    HRESULT DeserializeFromBlob(const UINT8* pBuffer, UINT cbSize)
    {
        assert(m_pAttributes);
        return MFInitAttributesFromBlob(m_pAttributes, pBuffer, cbSize);
    }

    HRESULT GetRatio(REFGUID guidKey, UINT32* pnNumerator, UINT32* punDenominator)
    {
        assert(m_pAttributes);
        return MFGetAttributeRatio(m_pAttributes, guidKey, pnNumerator, punDenominator);
    }

    HRESULT SetRatio(REFGUID guidKey, UINT32 unNumerator, UINT32 unDenominator)
    {
        assert(m_pAttributes);
        return MFSetAttributeRatio(m_pAttributes, guidKey, unNumerator, unDenominator);
    }

    // Gets an attribute whose value represents the size of something (eg a video frame).
    HRESULT GetSize(REFGUID guidKey, UINT32* punWidth, UINT32* punHeight)
    {
        assert(m_pAttributes);
        return MFGetAttributeSize(m_pAttributes, guidKey, punWidth, punHeight);
    }

    // Sets an attribute whose value represents the size of something (eg a video frame).
    HRESULT SetSize(REFGUID guidKey, UINT32 unWidth, UINT32 unHeight)
    {
        assert(m_pAttributes);
        return MFSetAttributeSize (m_pAttributes, guidKey, unWidth, unHeight);
    }
};
```



<span data-ttu-id="40ff1-165">Il codice seguente mostra come derivare una classe da questo modello:</span><span class="sxs-lookup"><span data-stu-id="40ff1-165">The following code shows how to derive a class from this template:</span></span>


```C++
#include <shlwapi.h>

class MyObject : public CBaseAttributes<>
{
    MyObject() : m_nRefCount(1) { }
    ~MyObject() { }

    long m_nRefCount;

public:

    // IUnknown
    STDMETHODIMP MyObject::QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(MyObject, IMFAttributes),
            { 0 },
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) MyObject::AddRef()
    {
        return InterlockedIncrement(&m_nRefCount);
    }

    STDMETHODIMP_(ULONG) MyObject::Release()
    {
        ULONG uCount = InterlockedDecrement(&m_nRefCount);
        if (uCount == 0)
        {
            delete this;
        }
        return uCount;
    }

    // Static function to create an instance of the object.

    static HRESULT CreateInstance(MyObject **ppObject)
    {
        HRESULT hr = S_OK;

        MyObject *pObject = new MyObject();
        if (pObject == NULL)
        {
            return E_OUTOFMEMORY;
        }

        // Initialize the attribute store.
        hr = pObject->Initialize();

        if (FAILED(hr))
        {
            delete pObject;
            return hr;
        }

        *ppObject = pObject;
        (*ppObject)->AddRef();

        return S_OK;
    }
};
```



<span data-ttu-id="40ff1-166">È necessario chiamare `CBaseAttributes::Initialize` per creare l'archivio di attributi.</span><span class="sxs-lookup"><span data-stu-id="40ff1-166">You must call `CBaseAttributes::Initialize` to create the attribute store.</span></span> <span data-ttu-id="40ff1-167">Nell'esempio precedente, questa operazione viene eseguita all'interno di una funzione di creazione statica.</span><span class="sxs-lookup"><span data-stu-id="40ff1-167">In the previous example, that is done inside a static creation function.</span></span>

<span data-ttu-id="40ff1-168">L'argomento di modello è un tipo di interfaccia, che per impostazione predefinita è [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span><span class="sxs-lookup"><span data-stu-id="40ff1-168">The template argument is an interface type, which defaults to [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span></span> <span data-ttu-id="40ff1-169">Se l'oggetto implementa un'interfaccia che eredita **IMFAttributes**, ad esempio [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate), impostare l'argomento del modello uguale al nome dell'interfaccia derivata.</span><span class="sxs-lookup"><span data-stu-id="40ff1-169">If your object implements an interface that inherits **IMFAttributes**, such as [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate), set the template argument equal to name of the derived interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40ff1-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="40ff1-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40ff1-171">Primitive Media Foundation</span><span class="sxs-lookup"><span data-stu-id="40ff1-171">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> </dl>

 

 



