---
description: 'Il metodo Activate crea la finestra di dialogo. Questo metodo implementa il Metodo IPropertyPage:: Activate.'
ms.assetid: 8f030dc5-1d14-46b5-9d40-7f07a1177dbe
title: Metodo CBasePropertyPage. Activate (Cprop. h)
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
ms.openlocfilehash: 4b851cfc4490d25e7e30dfd2cf0e7c33b0e76224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328077"
---
# <a name="cbasepropertypageactivate-method"></a>Metodo CBasePropertyPage. Activate

Il `Activate` metodo crea la finestra di dialogo. Questo metodo implementa il metodo **IPropertyPage:: Activate** .

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

Puntatore a una struttura **Rect** che contiene informazioni sul posizionamento per la finestra di dialogo.

</dd> <dt>

*fModal* 
</dt> <dd>

Valore booleano che indica se il frame della finestra di dialogo è modale (**true**) o non modale (**false**).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                   | Descrizione                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Esito positivo.<br/>                   |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>       |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Argomento puntatore **null** .<br/> |
| <dl> <dt>**E \_ imprevisto**</dt> </dl>  | Errore imprevisto.<br/>        |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Cprop. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> <dt>

[**CBasePropertyPage:: OnActivate**](cbasepropertypage-onactivate.md)
</dt> </dl>

 

 




