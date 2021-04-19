---
description: La funzione CopyMediaType copia una \_ struttura del tipo di supporto am \_ in un'altra struttura, incluso il blocco di formato
ms.assetid: 5b47e197-abb5-4b2c-ad65-a506c5e239be
title: Funzione CopyMediaType (mtype. h)
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
ms.openlocfilehash: 2e37f277244ae9b82c395d7901917e1fc1e78b35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330219"
---
# <a name="copymediatype-function"></a>CopyMediaType (funzione)

La funzione **CopyMediaType** copia una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) in un'altra struttura, incluso il blocco di formato

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

Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Il metodo copia il tipo di supporto in questa struttura.

</dd> <dt>

*pmtSource* 
</dt> <dd>

Puntatore a una struttura [**di \_ \_ tipo multimediale**](/windows/win32/api/strmif/ns-strmif-am_media_type) di origine per la copia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o e \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Questa funzione alloca la memoria per il blocco di formato. Se il parametro *pmtTarget* contiene già un blocco di formato allocato, si verificherà una perdita di memoria. Per evitare una perdita di memoria, chiamare [**FreeMediaType**](freemediatype.md) prima di chiamare questa funzione.

Dopo la restituzione del metodo, chiamare [**FreeMediaType**](freemediatype.md) su *pmtTarget* per liberare il blocco di formato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni di tipo multimediale**](media-type-functions.md)
</dt> </dl>

 

 




