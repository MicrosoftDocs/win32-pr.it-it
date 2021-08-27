---
description: Notifica a un'applicazione quando l'elaborazione candidata è terminata e l'IME sta per spostare la finestra candidata. L'applicazione riceve questo comando tramite il messaggio WM \_ IME \_ NOTIFY con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: 64252d88-130b-44c3-854a-78b01def7a13
title: IMN_SETCANDIDATEPOS di notifica (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 689dfe0c38f5508c853af94e271bb1f333bfbad0df18b3fab09450d73497e7fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107061"
---
# <a name="imn_setcandidatepos-notification-code"></a>Codice di \_ notifica IMN SETCANDIDATEPOS

Notifica a un'applicazione quando l'elaborazione candidata è terminata e l'IME sta per spostare la finestra candidata. L'applicazione riceve questo comando tramite il messaggio [**WM \_ IME \_ NOTIFY**](wm-ime-notify.md) con le impostazioni dei parametri, come illustrato di seguito.


```C++
IMN_SETCANDIDATEPOS
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Impostare su IMN \_ SETCANDIDATEPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Flag dell'elenco di candidati. Ogni bit corrisponde a un elenco di candidati: bit 0 al primo elenco, bit 1 al secondo e così via. Se un bit specificato è 1, la finestra candidata corrispondente sta per essere spostata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo comando non ha alcun valore restituito.

## <a name="remarks"></a>Commenti

Un'applicazione deve elaborare questo comando se visualizza la finestra candidata stessa.

La finestra IME sposta la finestra candidata quando elabora questo comando.

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

[**WM \_ IME \_ NOTIFY**](wm-ime-notify.md)
</dt> </dl>

 

 




