---
description: Indica a una finestra IME di ottenere la posizione della finestra di stato. Per inviare questo comando, l'applicazione usa il \_ \_ messaggio di controllo IME WM con le impostazioni dei parametri mostrate di seguito.
ms.assetid: 59c7baae-1b8a-4761-9814-31afd8d39691
title: Comando IMC_GETSTATUSWINDOWPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfd17c5787d9ef8c787e62a556afa2f136bd65c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307863"
---
# <a name="imc_getstatuswindowpos-command"></a>\_Comando GETSTATUSWINDOWPOS IMC

Indica a una finestra IME di ottenere la posizione della finestra di stato. Per inviare questo comando, l'applicazione usa il messaggio di [**\_ \_ controllo IME WM**](wm-ime-control.md) con le impostazioni dei parametri mostrate di seguito.


```C++
LRESULT IMC_GETSTATUSWINDOWPOS
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Impostare su IMC \_ GETSTATUSWINDOWPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) che contiene la coordinata x e la coordinata y della posizione della finestra di stato nelle coordinate dello schermo, rispetto all'angolo superiore sinistro dello schermo.

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

 

 
