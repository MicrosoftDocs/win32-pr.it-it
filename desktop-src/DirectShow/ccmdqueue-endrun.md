---
description: Il metodo EndRun passa alla modalità arrestata o sospesa.
ms.assetid: 2c41262c-a809-4f3b-898c-02c0891dc6f8
title: Metodo CCmdQueue. EndRun (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.EndRun
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 367ef026402ff191ceb04657c21d6f3bd11ebe73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324485"
---
# <a name="ccmdqueueendrun-method"></a>CCmdQueue. EndRun, metodo

Il `EndRun` metodo passa alla modalità arrestata o sospesa.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT EndRun();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** che dipende dall'implementazione di.

## <a name="remarks"></a>Commenti

Il mapping dell'ora tra il tempo di flusso e l'ora di presentazione non è noto dopo la chiamata di questa funzione membro. Chiamare la funzione membro [**CCmdQueue:: Run**](ccmdqueue-run.md) per eseguire questo mapping.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




