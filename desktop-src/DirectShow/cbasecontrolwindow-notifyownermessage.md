---
description: Il metodo NotifyOwnerMessage passa messaggi specifici alla finestra video.
ms.assetid: 8b27281a-5b8a-46c3-aa66-390d4496f30e
title: Metodo CBaseControlWindow.NotifyOwnerMessage (Ctlutil.h)
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
ms.openlocfilehash: 35d71057027bd8fbd572dffd714f761ff101ba0de95dd42dcf058009b0cb1b04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526851"
---
# <a name="cbasecontrolwindownotifyownermessage-method"></a>Metodo CBaseControlWindow.NotifyOwnerMessage

Il `NotifyOwnerMessage` metodo passa messaggi specifici alla finestra video.

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

*Hwnd* 
</dt> <dd>

Handle per la finestra video.

</dd> <dt>

*Umsg* 
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

Restituisce NO \_ ERROR.

## <a name="remarks"></a>Commenti

Quando la finestra video è figlio di un'altra finestra, non riceve determinati messaggi della finestra di primo livello. Questi messaggi possono essere utili per un renderer, perché potrebbero influire sul relativo comportamento. `NotifyOwnerMessage` passa uno dei messaggi seguenti alla finestra del video.

-   WM \_ ACTIVATEAPP
-   WM \_ DEVMODECHANGE
-   WM \_ DISPLAYCHANGE
-   WM \_ PALETTECHANGED
-   WM \_ PALETTEISCHANGING
-   WM \_ QUERYNEWPALETTE
-   WM \_ SYSCOLORCHANGE

È possibile richiedere al distributore del plug-in [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (PID) di rendere una finestra figlio di un'altra finestra. In questo caso, il PID cerca alcuni messaggi che potrebbero essere inviati alla finestra proprietaria. Il PID inoltra quindi i messaggi alla finestra di proprietà. L'elaborazione predefinita per i messaggi è di inviarli alla routine della finestra di proprietà in modo sincrono chiamando la funzione **SendMessage** Win32.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




