---
description: Metodo del costruttore.
ms.assetid: e697e377-6407-4316-9f04-fe3bdb814175
title: Costruttore CBaseAllocator. CBaseAllocator (Amfilter. h)
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
ms.openlocfilehash: 98a1ba1163058f92fba666177d0ff82331dd528c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324041"
---
# <a name="cbaseallocatorcbaseallocator-constructor"></a>Costruttore CBaseAllocator. CBaseAllocator

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

*pName* 
</dt> <dd>

Puntatore a una stringa contenente il nome di debug dell'allocatore. Per ulteriori informazioni, vedere [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pUnk* 
</dt> <dd>

Puntatore al proprietario di questo oggetto. Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown** dell'oggetto di aggregazione. In caso contrario, impostare questo parametro su **null**.

</dd> <dt>

*PHR* 
</dt> <dd>

Puntatore a un valore **HRESULT** . Impostare il valore su S \_ OK prima di creare l'oggetto. Se il costruttore ha esito negativo, il valore viene impostato su un codice di errore.

</dd> <dt>

*con lo sfogo* 
</dt> <dd>

Valore booleano che indica se creare un semaforo. Se **true**, l'allocatore crea un semaforo ([**CBaseAllocator:: m \_ hSem**](cbaseallocator-m-hsem.md)), che viene segnalato ogni volta che un campione diventa disponibile. Impostare il valore su **false** se si implementa una classe derivata che non richiede un semaforo.

</dd> <dt>

*fEnableReleaseCallback* 
</dt> <dd>

Valore booleano che indica se il meccanismo di richiamata della versione è abilitato. Impostare il valore su **true** se si desidera fornire un'interfaccia di callback, che viene chiamata quando vengono rilasciati i buffer. Specificare il callback chiamando il metodo [**CBaseAllocator:: senotify**](cbaseallocator-setnotify.md) .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




