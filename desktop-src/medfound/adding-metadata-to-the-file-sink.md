---
description: Informazioni sull'aggiunta di metadati al sink di file ASF, che un'applicazione può usare per archiviare i dati multimediali asf in un file.
ms.assetid: ecfddf4e-71b4-42c4-8b54-9868cec6ed9b
title: Aggiunta di metadati al sink di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16ea86a09ff9e3d2a25bbf8d00d46691fd803365
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409964"
---
# <a name="adding-metadata-to-the-file-sink"></a>Aggiunta di metadati al sink di file

Il sink di file ASF è un'implementazione di [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fornita da Media Foundation che un'applicazione può usare per archiviare i dati multimediali asf in un file. Per informazioni sul modello a oggetti di ASF Media Sinks e sull'utilizzo generale, vedere [ASF Media Sinks](asf-media-sinks.md).

Dopo [aver creato il sink di file ASF,](creating-the-asf-file-sink.md)è necessario configurarlo con informazioni sui flussi e le informazioni di codifica nel file di output. Queste procedure sono descritte in [Aggiunta di informazioni sul flusso al sink di file ASF](adding-stream-information-to-the-asf-file-sink.md) e [impostazione delle proprietà nel sink di file](setting-properties-in-the-file-sink.md). È anche possibile aggiungere informazioni sui metadati includendo coppie nome/valore, ad esempio "Autore", Titolo". Questo argomento descrive il processo di aggiunta di informazioni sui metadati al sink di file in modo che venga visualizzato nell'oggetto intestazione [ASF finale.](asf-file-structure.md)

È possibile aggiungere informazioni sui metadati al sink del file ASF prima di compilare la topologia di codifica. L'oggetto ContentInfo asf per il sink di file tiene traccia delle proprietà dei metadati e viene esposto all'applicazione tramite [**l'interfaccia IMFMetadata.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) Alcune di queste proprietà, ad esempio "IsVBR" che indica se il file contiene flussi VBR (Variable Bit Rate), vengono impostate automaticamente dal sink di file analizzando le proprietà di codifica del flusso impostate.

Per un elenco completo delle proprietà, vedere l'argomento "Elenco attributi" nella documentazione di Format SDK.

## <a name="using-the-imfmetadata-interface-on-the-asf-file-sink"></a>Uso dell'interfaccia IMFMetadata nel sink di file ASF

1.  Eseguire una query sull'oggetto sink del file ASF per ottenere un puntatore all'implementazione [**dell'interfaccia IMFMetadataProvider.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)
2.  Chiamare [**IMFMetadataProvider::GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) per ottenere un [**puntatore IMFMetadata.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)

    Il *parametro pPresentationDescriptor* viene ignorato e l'applicazione può passare **NULL.** Se l'applicazione passa zero come identificatore di flusso nel *parametro dwStreamIdentifier,* il metodo recupera i metadati applicabili all'intero file ASF. In caso contrario, vengono recuperati solo i metadati per il flusso.

3.  Chiamare [**IMFMetadata::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) per recuperare l'elenco delle proprietà di codifica file impostate nel contenuto multimediale.
4.  Chiamare [**IMFMetadata::GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) per ottenere i valori della proprietà.

## <a name="example"></a>Esempio

Il codice di esempio seguente illustra come enumerare i nomi e i valori delle proprietà impostati nel file ASF.


```C++
/////////////////////////////////////////////////////////////////////
// Name: ListASFProperties
//
// Enumerates the metadata properties of the ASF file. 
//
// pContentInfo: Pointer to the ASF ContentInfo object.
/////////////////////////////////////////////////////////////////////

HRESULT ListASFProperties(IMFASFContentInfo *pContentInfo)
{
    HRESULT hr = S_OK;
    
    PROPVARIANT varNames;
    PropVariantInit(&varNames);

    PROPVARIANT varValue;
    PropVariantInit(&varValue);

    IMFMetadataProvider* pProvider = NULL;
    IMFMetadata* pMetadata = NULL;

    // Query the ContentInfo object for IMFMetadataProvider.
    CHECK_HR(hr = pContentInfo->QueryInterface(IID_IMFMetadataProvider,
        (void**)&pProvider));

    // Get a pointer to IMFMetadata for file-wide metadata.
    CHECK_HR(hr = pProvider->GetMFMetadata(NULL, 0, 0, &pMetadata));

    // Get the property names that are stored in the metadata object.
    CHECK_HR(hr = pMetadata->GetAllPropertyNames(&varNames));

    // Loop through the properties and get their values.
    if (varNames.vt == (VT_VECTOR | VT_LPWSTR))
    {
        ULONG cElements = varNames.calpwstr.cElems;
        for (ULONG i = 0; i < cElements; i++)
        {
            const WCHAR* sName = varNames.calpwstr.pElems[i];
            CHECK_HR(hr = pMetadata->GetProperty(sName, &varValue));
            //Use the property values. Not shown.
            PropVariantClear(&varValue);
        }
    }
done:
    PropVariantClear(&varNames);
    PropVariantClear(&varValue);
    SAFE_RELEASE (pMetaData);
    SAFE_RELEASE (pProvider);
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sink di supporti ASF](asf-media-sinks.md)
</dt> <dt>

[Componenti ASF del livello pipeline](pipeline-layer-asf-components.md)
</dt> <dt>

[Supporto di ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



