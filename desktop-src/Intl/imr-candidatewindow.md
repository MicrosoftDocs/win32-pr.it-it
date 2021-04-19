---
description: Notfies un'applicazione quando un IME selezionato richiede informazioni sulla finestra candidata. L'applicazione riceve questo comando tramite il \_ \_ messaggio di richiesta IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: 35849290-a5be-406f-82f5-4a7e2af48586
title: Codice di notifica IMR_CANDIDATEWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb905acace27cc9bb04ce2b14dc6a685b7c4f8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311759"
---
# <a name="imr_candidatewindow-notification-code"></a>\_Codice di notifica CANDIDATEWINDOW di IMR

Notfies un'applicazione quando un IME selezionato richiede informazioni sulla finestra candidata. L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ richiesta IME WM**](wm-ime-request.md) con le impostazioni dei parametri, come illustrato di seguito.


```C++
LRESULT IMR_CANDIDATEWINDOW
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Impostare su IMR \_ CANDIDATEWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Puntatore a un buffer contenente una struttura [**Campo CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) . Il membro **dwIndex** contiene l'indice per la finestra candidata a cui si fa riferimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se l'applicazione compila la struttura [**Campo CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) . In caso contrario, il comando restituisce 0.

## <a name="remarks"></a>Commenti

Questo comando può essere inviato dall'IME a una finestra che ha cancellato il \_ flag SHOWUICANDIDATEWINDOW di ISC nel gestore di messaggi di [**contesto di WM \_ IME \_**](wm-ime-setcontext.md) .

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

[**Campo CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[**\_richiesta IME \_ WM**](wm-ime-request.md)
</dt> <dt>

[**\_CONtesting IME WM \_**](wm-ime-setcontext.md)
</dt> </dl>

 

 




