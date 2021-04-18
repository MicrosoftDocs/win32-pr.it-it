---
description: 'Il metodo InitialThreadProc chiama il metodo COutputQueue:: ThreadProc quando viene creato il thread.'
ms.assetid: 6093f0c3-ec58-418d-bb8c-618163c43ac7
title: Metodo COutputQueue.InitialThreadProc (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfc7b8660d838b6ad31dd298c509b6282ab61810
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331460"
---
# <a name="coutputqueueinitialthreadproc-method"></a>Metodo tialThreadProc COutputQueue.Ini

Il `InitialThreadProc` metodo chiama il metodo [**COutputQueue:: ThreadProc**](coutputqueue-threadproc.md) quando viene creato il thread.

## <a name="syntax"></a>Sintassi


```C++
static DWORD WINAPI InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PV* 
</dt> <dd>

`this` puntatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore restituito dal metodo [**COutputQueue:: ThreadProc**](coutputqueue-threadproc.md) .

## <a name="remarks"></a>Commenti

Questo metodo è la procedura del thread per il thread di lavoro dell'oggetto. Il puntatore dell'oggetto `this` è il parametro thread. Il metodo consente di dereferenziare questo oggetto per chiamare **ThreadProc**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




