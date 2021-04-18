---
description: "Il Metodo SetPageSite Inizializza la pagina delle proprietà e fornisce un puntatore all'interfaccia IPropertyPageSite del frame della proprietà. Questo metodo implementa il Metodo IPropertyPage:: SetPageSite."
ms.assetid: 16c4633f-2f91-4b1b-a47c-4ef945c3af00
title: Metodo CBasePropertyPage. SetPageSite (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetPageSite
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a165ff60971cef3d2373e0f07b2abee554308279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325369"
---
# <a name="cbasepropertypagesetpagesite-method"></a>CBasePropertyPage. SetPageSite, metodo

Il `SetPageSite` metodo inizializza la pagina delle proprietà e fornisce un puntatore all'interfaccia **IPropertyPageSite** del frame della proprietà. Questo metodo implementa il metodo **IPropertyPage:: SetPageSite** .

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetPageSite(
   IPropertyPageSite *pPageSite
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPageSite* 
</dt> <dd>

Puntatore all'interfaccia **IPropertyPageSite** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                  | Descrizione                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Esito positivo.<br/>            |
| <dl> <dt>**E \_ imprevisto**</dt> </dl> | Errore imprevisto.<br/> |



 

## <a name="remarks"></a>Commenti

Il metodo archivia il puntatore *pPageSite* nella variabile membro [**CBasePropertyPage:: m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Cprop. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




