---
description: Enumerazione dei tipi di supporto
ms.assetid: 7878885f-c285-4744-8eab-445678dcfd49
title: Enumerazione dei tipi di supporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3909c25e9ae5f90a3084eebb531431cc93ef46cd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351391"
---
# <a name="enumerating-media-types"></a>Enumerazione dei tipi di supporto

I pin supportano il metodo [**Ipin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) , che enumera i tipi di supporto preferiti del PIN. Restituisce un puntatore all'interfaccia [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) . Il metodo [**IEnumMediaTypes:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) recupera i puntatori alle strutture del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) che descrivono i tipi di supporto.

L'enumeratore Media Type esiste principalmente per consentire a Filter Graph Manager di effettuare connessioni intelligenti e probabilmente non verrà usato dalle applicazioni. Un PIN non restituisce necessariamente i tipi di supporto preferiti. Inoltre, i tipi di supporto restituiti potrebbero dipendere dallo stato di connessione del filtro. Ad esempio, un pin di output di un filtro potrebbe restituire un set di tipi di supporti diverso a seconda del tipo di supporto impostato per il pin di input del filtro.

Nell'esempio seguente viene trovato un tipo di supporto preferito che corrisponde a un tipo principale, un sottotipo o un tipo di formato specificati.


```C++
// Given a pin, find a preferred media type 
//
// pPin         Pointer to the pin.
// majorType    Preferred major type (GUID_NULL = don't care).
// subType      Preferred subtype (GUID_NULL = don't care).
// formatType   Preferred format type (GUID_NULL = don't care).
// ppmt         Receives a pointer to the media type. Can be NULL.
//
// Note: If you want to check whether a pin supports a desired media type,
//       but do not need the format details, set ppmt to NULL.
//
//       If ppmt is not NULL and the method succeeds, the caller must
//       delete the media type, including the format block. 

HRESULT GetPinMediaType(
    IPin *pPin,             // pointer to the pin
    REFGUID majorType,      // desired major type, or GUID_NULL = don't care
    REFGUID subType,        // desired subtype, or GUID_NULL = don't care
    REFGUID formatType,     // desired format type, of GUID_NULL = don't care
    AM_MEDIA_TYPE **ppmt    // Receives a pointer to the media type. (Can be NULL)
    )
{
    *ppmt = NULL;

    IEnumMediaTypes *pEnum = NULL;
    AM_MEDIA_TYPE *pmt = NULL;
    BOOL bFound = FALSE;
    
    HRESULT hr = pPin->EnumMediaTypes(&pEnum);
    if (FAILED(hr))
    {
        return hr;
    }

    while (hr = pEnum->Next(1, &pmt, NULL), hr == S_OK)
    {
        if ((majorType == GUID_NULL) || (majorType == pmt->majortype))
        {
            if ((subType == GUID_NULL) || (subType == pmt->subtype))
            {
                if ((formatType == GUID_NULL) || 
                    (formatType == pmt->formattype))
                {
                    // Found a match. 
                    if (ppmt)
                    {
                        *ppmt = pmt;  // Return it to the caller
                    }
                    else
                    {
                        _DeleteMediaType(pmt);
                    }
                    bFound = TRUE;
                    break;
                }
            }
        }
        _DeleteMediaType(pmt);
    }

    SafeRelease(&pEnum);
    if (SUCCEEDED(hr))
    {
        if (!bFound)
        {
            hr = VFW_E_NOT_FOUND;
        }
    }
    return hr;
}
```



> [!Note]  
> Questo esempio usa la funzione [SafeRelease](/windows/desktop/medfound/saferelease) per rilasciare i puntatori a interfaccia.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Enumerazione di oggetti in un grafico di filtro](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)
</dt> </dl>

 

 
