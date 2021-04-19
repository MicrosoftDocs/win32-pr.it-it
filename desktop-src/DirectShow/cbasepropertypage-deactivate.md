---
description: Il metodo Deactivate Elimina la finestra di dialogo. Questo metodo implementa il Metodo IPropertyPage::D ttiva.
ms.assetid: f2d2f15f-15f6-4902-bafc-f58a684ff193
title: Metodo CBasePropertyPage. Deactivate (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Deactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63a843502fc735cc41ff3656e83ef3d6cb839a19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329420"
---
# <a name="cbasepropertypagedeactivate-method"></a>Metodo CBasePropertyPage. Deactivate

Il `Deactivate` metodo elimina la finestra di dialogo. Questo metodo implementa il metodo **IPropertyPage::D ttiva** .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Deactivate();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                  | Descrizione                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Esito positivo.<br/>            |
| <dl> <dt>**E \_ imprevisto**</dt> </dl> | Errore imprevisto.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Cprop. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> <dt>

[**CBasePropertyPage:: OnDeactivate**](cbasepropertypage-ondeactivate.md)
</dt> </dl>

 

 




