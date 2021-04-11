---
description: Inviato alla finestra in primo piano interessata dopo la modifica della lingua di input di un'applicazione. È necessario apportare le impostazioni specifiche dell'applicazione e passare il messaggio alla funzione DefWindowProc, che passa il messaggio a tutte le finestre figlio di primo livello.
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: Messaggio WM_INPUTLANGCHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0cdf04a775873e4cefe2c79269c14bd3d4da8d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128962"
---
# <a name="wm_inputlangchange-message"></a>\_Messaggio INPUTLANGCHANGE WM

Inviato alla finestra in primo piano interessata dopo la modifica della lingua di input di un'applicazione. È necessario apportare le impostazioni specifiche dell'applicazione e passare il messaggio alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , che passa il messaggio a tutte le finestre figlio di primo livello. Queste finestre figlio possono passare il messaggio a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per passare il messaggio alle finestre figlio e così via.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_INPUTLANGCHANGE              0x0051
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Set di caratteri delle nuove impostazioni locali.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificatore delle impostazioni locali di input. Per altre informazioni, vedere [lingue, impostazioni locali e layout di tastiera](../inputdev/about-keyboard-input.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Un'applicazione deve restituire un valore diverso da zero se elabora questo messaggio.

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

[**\_INPUTLANGCHANGEREQUEST WM**](wm-inputlangchangerequest.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
