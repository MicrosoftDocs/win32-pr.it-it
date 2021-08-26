---
description: Il metodo ConnectedTo recupera un puntatore al pin connesso, se presente. Questo metodo implementa il metodo IPin::ConnectedTo.
ms.assetid: d8978c9a-e498-4411-a052-f3c2fca570ef
title: Metodo CBasePin.ConnectedTo (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectedTo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a37eafe9abf226be20cf5d573abc91bc52ee070e7667dbab3a8799f74022c92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916761"
---
# <a name="cbasepinconnectedto-method"></a>Metodo CBasePin.ConnectedTo

Il `ConnectedTo` metodo recupera un puntatore al pin connesso, se presente. Questo metodo implementa il [**metodo IPin::ConnectedTo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto)

## <a name="syntax"></a>Sintassi


```C++
HRESULT ConnectedTo(
   IPin **ppPin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppPin* 
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore [**all'interfaccia IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) dell'altro pin.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili sono quelli riportati nella tabella seguente.



| Codice restituito                                                                                           | Descrizione                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operazione completata.<br/>                   |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>             | Argomento del puntatore **NULL.**<br/> |
| <dl> <dt>**VFW \_ E \_ NON \_ CONNESSO**</dt> </dl> | Il pin non è connesso.<br/>      |



 

## <a name="remarks"></a>Commenti

Se il metodo ha esito positivo, **l'interfaccia IPin** restituita ha un conteggio dei riferimenti in sospeso. Al termine, assicurarsi di rilasciarlo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




