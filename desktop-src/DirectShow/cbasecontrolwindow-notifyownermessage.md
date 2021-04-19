---
description: Il metodo NotifyOwnerMessage passa i messaggi specifici alla finestra del video.
ms.assetid: 8b27281a-5b8a-46c3-aa66-390d4496f30e
title: Metodo CBaseControlWindow. NotifyOwnerMessage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.NotifyOwnerMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9073d37987404849ba8aa3acbda9919df840b410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333613"
---
# <a name="cbasecontrolwindownotifyownermessage-method"></a>CBaseControlWindow. NotifyOwnerMessage, metodo

Il `NotifyOwnerMessage` metodo passa i messaggi specifici alla finestra del video.

## <a name="syntax"></a>Sintassi


```C++
HRESULT NotifyOwnerMessage(
   long     hwnd,
   long     uMsg,
   LONG_PTR wParam,
   LONG_PTR lParam
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* 
</dt> <dd>

Handle per la finestra del video.

</dd> <dt>

*uMsg* 
</dt> <dd>

Dettagli del messaggio.

</dd> <dt>

*wParam* 
</dt> <dd>

Primo parametro del messaggio.

</dd> <dt>

*lParam* 
</dt> <dd>

Secondo parametro del messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Non restituisce alcun \_ errore.

## <a name="remarks"></a>Commenti

Quando la finestra video è un elemento figlio di un'altra finestra, non riceve alcuni messaggi della finestra di primo livello. Questi messaggi possono essere utili per un renderer, perché potrebbero influire sul comportamento. `NotifyOwnerMessage` passa uno dei messaggi seguenti alla finestra del video.

-   \_ACTIVATEAPP WM
-   \_DEVMODECHANGE WM
-   \_DISPLAYCHANGE WM
-   \_PALETTECHANGED WM
-   \_PALETTEISCHANGING WM
-   \_QUERYNEWPALETTE WM
-   \_SYSCOLORCHANGE WM

È possibile richiedere che il server di distribuzione plug-in [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (PID) renda una finestra diventata un elemento figlio di un'altra finestra. Quando si verifica questo problema, il PID cercherà determinati messaggi che potrebbero essere inviati alla finestra proprietaria. Il PID li inoltrerà quindi alla finestra di proprietà. L'elaborazione predefinita per i messaggi consiste nell'inviarli in modo sincrono alla routine di proprietà della finestra chiamando la funzione **SendMessage** Win32.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




