---
description: Il metodo CheckRequest controlla se è presente una richiesta di thread senza blocco.
ms.assetid: b4691dde-abec-4671-bea6-0f22cc4e7c61
title: Metodo CSourceStream. CheckRequest (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3100d449d2f29b2080541c5968cad6abc5643b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329030"
---
# <a name="csourcestreamcheckrequest-method"></a>CSourceStream. CheckRequest, metodo

Il `CheckRequest` metodo verifica se è presente una richiesta di thread senza blocco.

## <a name="syntax"></a>Sintassi


```C++
BOOL CheckRequest(
   Command *pCom
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*MOCF* 
</dt> <dd>

Puntatore a una variabile che riceve il valore passato nell'ultima chiamata al metodo [**CAMThread:: CallWorker**](camthread-callworker.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se è presente una richiesta in sospeso; in caso contrario, **false** .

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CAMThread:: CheckRequest**](camthread-checkrequest.md) per eseguire il controllo dei tipi. La classe **CSourceStream** definisce il tipo enumerato seguente per il parametro *MOCF* :


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source. h (Includi Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




