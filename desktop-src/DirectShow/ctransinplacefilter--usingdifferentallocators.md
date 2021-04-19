---
description: Il metodo UsingDifferentAllocators determina se i pin di input e di output utilizzano allocatori diversi.
ms.assetid: 75feaa6e-6395-4d47-ae92-10a857f8764b
title: Metodo CTransInPlaceFilter. UsingDifferentAllocators (Transip. h)
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
ms.openlocfilehash: f20802836adb665614e2bbfb8cb79bdccd5a36ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332984"
---
# <a name="ctransinplacefilterusingdifferentallocators-method"></a>CTransInPlaceFilter. UsingDifferentAllocators, metodo

Il `UsingDifferentAllocators` metodo determina se i pin di input e di output utilizzano allocatori diversi.

## <a name="syntax"></a>Sintassi


```C++
BOOL UsingDifferentAllocators() const;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **true** se i pin di input e di output utilizzano allocatori diversi. in caso contrario, **false** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




