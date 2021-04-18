---
description: Il metodo attivo notifica al pin che il filtro è ora attivo.
ms.assetid: 35df4305-0e2c-4ee1-bc63-db5aec864c46
title: Metodo CBaseOutputPin. Active (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 249cddac4027fa434996b1118cc692937b686a83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329558"
---
# <a name="cbaseoutputpinactive-method"></a>Metodo CBaseOutputPin. Active

Il `Active` metodo notifica al pin che il filtro è ora attivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                          | Descrizione                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                 | Esito positivo.<br/>                   |
| <dl> <dt>**\_ \_ \_ allocatore E nessun allocatore**</dt> </dl> | Nessun allocatore disponibile.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CBasePin:: Active**](cbasepin-active.md) . Chiama il metodo [**IMemAllocator:: commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) sull'allocatore per allocare memoria per i buffer.

Se si esegue l'override di questo metodo, chiamare il metodo della classe base dal metodo che esegue l'override.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




