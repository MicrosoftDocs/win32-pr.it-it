---
description: Consente l'uso di una trasformazione di Media Foundation asincrona (MFT).
ms.assetid: e12ab57e-ebc2-46af-afdf-d78d4db16fcf
title: Attributo MF_TRANSFORM_ASYNC_UNLOCK (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e7876b3f1fca80e881414399d40e69112a64d8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527402"
---
# <a name="mf_transform_async_unlock-attribute"></a>Attributo di sblocco di MF \_ Transform \_ Async \_

Consente l'uso di una trasformazione di Media Foundation asincrona (MFT).

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

MFTs asincroni non sono compatibili con le versioni precedenti di Microsoft Media Foundation. Per evitare che le applicazioni esistenti utilizzino accidentalmente un MFT asincrono, questo attributo deve essere impostato su un valore diverso da zero prima di poter utilizzare un MFT asincrono. La pipeline Media Foundation imposta automaticamente l'attributo, in modo che la maggior parte delle applicazioni non debba utilizzare questo attributo. Tuttavia, se un'applicazione usa una MFT asincrona al di fuori della pipeline di Media Foundation, l'applicazione deve impostare questo attributo.

MFTs sincroni non richiedono questo attributo.

Per verificare se un MFT è asincrono, ottenere il valore dell'attributo [MF \_ Transform \_ Async](mf-transform-async.md) in MFT.

## <a name="examples"></a>Esempio

Il codice seguente sblocca un MFT asincrono.


```C++
HRESULT UnlockAsyncMFT(IMFTransform *pMFT)
{
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = hr = pMFT->GetAttributes(&pAttributes);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_TRANSFORM_ASYNC_UNLOCK, TRUE);
        pAttributes->Release();
    }
    
    return hr;
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
</dt> </dl>

 

 




