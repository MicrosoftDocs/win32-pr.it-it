---
description: 'Metodo CBaseInputPin.Inactive: il metodo Inactive notifica al pin che il filtro non è più attivo.'
ms.assetid: e00e1562-54bb-4968-8a86-b29e1077d7a5
title: Metodo CBaseInputPin.Inactive (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dec73f0c691c7c644ead6456cc76fb1758202497ffcd968893780b2f0f61f93b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403460"
---
# <a name="cbaseinputpininactive-method"></a>Metodo CBaseInputPin.Inactive

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

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




