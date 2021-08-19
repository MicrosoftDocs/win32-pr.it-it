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
ms.openlocfilehash: 71d7ca547556c151107c35c9ece1f4ee0d0ca6a80feb6db0cebb06878ddbca01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131221"
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
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageAllocator**](cimageallocator.md)
</dt> </dl>

 

 




