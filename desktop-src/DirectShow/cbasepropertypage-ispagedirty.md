---
description: "Il metodo IsPageDirty indica se la pagina delle proprietà è stata modificata dopo l'attivazione o dopo la chiamata più recente a IPropertyPage:: Apply. Questo metodo implementa il Metodo IPropertyPage:: IsPageDirty."
ms.assetid: 95eeec26-7dbb-4add-a827-6505b40afe48
title: Metodo CBasePropertyPage. IsPageDirty (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.IsPageDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c69c2e7d480f63542e146c73e56b9e692693f665
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330687"
---
# <a name="cbasepropertypageispagedirty-method"></a>CBasePropertyPage. IsPageDirty, metodo

Il `IsPageDirty` metodo indica se la pagina delle proprietà è stata modificata dopo l'attivazione o dopo la chiamata più recente a **IPropertyPage:: Apply**. Questo metodo implementa il metodo **IPropertyPage:: IsPageDirty** .

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsPageDirty();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se [**CBasePropertyPage:: m \_ bDirty**](cbasepropertypage-m-bdirty.md) è **true** oppure S \_ false in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Cprop. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




