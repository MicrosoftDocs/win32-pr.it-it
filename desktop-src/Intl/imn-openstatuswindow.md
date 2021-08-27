---
description: Notifica a un'applicazione quando un IME sta per creare la finestra di stato. L'applicazione riceve questo comando tramite il messaggio WM \_ IME \_ NOTIFY con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: bbd85c72-aa78-4e1d-8a7a-490650b2d782
title: IMN_OPENSTATUSWINDOW di notifica (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1726ca2433f450f92ddf7da4752b1a53b23e4176b8f0c6f14d03f6fa279f9daa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107111"
---
# <a name="imn_openstatuswindow-notification-code"></a>Codice di notifica \_ IMN OPENSTATUSWINDOW

Notifica a un'applicazione quando un IME sta per creare la finestra di stato. L'applicazione riceve questo comando tramite il messaggio [**WM \_ IME \_ NOTIFY**](wm-ime-notify.md) con le impostazioni dei parametri, come illustrato di seguito.


```C++
IMN_OPENSTATUSWINDOW
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Impostare su IMN \_ OPENSTATUSWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo comando non ha alcun valore restituito.

## <a name="remarks"></a>Commenti

Un'applicazione elabora questo comando per visualizzare la finestra di stato per l'IME da sola.

La finestra IME crea una finestra di stato quando elabora questo comando e imposta le stringhe da visualizzare nella finestra nel contesto di input. Le applicazioni possono ottenere informazioni sulla finestra di stato usando la [**funzione ImmGetConversionStatus.**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)

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

[**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[**WM \_ IME \_ NOTIFY**](wm-ime-notify.md)
</dt> </dl>

 

 




