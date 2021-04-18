---
description: Il metodo GetOwner recupera un puntatore all'interfaccia IUnknown del componente proprietario. Per un componente aggregato, il proprietario è il componente esterno. In caso contrario, il componente è proprietario.
ms.assetid: 7d8af9d1-52c0-4f2b-9d05-6ddff85ab508
title: Metodo CUnknown. GetOwner (ComBase. h)
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
ms.openlocfilehash: e3cb1cd1d5b183857b6d75db79ee0fcdc6cb2d30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331451"
---
# <a name="cunknowngetowner-method"></a>Metodo CUnknown. GetOwner

Il `GetOwner` metodo recupera un puntatore all'interfaccia **IUnknown** del componente proprietario. Per un componente aggregato, il proprietario è il componente esterno. In caso contrario, il componente è proprietario.

## <a name="syntax"></a>Sintassi


```C++
LPUNKNOWN GetOwner();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore all'interfaccia **IUnknown** di controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>ComBase. h (Includi Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




