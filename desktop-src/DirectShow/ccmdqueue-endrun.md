---
description: Il metodo EndRun passa alla modalità arrestata o sospesa.
ms.assetid: 2c41262c-a809-4f3b-898c-02c0891dc6f8
title: Metodo CCmdQueue.EndRun (Winutil.h)
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
ms.openlocfilehash: 2c5a20917c82ba26c941b063941e8667a3a30adce15176aed52362140a15ce90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757361"
---
# <a name="ccmdqueueendrun-method"></a>Metodo CCmdQueue.EndRun

Il `EndRun` metodo passa alla modalità arrestata o sospesa.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT EndRun();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT** che dipende dall'implementazione.

## <a name="remarks"></a>Commenti

Il mapping dell'ora tra l'ora del flusso e l'ora di presentazione non è noto dopo la chiamata di questa funzione membro. Chiamare la [**funzione membro CCmdQueue::Run**](ccmdqueue-run.md) per eseguire questo mapping.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




