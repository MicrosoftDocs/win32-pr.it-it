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
# <a name="properties-common-elements"></a>Proprietà (elementi comuni)

Framework servizi di testo (TSF) fornisce proprietà che associano metadati a un intervallo di testo. Queste proprietà includono, ma non sono limitate, gli attributi di visualizzazione, ad esempio il testo in grassetto, l'identificatore della lingua del testo e i dati non elaborati forniti da un servizio di testo, ad esempio i dati audio associati al testo dal servizio di riconoscimento vocale.

L'esempio seguente illustra come visualizzare una proprietà di colore del testo ipotetica con i possibili valori rosso (R), verde (G) o blu (B).


```C++
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



Le proprietà di tipi diversi possono sovrapporsi. Si consideri ad esempio l'esempio precedente e si aggiunge un attributo di testo che può essere in grassetto (B) o corsivo (I).


```C++
ATTRIB:BBBBBBB      IIIIIIIIIIII
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



Il testo "this" sarebbe in grassetto, "is" sarebbe sia grassetto che rosso, "some" verrebbe visualizzato normalmente, "colored" sarebbe verde e corsivo e "text" sarebbe in corsivo.

Le proprietà dello stesso tipo non possono sovrapporsi. Ad esempio, la situazione seguente non è consentita perché "is" e "colored" hanno valori sovrapposti degli stessi tipi.


```C++
COLOR: GGG GGGG RRR BBBBGGG     
COLOR:      RR      GGGGGGGG
TEXT:  this is some colored text
```



## <a name="property-types"></a>Tipi di proprietà

TSF definisce tre tipi diversi di proprietà.



|   Tipo di proprietà             |   Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Static         | Un oggetto proprietà statica archivia i dati della proprietà con testo. Archivia inoltre l'intervallo di informazioni di testo per ogni intervallo a cui si applica la proprietà . ITfReadOnlyProperty::GetType restituisce la categoria GUID \_ TFCAT \_ PROPSTYLE \_ STATIC.                                                                                                                                                                                                                      |
| Static-Compact | Un oggetto proprietà compatta statica è identico a un oggetto proprietà statica, ad eccezione di una proprietà compatta statica che non archivia dati di intervallo. Quando viene richiesto l'intervallo coperto da una proprietà compatta statica, viene creato un intervallo per ogni gruppo di proprietà adiacenti. Le proprietà compatte statiche sono il modo più efficiente per archiviare le proprietà in base al singolo carattere. ITfReadOnlyProperty::GetType restituisce la categoria \_ GUID TFCAT \_ PROPSTYLE \_ STATICCOMPACT. |
| Personalizzato         | Un oggetto proprietà personalizzata archivia le informazioni sull'intervallo per ogni intervallo a cui si applica la proprietà . Non archivia tuttavia i dati effettivi per la proprietà . Una proprietà personalizzata archivia invece un oggetto ITfPropertyStore. TSF Manager usa questo oggetto per accedere ai dati delle proprietà e gestirvi. ITfReadOnlyProperty::GetType restituisce la categoria GUID \_ TFCAT \_ PROPSTYLE \_ CUSTOM.                                                                    |



 

## <a name="working-with-properties"></a>Uso di proprietà

Il valore e gli attributi della proprietà vengono ottenuti usando [l'interfaccia ITfReadOnlyProperty](/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty) e modificati tramite [l'interfaccia ITfProperty.](/windows/desktop/api/Msctf/nn-msctf-itfproperty)

Se è necessario un tipo di proprietà specifico, viene [usato ITfContext::GetProperty.](/windows/desktop/api/msctf/nf-msctf-itfcontext-getproperty) **ITfContext::GetProperty** richiede un **GUID** che identifica la proprietà da ottenere. TSF definisce un set di identificatori di [proprietà](predefined-properties.md) predefiniti usati oppure un servizio di testo può definire i propri identificatori di proprietà. Se si usa una proprietà personalizzata, il provider di proprietà deve pubblicare il **GUID** della proprietà e il formato dei dati ottenuti.

Ad esempio, per ottenere il **CLSID** per il proprietario di un intervallo di testo, chiamare **ITfContext::GetProperty** per ottenere l'oggetto proprietà, chiamare [ITfProperty::FindRange](/windows/desktop/api/msctf/nf-msctf-itfproperty-findrange) per ottenere l'intervallo che copre interamente la proprietà, quindi chiamare [ITfReadOnlyProperty::GetValue](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-getvalue) per ottenere un [oggetto TfGuidAtom](/windows/desktop/TSF/tfguidatom) che rappresenta il **CLSID** del servizio di testo proprietario del testo. Nell'esempio seguente viene illustrata una funzione che, dati un contesto, un intervallo e un cookie di modifica, o ottiene il **CLSID** del servizio di testo proprietario del testo.


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



