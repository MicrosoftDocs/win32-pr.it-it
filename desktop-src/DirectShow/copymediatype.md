---
description: La funzione CopyMediaType copia una struttura AM \_ MEDIA \_ TYPE in un'altra struttura, incluso il blocco di formato
ms.assetid: 5b47e197-abb5-4b2c-ad65-a506c5e239be
title: Funzione CopyMediaType (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CopyMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b193f64edb55a342546f26db1975080490f0e69b2caa91695b3bc63240750983
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634375"
---
# <a name="copymediatype-function"></a>Funzione CopyMediaType

La **funzione CopyMediaType** copia una struttura [**AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) in un'altra struttura, incluso il blocco di formato

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI CopyMediaType(
         AM_MEDIA_TYPE *pmtTarget,
   const AM_MEDIA_TYPE *pmtSource
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pmtTarget* 
</dt> <dd>

Puntatore a una [**struttura AM \_ MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) Il metodo copia il tipo di supporto in questa struttura .

</dd> <dt>

*pmtSource* 
</dt> <dd>

Puntatore a una struttura [**AM \_ MEDIA TYPE \_ di**](/windows/win32/api/strmif/ns-strmif-am_media_type) origine da copiare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Questa funzione alloca la memoria per il blocco di formato. Se il *parametro pmtTarget* contiene già un blocco di formato allocato, si verificherà una perdita di memoria. Per evitare una perdita di memoria, chiamare [**FreeMediaType**](freemediatype.md) prima di chiamare questa funzione.

Al termine del metodo, chiamare [**FreeMediaType**](freemediatype.md) su *pmtTarget* per liberare il blocco di formato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype.h (includere Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni del tipo di supporto**](media-type-functions.md)
</dt> </dl>

 

 




