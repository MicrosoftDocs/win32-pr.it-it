---
description: Notifica a un'applicazione quando viene aggiornato lo stile o la posizione della finestra di composizione. L'applicazione riceve questo comando tramite il messaggio WM \_ IME \_ NOTIFY con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: 07a9f0f6-587e-47c6-8f18-b48bdab0a541
title: IMN_SETCOMPOSITIONWINDOW di notifica (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fed8e69c03250166e155b07d34a2ce19b5d5fd9336af6cf82133c258c2b88d46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107051"
---
# <a name="imn_setcompositionwindow-notification-code"></a>Codice di notifica \_ IMN SETCOMPOSITIONWINDOW

Notifica a un'applicazione quando viene aggiornato lo stile o la posizione della finestra di composizione. L'applicazione riceve questo comando tramite il [**messaggio WM \_ IME \_ NOTIFY**](wm-ime-notify.md) con le impostazioni dei parametri, come illustrato di seguito.


```C++
IMN_SETCOMPOSITIONWINDOW
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Impostare su IMN \_ SETCOMPOSITIONWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo comando non ha alcun valore restituito.

## <a name="remarks"></a>Commenti

L'applicazione può ottenere informazioni sul modulo di composizione usando il [**comando IMC \_ GETCOMPOSITIONWINDOW.**](imc-getcompositionwindow.md)

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

[**IMC \_ GETCOMPOSITIONWINDOW**](imc-getcompositionwindow.md)
</dt> <dt>

[**NOTIFICA \_ IME \_ WM**](wm-ime-notify.md)
</dt> </dl>

 

 




