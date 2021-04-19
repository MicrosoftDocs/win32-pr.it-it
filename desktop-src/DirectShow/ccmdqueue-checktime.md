---
description: Il metodo CheckTime determina se è previsto un periodo di tempo specificato.
ms.assetid: 522bc7ae-f998-4a7d-8bc3-caf09b4108a6
title: Metodo CCmdQueue. CheckTime (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.CheckTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17fd67973e122830e53d93d1d8db17046f716507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333484"
---
# <a name="ccmdqueuechecktime-method"></a>CCmdQueue. CheckTime, metodo

Il `CheckTime` metodo determina se è previsto un periodo di tempo specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL CheckTime(
   CRefTime time,
   BOOL     bStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*time* 
</dt> <dd>

Tempo da verificare.

</dd> <dt>

*bStream* 
</dt> <dd>

**True** se il parametro *Time* è un valore del flusso di tempo; **False** se *Time* è un valore in fase di presentazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'ora specificata non è stata ancora superata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




