---
description: 'Costruttore CAMThread.CAMThread : metodo costruttore.'
ms.assetid: 0057adfe-e397-476b-90f9-7edbf7377b65
title: Costruttore CAMThread.CAMThread (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e042624573cd0c421e8ecd202cde971a49eef95cc5f3c6c0ac64bf45b4cf9c19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103331"
---
# <a name="camthreadcamthread-constructor"></a>Costruttore CAMThread.CAMThread

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CAMThread(
   HRESULT *phr = NULL
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Phr* 
</dt> <dd>

Puntatore a un **valore HRESULT.** Se il costruttore ha esito negativo, questo parametro riceve un codice di errore. In questo caso, l'oggetto non è in uno stato valido.

Per la compatibilità con le versioni precedenti di strmbase.lib, il valore predefinito di questo parametro è **NULL.** Tuttavia, è preferibile passare un valore non **NULL,** in modo che il chiamante possa controllare lo stato dell'oggetto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il metodo del costruttore non crea il thread. Per creare il thread, chiamare il [**metodo CAMThread::Create.**](camthread-create.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




