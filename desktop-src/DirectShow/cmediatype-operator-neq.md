---
description: Questo operatore verifica la disuguaglianza tra gli oggetti CMediaType.
ms.assetid: 9caf4cb9-f049-42e7-abe4-79f8bf0ea542
title: Metodo CMediaType.CMediaType::operator!= (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator!=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c17db60821be2f5243afab83ed62ec9b5b5b50e5d7a3f500d159ec185260a402
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156239"
---
# <a name="cmediatypecmediatypeoperator-method"></a>Metodo CMediaType.CMediaType::operator!=

Questo operatore verifica la disuguaglianza tra [**gli oggetti CMediaType.**](cmediatype.md)

## <a name="syntax"></a>Sintassi


```C++
BOOL CMediaType::operator!=(
  [ref] const CMediaType &rt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rt* \[ Ref\]
</dt> <dd>

Riferimento **all'oggetto CMediaType** da confrontare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se *rt* non è uguale a questo oggetto. In caso contrario, **restituisce FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype.h (includere Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




