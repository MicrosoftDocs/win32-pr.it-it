---
description: 'Il metodo GetPageInfo recupera le informazioni sulla pagina delle proprietà. Questo metodo implementa il Metodo IPropertyPage:: GetPageInfo.'
ms.assetid: f2e04652-7c71-48b2-b964-4e07ac98d367
title: Metodo CBasePropertyPage. GetPageInfo (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.GetPageInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27faecf50381b098dfcbee34d1494e37c77a36ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330694"
---
# <a name="cbasepropertypagegetpageinfo-method"></a>CBasePropertyPage. GetPageInfo, metodo

Il `GetPageInfo` metodo recupera le informazioni sulla pagina delle proprietà. Questo metodo implementa il metodo **IPropertyPage:: GetPageInfo** .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPageInfo(
   LPPROPPAGEINFO pPageInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPageInfo* 
</dt> <dd>

Puntatore a una struttura **PROPPAGEINFO** allocata dal chiamante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                   | Descrizione                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Esito positivo.<br/>             |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Cprop. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




