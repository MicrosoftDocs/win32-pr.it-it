---
description: Indica se l'oggetto è stato modificato dopo l'ultimo salvataggio nel flusso corrente.
ms.assetid: 69840be6-062e-4505-8381-ea04e822c660
title: Metodo CPersistStream. IsDirty (pStream. h)
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
ms.openlocfilehash: 4f3bc57998b63ece5ca32543fc00d1d3b5b4389b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328928"
---
# <a name="cpersiststreamisdirty-method"></a>Metodo CPersistStream. IsDirty

Indica se l'oggetto è stato modificato dopo l'ultimo salvataggio nel flusso corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsDirty();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se il filtro deve essere salvato e \_ false se non è necessario salvarlo.

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il metodo **IPersistStream:: IsDirty** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PStream. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




