---
description: 'Costruttore CBaseAllocator.CBaseAllocator : metodo costruttore.'
ms.assetid: e697e377-6407-4316-9f04-fe3bdb814175
title: Costruttore CBaseAllocator.CBaseAllocator (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21da9f5dda7f60fd4a88e85eb28f2197bdc9847d0b56d413bd6b49cb5abfe658
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641001"
---
# <a name="cbaseallocatorcbaseallocator-constructor"></a>Costruttore CBaseAllocator.CBaseAllocator

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CBaseAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   BOOL      bEvent = TRUE,
   BOOL      fEnableReleaseCallback = FALSE
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pname* 
</dt> <dd>

Puntatore a una stringa contenente il nome di debug dell'allocatore. Per altre informazioni, vedere [**CBaseObject.**](cbaseobject.md)

</dd> <dt>

*Punk* 
</dt> <dd>

Puntatore al proprietario di questo oggetto. Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown dell'oggetto** aggregatore. In caso contrario, impostare questo parametro su **NULL.**

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a un **valore HRESULT.** Impostare il valore su S \_ OK prima di creare l'oggetto. Se il costruttore ha esito negativo, il valore viene impostato su un codice di errore.

</dd> <dt>

*bEvent* 
</dt> <dd>

Valore booleano che indica se creare un semaforo. Se **TRUE,** l'allocatore crea un semaforo ([**CBaseAllocator::m \_ hSem**](cbaseallocator-m-hsem.md)), che viene segnalato ogni volta che un campione diventa disponibile. Impostare il valore **su FALSE** se si implementa una classe derivata che non richiede un semaforo.

</dd> <dt>

*fEnableReleaseCallback* 
</dt> <dd>

Valore booleano che indica se il meccanismo di callback di rilascio è abilitato. Impostare il valore su **TRUE** se si vuole fornire un'interfaccia di callback, che viene chiamata quando vengono rilasciati i buffer. Specificare il callback chiamando il [**metodo CBaseAllocator::SetNotify.**](cbaseallocator-setnotify.md)

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




