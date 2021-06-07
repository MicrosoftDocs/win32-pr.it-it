---
title: Proprietà (elementi comuni)
description: Framework servizi di testo (TSF) fornisce proprietà che associano metadati a un intervallo di testo.
ms.assetid: d1d0dd99-f303-4355-9835-917de9491a0b
keywords:
- Framework servizi di testo (TSF), proprietà
- TSF (Framework servizi di testo),properties
- servizi di testo, proprietà
- applicazioni abilitate per TSF,proprietà
- properties
- Framework servizi di testo (TSF), tipi di proprietà
- TSF (Framework servizi di testo),tipi di proprietà
- servizi di testo, tipi di proprietà
- applicazioni abilitate per TSF, tipi di proprietà
- proprietà (tipi)
- Framework servizi di testo (TSF), archiviazione permanente delle proprietà
- TSF (Framework servizi di testo),archiviazione permanente delle proprietà
- servizi di testo, archiviazione permanente delle proprietà
- Applicazioni abilitate per TSF, archiviazione permanente delle proprietà
- archiviazione permanente delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b94a1f6c504fcd3e6491af9e66b399d59a3eeb
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524215"
---
# <a name="properties-common-elements"></a><span data-ttu-id="46569-118">Proprietà (elementi comuni)</span><span class="sxs-lookup"><span data-stu-id="46569-118">Properties (Common Elements)</span></span>

<span data-ttu-id="46569-119">Framework servizi di testo (TSF) fornisce proprietà che associano metadati a un intervallo di testo.</span><span class="sxs-lookup"><span data-stu-id="46569-119">Text Services Framework (TSF) provides properties that associate metadata with a range of text.</span></span> <span data-ttu-id="46569-120">Queste proprietà includono, ma non sono limitate, gli attributi di visualizzazione, ad esempio il testo in grassetto, l'identificatore della lingua del testo e i dati non elaborati forniti da un servizio di testo, ad esempio i dati audio associati al testo dal servizio di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="46569-120">These properties include, but are not limited to, display attributes such as bold text, the language identifier of the text, and raw data provided by a text service such as the audio data associated with text from the speech text service.</span></span>

<span data-ttu-id="46569-121">L'esempio seguente illustra come visualizzare una proprietà di colore del testo ipotetica con i possibili valori rosso (R), verde (G) o blu (B).</span><span class="sxs-lookup"><span data-stu-id="46569-121">The following example demonstrates how a hypothetical text color property with possible values of red (R), green (G), or blue (B) can be viewed.</span></span>


```C++
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



<span data-ttu-id="46569-122">Le proprietà di tipi diversi possono sovrapporsi.</span><span class="sxs-lookup"><span data-stu-id="46569-122">Properties of different types can overlap.</span></span> <span data-ttu-id="46569-123">Si consideri ad esempio l'esempio precedente e si aggiunge un attributo di testo che può essere in grassetto (B) o corsivo (I).</span><span class="sxs-lookup"><span data-stu-id="46569-123">For example, take the previous example and add a text attribute that can be either bold (B) or italic (I).</span></span>


```C++
ATTRIB:BBBBBBB      IIIIIIIIIIII
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



<span data-ttu-id="46569-124">Il testo "this" sarebbe in grassetto, "is" sarebbe sia grassetto che rosso, "some" verrebbe visualizzato normalmente, "colored" sarebbe verde e corsivo e "text" sarebbe in corsivo.</span><span class="sxs-lookup"><span data-stu-id="46569-124">The text "this" would be bold, "is" would be both bold and red, "some" would be displayed normally, "colored" would be green and italicized and "text" would be italicized.</span></span>

<span data-ttu-id="46569-125">Le proprietà dello stesso tipo non possono sovrapporsi.</span><span class="sxs-lookup"><span data-stu-id="46569-125">Properties of the same type cannot overlap.</span></span> <span data-ttu-id="46569-126">Ad esempio, la situazione seguente non è consentita perché "is" e "colored" hanno valori sovrapposti degli stessi tipi.</span><span class="sxs-lookup"><span data-stu-id="46569-126">For example, the following situation is not allowed because "is" and "colored" have overlapping values of the same types.</span></span>


