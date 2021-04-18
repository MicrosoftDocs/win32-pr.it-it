---
description: "Il metodo Apply applica i valori correnti della pagina delle proprietà all'oggetto associato alla pagina delle proprietà. Questo metodo implementa il Metodo IPropertyPage:: Apply."
ms.assetid: 9fe759d1-2b46-4489-b7b8-b5a35330091d
title: Metodo CBasePropertyPage. Apply (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Apply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21d1208979cca167b059cb720c492ac51c362c39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329421"
---
# <a name="cbasepropertypageapply-method"></a>Metodo CBasePropertyPage. Apply

Il `Apply` metodo applica i valori correnti della pagina delle proprietà all'oggetto associato alla pagina delle proprietà. Questo metodo implementa il metodo **IPropertyPage:: Apply** .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Apply();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                  | Descrizione                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Esito positivo.<br/>            |
| <dl> <dt>**E \_ imprevisto**</dt> </dl> | Errore imprevisto.<br/> |



 

## <a name="remarks"></a>Commenti

Se il flag [**CBasePropertyPage:: m \_ BDirty**](cbasepropertypage-m-bdirty.md) è **true**, questo metodo chiama il metodo [**CBasePropertyPage:: OnApplyChanges**](cbasepropertypage-onapplychanges.md) . Eseguire l'override di **OnApplyChanges** per applicare le modifiche all'oggetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Cprop. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




