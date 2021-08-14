---
description: Il metodo OnApplyChanges viene chiamato quando l'utente applica modifiche alla pagina delle proprietà.
ms.assetid: 15a55644-b7bf-4c72-8e26-18fc4fb714b9
title: Metodo CBasePropertyPage.OnApplyChanges (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnApplyChanges
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f822bed433af6e3fab0250e06a04911ee10187039036211974b046b32df6b7b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823107"
---
# <a name="cbasepropertypageonapplychanges-method"></a>Metodo CBasePropertyPage.OnApplyChanges

Il `OnApplyChanges` metodo viene chiamato quando l'utente applica modifiche alla pagina delle proprietà.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT OnApplyChanges();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

L'implementazione della classe base restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Il [**metodo CBasePropertyPage::Apply**](cbasepropertypage-apply.md) chiama `OnApplyChanges` se il flag [**CBasePropertyPage::m \_ bDirty**](cbasepropertypage-m-bdirty.md) è **TRUE.** Eseguire `OnApplyChanges` l'override di per elaborare le modifiche e **reimpostare m \_ bDirty** su **FALSE.**

## <a name="examples"></a>Esempio


```C++
HRESULT CMyProp::OnApplyChanges(void)
{
    ASSERT(m_pOwningFilter != NULL);
    return m_pOwningFilter->SetSomeProperty(&m_lNewVal);
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Cprop.h (includere Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