Le proprietà possono essere enumerate anche ottenendo [un'interfaccia IEnumTfProperties](/windows/desktop/api/msctf/nn-msctf-ienumtfproperties) da [ITfContext::EnumProperties](/windows/desktop/api/msctf/nf-msctf-itfcontext-enumproperties).

## <a name="persistent-storage-of-properties"></a>Archiviazione permanente delle proprietà

Spesso le proprietà sono trasparenti per un'applicazione e vengono usate da uno o più servizi di testo. Per mantenere i dati delle proprietà, ad esempio durante il salvataggio in un file, un'applicazione deve serializzare i dati della proprietà quando vengono archiviati e annullare la deserializzazione dei dati della proprietà quando i dati vengono ripristinati. In questo caso, l'applicazione non deve essere interessata alle singole proprietà, ma deve enumerare tutte le proprietà nel contesto e archiviarle.

Quando si archiviano i dati delle proprietà, un'applicazione deve eseguire i passaggi seguenti.

1.  Ottenere un enumeratore di proprietà chiamando **ITfContext::EnumProperties**.
2.  Enumerare ogni proprietà chiamando [IEnumTfProperties::Next.](/windows/desktop/api/msctf/nf-msctf-ienumtfproperties-next)
3.  Per ogni proprietà, ottenere un enumeratore di intervallo chiamando [ITfReadOnlyProperty::EnumRanges](/windows/desktop/api/msctf/nf-msctf-itfreadonlyproperty-enumranges).
4.  Enumerare ogni intervallo nella proprietà chiamando [IEnumTfRanges::Next.](/windows/desktop/api/msctf/nf-msctf-ienumtfranges-next)
5.  Per ogni intervallo nella proprietà , chiamare [ITextStoreACPServices::Serialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize) con la proprietà , l'intervallo, una struttura [ \_ \_ \_ \_ ACP TF PERSISTENT PROPERTY HEADER](/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp) e un oggetto flusso implementato dall'applicazione.
6.  Scrivere il contenuto della struttura **TF \_ PERSISTENT PROPERTY \_ HEADER \_ \_ ACP** nella memoria persistente.
7.  Scrivere il contenuto dell'oggetto flusso nella memoria persistente.
8.  Continuare i passaggi precedenti per tutti gli intervalli in tutte le proprietà.
9.  L'applicazione deve scrivere un tipo di terminiator nel flusso in modo che, quando i dati vengono ripristinati, sia possibile identificare un punto di arresto.


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



**ITextStoreACPServices::Serialize**[ITfPropertyStore::Serialize](/windows/desktop/api/msctf/nf-msctf-itfpropertystore-serialize)

Quando si ripristinano i dati delle proprietà, un'applicazione deve eseguire i passaggi seguenti.

1.  Impostare il puntatore del flusso all'inizio della prima struttura **TF \_ PERSISTENT PROPERTY \_ HEADER \_ \_ ACP.**
2.  Leggere la struttura **TF \_ PERSISTENT PROPERTY \_ HEADER \_ \_ ACP.**
3.  Chiamare **ITfContext::GetProperty con** il **membro guidType** della struttura **ACP TF \_ PERSISTENT PROPERTY \_ \_ HEADER. \_**
4.  A questo punto, l'applicazione può eseguire una delle due operazioni seguenti.
    1.  Creare un'istanza di [un oggetto ITfPersistentPropertyLoaderACP](/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp) che l'applicazione deve implementare. Chiamare quindi [ITextStoreACPServices::Unserialize](/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize) con **NULL** per *pStream* e **il puntatore ITfPersistentPropertyLoaderACP.**
    2.  Passare il flusso di input **a ITextStoreACPServices::Unserialize** e **NULL per** *pLoader*.

    Il primo metodo è preferibile perché è il più efficiente. L'implementazione del secondo metodo fa sì che tutti i dati della proprietà siano letti dal flusso durante la **chiamata ITextStoreACPServices::Unserialize.** Il primo metodo fa sì che i dati della proprietà siano letti su richiesta in un secondo momento.
5.  Ripetere i passaggi precedenti fino a quando tutti i blocchi di proprietà non vengono deserializzati.


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



 

 
