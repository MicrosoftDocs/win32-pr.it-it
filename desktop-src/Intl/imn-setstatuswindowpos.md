---
description: Notifica a un'applicazione quando viene aggiornata la posizione della finestra di stato nel contesto di input. L'applicazione riceve questo comando tramite il messaggio WM \_ IME \_ NOTIFY con le impostazioni dei parametri come indicato di seguito.
ms.assetid: 15e65aff-67d9-4d1a-a6a7-b921cecb3aec
title: IMN_SETSTATUSWINDOWPOS codice di notifica (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0c414de9ba8e75a85d6649d747173c73af274c3527cf9f0dc5b7540a3bf8669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117810128"
---
# <a name="imn_setstatuswindowpos-notification-code"></a>Codice di notifica \_ IMN SETSTATUSWINDOWPOS

Notifica a un'applicazione quando viene aggiornata la posizione della finestra di stato nel contesto di input. L'applicazione riceve questo comando tramite il [**messaggio WM \_ IME \_ NOTIFY**](wm-ime-notify.md) con le impostazioni dei parametri come indicato di seguito.


```C++
IMN_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Impostare su IMN \_ SETSTATUSWINDOWPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo comando non ha alcun valore restituito.

## <a name="remarks"></a>Commenti

L'applicazione può ottenere informazioni sulla posizione della finestra di stato usando il [**comando IMC \_ GETSTATUSWINDOWPOS.**](imc-getstatuswindowpos.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>Imm.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione metodi di input](input-method-manager.md)
</dt> <dt>

[Comandi di Gestione metodi di input](input-method-manager-commands.md)
</dt> <dt>

[**IMC \_ GETSTATUSWINDOWPOS**](imc-getstatuswindowpos.md)
</dt> <dt>

[**NOTIFICA \_ IME \_ WM**](wm-ime-notify.md)
</dt> </dl>

 

 




