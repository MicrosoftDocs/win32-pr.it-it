---
description: Flag che indica se il pin tenta i propri tipi di supporti preferiti prima di quelli del pin ricevente.
ms.assetid: 50462ee4-4a61-472f-9a7e-9cdb39be4dea
title: Membro CBasePin::m_bTryMyTypesFirst (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bTryMyTypesFirst
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df94a95783d15c09fd53bd8659db71f2ce0b1aefe5d855fef5f5a03e71445493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158372"
---
# <a name="cbasepinm_btrymytypesfirst-member"></a>Membro CBasePin::m \_ bTryMyTypesFirst

Flag che indica se il pin tenta i propri tipi di supporti preferiti prima di quelli del pin ricevente.

## <a name="syntax"></a>Sintassi


```C++
bool m_bTryMyTypesFirst;
```



## <a name="remarks"></a>Osservazioni

Il valore predefinito di questo flag **è FALSE.** Se il flag è **TRUE,** il [**metodo CBasePin::AgreeMediaType**](cbasepin-agreemediatype.md) inverte l'ordine in cui tenta i tipi di supporti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




