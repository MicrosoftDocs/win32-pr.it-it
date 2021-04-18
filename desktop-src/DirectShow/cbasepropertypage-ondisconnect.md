---
description: Il metodo Disconnect viene chiamato quando la pagina delle proprietà deve rilasciare l'oggetto associato.
ms.assetid: 55bab0ca-587e-405c-9025-f391cf08a620
title: Metodo CBasePropertyPage. Disconnect (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDisconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd251d20ca82ad0374a613d9ee73f0eaee21d31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325198"
---
# <a name="cbasepropertypageondisconnect-method"></a>Metodo CBasePropertyPage. Disconnect

Il `OnDisconnect` metodo viene chiamato quando la pagina delle proprietà deve rilasciare l'oggetto associato.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT OnDisconnect();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

L'implementazione della classe di base restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Il metodo [**CBasePropertyPage:: Seobjects**](cbasepropertypage-setobjects.md) chiama il `OnDisconnect` metodo. Eseguire l'override `OnDisconnect` per rilasciare tutti i puntatori ottenuti nel metodo [**CBasePropertyPage:: OnConnect**](cbasepropertypage-onconnect.md) .

## <a name="examples"></a>Esempio


```C++
HRESULT CMyProp::OnDisconnect(void)
{
    if (m_pOwningFilter)
    {
        m_pOwningFilter->Release();
        m_pOwningFilter = NULL;
    }
    return S_OK;
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

 

 




