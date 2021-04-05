---
description: Inviato a una finestra quando la dimensione o la posizione della finestra sta per essere modificata. Un'applicazione può utilizzare questo messaggio per eseguire l'override delle dimensioni e della posizione ingrandite predefinite della finestra o della dimensione minima o massima predefinita del rilevamento.
ms.assetid: af2295e0-2d0b-4ac0-b689-16138022f4b7
title: Messaggio WM_GETMINMAXINFO (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29cbca97d38f7fca90c93ef7bf0606ea49306da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883402"
---
# <a name="wm_getminmaxinfo-message"></a>\_Messaggio GETMINMAXINFO WM

Inviato a una finestra quando la dimensione o la posizione della finestra sta per essere modificata. Un'applicazione può utilizzare questo messaggio per eseguire l'override delle dimensioni e della posizione ingrandite predefinite della finestra o della dimensione minima o massima predefinita del rilevamento.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_GETMINMAXINFO                0x0024
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) che contiene la posizione e le dimensioni ingrandite predefinite e le dimensioni minime e massime predefinite del rilevamento. Un'applicazione può eseguire l'override delle impostazioni predefinite impostando i membri della struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

La dimensione massima del rilevamento è la dimensione della finestra più grande che può essere prodotta usando i bordi per ridimensionare la finestra. La dimensione minima del rilevamento è la dimensione minima della finestra che può essere prodotta usando i bordi per ridimensionare la finestra.

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

[**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
