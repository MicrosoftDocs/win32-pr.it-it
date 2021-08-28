---
description: Notifica a un'applicazione quando un IME sta per chiudere la finestra dei candidati. L'applicazione riceve questo comando tramite il messaggio WM \_ IME \_ NOTIFY con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: d96cea0a-1fc4-4ba7-bb96-7e9c0b67ce5b
title: IMN_CLOSECANDIDATE codice di notifica (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dd0a71eac28b2c7dc170724e40c9b4ba6707cd5774145f38efdd791e7ebd8b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107151"
---
# <a name="imn_closecandidate-notification-code"></a>Codice di notifica \_ IMN CLOSECANDIDATE

Notifica a un'applicazione quando un IME sta per chiudere la finestra dei candidati. L'applicazione riceve questo comando tramite il messaggio [**WM \_ IME \_ NOTIFY**](wm-ime-notify.md) con le impostazioni dei parametri, come illustrato di seguito.


```C++
IMN_CLOSECANDIDATE
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Impostare su IMN \_ CLOSECANDIDATE.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Flag dell'elenco di candidati. Ogni bit corrisponde a un elenco di candidati: bit 0 al primo elenco, bit 1 al secondo e così via. Se un bit specificato è 1, la finestra dei candidati corrispondente sta per essere chiusa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo comando non ha alcun valore restituito.

## <a name="remarks"></a>Commenti

Un'applicazione deve elaborare questo comando se visualizza i candidati stessi.

Per impostazione predefinita, la finestra IME elimina una finestra candidata quando elabora questo comando.

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

[**NOTIFICA \_ IME \_ WM**](wm-ime-notify.md)
</dt> </dl>

 

 




