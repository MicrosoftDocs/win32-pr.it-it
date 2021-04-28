---
description: Costruttore CImageAllocator.CImageAllocator - Metodo costruttore.
ms.assetid: 8c215b16-98e5-42fb-a95b-b6df1ade180e
title: Costruttore CImageAllocator.CImageAllocator (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f17ae78b668f6cc35e454c5e4e83d38727077ef7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085759"
---
# <a name="cimageallocatorcimageallocator-constructor"></a>Costruttore CImageAllocator.CImageAllocator

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CImageAllocator(
   CBaseFilter *pFilter,
   TCHAR       *pName,
   HRESULT     *phr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFilter* 
</dt> <dd>

Puntatore al filtro proprietario.

</dd> <dt>

*Pname* 
</dt> <dd>

Puntatore a una stringa contenente il nome di debug dell'allocatore. Per altre informazioni, vedere [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a un **valore HRESULT.** Impostare il valore su S \_ OK prima di creare l'oggetto. Se il costruttore ha esito negativo, il valore viene impostato su un codice di errore.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageAllocator**](cimageallocator.md)
</dt> </dl>

 

 




