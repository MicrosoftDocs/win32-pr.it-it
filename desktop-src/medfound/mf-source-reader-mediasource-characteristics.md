---
description: Ottiene le caratteristiche dell'origine multimediale dal lettore di origine.
ms.assetid: 4cd48b69-6f7b-4b13-86f3-b38969025f70
title: Attributo MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de4d1ed026f7b74f290446af74a6cf9947612617
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351711"
---
# <a name="mf_source_reader_mediasource_characteristics-attribute"></a>\_ \_ \_ Attributo caratteristiche di lettura origine (MF) \_

Ottiene le caratteristiche dell'origine multimediale dal lettore di [origine](source-reader.md).

## <a name="data-type"></a>Tipo di dati

**UINT32**

Il valore è **un operatore OR** bit per bit di flag dell'enumerazione delle [**\_ caratteristiche MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .

## <a name="remarks"></a>Commenti

Per ottenere questo attributo, chiamare il metodo [**IMFSourceReader:: GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) nel lettore di origine. Impostare il parametro *dwStreamIndex* su **MF \_ source \_ Reader \_ MEDIASOURCE** e il parametro *guidAttribute* per MF \_ source \_ Reader \_ MediaSource \_ caratteristiche.

Il tipo **PROPVARIANT** per questo attributo è **VT \_ UI4**.

## <a name="examples"></a>Esempio


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | App desktop di Windows Server 2008 R2 \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lettore di origine](source-reader.md)
</dt> </dl>

 

 




