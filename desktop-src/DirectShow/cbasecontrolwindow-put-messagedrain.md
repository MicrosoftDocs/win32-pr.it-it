---
description: Il \_ metodo Put MessageDrain imposta la finestra per la ricezione di messaggi della finestra inviati al renderer video.
ms.assetid: b2d2d489-a66f-474a-b8bf-b019179f6f69
title: Metodo CBaseControlWindow.put_MessageDrain (Ctlutil. h)
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
ms.openlocfilehash: f03f944a6af6ac99de6000a2507178eea510c06a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331943"
---
# <a name="cbasecontrolwindowput_messagedrain-method"></a>CBaseControlWindow. put \_ MessageDrain (metodo)

Il `put_MessageDrain` metodo imposta la finestra per la ricezione di messaggi della finestra inviati al renderer video.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_MessageDrain(
   OAHWND Drain
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Scarico* 
</dt> <dd>

Finestra in cui pubblicare i messaggi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

I messaggi inviati al filtro renderer video possono essere inseriti in un'altra finestra. Questa funzione membro registra la finestra per ricevere questi messaggi. A differenza della funzione membro [**CBaseControlWindow::p UT \_ owner**](cbasecontrolwindow-put-owner.md) , questa funzione membro non rende la finestra video un elemento figlio di un'altra finestra. È particolarmente utile per i renderer video a schermo intero, che non possono essere finestre figlio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




