---
description: Il metodo seTYPE specifica il tipo principale.
ms.assetid: 3fd93d5e-73ea-453e-8f08-652d5a81239f
title: Metodo CMediaType. seTYPE (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfcf6ca634bce92701eb89f26dcfb6bdfb51f698
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332209"
---
# <a name="cmediatypesettype-method"></a>Metodo CMediaType. seTYPE

Il `SetType` metodo specifica il tipo principale.

## <a name="syntax"></a>Sintassi


```C++
void SetType(
   const GUID *ptype
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pType* 
</dt> <dd>

Puntatore a un **GUID** che specifica il tipo principale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




