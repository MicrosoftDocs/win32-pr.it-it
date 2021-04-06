---
description: Imposta il testo di una finestra.
ms.assetid: 1b48c309-6903-4139-bf42-e8526963e681
title: Messaggio WM_SETTEXT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3284855d817d5207b0d7572a41774e961c0113f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759494"
---
# <a name="wm_settext-message"></a>\_Messaggio di testo WM

Imposta il testo di una finestra.


```C++
#define WM_SETTEXT                      0x000C
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una stringa con terminazione null che rappresenta il testo della finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Il valore restituito è **true** se il testo è impostato. È **false** (per un controllo di modifica), **lb \_ ERRSPACE** (per una casella di riepilogo) o **CB \_ ERRSPACE** (per una casella combinata) se è disponibile spazio insufficiente per impostare il testo nel controllo di modifica. È **CB \_ Err** se questo messaggio viene inviato a una casella combinata senza un controllo di modifica.

## <a name="remarks"></a>Commenti

La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) imposta e visualizza il testo della finestra. Per un controllo di modifica, il testo è il contenuto del controllo di modifica. Per una casella combinata, il testo è il contenuto della parte relativa al controllo di modifica della casella combinata. Per un pulsante, il testo è il nome del pulsante. Per le altre finestre, il testo è il titolo della finestra.

Questo messaggio non modifica la selezione corrente nella casella di riepilogo di una casella combinata. Un'applicazione deve usare il messaggio [**CB \_ SELECTSTRING**](../controls/cb-selectstring.md) per selezionare l'elemento in una casella di riepilogo che corrisponde al testo nel controllo di modifica.

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

[**WM \_ GETtext**](wm-gettext.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**CB \_ SELECTSTRING**](../controls/cb-selectstring.md)
</dt> </dl>

 

 
