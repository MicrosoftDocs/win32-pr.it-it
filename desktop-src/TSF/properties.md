---
title: Proprietà (elementi comuni)
description: Il Framework di servizi di testo (TSF) fornisce proprietà che associano metadati a un intervallo di testo.
ms.assetid: d1d0dd99-f303-4355-9835-917de9491a0b
keywords:
- Framework servizi di testo (TSF), proprietà
- TSF (Framework di servizi di testo), proprietà
- Servizi di testo, proprietà
- Applicazioni abilitate per TSF, proprietà
- properties
- Framework servizi di testo (TSF), tipi di proprietà
- TSF (Framework dei servizi di testo), tipi di proprietà
- Servizi di testo, tipi di proprietà
- Applicazioni abilitate per TSF, tipi di proprietà
- proprietà (tipi)
- Framework servizi di testo (TSF), archivio permanente delle proprietà
- TSF (Framework dei servizi di testo), archivio permanente delle proprietà
- Servizi di testo, archivio permanente delle proprietà
- Applicazioni abilitate per TSF, archiviazione persistente delle proprietà
- archiviazione persistente delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff852bccfb7d9b6c94e57a2fa0cf8eef6fbdf18
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300868"
---
# <a name="properties-common-elements"></a><span data-ttu-id="feccd-118">Proprietà (elementi comuni)</span><span class="sxs-lookup"><span data-stu-id="feccd-118">Properties (Common Elements)</span></span>

<span data-ttu-id="feccd-119">Il Framework di servizi di testo (TSF) fornisce proprietà che associano metadati a un intervallo di testo.</span><span class="sxs-lookup"><span data-stu-id="feccd-119">Text Services Framework (TSF) provides properties that associate metadata with a range of text.</span></span> <span data-ttu-id="feccd-120">Queste proprietà includono, a differenza di, gli attributi di visualizzazione come testo in grassetto, l'identificatore di lingua del testo e i dati non elaborati forniti da un servizio di testo, ad esempio i dati audio associati al testo dal servizio di testo vocale.</span><span class="sxs-lookup"><span data-stu-id="feccd-120">These properties include, but are not limited to, display attributes such as bold text, the language identifier of the text, and raw data provided by a text service such as the audio data associated with text from the speech text service.</span></span>

<span data-ttu-id="feccd-121">Nell'esempio seguente viene illustrato come è possibile visualizzare una proprietà del colore del testo ipotetico con i valori possibili di rosso (R), verde (G) o blu (B).</span><span class="sxs-lookup"><span data-stu-id="feccd-121">The following example demonstrates how a hypothetical text color property with possible values of red (R), green (G), or blue (B) can be viewed.</span></span>


```C++
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



<span data-ttu-id="feccd-122">Le proprietà di tipi diversi possono sovrapporsi.</span><span class="sxs-lookup"><span data-stu-id="feccd-122">Properties of different types can overlap.</span></span> <span data-ttu-id="feccd-123">Si prenda, ad esempio, l'esempio precedente e si aggiunge un attributo di testo che può essere grassetto (B) o corsivo (I).</span><span class="sxs-lookup"><span data-stu-id="feccd-123">For example, take the previous example and add a text attribute that can be either bold (B) or italic (I).</span></span>


```C++
ATTRIB:BBBBBBB      IIIIIIIIIIII
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



<span data-ttu-id="feccd-124">Il testo "This" sarebbe grassetto, "is" sarà sia grassetto che rosso, "some" verrebbe visualizzato normalmente, "colorato" sarebbe verde e in corsivo e "Text" verrebbe formattato in corsivo.</span><span class="sxs-lookup"><span data-stu-id="feccd-124">The text "this" would be bold, "is" would be both bold and red, "some" would be displayed normally, "colored" would be green and italicized and "text" would be italicized.</span></span>

<span data-ttu-id="feccd-125">Le proprietà dello stesso tipo non possono sovrapporsi.</span><span class="sxs-lookup"><span data-stu-id="feccd-125">Properties of the same type cannot overlap.</span></span> <span data-ttu-id="feccd-126">La situazione seguente, ad esempio, non è consentita perché "is" e "colorati" presentano valori sovrapposti degli stessi tipi.</span><span class="sxs-lookup"><span data-stu-id="feccd-126">For example, the following situation is not allowed because "is" and "colored" have overlapping values of the same types.</span></span>


