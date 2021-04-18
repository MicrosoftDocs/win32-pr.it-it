---
description: Metodo del costruttore.
ms.assetid: 0057adfe-e397-476b-90f9-7edbf7377b65
title: Costruttore CAMThread. CAMThread (Wxutil. h)
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
ms.openlocfilehash: abaac0c3b0330cd41db7ecd21f894733de10a1b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331946"
---
# <a name="camthreadcamthread-constructor"></a>Costruttore CAMThread. CAMThread

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CAMThread(
   HRESULT *phr = NULL
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PHR* 
</dt> <dd>

Puntatore a un valore **HRESULT** . Se il costruttore ha esito negativo, questo parametro riceve un codice di errore. In tal caso, lo stato dell'oggetto non è valido.

Per la compatibilità con le versioni precedenti di strmbase. lib, il valore predefinito di questo parametro è **null**. Tuttavia, è preferibile passare un valore non **null** , in modo che il chiamante possa controllare lo stato dell'oggetto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il metodo del costruttore non crea il thread. Per creare il thread, chiamare il metodo [**CAMThread:: create**](camthread-create.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




