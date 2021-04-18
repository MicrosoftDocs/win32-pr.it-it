---
description: 'Il metodo TranslateAccelerator indica alla pagina delle proprietà di elaborare una sequenza di tasti. Questo metodo implementa il Metodo IPropertyPage:: TranslateAccelerator.'
ms.assetid: 2da214c9-35dc-470c-9b7f-2f4ef6bcd40a
title: Metodo CBasePropertyPage. TranslateAccelerator (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.TranslateAccelerator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3116e85eec8fbf3a00bf434a1f88c8cac662ed0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324491"
---
# <a name="cbasepropertypagetranslateaccelerator-method"></a>CBasePropertyPage. TranslateAccelerator, metodo

Il `TranslateAccelerator` metodo indica alla pagina delle proprietà di elaborare una sequenza di tasti. Questo metodo implementa il metodo **IPropertyPage:: TranslateAccelerator** .

## <a name="syntax"></a>Sintassi


```C++
HRESULT TranslateAccelerator(
   LPMSG lpMsg
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpMsg* 
</dt> <dd>

Puntatore a una struttura **msg** che descrive la sequenza di tasti da elaborare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E \_ NOTIMPL.

## <a name="remarks"></a>Commenti

Eseguire l'override di questo metodo se si desidera fornire tasti di scelta rapida per la pagina delle proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Cprop. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




