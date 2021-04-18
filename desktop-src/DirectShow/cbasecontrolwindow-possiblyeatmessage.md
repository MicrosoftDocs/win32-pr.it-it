---
description: Il metodo PossiblyEatMessage trasmette i messaggi della tastiera e del mouse alla finestra di svuotamento del messaggio.
ms.assetid: 8e344c5d-2f94-454f-89b7-45c539b6e833
title: Metodo CBaseControlWindow. PossiblyEatMessage (Ctlutil. h)
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
ms.openlocfilehash: 9bfadcfbbd6833d8f3e9b65bd39d0cdbef4a006e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327226"
---
# <a name="cbasecontrolwindowpossiblyeatmessage-method"></a>CBaseControlWindow. PossiblyEatMessage, metodo

Il `PossiblyEatMessage` metodo trasmette i messaggi della tastiera e del mouse alla finestra di svuotamento del messaggio.

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

*uMsg* 
</dt> <dd>

Messaggio finestra.

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

Restituisce **true** se il messaggio è stato inviato alla finestra; in caso contrario, **false** .

## <a name="remarks"></a>Commenti

La finestra di svuotamento dei messaggi è una finestra progettata per ricevere determinati messaggi di mouse e tastiera. Inizialmente la finestra è **null**; può essere impostata chiamando [**CBaseControlWindow::p UT \_ MessageDrain**](cbasecontrolwindow-put-messagedrain.md).

Se la finestra di svuotamento dei messaggi è non **null**, `PossiblyEatMessage` inserisce i messaggi seguenti in tale finestra:

-   \_carattere WM
-   \_DEADCHAR WM
-   KeyDown di WM \_
-   KEYUP di WM \_
-   \_LBUTTONDBLCLK WM
-   \_LBUTTONDOWN WM
-   \_LBUTTONUP WM
-   \_MBUTTONDBLCLK WM
-   \_MBUTTONDOWN WM
-   \_MBUTTONUP WM
-   \_MOUSEACTIVATE WM
-   MOUSEMOVE di WM \_
-   \_NCLBUTTONDBLCLK WM
-   \_NCLBUTTONDOWN WM
-   \_NCLBUTTONUP WM
-   \_NCMBUTTONDBLCLK WM
-   \_NCMBUTTONDOWN WM
-   \_NCMBUTTONUP WM
-   \_NCMOUSEMOVE WM
-   \_NCRBUTTONDBLCLK WM
-   \_NCRBUTTONDOWN WM
-   \_NCRBUTTONUP WM
-   \_RBUTTONDBLCLK WM
-   \_RBUTTONDOWN WM
-   \_RBUTTONUP WM
-   \_SYSCHAR WM
-   \_SYSDEADCHAR WM
-   \_SYSKEYDOWN WM
-   \_SYSKEYUP WM

Ignora gli altri messaggi. Se la finestra di svuotamento dei messaggi è **null**, il metodo ignorerà tutti i messaggi della finestra. Il metodo restituisce **true** se inserisce il messaggio o **false** in caso contrario. La classe **CBaseWindow** chiama questo metodo quando riceve un messaggio di finestra.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




