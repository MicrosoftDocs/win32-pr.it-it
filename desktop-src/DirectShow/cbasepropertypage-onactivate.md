---
description: Il metodo OnActivate viene chiamato quando la pagina delle proprietà viene attivata.
ms.assetid: aff843d4-cfb2-4255-a59c-0579f1cd24bd
title: Metodo CBasePropertyPage. OnActivate (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnActivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5093cb2ac71e8010bc689e4517b3d8bb758c8436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329411"
---
# <a name="cbasepropertypageonactivate-method"></a>Metodo CBasePropertyPage. OnActivate

Il `OnActivate` metodo viene chiamato quando la pagina delle proprietà viene attivata.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT OnActivate();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

L'implementazione della classe di base restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Il metodo [**CBasePropertyPage:: Activate**](cbasepropertypage-activate.md) chiama il `OnActivate` metodo. Nella classe derivata eseguire l'override `OnActivate` di per inizializzare la finestra di dialogo.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene inizializzato un controllo TrackBar. Questo esempio si basa sul presupposto che **m \_ pOwningFilter** sia un puntatore a un'interfaccia personalizzata nel filtro associato alla pagina delle proprietà. Usare il metodo [**CBasePropertyPage:: OnConnect**](cbasepropertypage-onconnect.md) per inizializzare tali puntatori.


```C++
HRESULT CMyProp::OnActivate(void)
{
    ASSERT(m_pOwningFilter != NULL);
    m_pOwningFilter->GetSomeProperty(&m_lOldVal);
    
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETRANGE, 0, MAKELONG(0, 100));
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETTICFREQ, 10, 0);
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1, m_lOldVal);
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

 

 




