---
description: Il metodo IsValid determina se a questo oggetto è stato assegnato un tipo principale.
ms.assetid: 22d28019-f360-4b93-972c-d1dfe83938f0
title: Metodo CMediaType.IsValid (Mtype.h)
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
ms.openlocfilehash: 3611d36cfe19623840f102b820b2b312138b1e116d32fc399927da57e7f47300
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016265"
---
# <a name="cmediatypeisvalid-method"></a>Metodo CMediaType.IsValid

Il `IsValid` metodo determina se a questo oggetto è stato assegnato un tipo principale.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsValid() const;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se a questo oggetto è stato assegnato un tipo principale. In caso contrario, **restituisce FALSE.**

## <a name="remarks"></a>Commenti

Per impostazione predefinita, [**gli oggetti CMediaType**](cmediatype.md) vengono inizializzati con un tipo principale di GUID \_ NULL. Chiamare questo metodo per determinare se l'oggetto è stato inizializzato correttamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype.h (includere Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




