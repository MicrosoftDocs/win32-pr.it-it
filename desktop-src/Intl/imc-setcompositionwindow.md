---
description: Indica a una finestra IME di impostare lo stile della finestra di composizione. Per inviare questo comando, l'applicazione usa il \_ \_ messaggio di controllo IME WM con le impostazioni dei parametri mostrate di seguito.
ms.assetid: 19b99228-a1fc-4cd5-8f37-5462bf767f85
title: Comando IMC_SETCOMPOSITIONWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b06c53b1ff2ec343d6382dd48d0d4108cf403c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307862"
---
# <a name="imc_setcompositionwindow-command"></a>\_Comando SETCOMPOSITIONWINDOW IMC

Indica a una finestra IME di impostare lo stile della finestra di composizione. Per inviare questo comando, l'applicazione usa il messaggio di [**\_ \_ controllo IME WM**](wm-ime-control.md) con le impostazioni dei parametri mostrate di seguito.


```C++
LRESULT IMC_SETCOMPOSITIONWINDOW
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Impostare su IMC \_ SETCOMPOSITIONWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Puntatore a una struttura [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) che contiene le informazioni sullo stile.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 se ha esito positivo o un valore diverso da zero. in caso contrario,.

## <a name="remarks"></a>Commenti

Questo comando imposta lo stile nel contesto di input corrente e lo stile viene applicato successivamente a ogni finestra IME che riceve il contesto di input.

Per impostazione predefinita, la finestra IME presenta lo \_ stile punto di CFS. Con questo stile, la finestra IME usa la posizione corrente del cursore e l'area client della finestra quando viene aperta una finestra di composizione.

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

[**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[**\_controllo IME \_ WM**](wm-ime-control.md)
</dt> </dl>

 

 