```C++
COLOR: GGG GGGG RRR BBBBGGG     
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



## <a name="property-types"></a><span data-ttu-id="feccd-127">Tipi di proprietà</span><span class="sxs-lookup"><span data-stu-id="feccd-127">Property Types</span></span>

<span data-ttu-id="feccd-128">TSF definisce tre diversi tipi di proprietà.</span><span class="sxs-lookup"><span data-stu-id="feccd-128">TSF defines three different types of properties.</span></span>



|                |                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="feccd-129">Static</span><span class="sxs-lookup"><span data-stu-id="feccd-129">Static</span></span>         | <span data-ttu-id="feccd-130">Un oggetto proprietà statico archivia i dati della proprietà con testo.</span><span class="sxs-lookup"><span data-stu-id="feccd-130">A static property object stores the property data with text.</span></span> <span data-ttu-id="feccd-131">Archivia inoltre l'intervallo di informazioni di testo per ogni intervallo a cui viene applicata la proprietà.</span><span class="sxs-lookup"><span data-stu-id="feccd-131">It also stores the range of text information for each range that the property applies to.</span></span> <span data-ttu-id="feccd-132">ITfReadOnlyProperty:: GetType restituisce la \_ \_ categoria statica GUID TFCAT PROPSTYLE \_ .</span><span class="sxs-lookup"><span data-stu-id="feccd-132">ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_STATIC category.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="feccd-133">Static-Compact</span><span class="sxs-lookup"><span data-stu-id="feccd-133">Static-Compact</span></span> | <span data-ttu-id="feccd-134">Un oggetto proprietà statico-Compact è identico a un oggetto proprietà statico, ad eccezione del fatto che la proprietà static-Compact non archivia i dati dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="feccd-134">A static-compact property object is identical to a static property object except a static-compact property does not store range data.</span></span> <span data-ttu-id="feccd-135">Quando viene richiesto l'intervallo coperto da una proprietà static-Compact, viene creato un intervallo per ogni gruppo di proprietà adiacenti.</span><span class="sxs-lookup"><span data-stu-id="feccd-135">When the range covered by a static-compact property is requested, a range is created for each group of adjacent properties.</span></span> <span data-ttu-id="feccd-136">Le proprietà statiche compatte rappresentano il modo più efficiente per archiviare le proprietà in base ai singoli caratteri.</span><span class="sxs-lookup"><span data-stu-id="feccd-136">Static-compact properties are the most efficient way to store properties on a per-character basis.</span></span> <span data-ttu-id="feccd-137">ITfReadOnlyProperty:: GetType restituisce la \_ categoria GUID TFCAT \_ PROPSTYLE \_ STATICCOMPACT.</span><span class="sxs-lookup"><span data-stu-id="feccd-137">ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_STATICCOMPACT category.</span></span> |
| <span data-ttu-id="feccd-138">Personalizzato</span><span class="sxs-lookup"><span data-stu-id="feccd-138">Custom</span></span>         | <span data-ttu-id="feccd-139">Un oggetto proprietà personalizzato archivia le informazioni sull'intervallo per ogni intervallo a cui viene applicata la proprietà.</span><span class="sxs-lookup"><span data-stu-id="feccd-139">A custom property object stores the range information for each range that the property applies to.</span></span> <span data-ttu-id="feccd-140">Non archivia tuttavia i dati effettivi per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="feccd-140">It does not, however, store the actual data for the property.</span></span> <span data-ttu-id="feccd-141">Una proprietà personalizzata archivia invece un oggetto ITfPropertyStore.</span><span class="sxs-lookup"><span data-stu-id="feccd-141">Instead, a custom property stores an ITfPropertyStore object.</span></span> <span data-ttu-id="feccd-142">Il gestore TSF utilizza questo oggetto per accedere e gestire i dati della proprietà. ITfReadOnlyProperty:: GetType restituisce la \_ \_ categoria personalizzata GUID TFCAT PROPSTYLE \_ .</span><span class="sxs-lookup"><span data-stu-id="feccd-142">The TSF manager uses this object to access and maintain the property data.ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_CUSTOM category.</span></span>                                                                    |



 

## <a name="working-with-properties"></a><span data-ttu-id="feccd-143">Uso di proprietà</span><span class="sxs-lookup"><span data-stu-id="feccd-143">Working with Properties</span></span>

<span data-ttu-id="feccd-144">Il valore della proprietà e gli attributi vengono ottenuti usando l'interfaccia [ITfReadOnlyProperty](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) e modificati usando l'interfaccia [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) .</span><span class="sxs-lookup"><span data-stu-id="feccd-144">The property value and attributes are obtained using the [ITfReadOnlyProperty](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) interface and modified using the [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) interface.</span></span>

<span data-ttu-id="feccd-145">Se è necessario un tipo di proprietà specifico, viene usato [ITfContext:: GetProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty) .</span><span class="sxs-lookup"><span data-stu-id="feccd-145">If a specific property type is required, then [ITfContext::GetProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty) is used.</span></span> <span data-ttu-id="feccd-146">**ITfContext:: GetProperty** richiede un **GUID** che identifichi la proprietà da ottenere.</span><span class="sxs-lookup"><span data-stu-id="feccd-146">**ITfContext::GetProperty** requires a **GUID** that identifies the property to obtain.</span></span> <span data-ttu-id="feccd-147">TSF definisce un set di [identificatori di proprietà predefiniti](predefined-properties.md) utilizzati o un servizio di testo può definire i propri identificatori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="feccd-147">TSF defines a set of [predefined property identifiers](predefined-properties.md) used or a text service can define its own property identifiers.</span></span> <span data-ttu-id="feccd-148">Se viene utilizzata una proprietà personalizzata, il provider di proprietà deve pubblicare il **GUID** della proprietà e il formato dei dati ottenuti.</span><span class="sxs-lookup"><span data-stu-id="feccd-148">If a custom property is used, the property provider must publish the property **GUID** and the format of the data obtained.</span></span>

<span data-ttu-id="feccd-149">Per ottenere, ad esempio, **il CLSID** per il proprietario di un intervallo di testo, **chiamare ITfContext:: GetProperty** per ottenere l'oggetto Property, chiamare [ITfProperty:: FindRange](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) per ottenere l'intervallo che copre interamente la proprietà, quindi chiamare [ITfReadOnlyProperty:: GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) per ottenere un [TfGuidAtom](/windows/desktop/TSF/tfguidatom) che rappresenta il **CLSID** del servizio di testo proprietario del testo.</span><span class="sxs-lookup"><span data-stu-id="feccd-149">For example, to obtain the **CLSID** for the owner of a range of text, call **ITfContext::GetProperty** to obtain the property object, call [ITfProperty::FindRange](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) to obtain the range that entirely covers the property, then call [ITfReadOnlyProperty::GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) to get a [TfGuidAtom](/windows/desktop/TSF/tfguidatom) that represents the **CLSID** of the text service that owns the text.</span></span> <span data-ttu-id="feccd-150">Nell'esempio seguente viene illustrata una funzione che, dati un contesto, un intervallo e un cookie di modifica, otterrà il **CLSID** del servizio di testo proprietario del testo.</span><span class="sxs-lookup"><span data-stu-id="feccd-150">The following example shows a function that, given a context, range and an edit cookie, will obtain the **CLSID** of the text service that owns the text.</span></span>


```C++
HRESULT GetTextOwner(   ITfContext *pContext, 
                        ITfRange *pRange, 
                        TfEditCookie ec, 
                        CLSID *pclsidOwner)
{
    HRESULT     hr;
    ITfProperty *pProp;

    *pclsidOwner = GUID_NULL;

    hr = pContext->GetProperty(GUID_PROP_TEXTOWNER, &pProp);
    if(S_OK == hr)
    {
        ITfRange    *pPropRange;

        hr = pProp->FindRange(ec, pRange, &pPropRange, TF_ANCHOR_START);
        if(S_OK == hr)
        {
            VARIANT var;

            VariantInit(&var);
            hr = pProp->GetValue(ec, pPropRange, &var);
            if(S_OK == hr)
            {
                if(VT_I4 == var.vt)
                {
                    /*
                    var.lVal is a TfGuidAtom that represents the CLSID of the 
                    text owner. Use ITfCategoryMgr to obtain the CLSID from 
                    the TfGuidAtom.
                    */
                    ITfCategoryMgr  *pCatMgr;

                    hr = CoCreateInstance(  CLSID_TF_CategoryMgr,
                                            NULL, 
                                            CLSCTX_INPROC_SERVER, 
                                            IID_ITfCategoryMgr, 
                                            (LPVOID*)&pCatMgr);
                    if(SUCCEEDED(hr))
                    {
                        hr = pCatMgr->GetGUID((TfGuidAtom)var.lVal, pclsidOwner);
                        if(SUCCEEDED(hr))
                        {
                            /*
                            *pclsidOwner now contains the CLSID of the text 
                            service that owns the text at the selection.
                            */
                        }

                        pCatMgr->Release();
                    }
                }
                else
                {
                    //Unrecognized VARIANT type 
                    hr = E_FAIL;
                }
                
                VariantClear(&var);
            }
            
            pPropRange->Release();
        }
        
        pProp->Release();
    }

    return hr;
}

