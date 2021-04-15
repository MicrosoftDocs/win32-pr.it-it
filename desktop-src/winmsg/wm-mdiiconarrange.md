---
description: Un'applicazione invia il \_ messaggio WM MDIICONARRANGE a una finestra del client di interfaccia a documenti multipli (MDI) per disporre tutte le finestre figlio MDI ridotte a icona. Non influisce sulle finestre figlio non ridotte a icona.
ms.assetid: 935b9e29-224d-449e-b89f-b6062bed7702
title: Messaggio WM_MDIICONARRANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2d50d4bccebe3e9758752cc7d0d259e973875c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484756"
---
# <a name="wm_mdiiconarrange-message"></a>\_Messaggio MDIICONARRANGE WM

Un'applicazione invia il messaggio **WM \_ MDIICONARRANGE** a una finestra del client di interfaccia a documenti multipli (MDI) per disporre tutte le finestre figlio MDI ridotte a icona. Non influisce sulle finestre figlio non ridotte a icona.


```C++
#define WM_MDIICONARRANGE               0x0228
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_MDICASCADE WM**](wm-mdicascade.md)
</dt> <dt>

[**\_MDITILE WM**](wm-mditile.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Interfaccia a documenti multipli](multiple-document-interface.md)
</dt> </dl>

 

 




