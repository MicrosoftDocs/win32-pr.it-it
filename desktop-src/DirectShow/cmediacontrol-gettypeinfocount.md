---
description: Recupera il numero di interfacce di informazioni sul tipo fornite da un oggetto.
ms.assetid: 29575325-8f97-4f39-8272-86a917d9144f
title: Metodo CMediaControl. GetTypeInfoCount (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2454e503a045a02db20c0dc457b6367f6d3b427
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332211"
---
# <a name="cmediacontrolgettypeinfocount-method"></a>CMediaControl. GetTypeInfoCount, metodo

Recupera il numero di interfacce di informazioni sul tipo fornite da un oggetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pctinfo* 
</dt> <dd>

Puntatore al numero di interfacce di informazioni sul tipo fornite dall'oggetto. Se l'oggetto fornisce informazioni sul tipo, questo numero è 1; in caso contrario, il numero è 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un \_ puntatore E se *pcTInfo* non è valido; in caso contrario, restituisce S \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaControl**](cmediacontrol.md)
</dt> </dl>

 

 




