---
description: Notifica a un'applicazione il completamento dell'elaborazione del candidato e l'IME sta per spostare la finestra candidata. L'applicazione riceve questo comando tramite il \_ \_ messaggio di notifica dell'IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: 64252d88-130b-44c3-854a-78b01def7a13
title: Codice di notifica IMN_SETCANDIDATEPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03171a76ce94572d2425f8e75f1cbe45b7efe4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312863"
---
# <a name="imn_setcandidatepos-notification-code"></a>\_Codice di notifica SETCANDIDATEPOS di IMN

Notifica a un'applicazione il completamento dell'elaborazione del candidato e l'IME sta per spostare la finestra candidata. L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ notifica dell'IME WM**](wm-ime-notify.md) con le impostazioni dei parametri, come illustrato di seguito.


```C++
IMN_SETCANDIDATEPOS
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Impostare su IMN \_ SETCANDIDATEPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Flag elenco candidati. Ogni bit corrisponde a un elenco di candidati: bit 0 per il primo elenco, bit 1 al secondo e così via. Se un bit specificato è 1, la finestra candidata corrispondente sta per essere spostata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo comando non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Un'applicazione deve elaborare questo comando se Visualizza la finestra candidata.

La finestra IME sposta la finestra candidata durante l'elaborazione del comando.

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

 

 




