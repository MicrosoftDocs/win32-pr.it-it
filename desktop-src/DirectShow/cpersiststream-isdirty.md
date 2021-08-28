---
description: Indica se l'oggetto è stato modificato dopo l'ultimo salvataggio nel flusso corrente.
ms.assetid: 69840be6-062e-4505-8381-ea04e822c660
title: Metodo CPersistStream.IsDirty (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.IsDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e28285bd5660d6ba81fe77718cd9d38f325c51184a7bbd035cf3d7cb2ce6aa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108441"
---
# <a name="cpersiststreamisdirty-method"></a>Metodo CPersistStream.IsDirty

Indica se l'oggetto è stato modificato dopo l'ultimo salvataggio nel flusso corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsDirty();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK se il filtro richiede il salvataggio e S FALSE se non è necessario \_ salvare.

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il **metodo IPersistStream::IsDirty.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pstream.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




