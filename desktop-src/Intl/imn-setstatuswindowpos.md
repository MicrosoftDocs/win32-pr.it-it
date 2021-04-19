---
description: Notifica a un'applicazione quando viene aggiornata la posizione della finestra di stato nel contesto di input. L'applicazione riceve questo comando tramite il \_ messaggio di \_ notifica di WM IME con le impostazioni dei parametri come indicato di seguito.
ms.assetid: 15e65aff-67d9-4d1a-a6a7-b921cecb3aec
title: Codice di notifica IMN_SETSTATUSWINDOWPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91d76a962e9cc509a6f9ffaac900b761b868f960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311761"
---
# <a name="imn_setstatuswindowpos-notification-code"></a>\_Codice di notifica SETSTATUSWINDOWPOS di IMN

Notifica a un'applicazione quando viene aggiornata la posizione della finestra di stato nel contesto di input. L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ notifica di WM IME**](wm-ime-notify.md) con le impostazioni dei parametri come indicato di seguito.


```C++
IMN_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Impostare su IMN \_ SETSTATUSWINDOWPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo comando non restituisce alcun valore.

## <a name="remarks"></a>Commenti

L'applicazione può ottenere informazioni sulla posizione della finestra di stato usando il comando [**IMC \_ GETSTATUSWINDOWPOS**](imc-getstatuswindowpos.md) .

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

[**\_GETSTATUSWINDOWPOS IMC**](imc-getstatuswindowpos.md)
</dt> <dt>

[**\_notifica IME \_ WM**](wm-ime-notify.md)
</dt> </dl>

 

 




