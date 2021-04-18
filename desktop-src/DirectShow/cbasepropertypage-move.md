---
description: 'Il metodo Move posiziona e ridimensiona la finestra di dialogo. Questo metodo implementa il Metodo IPropertyPage:: Move.'
ms.assetid: b6cabb5c-196d-489b-9dd4-194d26f4de83
title: Metodo CBasePropertyPage. Move (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Move
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d293f6ccb6a1bcd730ce997367c179f1747f66e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329416"
---
# <a name="cbasepropertypagemove-method"></a>Metodo CBasePropertyPage. Move

Il `Move` Metodo posiziona e ridimensiona la finestra di dialogo. Questo metodo implementa il metodo **IPropertyPage:: Move** .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Move(
   LPCRECT prect
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*prect* 
</dt> <dd>

Puntatore a una struttura **Rect** contenente le informazioni sul posizionamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                  | Descrizione                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Esito positivo.<br/>                   |
| <dl> <dt>**\_puntatore E**</dt> </dl>    | Argomento puntatore **null** .<br/> |
| <dl> <dt>**E \_ imprevisto**</dt> </dl> | Errore imprevisto.<br/>        |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Cprop. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




