---
description: Un'applicazione invia il \_ messaggio WM MDIGETACTIVE a una finestra del client di interfaccia a documenti multipli (MDI) per recuperare l'handle per la finestra figlio MDI attiva.
ms.assetid: 3ee445be-dd55-4825-8508-fa18a346ffcd
title: Messaggio WM_MDIGETACTIVE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c49f4ec321f526cd4c9766555e2361ef2cfbd040
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314860"
---
# <a name="wm_mdigetactive-message"></a>\_Messaggio MDIGETACTIVE WM

Un'applicazione invia il messaggio **WM \_ MDIGETACTIVE** a una finestra del client di interfaccia a documenti multipli (MDI) per recuperare l'handle per la finestra figlio MDI attiva.


```C++
#define WM_MDIGETACTIVE                  0x0229
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Stato ingrandito. Se questo parametro non è **null**, è un puntatore a un valore che indica lo stato ingrandito della finestra figlio MDI. Se il valore è **true**, la finestra è ingrandita; il valore **false** indica che non lo è. Se questo parametro è **null**, il parametro viene ignorato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HWND**

Il valore restituito è l'handle per la finestra figlio MDI attiva.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica dell'interfaccia a più documenti](multiple-document-interface.md)
</dt> </dl>

 

 




