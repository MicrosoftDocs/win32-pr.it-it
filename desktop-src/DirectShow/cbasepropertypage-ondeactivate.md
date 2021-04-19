---
description: Il metodo OnDeactivate viene chiamato quando la finestra di dialogo viene eliminata definitivamente.
ms.assetid: 47320e61-324f-4f64-abe1-38fe70e82787
title: Metodo CBasePropertyPage. OnDeactivate (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDeactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27191e4895c911d3d13a795306eee2b0ad6989ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333085"
---
# <a name="cbasepropertypageondeactivate-method"></a>CBasePropertyPage. OnDeactivate, metodo

Il `OnDeactivate` metodo viene chiamato quando la finestra di dialogo viene eliminata definitivamente.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT OnDeactivate();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

L'implementazione della classe di base restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Il metodo [**CBasePropertyPage::D ttiva**](cbasepropertypage-deactivate.md) chiama il `OnDeactivate` metodo. Eseguire l'override `OnDeactivate` per rilasciare tutte le risorse ottenute dalla classe derivata nel metodo [**CBasePropertyPage:: OnActivate**](cbasepropertypage-onactivate.md) oppure per eseguire altre attività in base alle esigenze.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Cprop. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




