---
description: Il \_ metodo Put BorderColor modifica il colore del bordo.
ms.assetid: bb19d338-7fd1-448c-be94-1c71d4a9a330
title: Metodo CBaseControlWindow.put_BorderColor (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54db6de704f2ee0fde1a5087e83df4b362a57959
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328354"
---
# <a name="cbasecontrolwindowput_bordercolor-method"></a>CBaseControlWindow. Put, \_ Metodo BorderColor

Il `put_BorderColor` metodo modifica il colore del bordo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_BorderColor(
   long Color
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Colore* 
</dt> <dd>

Colore nuovo bordo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Un'applicazione può stabilire un rettangolo di destinazione in cui deve essere visualizzato il video. Questo rettangolo è relativo all'area client per la finestra. Se questa operazione viene eseguita (l'impostazione predefinita consiste nel disegnare sempre l'intera finestra), è presente un bordo che circonda il video. Questa proprietà influiscono sul colore utilizzato dal bordo. Anche se il parametro viene specificato come tipo **Long** , si tratta in realtà di un valore **COLORREF** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




