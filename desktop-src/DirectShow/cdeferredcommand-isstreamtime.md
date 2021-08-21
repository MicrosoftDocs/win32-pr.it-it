---
description: Il metodo IsStreamTime specifica se il comando deve essere eseguito in fase di flusso o di presentazione.
ms.assetid: 4fb315a4-1bc6-49c8-a47f-0a8a46f3f790
title: Metodo CDeferredCommand.IsStreamTime (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.IsStreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 82c541220a2b89ecdd23e4676175f4c7b2aacd93aac008546349b38e7bc2455a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657204"
---
# <a name="cdeferredcommandisstreamtime-method"></a>Metodo CDeferredCommand.IsStreamTime

Il metodo specifica se il comando deve essere eseguito in fase di `IsStreamTime` flusso o di presentazione.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsStreamTime();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** impostato sul tempo di flusso. In caso contrario, restituisce **FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




