---
description: Il metodo put \_ MessageDrain imposta la finestra per ricevere i messaggi della finestra inviati al renderer video.
ms.assetid: b2d2d489-a66f-474a-b8bf-b019179f6f69
title: CBaseControlWindow.put_MessageDrain metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b58ac59d83023530ca6da51efc2f84ba42c4bef9ac0d3f25ad9a234a320291f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017259"
---
# <a name="cbasecontrolwindowput_messagedrain-method"></a>Metodo CBaseControlWindow.put \_ MessageDrain

Il `put_MessageDrain` metodo imposta la finestra per ricevere i messaggi della finestra inviati al renderer video.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_MessageDrain(
   OAHWND Drain
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Drenaggio* 
</dt> <dd>

Finestra in cui inviare messaggi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

I messaggi inviati al filtro del renderer video possono essere inviati in un'altra finestra. Questa funzione membro registra la finestra per ricevere questi messaggi. A differenza della funzione membro [**CBaseControlWindow::p ut \_ Owner,**](cbasecontrolwindow-put-owner.md) questa funzione membro non rende la finestra video un elemento figlio di un'altra finestra. È particolarmente utile per renderer video a schermo intero, che non possono essere finestre figlio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




