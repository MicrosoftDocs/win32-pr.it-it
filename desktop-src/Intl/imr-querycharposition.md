---
description: Notifica a un'applicazione quando l'IME selezionato richiede informazioni sulle coordinate di un carattere nella stringa di composizione. L'applicazione riceve questo comando tramite il \_ \_ messaggio di richiesta IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: cae7e5b3-8aaf-452d-80df-fb0ae04a342c
title: Codice di notifica IMR_QUERYCHARPOSITION (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947eec9b3dd1f678d9266bb795214cf392629193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311755"
---
# <a name="imr_querycharposition-notification-code"></a>\_Codice di notifica QUERYCHARPOSITION di IMR

Notifica a un'applicazione quando l'IME selezionato richiede informazioni sulle coordinate di un carattere nella stringa di composizione. L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ richiesta IME WM**](wm-ime-request.md) con le impostazioni dei parametri, come illustrato di seguito.


```C++
LRESULT IMR_QUERYCHARPOSITION
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Impostare su IMR \_ QUERYCHARPOSITION.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Puntatore a una struttura [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) che contiene la posizione del carattere nella finestra di composizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se l'applicazione riempie la struttura [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) . In caso contrario, il comando restituisce 0.

## <a name="remarks"></a>Commenti

Un'applicazione che disegna la stringa di composizione, anziché basarsi sull'IME, è responsabile del riempimento di tutti i membri della struttura [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) . In caso contrario, l'applicazione deve passare il comando a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) o [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea) se dispone di una propria finestra dell'interfaccia utente IME.

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

[**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition)
</dt> <dt>

[**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> <dt>

[**\_richiesta IME \_ WM**](wm-ime-request.md)
</dt> </dl>

 

 
