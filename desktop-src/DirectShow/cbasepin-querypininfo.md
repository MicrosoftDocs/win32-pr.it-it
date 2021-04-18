---
description: 'Il metodo QueryPinInfo recupera le informazioni sul pin. Questo metodo implementa il metodo IPin:: QueryPinInfo.'
ms.assetid: 9de41f61-9f03-4594-a320-2f7f0ed734fd
title: Metodo CBasePin. QueryPinInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f69977a15deb7d84b3370bb6e08c02a4e5129212
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328258"
---
# <a name="cbasepinquerypininfo-method"></a>CBasePin. QueryPinInfo, metodo

Il `QueryPinInfo` metodo recupera le informazioni sul pin. Questo metodo implementa il metodo [**Ipin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT QueryPinInfo(
   PIN_INFO *pInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInfo* 
</dt> <dd>

Puntatore a una struttura di [**\_ informazioni sul pin**](/windows/win32/api/strmif/ns-strmif-pin_info) che riceve le informazioni sul pin.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un \_ puntatore S OK o e \_ .

## <a name="remarks"></a>Commenti

Questo metodo usa la variabile membro [**CBasePin:: m \_ pname**](cbasepin-m-pname.md) per il membro **achName** della struttura di \_ informazioni del PIN.

Quando il metodo restituisce un risultato, se il membro **pFilter** della \_ struttura di informazioni del PIN è diverso da **null**, è presente un conteggio dei riferimenti in attesa. Al termine, assicurarsi di rilasciare l'interfaccia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




