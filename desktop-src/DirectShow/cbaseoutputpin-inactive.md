---
description: 'Metodo CBaseOutputPin.Inactive: il metodo Inactive notifica al pin che il filtro non è più attivo.'
ms.assetid: 14a020de-2102-4d49-8a34-d59abe6698d1
title: Metodo CBaseOutputPin.Inactive (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0600402301bf416dc0863c4ccff05cac698ec53871b03fd8a84f3873fd43163a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983421"
---
# <a name="cbaseoutputpininactive-method"></a>Metodo CBaseOutputPin.Inactive

Il `Inactive` metodo notifica al segnaposto che il filtro non è più attivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                          | Descrizione                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                 | Operazione completata.<br/>                          |
| <dl> <dt>**VFW \_ E \_ NO \_ ALLOCATOR**</dt> </dl> | Nessun allocatore di memoria disponibile.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CBasePin::Inactive.**](cbasepin-inactive.md) Chiama il metodo [**IMemAllocator::D ecommit per decommettere**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) l'allocatore di memoria.

Se si esegue l'override di questo metodo, chiamare il metodo della classe base dal metodo di override.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




