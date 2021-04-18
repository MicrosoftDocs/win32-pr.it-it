---
description: Notifica a un'applicazione quando un IME sta per chiudere la finestra candidati. L'applicazione riceve questo comando tramite il \_ \_ messaggio di notifica dell'IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: d96cea0a-1fc4-4ba7-bb96-7e9c0b67ce5b
title: Codice di notifica IMN_CLOSECANDIDATE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3414d2aa37a50b7f35f0dfb936b641b7c86a932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312871"
---
# <a name="imn_closecandidate-notification-code"></a>\_Codice di notifica CLOSECANDIDATE di IMN

Notifica a un'applicazione quando un IME sta per chiudere la finestra candidati. L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ notifica dell'IME WM**](wm-ime-notify.md) con le impostazioni dei parametri, come illustrato di seguito.


```C++
IMN_CLOSECANDIDATE
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Impostare su IMN \_ CLOSECANDIDATE.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Flag elenco candidati. Ogni bit corrisponde a un elenco di candidati: bit 0 per il primo elenco, bit 1 al secondo e così via. Se un bit specificato è 1, la finestra candidati corrispondente sta per essere chiusa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo comando non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Un'applicazione deve elaborare questo comando se Visualizza i candidati stessi.

Per impostazione predefinita, la finestra IME Elimina una finestra candidata durante l'elaborazione del comando.

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

[**\_notifica IME \_ WM**](wm-ime-notify.md)
</dt> </dl>

 

 




