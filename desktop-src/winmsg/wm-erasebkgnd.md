---
description: Inviato quando lo sfondo della finestra deve essere cancellato (ad esempio, quando una finestra viene ridimensionata). Il messaggio viene inviato per preparare una parte invalidata di una finestra per il disegno.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8acbe1
title: Messaggio WM_ERASEBKGND (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dccde6ab4efa8a6589fe7d422dd9e1c04e425f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232463"
---
# <a name="wm_erasebkgnd-message"></a>\_Messaggio ERASEBKGND WM

Inviato quando lo sfondo della finestra deve essere cancellato (ad esempio, quando una finestra viene ridimensionata). Il messaggio viene inviato per preparare una parte invalidata di una finestra per il disegno.


```C++
#define WM_ERASEBKGND                   0x0014
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il contesto di dispositivo.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Un'applicazione deve restituire un valore diverso da zero se cancella lo sfondo; in caso contrario, deve restituire zero.

## <a name="remarks"></a>Commenti

La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Cancella lo sfondo utilizzando il pennello di sfondo della classe specificato dal membro **HbrBackground** della struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) . Se **hbrBackground** è **null**, l'applicazione deve elaborare il messaggio **WM \_ ERASEBKGND** e cancellare lo sfondo.

Un'applicazione deve restituire un valore diverso da zero in risposta a **WM \_ ERASEBKGND** se elabora il messaggio e cancella lo sfondo. ciò indica che non è necessaria alcuna ulteriore cancellazione. Se l'applicazione restituisce zero, la finestra rimarrà contrassegnata per la cancellazione. In genere, ciò indica che il membro **fErase** della struttura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) sarà **true**.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Icone](../menurc/icons.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint)
</dt> <dt>

[**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)
</dt> </dl>

 

 
