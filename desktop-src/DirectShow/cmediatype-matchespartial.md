---
description: Il metodo MatchesPartial determina se questo tipo di supporto corrisponde a un tipo di supporto parzialmente specificato.
ms.assetid: 62d531f3-5aa2-4af2-b951-584a49a849fc
title: Metodo CMediaType.MatchesPartial (Mtype.h)
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
ms.openlocfilehash: a6049ad4526d8776b25e81fe4d75b727196f8fa1251a1959662cca71b161fbc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073975"
---
# <a name="cmediatypematchespartial-method"></a>Metodo CMediaType.MatchesPartial

Il metodo determina se questo tipo di supporto corrisponde a un tipo di supporto `MatchesPartial` parzialmente specificato.

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

Puntatore al tipo di supporto di cui trovare la corrispondenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** i tipi di supporti corrispondono. In caso contrario, restituisce **FALSE.**

## <a name="remarks"></a>Commenti

Il tipo di supporto specificato *da ppartial* può avere un valore GUID NULL per il tipo principale, il \_ sottotipo o il tipo di formato. I membri con valori \_ NULL GUID non vengono testati. (In effetti, GUID \_ NULL funge da carattere jolly. I membri con valori diversi da GUID \_ NULL devono corrispondere perché il tipo di supporto corrisponda.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype.h (includere Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




