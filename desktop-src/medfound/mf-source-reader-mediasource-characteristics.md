---
description: Ottiene le caratteristiche dell'origine multimediale dal lettore di origine.
ms.assetid: 4cd48b69-6f7b-4b13-86f3-b38969025f70
title: MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS attributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5ec5461bc289517490ae11bdd507895cd1ad434c53b1665ac5c6394907f15a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739968"
---
# <a name="mf_source_reader_mediasource_characteristics-attribute"></a>Attributo MF \_ SOURCE \_ READER \_ MEDIASOURCE \_ CHARACTERISTICS

Ottiene le caratteristiche dell'origine multimediale dal [lettore di origine.](source-reader.md)

## <a name="data-type"></a>Tipo di dati

**UINT32**

Il valore è un **OR** bit per bit di flag dell'enumerazione [**CHARACTERISTICS di MFMEDIASOURCE. \_**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics)

## <a name="remarks"></a>Commenti

Per ottenere questo attributo, chiamare il [**metodo IMFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) nel lettore di origine. Impostare il *parametro dwStreamIndex* su **MF \_ SOURCE READER \_ \_ MEDIASOURCE** e il parametro *guidAttribute* su MF \_ SOURCE READER \_ \_ \_ MEDIASOURCE CHARACTERISTICS.

Il **tipo PROPVARIANT** per questo attributo è **VT \_ UI4.**

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
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 R2 \[ \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi Media Foundation alfabetici](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lettore di origine](source-reader.md)
</dt> </dl>

 

 




