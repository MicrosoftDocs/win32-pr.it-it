---
description: Un'applicazione invia il messaggio WM MDIGETACTIVE a una finestra \_ client MDI (Multiple-Document Interface) per recuperare l'handle per la finestra figlio MDI attiva.
ms.assetid: 3ee445be-dd55-4825-8508-fa18a346ffcd
title: WM_MDIGETACTIVE messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7716138028f7fe7447cc89d8feded7806f4f8757cd4a18b4bef6f2d812de3f17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200141"
---
# <a name="wm_mdigetactive-message"></a>Messaggio \_ DI WM MDIGETACTIVE

Un'applicazione invia il messaggio **\_ WM MDIGETACTIVE** a una finestra client MDI (Multiple-Document Interface) per recuperare l'handle per la finestra figlio MDI attiva.


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

Stato ingrandito. Se questo parametro non è **NULL,** è un puntatore a un valore che indica lo stato ingrandito della finestra figlio MDI. Se il valore è **TRUE,** la finestra viene ingrandita; il valore **FALSE** indica che non lo è. Se questo parametro è **NULL,** il parametro viene ignorato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HWND**

Il valore restituito è l'handle per la finestra figlio MDI attiva.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica dell'interfaccia a documenti multipli](multiple-document-interface.md)
</dt> </dl>

 

 




