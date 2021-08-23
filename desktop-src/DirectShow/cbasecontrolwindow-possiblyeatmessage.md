---
description: Il metodo PossiblyEatMessage inoltra i messaggi della tastiera e del mouse alla finestra di svuotamento dei messaggi.
ms.assetid: 8e344c5d-2f94-454f-89b7-45c539b6e833
title: Metodo CBaseControlWindow.PossiblyEatMessage (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 403fb4d170f9c3cf0b7d68d3ac6ce1fdcc9c81a14b1c76d74e67bb64d4d9cc8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017339"
---
# <a name="cbasecontrolwindowpossiblyeatmessage-method"></a>Metodo CBaseControlWindow.PossiblyEatMessage

Il `PossiblyEatMessage` metodo inoltra i messaggi della tastiera e del mouse alla finestra di svuotamento dei messaggi.

## <a name="syntax"></a>Sintassi


```C++
BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Umsg* 
</dt> <dd>

Messaggio della finestra.

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

Restituisce **TRUE** se il messaggio è stato inoltrato alla finestra oppure **FALSE in caso** contrario.

## <a name="remarks"></a>Commenti

La finestra di svuotamento dei messaggi è una finestra designata per ricevere determinati messaggi del mouse e della tastiera. Inizialmente la finestra è **NULL.** Può essere impostato chiamando [**CBaseControlWindow::p ut \_ MessageDrain**](cbasecontrolwindow-put-messagedrain.md).

Se la finestra di svuotamento dei messaggi è non **NULL,** `PossiblyEatMessage` invia i messaggi seguenti a tale finestra:

-   WM \_ CHAR
-   WM \_ DEADCHAR
-   WM \_ KEYDOWN
-   WM \_ KEYUP
-   WM \_ LBUTTONDBLCLK
-   WM \_ LBUTTONDOWN
-   WM \_ LBUTTONUP
-   WM \_ MBUTTONDBLCLK
-   WM \_ MBUTTONDOWN
-   WM \_ MBUTTONUP
-   WM \_ MOUSEACTIVATE
-   WM \_ MOUSEMOVE
-   WM \_ NCLBUTTONDBLCLK
-   WM \_ NCLBUTTONDOWN
-   WM \_ NCLBUTTONUP
-   WM \_ NCMBUTTONDBLCLK
-   WM \_ NCMBUTTONDOWN
-   WM \_ NCMBUTTONUP
-   WM \_ NCMOUSEMOVE
-   WM \_ NCRBUTTONDBLCLK
-   WM \_ NCRBUTTONDOWN
-   WM \_ NCRBUTTONUP
-   WM \_ RBUTTONDBLCLK
-   WM \_ RBUTTONDOWN
-   WM \_ RBUTTONUP
-   WM \_ SYSCHAR
-   WM \_ SYSDEADCHAR
-   WM \_ SYSKEYDOWN
-   WM \_ SYSKEYUP

Ignora gli altri messaggi. Se la finestra di svuotamento dei messaggi **è NULL,** il metodo ignora tutti i messaggi della finestra. Il metodo restituisce **TRUE se** invia il messaggio oppure FALSE **in caso** contrario. La **classe CBaseWindow** chiama questo metodo quando riceve un messaggio di finestra.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




