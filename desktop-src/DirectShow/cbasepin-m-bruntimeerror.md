---
description: Flag che indica se si è verificato un errore di run-time.
ms.assetid: 917bcb21-a11e-4ac5-af96-565f61c155cd
title: Membro CBasePin::m_bRunTimeError (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bRunTimeError
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ffc07a15f7c34744be52c5e2c7b5233e1885b58c5b9b7d078871277f8fc0efd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823333"
---
# <a name="cbasepinm_bruntimeerror-member"></a>Membro CBasePin::m \_ bRunTimeError

Flag che indica se si è verificato un errore di run-time.

## <a name="syntax"></a>Sintassi


```C++
bool m_bRunTimeError;
```



## <a name="remarks"></a>Osservazioni

Il valore predefinito di questo flag è **FALSE.** Impostare il flag su **TRUE se** si verifica un errore di run-time durante lo streaming. Il [**metodo CBasePin::Inactive**](cbasepin-inactive.md) reimposta il flag su **FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




