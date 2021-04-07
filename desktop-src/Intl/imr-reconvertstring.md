---
description: Notifica a un'applicazione quando per un IME selezionato è necessaria una stringa per la riconversione. L'applicazione riceve questo comando tramite il \_ \_ messaggio di richiesta IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: 82ef20b5-bdfa-4bde-abb4-3d14ae35c116
title: Codice di notifica IMR_RECONVERTSTRING (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cbb1caeedb729b176f116a15e64879d79d519fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881526"
---
# <a name="imr_reconvertstring-notification-code"></a>\_Codice di notifica RECONVERTSTRING di IMR

Notifica a un'applicazione quando per un IME selezionato è necessaria una stringa per la riconversione. L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ richiesta IME WM**](wm-ime-request.md) con le impostazioni dei parametri, come illustrato di seguito.


```C++
LRESULT IMR_RECONVERTSTRING
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Impostare su IMR \_ RECONVERTSTRING.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Puntatore a un buffer contenente la struttura e le stringhe [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la struttura della stringa di riconversione corrente. Se *lParam* è impostato su **null**, l'applicazione restituisce la dimensione per il buffer necessario per mantenere la struttura. Se l'operazione non riesce, il comando restituisce 0.

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

[**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**\_richiesta IME \_ WM**](wm-ime-request.md)
</dt> </dl>

 

 




