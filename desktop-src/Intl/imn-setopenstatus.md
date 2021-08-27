---
description: Notifica a un'applicazione quando viene aggiornato lo stato aperto del contesto di input. L'applicazione riceve questo comando tramite il messaggio WM \_ IME \_ NOTIFY con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: cc6fa7f4-b85a-486a-985d-53c071321bd1
title: IMN_SETOPENSTATUS di notifica (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57797210f9c0595a952315ca75858890b1998fe16e49049b3a22fb8ed72a5aea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107041"
---
# <a name="imn_setopenstatus-notification-code"></a>Codice di notifica \_ IMN SETOPENSTATUS

Notifica a un'applicazione quando viene aggiornato lo stato aperto del contesto di input. L'applicazione riceve questo comando tramite il messaggio [**WM \_ IME \_ NOTIFY**](wm-ime-notify.md) con le impostazioni dei parametri, come illustrato di seguito.


```C++
IMN_SETOPENSTATUS
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Impostare su IMN \_ SETOPENSTATUS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo comando non ha alcun valore restituito.

## <a name="remarks"></a>Commenti

L'applicazione può ottenere informazioni sullo stato di apertura usando la [**funzione ImmGetOpenStatus.**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus)

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

[**ImmGetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus)
</dt> <dt>

[**WM \_ IME \_ NOTIFY**](wm-ime-notify.md)
</dt> </dl>

 

 




