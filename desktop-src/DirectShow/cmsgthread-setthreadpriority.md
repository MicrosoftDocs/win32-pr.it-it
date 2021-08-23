---
description: Usa la funzione Microsoft Win32 SetThreadPriority per impostare la priorità del thread su un nuovo valore.
ms.assetid: 5b8ad024-e651-47e5-b32a-c44d56c086cd
title: Metodo CMsgThread.SetThreadPriority (Msgthrd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SetThreadPriority
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce293f32f765a89451ecf07b4532afc5fc4a7a132287d5b09b54962f93135215
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585671"
---
# <a name="cmsgthreadsetthreadpriority-method"></a>Metodo CMsgThread.SetThreadPriority

Usa la funzione Microsoft Win32 **SetThreadPriority** per impostare la priorità del thread su un nuovo valore.

## <a name="syntax"></a>Sintassi


```C++
BOOL SetThreadPriority(
   int nPriority
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nPriority* 
</dt> <dd>

Priorità del thread.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori seguenti.



| Codice restituito                                                                              | Descrizione                               |
|------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>TRUE****</dt> </dl>  | La priorità è stata impostata correttamente.<br/> |
| <dl> <dt>FALSE****</dt> </dl> | La priorità non è stata impostata.<br/>          |



 

## <a name="remarks"></a>Commenti

Il client e il thread di lavoro possono chiamare questa funzione membro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Msgthrd.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




