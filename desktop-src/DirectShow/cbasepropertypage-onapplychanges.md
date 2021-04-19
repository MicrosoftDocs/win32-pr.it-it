---
description: Il metodo OnApplyChanges viene chiamato quando l'utente applica le modifiche alla pagina delle proprietà.
ms.assetid: 15a55644-b7bf-4c72-8e26-18fc4fb714b9
title: Metodo CBasePropertyPage. OnApplyChanges (Cprop. h)
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
ms.openlocfilehash: cbcea308a8daaa8b9fdf15be765dc5d3a0df182c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332649"
---
# <a name="cbasepropertypageonapplychanges-method"></a>CBasePropertyPage. OnApplyChanges, metodo

Il `OnApplyChanges` metodo viene chiamato quando l'utente applica le modifiche alla pagina delle proprietà.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT OnApplyChanges();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

L'implementazione della classe di base restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Il metodo [**CBasePropertyPage:: Apply**](cbasepropertypage-apply.md) chiama `OnApplyChanges` se il flag [**CBasePropertyPage:: m \_ bDirty**](cbasepropertypage-m-bdirty.md) è **true**. Eseguire l'override `OnApplyChanges` di per elaborare le modifiche e reimpostare **m \_ bDirty** su **false**.

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
| Intestazione<br/>  | <dl> <dt>Cprop. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