```



<span data-ttu-id="feccd-151">È anche possibile enumerare le proprietà ottenendo un'interfaccia [IEnumTfProperties](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) da [ITfContext:: EnumProperties](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties).</span><span class="sxs-lookup"><span data-stu-id="feccd-151">Properties can also be enumerated by obtaining an [IEnumTfProperties](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) interface from [ITfContext::EnumProperties](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties).</span></span>

## <a name="persistent-storage-of-properties"></a><span data-ttu-id="feccd-152">Archiviazione persistente delle proprietà</span><span class="sxs-lookup"><span data-stu-id="feccd-152">Persistent Storage of Properties</span></span>

<span data-ttu-id="feccd-153">Spesso le proprietà sono trasparenti per un'applicazione e vengono utilizzate da uno o più servizi di testo.</span><span class="sxs-lookup"><span data-stu-id="feccd-153">Often, properties are transparent to an application and are used by one or more text services.</span></span> <span data-ttu-id="feccd-154">Per mantenere i dati delle proprietà, ad esempio quando si esegue il salvataggio in un file, un'applicazione deve serializzare i dati della proprietà quando viene archiviata e deserializzare i dati della proprietà quando i dati vengono ripristinati.</span><span class="sxs-lookup"><span data-stu-id="feccd-154">In order to preserve the property data, such as when saving to a file, an application must serialize the property data when it is stored and unserialize the property data when the data is restored.</span></span> <span data-ttu-id="feccd-155">In questo caso, l'applicazione non deve essere interessata a singole proprietà, ma deve enumerare tutte le proprietà nel contesto e archiviarle.</span><span class="sxs-lookup"><span data-stu-id="feccd-155">In this case, the application should not be interested in individual properties, but should enumerate all properties in the context and store them.</span></span>

<span data-ttu-id="feccd-156">Quando si archiviano i dati delle proprietà, un'applicazione deve eseguire i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="feccd-156">When storing property data, an application should perform the following steps.</span></span>

1.  <span data-ttu-id="feccd-157">Ottenere un enumeratore di proprietà chiamando **ITfContext:: EnumProperties**.</span><span class="sxs-lookup"><span data-stu-id="feccd-157">Obtain a property enumerator by calling **ITfContext::EnumProperties**.</span></span>
2.  <span data-ttu-id="feccd-158">Enumerare ogni proprietà chiamando [IEnumTfProperties:: Next](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next).</span><span class="sxs-lookup"><span data-stu-id="feccd-158">Enumerate each property by calling [IEnumTfProperties::Next](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next).</span></span>
3.  <span data-ttu-id="feccd-159">Per ogni proprietà, ottenere un enumeratore di intervallo chiamando [ITfReadOnlyProperty:: EnumRanges](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges).</span><span class="sxs-lookup"><span data-stu-id="feccd-159">For each property, obtain a range enumerator by calling [ITfReadOnlyProperty::EnumRanges](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges).</span></span>
4.  <span data-ttu-id="feccd-160">Enumerare ogni intervallo nella proprietà chiamando [IEnumTfRanges:: Next](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next).</span><span class="sxs-lookup"><span data-stu-id="feccd-160">Enumerate each range in the property by calling [IEnumTfRanges::Next](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next).</span></span>
5.  <span data-ttu-id="feccd-161">Per ogni intervallo nella proprietà, chiamare [ITextStoreACPServices:: Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) con la proprietà, l'intervallo, una struttura di [ \_ \_ \_ intestazione \_ ACP persistente dell'intestazione della proprietà TF](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) e un oggetto Stream implementato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="feccd-161">For each range in the property, call [ITextStoreACPServices::Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) with the property, range, a [TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) structure, and a stream object implemented by the application.</span></span>
6.  <span data-ttu-id="feccd-162">Scrivere il contenuto della struttura **\_ ACP dell' \_ \_ intestazione della \_ proprietà persistente TF** nella memoria persistente.</span><span class="sxs-lookup"><span data-stu-id="feccd-162">Write the contents of the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure into persistent memory.</span></span>
7.  <span data-ttu-id="feccd-163">Scrivere il contenuto dell'oggetto flusso nella memoria permanente.</span><span class="sxs-lookup"><span data-stu-id="feccd-163">Write the contents of the stream object into persistent memory.</span></span>
8.  <span data-ttu-id="feccd-164">Continuare i passaggi precedenti per tutti gli intervalli in tutte le proprietà.</span><span class="sxs-lookup"><span data-stu-id="feccd-164">Continue the previous steps for all of the ranges in all of the properties.</span></span>
9.  <span data-ttu-id="feccd-165">L'applicazione deve scrivere un tipo di terminiator nel flusso in modo che, quando i dati vengono ripristinati, sia possibile identificare un punto di arresto.</span><span class="sxs-lookup"><span data-stu-id="feccd-165">The application should write some type of terminiator into the stream so that, when the data is restored, a stopping point can be identified.</span></span>


```C++
HRESULT SaveProperties( ITfContext *pContext, 
                        ITextStoreACPServices *pServices, 
                        TfEditCookie ec, 
                        IStream *pStream)
{
    HRESULT             hr;
    IEnumTfProperties   *pEnumProps;
    TF_PERSISTENT_PROPERTY_HEADER_ACP PropHeader;
    ULONG uWritten;
    
    //Enumerate the properties in the context. 
    hr = pContext->EnumProperties(&pEnumProps);
    if(SUCCEEDED(hr))
    {
        ITfProperty *pProp;
        ULONG       uFetched;

        while(SUCCEEDED(pEnumProps->Next(1, &pProp, &uFetched)) && uFetched)
        {
            //Enumerate all the ranges that contain the property. 
            IEnumTfRanges   *pEnumRanges;
            hr = pProp->EnumRanges(ec, &pEnumRanges, NULL);
            if(SUCCEEDED(hr))
            {
                IStream *pTempStream;

                //Create a temporary stream to write the property data to. 
                hr = CreateStreamOnHGlobal(NULL, TRUE, &pTempStream);
                if(SUCCEEDED(hr))
                {
                    ITfRange    *pRange;

                    while(SUCCEEDED(pEnumRanges->Next(1, &pRange, &uFetched)) && uFetched)
                    {
                        LARGE_INTEGER li;

                        //Reset the temporary stream pointer. 
                        li.QuadPart = 0;
                        pTempStream->Seek(li, STREAM_SEEK_SET, NULL);
                        
                        //Get the property header and data for the range. 
                        hr = pServices->Serialize(pProp, pRange, &PropHeader, pTempStream);

                        /*
                        Write the property header into the primary stream. 
                        The header also contains the size of the property 
                        data.
                        */
                        hr = pStream->Write(&PropHeader, sizeof(PropHeader), &uWritten);

                        //Reset the temporary stream pointer. 
                        li.QuadPart = 0;
                        pTempStream->Seek(li, STREAM_SEEK_SET, NULL);

                        //Copy the property data from the temporary stream into the primary stream. 
                        ULARGE_INTEGER  uli;
                        uli.QuadPart = PropHeader.cb;

                        hr = pTempStream->CopyTo(pStream, uli, NULL, NULL);

                        pRange->Release();
                    }
                    
                    pTempStream->Release();
                }
                
                pEnumRanges->Release();
            }
            
            pProp->Release();
        }
        
        pEnumProps->Release();
    }

    //Write a property header with zero size and guid into the stream as a terminator 
    ZeroMemory(&PropHeader, sizeof(PropHeader));
    hr = pStream->Write(&PropHeader, sizeof(PropHeader), &uWritten);

    return hr;
}

