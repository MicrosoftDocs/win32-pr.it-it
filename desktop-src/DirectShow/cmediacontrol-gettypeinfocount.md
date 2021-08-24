---
description: 'Metodo CMediaControl.GetTypeInfoCount: recupera il numero di interfacce di informazioni sul tipo fornite da un oggetto.'
ms.assetid: 29575325-8f97-4f39-8272-86a917d9144f
title: Metodo CMediaControl.GetTypeInfoCount (Ctlutil.h)
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
ms.openlocfilehash: a751c7ed9d10547d34ec491f2e90e5ca6f1ab1f19bc1221c04b15da427da4570
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832521"
---
# <a name="cmediacontrolgettypeinfocount-method"></a>Metodo CMediaControl.GetTypeInfoCount

Recupera il numero di interfacce di informazioni sul tipo fornite da un oggetto .

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

Puntatore al numero di interfacce di informazioni sul tipo fornite dall'oggetto . Se l'oggetto fornisce informazioni sul tipo, questo numero è 1; in caso contrario, il numero è 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E \_ POINTER se *pctinfo non* è valido. In caso contrario, restituisce S \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaControl**](cmediacontrol.md)
</dt> </dl>

 

 




