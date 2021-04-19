---
description: La funzione IsEqualObject controlla se due interfacce si trovano nello stesso oggetto.
ms.assetid: 51325e05-5a7f-4a80-a12e-2e7dedc028e2
title: Funzione IsEqualObject (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsEqualObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e959d687d7d6b11dc6055daeda789e728d875d70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326270"
---
# <a name="isequalobject-function"></a>IsEqualObject (funzione)

La `IsEqualObject` funzione controlla se due interfacce si trovano nello stesso oggetto.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI IsEqualObject(
   IUnknown *pFirst,
   IUnknown *pSecond
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFirst* 
</dt> <dd>

Puntatore a un'interfaccia.

</dd> <dt>

*pSecond* 
</dt> <dd>

Puntatore all'altra interfaccia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se le interfacce si trovano entrambi nello stesso oggetto. in caso contrario, **false** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni helper varie](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




