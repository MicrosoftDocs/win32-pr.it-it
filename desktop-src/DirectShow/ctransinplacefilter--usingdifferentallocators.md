---
description: Il metodo UsingDifferentAllocators determina se i pin di input e di output usano allocatori diversi.
ms.assetid: 75feaa6e-6395-4d47-ae92-10a857f8764b
title: Metodo CTransInPlaceFilter.UsingDifferentAllocators (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.UsingDifferentAllocators
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0033c0f5ded1fe741d27397078367049d72061c40a993833f714686d9f8a96fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953420"
---
# <a name="ctransinplacefilterusingdifferentallocators-method"></a>Metodo CTransInPlaceFilter.UsingDifferentAllocators

Il `UsingDifferentAllocators` metodo determina se i pin di input e output usano allocatori diversi.

## <a name="syntax"></a>Sintassi


```C++
BOOL UsingDifferentAllocators() const;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** i pin di input e output usano allocatori diversi oppure FALSE in caso **contrario.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




