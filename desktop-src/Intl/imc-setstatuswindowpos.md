---
description: Indica a una finestra IME di impostare la posizione della finestra di stato. Per inviare questo comando, l'applicazione usa il messaggio WM \_ IME \_ CONTROL con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: d77de7ab-1fbc-42f4-829e-e9fb51668d21
title: IMC_SETSTATUSWINDOWPOS comando (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee41deac781f7885185df429c5b5231a36f9d5008b5754b718398e7ab4cd060a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107231"
---
# <a name="imc_setstatuswindowpos-command"></a>Comando \_ IMC SETSTATUSWINDOWPOS

Indica a una finestra IME di impostare la posizione della finestra di stato. Per inviare questo comando, l'applicazione usa il [**messaggio WM \_ IME \_ CONTROL**](wm-ime-control.md) con le impostazioni dei parametri, come illustrato di seguito.


```C++
LRESULT IMC_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Impostare su IMC \_ SETSTATUSWINDOWPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Puntatore a [**una struttura POINTS**](/previous-versions//dd162808(v=vs.85)) contenente la coordinata x e la coordinata y della posizione della finestra di stato. Le coordinate sono in coordinate dello schermo, relative all'angolo superiore sinistro dello schermo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo oppure un valore diverso da zero in caso contrario.

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

[**CONTROLLO \_ IME \_ WM**](wm-ime-control.md)
</dt> </dl>

 

 