```C++
COLOR: GGG GGGG RRR BBBBGGG     
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



## <a name="property-types"></a><span data-ttu-id="46569-127">Tipi di proprietà</span><span class="sxs-lookup"><span data-stu-id="46569-127">Property Types</span></span>

<span data-ttu-id="46569-128">TSF definisce tre tipi diversi di proprietà.</span><span class="sxs-lookup"><span data-stu-id="46569-128">TSF defines three different types of properties.</span></span>



|   <span data-ttu-id="46569-129">Tipo di proprietà</span><span class="sxs-lookup"><span data-stu-id="46569-129">Property type</span></span>             |   <span data-ttu-id="46569-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46569-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46569-131">Static</span><span class="sxs-lookup"><span data-stu-id="46569-131">Static</span></span>         | <span data-ttu-id="46569-132">Un oggetto proprietà statica archivia i dati della proprietà con testo.</span><span class="sxs-lookup"><span data-stu-id="46569-132">A static property object stores the property data with text.</span></span> <span data-ttu-id="46569-133">Archivia inoltre l'intervallo di informazioni di testo per ogni intervallo a cui si applica la proprietà .</span><span class="sxs-lookup"><span data-stu-id="46569-133">It also stores the range of text information for each range that the property applies to.</span></span> <span data-ttu-id="46569-134">ITfReadOnlyProperty::GetType restituisce la categoria GUID \_ TFCAT \_ PROPSTYLE \_ STATIC.</span><span class="sxs-lookup"><span data-stu-id="46569-134">ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_STATIC category.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="46569-135">Static-Compact</span><span class="sxs-lookup"><span data-stu-id="46569-135">Static-Compact</span></span> | <span data-ttu-id="46569-136">Un oggetto proprietà compatta statica è identico a un oggetto proprietà statica, ad eccezione di una proprietà compatta statica che non archivia dati di intervallo.</span><span class="sxs-lookup"><span data-stu-id="46569-136">A static-compact property object is identical to a static property object except a static-compact property does not store range data.</span></span> <span data-ttu-id="46569-137">Quando viene richiesto l'intervallo coperto da una proprietà compatta statica, viene creato un intervallo per ogni gruppo di proprietà adiacenti.</span><span class="sxs-lookup"><span data-stu-id="46569-137">When the range covered by a static-compact property is requested, a range is created for each group of adjacent properties.</span></span> <span data-ttu-id="46569-138">Le proprietà compatte statiche sono il modo più efficiente per archiviare le proprietà in base al singolo carattere.</span><span class="sxs-lookup"><span data-stu-id="46569-138">Static-compact properties are the most efficient way to store properties on a per-character basis.</span></span> <span data-ttu-id="46569-139">ITfReadOnlyProperty::GetType restituisce la categoria \_ GUID TFCAT \_ PROPSTYLE \_ STATICCOMPACT.</span><span class="sxs-lookup"><span data-stu-id="46569-139">ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_STATICCOMPACT category.</span></span> |
| <span data-ttu-id="46569-140">Personalizzato</span><span class="sxs-lookup"><span data-stu-id="46569-140">Custom</span></span>         | <span data-ttu-id="46569-141">Un oggetto proprietà personalizzata archivia le informazioni sull'intervallo per ogni intervallo a cui si applica la proprietà .</span><span class="sxs-lookup"><span data-stu-id="46569-141">A custom property object stores the range information for each range that the property applies to.</span></span> <span data-ttu-id="46569-142">Non archivia tuttavia i dati effettivi per la proprietà .</span><span class="sxs-lookup"><span data-stu-id="46569-142">It does not, however, store the actual data for the property.</span></span> <span data-ttu-id="46569-143">Una proprietà personalizzata archivia invece un oggetto ITfPropertyStore.</span><span class="sxs-lookup"><span data-stu-id="46569-143">Instead, a custom property stores an ITfPropertyStore object.</span></span> <span data-ttu-id="46569-144">TSF Manager usa questo oggetto per accedere ai dati delle proprietà e gestirvi. ITfReadOnlyProperty::GetType restituisce la categoria GUID \_ TFCAT \_ PROPSTYLE \_ CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="46569-144">The TSF manager uses this object to access and maintain the property data.ITfReadOnlyProperty::GetType returns the GUID\_TFCAT\_PROPSTYLE\_CUSTOM category.</span></span>                                                                    |



 

## <a name="working-with-properties"></a><span data-ttu-id="46569-145">Uso di proprietà</span><span class="sxs-lookup"><span data-stu-id="46569-145">Working with Properties</span></span>

<span data-ttu-id="46569-146">Il valore e gli attributi della proprietà vengono ottenuti usando [l'interfaccia ITfReadOnlyProperty](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) e modificati tramite [l'interfaccia ITfProperty.](/windows/desktop/api/Msctf/nn-msctf-itfproperty)</span><span class="sxs-lookup"><span data-stu-id="46569-146">The property value and attributes are obtained using the [ITfReadOnlyProperty](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) interface and modified using the [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) interface.</span></span>

<span data-ttu-id="46569-147">Se è necessario un tipo di proprietà specifico, viene [usato ITfContext::GetProperty.](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty)</span><span class="sxs-lookup"><span data-stu-id="46569-147">If a specific property type is required, then [ITfContext::GetProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty) is used.</span></span> <span data-ttu-id="46569-148">**ITfContext::GetProperty** richiede un **GUID** che identifica la proprietà da ottenere.</span><span class="sxs-lookup"><span data-stu-id="46569-148">**ITfContext::GetProperty** requires a **GUID** that identifies the property to obtain.</span></span> <span data-ttu-id="46569-149">TSF definisce un set di identificatori di [proprietà](predefined-properties.md) predefiniti usati oppure un servizio di testo può definire i propri identificatori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="46569-149">TSF defines a set of [predefined property identifiers](predefined-properties.md) used or a text service can define its own property identifiers.</span></span> <span data-ttu-id="46569-150">Se si usa una proprietà personalizzata, il provider di proprietà deve pubblicare il **GUID** della proprietà e il formato dei dati ottenuti.</span><span class="sxs-lookup"><span data-stu-id="46569-150">If a custom property is used, the property provider must publish the property **GUID** and the format of the data obtained.</span></span>

<span data-ttu-id="46569-151">Ad esempio, per ottenere il **CLSID** per il proprietario di un intervallo di testo, chiamare **ITfContext::GetProperty** per ottenere l'oggetto proprietà, chiamare [ITfProperty::FindRange](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) per ottenere l'intervallo che copre interamente la proprietà, quindi chiamare [ITfReadOnlyProperty::GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) per ottenere un [oggetto TfGuidAtom](/windows/desktop/TSF/tfguidatom) che rappresenta il **CLSID** del servizio di testo proprietario del testo.</span><span class="sxs-lookup"><span data-stu-id="46569-151">For example, to obtain the **CLSID** for the owner of a range of text, call **ITfContext::GetProperty** to obtain the property object, call [ITfProperty::FindRange](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) to obtain the range that entirely covers the property, then call [ITfReadOnlyProperty::GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) to get a [TfGuidAtom](/windows/desktop/TSF/tfguidatom) that represents the **CLSID** of the text service that owns the text.</span></span> <span data-ttu-id="46569-152">Nell'esempio seguente viene illustrata una funzione che, dati un contesto, un intervallo e un cookie di modifica, o ottiene il **CLSID** del servizio di testo proprietario del testo.</span><span class="sxs-lookup"><span data-stu-id="46569-152">The following example shows a function that, given a context, range and an edit cookie, will obtain the **CLSID** of the text service that owns the text.</span></span>


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



<span data-ttu-id="46569-153">Le proprietà possono essere enumerate anche ottenendo [un'interfaccia IEnumTfProperties](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) da [ITfContext::EnumProperties](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties).</span><span class="sxs-lookup"><span data-stu-id="46569-153">Properties can also be enumerated by obtaining an [IEnumTfProperties](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) interface from [ITfContext::EnumProperties](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties).</span></span>

## <a name="persistent-storage-of-properties"></a><span data-ttu-id="46569-154">Archiviazione permanente delle proprietà</span><span class="sxs-lookup"><span data-stu-id="46569-154">Persistent Storage of Properties</span></span>

<span data-ttu-id="46569-155">Spesso le proprietà sono trasparenti per un'applicazione e vengono usate da uno o più servizi di testo.</span><span class="sxs-lookup"><span data-stu-id="46569-155">Often, properties are transparent to an application and are used by one or more text services.</span></span> <span data-ttu-id="46569-156">Per mantenere i dati delle proprietà, ad esempio durante il salvataggio in un file, un'applicazione deve serializzare i dati della proprietà quando vengono archiviati e annullare la deserializzazione dei dati della proprietà quando i dati vengono ripristinati.</span><span class="sxs-lookup"><span data-stu-id="46569-156">In order to preserve the property data, such as when saving to a file, an application must serialize the property data when it is stored and unserialize the property data when the data is restored.</span></span> <span data-ttu-id="46569-157">In questo caso, l'applicazione non deve essere interessata alle singole proprietà, ma deve enumerare tutte le proprietà nel contesto e archiviarle.</span><span class="sxs-lookup"><span data-stu-id="46569-157">In this case, the application should not be interested in individual properties, but should enumerate all properties in the context and store them.</span></span>

<span data-ttu-id="46569-158">Quando si archiviano i dati delle proprietà, un'applicazione deve eseguire i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="46569-158">When storing property data, an application should perform the following steps.</span></span>

1.  <span data-ttu-id="46569-159">Ottenere un enumeratore di proprietà chiamando **ITfContext::EnumProperties**.</span><span class="sxs-lookup"><span data-stu-id="46569-159">Obtain a property enumerator by calling **ITfContext::EnumProperties**.</span></span>
2.  <span data-ttu-id="46569-160">Enumerare ogni proprietà chiamando [IEnumTfProperties::Next.](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next)</span><span class="sxs-lookup"><span data-stu-id="46569-160">Enumerate each property by calling [IEnumTfProperties::Next](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next).</span></span>
3.  <span data-ttu-id="46569-161">Per ogni proprietà, ottenere un enumeratore di intervallo chiamando [ITfReadOnlyProperty::EnumRanges](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges).</span><span class="sxs-lookup"><span data-stu-id="46569-161">For each property, obtain a range enumerator by calling [ITfReadOnlyProperty::EnumRanges](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges).</span></span>
4.  <span data-ttu-id="46569-162">Enumerare ogni intervallo nella proprietà chiamando [IEnumTfRanges::Next.](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next)</span><span class="sxs-lookup"><span data-stu-id="46569-162">Enumerate each range in the property by calling [IEnumTfRanges::Next](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next).</span></span>
5.  <span data-ttu-id="46569-163">Per ogni intervallo nella proprietà , chiamare [ITextStoreACPServices::Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) con la proprietà , l'intervallo, una struttura [ \_ \_ \_ \_ ACP TF PERSISTENT PROPERTY HEADER](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) e un oggetto flusso implementato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="46569-163">For each range in the property, call [ITextStoreACPServices::Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) with the property, range, a [TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) structure, and a stream object implemented by the application.</span></span>
6.  <span data-ttu-id="46569-164">Scrivere il contenuto della struttura **TF \_ PERSISTENT PROPERTY \_ HEADER \_ \_ ACP** nella memoria persistente.</span><span class="sxs-lookup"><span data-stu-id="46569-164">Write the contents of the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure into persistent memory.</span></span>
7.  <span data-ttu-id="46569-165">Scrivere il contenuto dell'oggetto flusso nella memoria persistente.</span><span class="sxs-lookup"><span data-stu-id="46569-165">Write the contents of the stream object into persistent memory.</span></span>
8.  <span data-ttu-id="46569-166">Continuare i passaggi precedenti per tutti gli intervalli in tutte le proprietà.</span><span class="sxs-lookup"><span data-stu-id="46569-166">Continue the previous steps for all of the ranges in all of the properties.</span></span>
9.  <span data-ttu-id="46569-167">L'applicazione deve scrivere un tipo di terminiator nel flusso in modo che, quando i dati vengono ripristinati, sia possibile identificare un punto di arresto.</span><span class="sxs-lookup"><span data-stu-id="46569-167">The application should write some type of terminiator into the stream so that, when the data is restored, a stopping point can be identified.</span></span>


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



<span data-ttu-id="46569-168">**ITextStoreACPServices::Serialize**[ITfPropertyStore::Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)</span><span class="sxs-lookup"><span data-stu-id="46569-168">**ITextStoreACPServices::Serialize**[ITfPropertyStore::Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)</span></span>

<span data-ttu-id="46569-169">Quando si ripristinano i dati delle proprietà, un'applicazione deve eseguire i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="46569-169">When restoring property data, an application should perform the following steps.</span></span>

1.  <span data-ttu-id="46569-170">Impostare il puntatore del flusso all'inizio della prima struttura **TF \_ PERSISTENT PROPERTY \_ HEADER \_ \_ ACP.**</span><span class="sxs-lookup"><span data-stu-id="46569-170">Set the stream pointer to the start of the first **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
2.  <span data-ttu-id="46569-171">Leggere la struttura **TF \_ PERSISTENT PROPERTY \_ HEADER \_ \_ ACP.**</span><span class="sxs-lookup"><span data-stu-id="46569-171">Read the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
3.  <span data-ttu-id="46569-172">Chiamare **ITfContext::GetProperty con** il **membro guidType** della struttura **ACP TF \_ PERSISTENT PROPERTY \_ \_ HEADER. \_**</span><span class="sxs-lookup"><span data-stu-id="46569-172">Call **ITfContext::GetProperty** with the **guidType** member of the **TF\_PERSISTENT\_PROPERTY\_HEADER\_ACP** structure.</span></span>
4.  <span data-ttu-id="46569-173">A questo punto, l'applicazione può eseguire una delle due operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="46569-173">The application can do one of two things at this point.</span></span>
    1.  <span data-ttu-id="46569-174">Creare un'istanza di [un oggetto ITfPersistentPropertyLoaderACP](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) che l'applicazione deve implementare.</span><span class="sxs-lookup"><span data-stu-id="46569-174">Create an instance of an [ITfPersistentPropertyLoaderACP](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) object that the application must implement.</span></span> <span data-ttu-id="46569-175">Chiamare quindi [ITextStoreACPServices::Unserialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) con **NULL** per *pStream* e **il puntatore ITfPersistentPropertyLoaderACP.**</span><span class="sxs-lookup"><span data-stu-id="46569-175">Then call [ITextStoreACPServices::Unserialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) with **NULL** for *pStream* and the **ITfPersistentPropertyLoaderACP** pointer.</span></span>
    2.  <span data-ttu-id="46569-176">Passare il flusso di input **a ITextStoreACPServices::Unserialize** e **NULL per** *pLoader*.</span><span class="sxs-lookup"><span data-stu-id="46569-176">Pass the input stream to **ITextStoreACPServices::Unserialize** and **NULL** for *pLoader*.</span></span>

    <span data-ttu-id="46569-177">Il primo metodo è preferibile perché è il più efficiente.</span><span class="sxs-lookup"><span data-stu-id="46569-177">The first method is preferred as it is the most efficient.</span></span> <span data-ttu-id="46569-178">L'implementazione del secondo metodo fa sì che tutti i dati della proprietà siano letti dal flusso durante la **chiamata ITextStoreACPServices::Unserialize.**</span><span class="sxs-lookup"><span data-stu-id="46569-178">Implementing the second method causes all of the property data to be read from the stream during the **ITextStoreACPServices::Unserialize** call.</span></span> <span data-ttu-id="46569-179">Il primo metodo fa sì che i dati della proprietà siano letti su richiesta in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="46569-179">The first method causes the property data to be read on demand at a later time.</span></span>
5.  <span data-ttu-id="46569-180">Ripetere i passaggi precedenti fino a quando tutti i blocchi di proprietà non vengono deserializzati.</span><span class="sxs-lookup"><span data-stu-id="46569-180">Repeat the previous steps until all property blocks are unserialized.</span></span>


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



 

 
