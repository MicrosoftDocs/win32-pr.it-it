---
description: Inviato quando un'applicazione richiede la creazione di una finestra chiamando la funzione CreateWindowEx o CreateWindow.
ms.assetid: d484d0fc-bad0-4fcb-bf4b-37cbc50846ee
title: Messaggio WM_CREATE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37437adbb4df714d7604af59a2abdd11ac9d00a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314871"
---
# <a name="wm_create-message"></a>\_Creazione messaggio WM

Inviato quando un'applicazione richiede la creazione di una finestra chiamando la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) o [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) . Il messaggio viene inviato prima che la funzione restituisca. La routine della finestra della nuova finestra riceve questo messaggio dopo la creazione della finestra, ma prima che la finestra diventi visibile.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_CREATE                       0x0001
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**struttura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) contenente informazioni sulla finestra da creare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se un'applicazione elabora il messaggio, deve restituire zero per continuare la creazione della finestra. Se l'applicazione restituisce-1, la finestra viene distrutta e la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) o [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) restituisce un handle **null** .

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

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**STRUTTURA CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**\_NCCREATE WM**](wm-nccreate.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
