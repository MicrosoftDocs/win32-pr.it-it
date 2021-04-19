---
description: Il \_ metodo Get MessageDrain recupera lo svuotamento del messaggio corrente.
ms.assetid: d679e7f7-4628-479b-b722-843cdd91ffe6
title: Metodo CBaseControlWindow.get_MessageDrain (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aaf51c3f4297f238e51bbe8677303730c04b89d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326068"
---
# <a name="cbasecontrolwindowget_messagedrain-method"></a>Metodo CBaseControlWindow. Get \_ MessageDrain

Il `get_MessageDrain` metodo recupera lo svuotamento del messaggio corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_MessageDrain(
   OAHWND *Drain
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Scarico* 
</dt> <dd>

Puntatore alla finestra corrente che riceve i messaggi della finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

I messaggi inviati al filtro renderer video possono essere inseriti in un'altra finestra. La finestra registrata per ricevere questi messaggi (usando la funzione membro **CBaseControlWindow:: Get \_ MessageDrain** ) è lo svuotamento del messaggio corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




