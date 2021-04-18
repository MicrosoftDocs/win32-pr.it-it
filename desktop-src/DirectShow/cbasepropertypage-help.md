---
description: 'Il metodo della guida richiama la guida della pagina delle proprietà. Questo metodo implementa il Metodo IPropertyPage:: help.'
ms.assetid: 8fe72b2e-a9f1-435d-8eda-27056f112c6d
title: Metodo CBasePropertyPage. Help (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Help
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b87c8ba76928fbf0e465a8b6a3a0aaf4730759f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330690"
---
# <a name="cbasepropertypagehelp-method"></a>Metodo CBasePropertyPage. Help

Il `Help` metodo richiama la guida della pagina delle proprietà. Questo metodo implementa il metodo **IPropertyPage:: Help** .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Help(
   LPCWSTR lpszHelpDir
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszHelpDir* 
</dt> <dd>

Puntatore alla stringa sotto la chiave **helpDir** nelle informazioni sul CLSID della pagina delle proprietà nel registro di sistema.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E \_ NOTIMPL.

## <a name="remarks"></a>Commenti

Nella classe base il metodo restituisce sempre E \_ NOTIMPL. Quando il metodo ha esito negativo, il frame chiama **IPropertyPage:: GetPageInfo** per ottenere il nome del file della guida e l'identificatore di contesto. Per impostazione predefinita, questi **valori sono null**. Per fornire la guida, pertanto, la classe derivata può eseguire l'override del metodo `Help` o del metodo [**CBasePropertyPage:: GetPageInfo**](cbasepropertypage-getpageinfo.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Cprop. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




