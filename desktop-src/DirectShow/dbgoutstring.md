---
description: La funzione DbgOutString invia una stringa al percorso di output di debug. Ignorato nelle compilazioni al dettaglio.
ms.assetid: 644bf4f7-ec2d-466e-85c6-690dd44da702
title: Funzione DbgOutString (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgOutString
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bdc12d4b73080f00a3d32c80074a801146ea4a74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327522"
---
# <a name="dbgoutstring-function"></a>DbgOutString (funzione)

La funzione **DbgOutString** invia una stringa al percorso di output di debug. Ignorato nelle compilazioni al dettaglio.

## <a name="syntax"></a>Sintassi


```C++
void DbgOutString(
   LPCTSTR psz
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PSZ* 
</dt> <dd>

Stringa da restituire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Nelle build di debug questa funzione restituisce sempre la stringa, indipendentemente dai livelli di output di debug correnti. Per un controllo più preciso sull'output, usare la macro [**DbgLog**](dbglog.md) .

## <a name="examples"></a>Esempio


```C++
DbgOutString("Creating the filter graph...\n"); 
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxdebug. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di output di debug](debug-output-functions.md)
</dt> </dl>

 

 




