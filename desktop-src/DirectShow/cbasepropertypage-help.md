---
description: Il metodo Help richiama la Guida della pagina delle proprietà. Questo metodo implementa il metodo IPropertyPage::Help.
ms.assetid: 8fe72b2e-a9f1-435d-8eda-27056f112c6d
title: Metodo CBasePropertyPage.Help (Cprop.h)
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
ms.openlocfilehash: e2f97f7edd1e719eb44ff1d41929d7cb3864d8117eabb383b4318688adfa537f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955090"
---
# <a name="cbasepropertypagehelp-method"></a>Metodo CBasePropertyPage.Help

Il `Help` metodo richiama la Guida della pagina delle proprietà. Questo metodo implementa il **metodo IPropertyPage::Help.**

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

Puntatore alla stringa sotto la **chiave HelpDir** nelle informazioni CLSID della pagina delle proprietà nel Registro di sistema.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E \_ NOTIMPL.

## <a name="remarks"></a>Commenti

Nella classe di base il metodo restituisce sempre E \_ NOTIMPL. Quando il metodo ha esito negativo, il frame chiama **IPropertyPage::GetPageInfo** per ottenere il nome del file della Guida e l'identificatore di contesto. Per impostazione predefinita, si tratta **di NULL.** Per fornire assistenza, pertanto, la classe derivata può eseguire l'override del metodo o del metodo `Help` [**CBasePropertyPage::GetPageInfo.**](cbasepropertypage-getpageinfo.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Cprop.h (includere Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




