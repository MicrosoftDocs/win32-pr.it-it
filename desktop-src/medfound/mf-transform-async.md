---
description: Specifica se una trasformazione Media Foundation (MFT) esegue l'elaborazione asincrona.
ms.assetid: fcc70282-cfac-487c-b9ff-39e62c836f8b
title: Attributo MF_TRANSFORM_ASYNC (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89622bd7bb7fa3e8306c94b02f90217b6367d21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753151"
---
# <a name="mf_transform_async-attribute"></a>MF \_ Transform ( \_ attributo asincrono)

Specifica se una trasformazione Media Foundation (MFT) esegue l'elaborazione asincrona.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

L'attributo è un valore booleano:

-   Se l'attributo è diverso da zero, il MFT esegue l'elaborazione asincrona.
-   Se l'attributo è 0 o non impostato, il MFT è sincrono.

Per ottenere questo attributo, chiamare prima [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) per ottenere l'archivio di attributi della MFT. Se il metodo ha esito positivo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) per ottenere il valore dell'attributo. Se uno dei due metodi ha esito negativo, il MFT è sincrono.

Per MFTs asincrono, questo attributo deve essere impostato su un valore diverso da zero. Per MFTs sincrono, questo attributo è facoltativo, ma deve essere impostato su 0 se presente.

MFTs asincroni non sono compatibili con le versioni precedenti di Media Foundation. Per usare un MFT asincrono, il client deve impostare l'attributo [**MF \_ Transform \_ Async \_ Unlock**](mf-transform-async-unlock.md) in MFT. La pipeline Microsoft Media Foundation esegue questo passaggio automaticamente.

## <a name="examples"></a>Esempio

Il codice seguente verifica se un'operazione MFT esegue l'elaborazione asincrona.


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
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | App desktop di Windows Server 2008 R2 \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs asincrono](asynchronous-mfts.md)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> <dt>

[**MF \_ trasforma \_ Async \_ sblocco**](mf-transform-async-unlock.md)
</dt> </dl>

 

 




