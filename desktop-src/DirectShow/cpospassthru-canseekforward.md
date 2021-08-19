---
description: Il metodo CanSeekForward determina se il flusso può essere cercato in avanti. Questo metodo implementa il metodo IMediaPosition::CanSeekForward.
ms.assetid: ccb2db8d-b52e-4e3d-b49b-9689197a974a
title: Metodo CPosPassThru.CanSeekForward (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekForward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f07491a94522280357c85d773d28ea4732f2f85879b55cf5d1b5a99ec72d23f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073565"
---
# <a name="cpospassthrucanseekforward-method"></a>Metodo CPosPassThru.CanSeekForward

Il `CanSeekForward` metodo determina se il flusso può essere cercato in avanti. Questo metodo implementa il [**metodo IMediaPosition::CanSeekForward.**](/windows/desktop/api/Control/nf-control-imediaposition-canseekforward)

## <a name="syntax"></a>Sintassi


```C++
HRESULT CanSeekForward(
   LONG *pCanSeekForward
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCanSeekForward* 
</dt> <dd>

Puntatore a una variabile che riceve il valore OATRUE se il filtro può eseguire la ricerca in avanti oppure OAFALSE in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il **valore HRESULT** dal pin connesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




