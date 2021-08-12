---
description: Abilita l'uso di una trasformazione Media Foundation asincrona (MFT).
ms.assetid: e12ab57e-ebc2-46af-afdf-d78d4db16fcf
title: MF_TRANSFORM_ASYNC_UNLOCK attributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82a0a8f328095c3a5c567171fa6a625a77e5623d126dfb2be9f34fef556984be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244177"
---
# <a name="mf_transform_async_unlock-attribute"></a>Attributo \_ MF TRANSFORM \_ ASYNC \_ UNLOCK

Abilita l'uso di una trasformazione Media Foundation asincrona (MFT).

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Commenti

Le MFT asincrone non sono compatibili con le versioni precedenti di Microsoft Media Foundation. Per impedire alle applicazioni esistenti di usare accidentalmente un MFT asincrono, questo attributo deve essere impostato su un valore diverso da zero prima di poter usare un MFT asincrono. La Media Foundation pipeline imposta automaticamente l'attributo, in modo che la maggior parte delle applicazioni non deve usare questo attributo. Tuttavia, se un'applicazione usa un MFT asincrono all'esterno della pipeline Media Foundation, l'applicazione deve impostare questo attributo.

I MFT sincroni non richiedono questo attributo.

Per verificare se un MFT è asincrono, ottenere il valore dell'attributo [ \_ \_ ASYNC MF TRANSFORM](mf-transform-async.md) in MFT.

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
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 R2 \[ \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFT asincroni](asynchronous-mfts.md)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 




