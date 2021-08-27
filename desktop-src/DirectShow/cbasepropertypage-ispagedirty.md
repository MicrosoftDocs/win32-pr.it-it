---
description: Il metodo IsPageDirty indica se la pagina delle proprietà è stata modificata dopo l'attivazione o dopo la chiamata più recente a IPropertyPage::Apply. Questo metodo implementa il metodo IPropertyPage::IsPageDirty.
ms.assetid: 95eeec26-7dbb-4add-a827-6505b40afe48
title: Metodo CBasePropertyPage.IsPageDirty (Cprop.h)
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
ms.openlocfilehash: 72b818ce117990f6f91ee58b8605e9d8cff9734fa9114d7f6114ed11d53a9521
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108501"
---
# <a name="cbasepropertypageispagedirty-method"></a>Metodo CBasePropertyPage.IsPageDirty

Il metodo indica se la pagina delle proprietà è stata modificata dopo l'attivazione o dopo la chiamata più `IsPageDirty` recente a **IPropertyPage::Apply.** Questo metodo implementa il **metodo IPropertyPage::IsPageDirty.**

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsPageDirty();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK se [**CBasePropertyPage::m \_ bDirty**](cbasepropertypage-m-bdirty.md) è **TRUE** o S FALSE in \_ caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Cprop.h (includere Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




