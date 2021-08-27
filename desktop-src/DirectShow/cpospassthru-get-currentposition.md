---
description: Il metodo get \_ CurrentPosition recupera la posizione corrente, relativa alla durata totale del flusso. Questo metodo implementa il metodo IMediaPosition::get \_ CurrentPosition.
ms.assetid: 6e68af98-440d-4ecc-b1aa-d5e241de4999
title: CPosPassThru.get_CurrentPosition metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: db49717284f597249603b3c18340855793ebd342632aeb2091861f9742963a02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084241"
---
# <a name="cpospassthruget_currentposition-method"></a>Metodo CPosPassThru.get \_ CurrentPosition

Il `get_CurrentPosition` metodo recupera la posizione corrente, rispetto alla durata totale del flusso. Questo metodo implementa il [**metodo IMediaPosition::get \_ CurrentPosition.**](/windows/desktop/api/Control/nf-control-imediaposition-get_currentposition)

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_CurrentPosition(
   REFTIME *pllTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pllTime* 
</dt> <dd>

Puntatore a una variabile che riceve la posizione corrente, in secondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il **valore HRESULT** dal pin connesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




