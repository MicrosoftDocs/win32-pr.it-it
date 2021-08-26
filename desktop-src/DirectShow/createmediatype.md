---
description: La funzione CreateMediaType alloca una nuova struttura AM \_ MEDIA \_ TYPE, incluso il blocco di formato.
ms.assetid: 841a8c51-6027-49d6-b3d8-b5e21e3d5f13
title: Funzione CreateMediaType (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0384b0a72e10b84cd94581816c0441de6a19fa5148a97fa9e55d72bdd63d678
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871411"
---
# <a name="createmediatype-function"></a>Funzione CreateMediaType

La **funzione CreateMediaType** alloca una nuova [**struttura AM MEDIA \_ \_ TYPE,**](/windows/win32/api/strmif/ns-strmif-am_media_type) incluso il blocco di formato.

## <a name="syntax"></a>Sintassi


```C++
AM_MEDIA_TYPE* WINAPI CreateMediaType(
   AM_MEDIA_TYPE const *pSrc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSrc* 
</dt> <dd>

Puntatore a una [**struttura \_ AM MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) Il metodo copia questa struttura nella nuova struttura .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce una nuova [**struttura AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) o **NULL** se si verifica un errore.

## <a name="remarks"></a>Commenti

Per liberare la memoria allocata da questa funzione, [**chiamare DeleteMediaType**](deletemediatype.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype.h (includere Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni per i tipi di supporti**](media-type-functions.md)
</dt> </dl>

 

 




