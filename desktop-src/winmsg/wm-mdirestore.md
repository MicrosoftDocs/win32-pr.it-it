---
description: Un'applicazione invia il \_ messaggio WM MDIRESTORE a una finestra del client di interfaccia a documenti multipli (MDI) per ripristinare una finestra figlio MDI dalla dimensione ingrandita o ridotta a icona.
ms.assetid: bb99fda1-9eb5-4307-9326-9a417a046c22
title: Messaggio WM_MDIRESTORE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc2cf36a0b428e1e9003682a5e766f613fd7ba81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306659"
---
# <a name="wm_mdirestore-message"></a>\_Messaggio MDIRESTORE WM

Un'applicazione invia il messaggio **WM \_ MDIRESTORE** a una finestra del client di interfaccia a documenti multipli (MDI) per ripristinare una finestra figlio MDI dalla dimensione ingrandita o ridotta a icona.


```C++
#define WM_MDIRESTORE                   0x0223
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra figlio MDI da ripristinare.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **zero**

Il valore restituito è sempre zero.

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

[**\_MDIMAXIMIZE WM**](wm-mdimaximize.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Interfaccia a documenti multipli](multiple-document-interface.md)
</dt> </dl>

 

 




