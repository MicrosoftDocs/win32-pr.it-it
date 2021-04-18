---
description: Questo operatore verifica l'uguaglianza tra gli oggetti CMediaType.
ms.assetid: d50f3a72-c5e8-44a5-aa0e-b1c40a19fee3
title: 'Metodo CMediaType. CMediaType:: operator = = (mtype. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator==
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79631415ce562f1cf3d7251e1f325960f5baa28b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330670"
---
# <a name="cmediatypecmediatypeoperator-method"></a>Metodo CMediaType. CMediaType:: operator = =

Questo operatore verifica l'uguaglianza tra gli oggetti [**CMediaType**](cmediatype.md) .

## <a name="syntax"></a>Sintassi


```C++
BOOL CMediaType::operator==(
  [ref] const CMediaType &rt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RT* \[ Ref\]
</dt> <dd>

Riferimento all'oggetto **CMediaType** da confrontare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se *RT* è uguale a questo oggetto. In caso contrario, restituisce **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




