---
description: Inviato quando lo sfondo della finestra deve essere cancellato(ad esempio, quando una finestra viene ridimensionata). Il messaggio viene inviato per preparare una parte invalidata di una finestra per il disegno.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8acbe1
title: WM_ERASEBKGND messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c74c3b0d1dd2e31e88715d0668f53676759c27cb986b6549fe9e001ab394579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931781"
---
# <a name="wm_erasebkgnd-message"></a>Messaggio \_ WM ERASEBKGND

Inviato quando lo sfondo della finestra deve essere cancellato(ad esempio, quando una finestra viene ridimensionata). Il messaggio viene inviato per preparare una parte invalidata di una finestra per il disegno.


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

Un'applicazione deve restituire un valore diverso da zero se cancella lo sfondo. In caso contrario, deve restituire zero.

## <a name="remarks"></a>Commenti

La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) cancella lo sfondo usando il pennello di sfondo della classe specificato dal membro **hbrBackground** della [**struttura WNDCLASS.**](/windows/win32/api/winuser/ns-winuser-wndclassa) Se **hbrBackground** è **NULL,** l'applicazione deve elaborare il **messaggio WM \_ ERASEBKGND** e cancellare lo sfondo.

Un'applicazione deve restituire un valore diverso da zero in risposta a **WM \_ ERASEBKGND** se elabora il messaggio e cancella lo sfondo. Ciò indica che non sono necessarie altre cancellazioni. Se l'applicazione restituisce zero, la finestra rimarrà contrassegnata per la cancellazione. In genere, ciò indica che il **membro fErase** della struttura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) sarà **TRUE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



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

[**Beginpaint**](/windows/win32/api/winuser/nf-winuser-beginpaint)
</dt> <dt>

[**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)
</dt> </dl>

 

 