```



<span data-ttu-id="feccd-166">**ITextStoreACPServices:: Serialize**[ITfPropertyStore:: Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)</span><span class="sxs-lookup"><span data-stu-id="feccd-166">**ITextStoreACPServices::Serialize**[ITfPropertyStore::Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)</span></span>

<span data-ttu-id="feccd-167">Quando si ripristinano i dati delle proprietà, un'applicazione deve eseguire i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="feccd-167">When restoring property data, an application should perform the following steps.</span></span>

1.  <span data-ttu-id="feccd-168">Impostare il puntatore del flusso all'inizio della prima struttura **\_ ACP dell' \_ \_ intestazione della \_ proprietà persistente TF** .</span><span class="sxs-lookup"><span data-stu-id="feccd-168">Set the stream pointer to the start of the first **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
2.  <span data-ttu-id="feccd-169">Leggere la **struttura \_ \_ ACP dell' \_ intestazione \_ della proprietà persistente TF** .</span><span class="sxs-lookup"><span data-stu-id="feccd-169">Read the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
3.  <span data-ttu-id="feccd-170">Chiamare **ITfContext:: GetProperty** con il membro **guidType** della **struttura \_ \_ ACP dell' \_ intestazione \_ della proprietà persistente TF** .</span><span class="sxs-lookup"><span data-stu-id="feccd-170">Call **ITfContext::GetProperty** with the **guidType** member of the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
4.  <span data-ttu-id="feccd-171">A questo punto, l'applicazione può eseguire una delle due operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="feccd-171">The application can do one of two things at this point.</span></span>
    1.  <span data-ttu-id="feccd-172">Creare un'istanza di un oggetto [ITfPersistentPropertyLoaderACP](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) che deve essere implementata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="feccd-172">Create an instance of an [ITfPersistentPropertyLoaderACP](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) object that the application must implement.</span></span> <span data-ttu-id="feccd-173">Chiamare quindi [ITextStoreACPServices:: unserialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) con **null** per *pStream* e il puntatore **ITfPersistentPropertyLoaderACP** .</span><span class="sxs-lookup"><span data-stu-id="feccd-173">Then call [ITextStoreACPServices::Unserialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) with **NULL** for *pStream* and the **ITfPersistentPropertyLoaderACP** pointer.</span></span>
    2.  <span data-ttu-id="feccd-174">Passare il flusso di input a **ITextStoreACPServices:: unserialize** e **null** per *pLoader*.</span><span class="sxs-lookup"><span data-stu-id="feccd-174">Pass the input stream to **ITextStoreACPServices::Unserialize** and **NULL** for *pLoader*.</span></span>

    <span data-ttu-id="feccd-175">Il primo metodo è preferibile perché è il più efficiente.</span><span class="sxs-lookup"><span data-stu-id="feccd-175">The first method is preferred as it is the most efficient.</span></span> <span data-ttu-id="feccd-176">L'implementazione del secondo metodo comporta la lettura di tutti i dati della proprietà dal flusso durante la chiamata **ITextStoreACPServices:: unserialize** .</span><span class="sxs-lookup"><span data-stu-id="feccd-176">Implementing the second method causes all of the property data to be read from the stream during the **ITextStoreACPServices::Unserialize** call.</span></span> <span data-ttu-id="feccd-177">Il primo metodo fa in modo che i dati della proprietà vengano letti su richiesta in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="feccd-177">The first method causes the property data to be read on demand at a later time.</span></span>
5.  <span data-ttu-id="feccd-178">Ripetere i passaggi precedenti fino a quando tutti i blocchi di proprietà non vengono serializzati.</span><span class="sxs-lookup"><span data-stu-id="feccd-178">Repeat the previous steps until all property blocks are unserialized.</span></span>


```C++
HRESULT LoadProperties( ITfContext *pContext, 
                        ITextStoreACPServices *pServices, 
                        IStream *pStream)
{
    HRESULT hr;
    ULONG   uRead;
    TF_PERSISTENT_PROPERTY_HEADER_ACP PropHeader;

    /*
    Read each property header and property data from the stream. The 
    list of properties is terminated by a TF_PERSISTENT_PROPERTY_HEADER_ACP 
    structure with a cb member of zero.
    */
    hr = pStream->Read(&PropHeader, sizeof(PropHeader), &uRead);
    while(  SUCCEEDED(hr) && 
            (sizeof(PropHeader) == uRead) && 
            (0 != PropHeader.cb))
    {
        ITfProperty *pProp;

        hr = pContext->GetProperty(PropHeader.guidType, &pProp);
        if(SUCCEEDED(hr))
        {
            /*
            Have TSF read the property data from the stream. This call 
            requests a read-only lock, so be sure it can be granted 
            or else this method will fail.
            */
            CTSFPersistentPropertyLoader *pLoader = new CTSFPersistentPropertyLoader(&PropHeader, pStream);
            hr = pServices->Unserialize(pProp, &PropHeader, NULL, pLoader);

            pProp->Release();
        }

        //Read the next header. 
        hr = pStream->Read(&PropHeader, sizeof(PropHeader), &uRead);
    }

    return hr;
}

```



 

 
