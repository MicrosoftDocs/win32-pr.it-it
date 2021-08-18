---
description: In Windows Vista, Microsoft Media Foundation i metadati tramite l'interfaccia IMFMetadata.
ms.assetid: a26e40c2-1717-4a13-8bf0-e41376a8d317
title: Provider di metadati in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1edf65b59e0f47e603b057f49a76d8721b8733849937cb29fd0afbe0b9b44920
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827071"
---
# <a name="metadata-providers-in-windows-vista"></a>Provider di metadati in Windows Vista

In Windows Vista, Microsoft Media Foundation i metadati tramite [**l'interfaccia IMFMetadata.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)

## <a name="reading-metadata"></a>Lettura di metadati

Per leggere i metadati da un'origine multimediale, seguire questa procedura:

1.  Ottenere un puntatore [**all'interfaccia IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) dell'origine multimediale. È possibile usare [**l'interfaccia IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) per ottenere un **puntatore IMFMediaSource.**
2.  Chiamare [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) per ottenere il descrittore di presentazione dell'origine multimediale.
3.  Chiamare [**MFGetService nell'origine**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) multimediale per ottenere un puntatore [**all'interfaccia IMFMetadataProvider.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) Nel parametro *guidService* di **MFGetService** specificare il valore **MF \_ METADATA PROVIDER \_ \_ SERVICE**. Se l'origine non supporta **l'interfaccia IMFMetadataProvider,** **MFGetService** restituisce **MF \_ E \_ UNSUPPORTED \_ SERVICE**.
4.  Chiamare [**IMFMetadataProvider::GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) e passare un puntatore al descrittore di presentazione. Questo metodo restituisce un puntatore [**all'interfaccia IMFMetadata.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)
    -   Per ottenere i metadati a livello di flusso, chiamare [**prima IMFStreamDescriptor::GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) per ottenere l'identificatore del flusso. Passare quindi l'identificatore del flusso *nel parametro dwStreamIdentifier* di [**GetMFMetadata.**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata)
    -   Per ottenere i metadati a livello di presentazione, *impostare dwStreamIdentifier* su zero.
5.  \[Facoltativo \] [**Chiamare IMFMetadata::GetAllLanguages**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getalllanguages) per ottenere un elenco delle lingue in cui sono disponibili i metadati. Le lingue vengono identificate usando tag di lingua conformi a RFC 1766.
6.  \[Facoltativo \] Chiamare [**IMFMetadata::SetLanguage**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage) per selezionare la lingua.
7.  \[Facoltativo \] [**Chiamare IMFMetadata::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) per ottenere un elenco dei nomi di tutte le proprietà dei metadati per questo flusso o presentazione.
8.  Chiamare [**IMFMetadata::GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) per ottenere un valore specifico della proprietà dei metadati, passando il nome della proprietà.

Il codice seguente illustra i passaggi da 2 a 4:


```C++
HRESULT GetMetadata(
    IMFMediaSource *pSource, IMFMetadata **ppMetadata, DWORD dwStream = 0)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFMetadataProvider *pProvider = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFGetService(
        pSource, MF_METADATA_PROVIDER_SERVICE, IID_PPV_ARGS(&pProvider));

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProvider->GetMFMetadata(pPD, dwStream, 0, ppMetadata);

done:
    SafeRelease(&pPD);
    SafeRelease(&pProvider);
    return hr;
}
```



Il codice seguente illustra i passaggi da 7 a 8. Si supponga `DisplayProperty` che sia una funzione che visualizza un valore **PROPVARIANT.**


```C++
HRESULT DisplayMetadata(IMFMetadata *pMetadata)
{
    PROPVARIANT varNames;
    HRESULT hr = pMetadata->GetAllPropertyNames(&varNames);
    if (FAILED(hr))
    {
        return hr;
    }

    for (ULONG i = 0; i < varNames.calpwstr.cElems; i++)
    {
        wprintf(L"%s\n", varNames.calpwstr.pElems[i]);

        PROPVARIANT varValue;
        hr = pMetadata->GetProperty( varNames.calpwstr.pElems[i], &varValue );
        if (SUCCEEDED(hr))
        {
            DisplayProperty(varValue);
            PropVariantClear(&varValue);
        }
    }

    PropVariantClear(&varNames);
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Metadati multimediali](media-metadata.md)
</dt> <dt>

[Provider di metadati della shell](shell-metadata-providers.md)
</dt> </dl>

 

 



