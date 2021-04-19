---
description: Notifica a un'applicazione quando un IME selezionato richiede informazioni sul tipo di carattere utilizzato dalla finestra di composizione. L'applicazione riceve questo comando tramite il \_ \_ messaggio di richiesta IME WM con i parametri, come illustrato di seguito.
ms.assetid: 46bb71ee-8dc9-4ef0-bc4e-59866c122bf7
title: Codice di notifica IMR_COMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be2751944e451475fd0bde9a34d8902dcaf30e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311758"
---
# <a name="imr_compositionfont-notification-code"></a>\_Codice di notifica COMPOSITIONFONT di IMR

Notifica a un'applicazione quando un IME selezionato richiede informazioni sul tipo di carattere utilizzato dalla finestra di composizione. L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ richiesta IME WM**](wm-ime-request.md) con i parametri, come illustrato di seguito.


```C++
LRESULT IMR_COMPOSITIONFONT
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Impostare su IMR \_ COMPOSITIONFONT.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Puntatore a un buffer contenente una struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) . L'applicazione compila i valori per la finestra di composizione corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se l'applicazione compila la struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) . In caso contrario, il comando restituisce 0.

## <a name="remarks"></a>Commenti

Questo comando può essere inviato dall'IME a una finestra che ha cancellato il \_ flag SHOWUICOMPOSITIONWINDOW di ISC nel gestore di messaggi di [**contesto di WM \_ IME \_**](wm-ime-setcontext.md) .

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

[**\_richiesta IME \_ WM**](wm-ime-request.md)
</dt> <dt>

[**\_CONtesting IME WM \_**](wm-ime-setcontext.md)
</dt> </dl>

 

 
