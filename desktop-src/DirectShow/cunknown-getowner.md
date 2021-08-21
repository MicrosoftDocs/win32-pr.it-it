---
description: Il metodo GetOwner recupera un puntatore all'interfaccia IUnknown del componente proprietario. Per un componente aggregato, il proprietario è il componente esterno. In caso contrario, il componente è proprietario di se stesso.
ms.assetid: 7d8af9d1-52c0-4f2b-9d05-6ddff85ab508
title: Metodo CUnknown.GetOwner (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.GetOwner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c741a6820d414d7a00ad0a9fef768d982f2335c9cb9d8417e42376ea243cc58b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076041"
---
# <a name="cunknowngetowner-method"></a>Metodo CUnknown.GetOwner

Il `GetOwner` metodo recupera un puntatore **all'interfaccia IUnknown** del componente proprietario. Per un componente aggregato, il proprietario è il componente esterno. In caso contrario, il componente è proprietario di se stesso.

## <a name="syntax"></a>Sintassi


```C++
LPUNKNOWN GetOwner();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore **all'interfaccia IUnknown di** controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Combase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




