---
description: Il metodo MatchesPartial determina se il tipo di supporto corrisponde a un tipo di supporto parzialmente specificato.
ms.assetid: 62d531f3-5aa2-4af2-b951-584a49a849fc
title: Metodo CMediaType. MatchesPartial (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.MatchesPartial
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f4d2d4232b64857ca209e6b43cd7081a42495fee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330674"
---
# <a name="cmediatypematchespartial-method"></a>CMediaType. MatchesPartial, metodo

Il `MatchesPartial` metodo determina se il tipo di supporto corrisponde a un tipo di supporto parzialmente specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL MatchesPartial(
   const CMediaType *ppartial
) const;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppartial* 
</dt> <dd>

Puntatore al tipo di supporto da confrontare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se i tipi di supporto corrispondono. In caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

Il tipo di supporto specificato da *ppartial* può avere un valore GUID \_ null per il tipo principale, il sottotipo o il tipo di formato. I membri con \_ valori null GUID non vengono sottoposti a test. (In effetti, GUID \_ NULL funge da carattere jolly). I membri con valori diversi da GUID \_ null devono corrispondere per il tipo di supporto di cui trovare la corrispondenza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




