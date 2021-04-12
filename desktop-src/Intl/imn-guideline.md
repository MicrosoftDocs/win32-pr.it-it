---
description: Notifica a un'applicazione quando un IME sta per visualizzare un messaggio di errore o altre informazioni. L'applicazione riceve questo comando tramite il \_ \_ messaggio di notifica dell'IME WM con le impostazioni dei parametri, come illustrato di seguito.
ms.assetid: b898283a-af1a-484f-bfb8-e5d5c0ac8ee1
title: Codice di notifica IMN_GUIDELINE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4efc222f7bfceadecce0f14573cab66471b119d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345766"
---
# <a name="imn_guideline-notification-code"></a>\_Codice di notifica linee guida IMN

Notifica a un'applicazione quando un IME sta per visualizzare un messaggio di errore o altre informazioni. L'applicazione riceve questo comando tramite il messaggio di [**\_ \_ notifica dell'IME WM**](wm-ime-notify.md) con le impostazioni dei parametri, come illustrato di seguito.


```C++
IMN_GUIDELINE
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Impostare sulla \_ linea guida IMN.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo comando non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Un'applicazione elabora questo comando chiamando la funzione [**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea) per recuperare il messaggio di errore o le informazioni dall'IME.

Nella finestra IME viene visualizzato il messaggio di errore o la stringa di informazioni in una finestra informazioni.

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

[**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea)
</dt> <dt>

[**\_notifica IME \_ WM**](wm-ime-notify.md)
</dt> </dl>

 

 




