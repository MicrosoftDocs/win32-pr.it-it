---
description: Inviato a un'icona quando l'utente richiede che la finestra venga ripristinata alle dimensioni e alla posizione precedenti.
ms.assetid: 6e14d5fd-6598-4d2e-a463-2b153c9c2aa3
title: Messaggio WM_QUERYOPEN (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 582fcfce280c0bf98fdf92234b7fab8aaa103a91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104050035"
---
# <a name="wm_queryopen-message"></a>\_Messaggio QUERYOPEN WM

Inviato a un'icona quando l'utente richiede che la finestra venga ripristinata alle dimensioni e alla posizione precedenti.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_QUERYOPEN                    0x0013
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se è possibile aprire l'icona, un'applicazione che elabora questo messaggio deve restituire **true**. in caso contrario, deve restituire **false** per impedire l'apertura dell'icona.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce **true**.

Durante l'elaborazione di questo messaggio, l'applicazione non deve eseguire alcuna azione che comporterebbe una modifica dell'attivazione o dello stato attivo (ad esempio, la creazione di una finestra di dialogo).

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

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
