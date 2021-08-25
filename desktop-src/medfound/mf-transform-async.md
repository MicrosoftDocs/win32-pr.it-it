---
description: Specifica se una trasformazione Media Foundation (MFT) esegue l'elaborazione asincrona.
ms.assetid: fcc70282-cfac-487c-b9ff-39e62c836f8b
title: MF_TRANSFORM_ASYNC attributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92a647ca122c138f2ef7e90670798200fc3fa629be48d6242b4e71dbc93151e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714350"
---
# <a name="mf_transform_async-attribute"></a>Attributo \_ ASYNC MF TRANSFORM \_

Specifica se una trasformazione Media Foundation (MFT) esegue l'elaborazione asincrona.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Commenti

L'attributo è un valore booleano:

-   Se l'attributo è diverso da zero, MFT esegue l'elaborazione asincrona.
-   Se l'attributo è 0 o non è impostato, MFT è sincrono.

Per ottenere questo attributo, chiamare prima [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) per ottenere l'archivio attributi di MFT. Se il metodo ha esito positivo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) per ottenere il valore dell'attributo. Se uno dei due metodi ha esito negativo, MFT è sincrono.

Per i MFT asincroni, questo attributo deve essere impostato su un valore diverso da zero. Per i MFT sincroni, questo attributo è facoltativo, ma deve essere impostato su 0, se presente.

Le MFT asincrone non sono compatibili con le versioni precedenti di Media Foundation. Per usare un MFT asincrono, il client deve impostare l'attributo [**\_ MF TRANSFORM \_ ASYNC \_ UNLOCK**](mf-transform-async-unlock.md) in MFT. La pipeline Microsoft Media Foundation esegue automaticamente questo passaggio.

## <a name="examples"></a>Esempio

Il codice seguente verifica se un MFT esegue l'elaborazione asincrona.


```C++
BOOL IsTransformAsync(IMFTransform *pMFT)
{
    BOOL bAsync = FALSE;
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bAsync = MFGetAttributeUINT32(pAttributes, MF_TRANSFORM_ASYNC, FALSE);
        pAttributes->Release();
    }

    return (bAsync != FALSE);
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop \| app UWP\]<br/>                                        |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 R2 \[ \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFT asincroni](asynchronous-mfts.md)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> <dt>

[**SBLOCCO \_ ASINCRONO MF \_ \_ TRANSFORM**](mf-transform-async-unlock.md)
</dt> </dl>

 

 




