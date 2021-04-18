---
description: Il metodo IsValid determina se un tipo principale è stato assegnato a questo oggetto.
ms.assetid: 22d28019-f360-4b93-972c-d1dfe83938f0
title: Metodo CMediaType. IsValid (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsValid
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d8e1731060021b61eb5037e1baeeda95021e8f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330675"
---
# <a name="cmediatypeisvalid-method"></a>Metodo CMediaType. IsValid

Il `IsValid` metodo determina se un tipo principale è stato assegnato a questo oggetto.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsValid() const;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **true** se è stato assegnato un tipo principale a questo oggetto. In caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, gli oggetti [**CMediaType**](cmediatype.md) vengono inizializzati con un tipo principale di GUID \_ null. Chiamare questo metodo per determinare se l'oggetto è stato inizializzato correttamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




