---
description: Notifica a un'applicazione quando un IME sta per chiudere la finestra di stato. L'applicazione riceve questo comando tramite il messaggio WM \_ IME \_ NOTIFY con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: d59fdf76-50e7-4a59-b1bd-a12cdb0026f6
title: IMN_CLOSESTATUSWINDOW di notifica (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a56093e5dac9c5b9b236c6819a627c1d8c1fc05aa8350824577f29f64c007e71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107161"
---
# <a name="imn_closestatuswindow-notification-code"></a>Codice di notifica IMN \_ CLOSESTATUSWINDOW

Notifica a un'applicazione quando un IME sta per chiudere la finestra di stato. L'applicazione riceve questo comando tramite il messaggio [**WM \_ IME \_ NOTIFY**](wm-ime-notify.md) con le impostazioni dei parametri, come illustrato di seguito.


```C++
IMN_CLOSESTATUSWINDOW
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Impostare su IMN \_ CLOSESTATUSWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo comando non ha alcun valore restituito.

## <a name="remarks"></a>Commenti

Un'applicazione deve elaborare questo comando se visualizza la finestra di stato per l'IME.

La finestra IME chiude la finestra di stato quando elabora questo comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>Imm.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione metodi di input](input-method-manager.md)
</dt> <dt>

[Comandi di Gestione metodi di input](input-method-manager-commands.md)
</dt> <dt>

[**WM \_ IME \_ NOTIFY**](wm-ime-notify.md)
</dt> </dl>

 

 




