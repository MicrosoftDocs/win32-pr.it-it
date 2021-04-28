---
description: 'Costruttore CBasePropertyPage.CBasePropertyPage : metodo costruttore.'
ms.assetid: 5d9863e7-fdd9-4df2-a603-34a240a2286c
title: Costruttore CBasePropertyPage.CBasePropertyPage (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 95821062b6b1199ea98a5329934d76e2197901d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119949"
---
# <a name="cbasepropertypagecbasepropertypage-constructor"></a>Costruttore CBasePropertyPage.CBasePropertyPage

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CBasePropertyPage(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   int       DialogId,
   int       TitleId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pname* 
</dt> <dd>

Stringa che contiene il nome dell'oggetto a scopo di debug. Per altre informazioni, vedere [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).

</dd> <dt>

*Punk* 
</dt> <dd>

Puntatore all'interfaccia **IUnknown aggregata.**

</dd> <dt>

*Id dialogo* 
</dt> <dd>

ID risorsa per la finestra di dialogo.

</dd> <dt>

*TitleId* 
</dt> <dd>

ID risorsa per la stringa che contiene il titolo della finestra di dialogo.

</dd> </dl>

## <a name="examples"></a>Esempio


```C++
CMyProp::CMyProp(IUnknown *pUnk) : 
    CBasePropertyPage(NAME("MyPropPage"), pUnk, IDD_PROPPAGE, IDS_TITLE),
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Cprop.h (include Streams.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




