---
description: Il metodo QueryPinInfo recupera informazioni sul pin. Questo metodo implementa il metodo IPin::QueryPinInfo.
ms.assetid: 9de41f61-9f03-4594-a320-2f7f0ed734fd
title: Metodo CBasePin.QueryPinInfo (Amfilter.h)
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
ms.openlocfilehash: 544039b1076848cb796f290ea98aa8aac359b26ebfb64f90a27d316a9d0cc34f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823235"
---
# <a name="cbasepinquerypininfo-method"></a>Metodo CBasePin.QueryPinInfo

Il `QueryPinInfo` metodo recupera informazioni sul pin. Questo metodo implementa il [**metodo IPin::QueryPinInfo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo)

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

Puntatore a una [**struttura \_ PIN INFO**](/windows/win32/api/strmif/ns-strmif-pin_info) che riceve le informazioni sul pin.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o E \_ POINTER.

## <a name="remarks"></a>Commenti

Questo metodo usa la [**variabile membro CBasePin::m \_ pName**](cbasepin-m-pname.md) per il **membro achName** della struttura PIN \_ INFO.

Quando il metodo termina, se il **membro pFilter** della struttura PIN INFO è diverso da \_ **NULL,** ha un conteggio dei riferimenti in sospeso. Assicurarsi di rilasciare l'interfaccia al termine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




