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
ms.openlocfilehash: 0c4b9c5f80e131ce089b6a2da924e9cca41a84f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096409"
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
| Intestazione<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




