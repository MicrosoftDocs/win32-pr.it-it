---
description: Il metodo Activate crea la finestra di dialogo. Questo metodo implementa il metodo IPropertyPage::Activate.
ms.assetid: 8f030dc5-1d14-46b5-9d40-7f07a1177dbe
title: Metodo CBasePropertyPage.Activate (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Activate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b525eb16f534f0da8c847f50365c43124cb9e37d89f16629842fa202925a0674
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108521"
---
# <a name="cbasepropertypageactivate-method"></a>Metodo CBasePropertyPage.Activate

Il `Activate` metodo crea la finestra di dialogo. Questo metodo implementa il **metodo IPropertyPage::Activate.**

## <a name="syntax"></a>Sintassi


```C++
HRESULT Activate(
   HWND    hwndParent,
   LPCRECT prect,
   BOOL    fModal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndParent* 
</dt> <dd>

Handle per la finestra padre della finestra di dialogo.

</dd> <dt>

*prect* 
</dt> <dd>

Puntatore a una **struttura RECT** che contiene informazioni sul posizionamento per la finestra di dialogo.

</dd> <dt>

*fModal* 
</dt> <dd>

Valore booleano che indica se la cornice della finestra di dialogo è modale (**TRUE**) o non modale **(FALSE).**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                   | Descrizione                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>       |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | Argomento del puntatore **NULL.**<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>  | Errore imprevisto.<br/>        |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Cprop.h (includere Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> <dt>

[**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md)
</dt> </dl>

 

 




