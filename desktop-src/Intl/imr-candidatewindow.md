---
description: Notifica un'applicazione quando un IME selezionato necessita di informazioni sulla finestra candidata. L'applicazione riceve questo comando tramite il messaggio WM \_ IME \_ REQUEST con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: 35849290-a5be-406f-82f5-4a7e2af48586
title: IMR_CANDIDATEWINDOW di notifica (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9376ff08e0406ff5505107ea1a04cf4e62898660065a8c7fdd54a1b8606850c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117810116"
---
# <a name="imr_candidatewindow-notification-code"></a>CODICE DI \_ NOTIFICA IMR CANDIDATEWINDOW

Notifica un'applicazione quando un IME selezionato necessita di informazioni sulla finestra candidata. L'applicazione riceve questo comando tramite il messaggio [**WM \_ IME \_ REQUEST**](wm-ime-request.md) con le impostazioni dei parametri, come illustrato di seguito.


```C++
LRESULT IMR_CANDIDATEWINDOW
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Impostare su IMR \_ CANDIDATEWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Puntatore a un buffer contenente una [**struttura CANDIDATEFORM.**](/windows/win32/api/imm/ns-imm-candidateform) Il **relativo membro dwIndex** contiene l'indice della finestra candidata a cui si fa riferimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se l'applicazione compila la [**struttura CANDIDATEFORM.**](/windows/win32/api/imm/ns-imm-candidateform) In caso contrario, il comando restituisce 0.

## <a name="remarks"></a>Commenti

Questo comando può essere inviato dall'IME a una finestra che ha cancellato il flag ISC SHOWUICANDIDATEWINDOW nel gestore di messaggi \_ [**WM \_ IME \_ SETCONTEXT.**](wm-ime-setcontext.md)

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

[**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[**RICHIESTA \_ IME \_ WM**](wm-ime-request.md)
</dt> <dt>

[**WM \_ IME \_ SETCONTEXT**](wm-ime-setcontext.md)
</dt> </dl>

 

 




