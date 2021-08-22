---
description: Il metodo put \_ Rate imposta la velocità di riproduzione. Questo metodo implementa il metodo IMediaPosition::p ut \_ Rate.
ms.assetid: c077f344-de34-4f8a-8e08-6d7086a5a4f1
title: CPosPassThru.put_Rate metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 90c89c9730ee057bea3bc776f551061c0e828385fe3c6ae054f4161bdb705ab1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565502"
---
# <a name="cpospassthruput_rate-method"></a>Metodo CPosPassThru.put \_ Rate

Il `put_Rate` metodo imposta la velocità di riproduzione. Questo metodo implementa il [**metodo IMediaPosition::p ut \_ Rate.**](/windows/desktop/api/Control/nf-control-imediaposition-put_rate)

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Rate(
   double dRate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dRate* 
</dt> <dd>

Velocità di riproduzione. Non deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E \_ INVALIDARG se *dRate* è zero. In caso contrario, restituisce il **valore HRESULT** dal pin connesso.

## <a name="remarks"></a>Commenti

I tassi negativi indicano il gioco inverso. Non tutti i supporti supporteranno la riproduzione inversa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




