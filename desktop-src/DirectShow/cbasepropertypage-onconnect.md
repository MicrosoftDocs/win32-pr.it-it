---
description: Il metodo OnConnect fornisce un puntatore IUnknown all'oggetto associato alla pagina delle proprietà.
ms.assetid: 74cae8e1-5347-4e3d-ba5f-6a4efec2ddae
title: Metodo CBasePropertyPage. OnConnect (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38f83a7c491f1591cece8d5d85eb4525a1059d2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332648"
---
# <a name="cbasepropertypageonconnect-method"></a>Metodo CBasePropertyPage. OnConnect

Il `OnConnect` metodo fornisce un puntatore **IUnknown** all'oggetto associato alla pagina delle proprietà.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT OnConnect(
   IUnknown *pUnknown
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pUnknown* 
</dt> <dd>

Puntatore all'interfaccia **IUnknown** dell'oggetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

L'implementazione della classe di base restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Il metodo [**CBasePropertyPage:: Seobjects**](cbasepropertypage-setobjects.md) chiama il `OnConnect` metodo. Eseguire l'override di questo metodo per archiviare un puntatore all'oggetto specificato da *pUnknown*. È possibile archiviare il puntatore *pUnknown* o eseguire una query su tale puntatore per altre interfacce. Se si archivia il puntatore *pUnknown* , chiamare **AddRef** prima di `OnConnect` restituire.

Nel metodo [**CBasePropertyPage:: OnActivate**](cbasepropertypage-onactivate.md) usare il puntatore o i puntatori archiviati per recuperare i valori iniziali per le proprietà della finestra di dialogo. Nel metodo [**CBasePropertyPage:: OnApplyChanges**](cbasepropertypage-onapplychanges.md) applicare tutte le modifiche all'oggetto. Rilascia tutti i puntatori nel metodo [**CBasePropertyPage:: Disconnect**](cbasepropertypage-ondisconnect.md) .

## <a name="examples"></a>Esempio


```C++
HRESULT CMyProp::OnConnect(IUnknown *pUnk)
{
    ASSERT(m_pOwningFilter == NULL);
    HRESULT hr;
    // Query pUnk for the filter's custom interface.
    hr = pUnk->QueryInterface(IID_ISomeCustomInterface,
             reinterpret_cast<void**>(&m_pOwningFilter));
    return hr;
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

 

 




