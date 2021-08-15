---
description: Il metodo get \_ MessageDrain recupera lo svuotamento dei messaggi corrente.
ms.assetid: d679e7f7-4628-479b-b722-843cdd91ffe6
title: CBaseControlWindow.get_MessageDrain metodo (Ctlutil.h)
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
ms.openlocfilehash: 9a1e63e96950093bb7cc5760032d0b1f622c5df93a6f31673c595f54e5ea8e70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017399"
---
# <a name="cbasecontrolwindowget_messagedrain-method"></a>Metodo CBaseControlWindow.get \_ MessageDrain

Il `get_MessageDrain` metodo recupera lo svuotamento dei messaggi corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_MessageDrain(
   OAHWND *Drain
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Drenaggio* 
</dt> <dd>

Puntatore alla finestra corrente che riceve i messaggi della finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

I messaggi inviati al filtro del renderer video possono essere inviati a un'altra finestra. La finestra registrata per ricevere questi messaggi (usando la funzione membro **CBaseControlWindow::get \_ MessageDrain)** è lo svuotamento dei messaggi corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




