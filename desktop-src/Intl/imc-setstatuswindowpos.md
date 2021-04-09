---
description: Indica a una finestra IME di impostare la posizione della finestra di stato. Per inviare questo comando, l'applicazione usa il \_ \_ messaggio di controllo IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: d77de7ab-1fbc-42f4-829e-e9fb51668d21
title: Comando IMC_SETSTATUSWINDOWPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99c57eef1a4748bb58018ee47aaee21eb677016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049561"
---
# <a name="imc_setstatuswindowpos-command"></a>\_Comando SETSTATUSWINDOWPOS IMC

Indica a una finestra IME di impostare la posizione della finestra di stato. Per inviare questo comando, l'applicazione usa il messaggio di [**\_ \_ controllo IME WM**](wm-ime-control.md) con le impostazioni dei parametri, come illustrato di seguito.


```C++
LRESULT IMC_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Impostare su IMC \_ SETSTATUSWINDOWPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Puntatore a una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) che contiene la coordinata x e la coordinata y della posizione della finestra di stato. Le coordinate sono espresse in coordinate dello schermo, rispetto all'angolo superiore sinistro della visualizzazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 se ha esito positivo o un valore diverso da zero. in caso contrario,.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>Imm. h (Includi Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione metodo di input](input-method-manager.md)
</dt> <dt>

[Comandi di input Method Manager](input-method-manager-commands.md)
</dt> <dt>

[**\_controllo IME \_ WM**](wm-ime-control.md)
</dt> </dl>

 

 
