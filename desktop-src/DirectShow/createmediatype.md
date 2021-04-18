---
description: La funzione CreateMediaType alloca una nuova \_ \_ struttura del tipo di supporto AM, incluso il blocco di formato.
ms.assetid: 841a8c51-6027-49d6-b3d8-b5e21e3d5f13
title: Funzione CreateMediaType (mtype. h)
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
ms.openlocfilehash: 03ea3eaee03ebf98ac22d702bde9a165fda21e51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331316"
---
# <a name="createmediatype-function"></a>CreateMediaType (funzione)

La funzione **CreateMediaType** alloca una nuova struttura [**del \_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , incluso il blocco di formato.

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

Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Il metodo copia questa struttura nella nuova struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce una nuova struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) oppure **null** se si verifica un errore.

## <a name="remarks"></a>Commenti

Per liberare la memoria allocata da questa funzione, chiamare [**DeleteMediaType**](deletemediatype.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni di tipo multimediale**](media-type-functions.md)
</dt> </dl>

 

 




