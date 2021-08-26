---
description: Imposta il testo di una finestra.
ms.assetid: 1b48c309-6903-4139-bf42-e8526963e681
title: WM_SETTEXT messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fc2ab860fd89d726b9763c198fe8d58caa1376a3b919fd3587ad39a612d6667
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055981"
---
# <a name="wm_settext-message"></a>Messaggio WM \_ SETTEXT

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

Puntatore a una stringa con terminazione Null che rappresenta il testo della finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Il valore restituito è **TRUE** se il testo è impostato. È **FALSE** (per un controllo di modifica), **LB \_ ERRSPACE** (per una casella di riepilogo) o **CB \_ ERRSPACE** (per una casella combinata) se non è disponibile spazio sufficiente per impostare il testo nel controllo di modifica. È **CB \_ ERR** se questo messaggio viene inviato a una casella combinata senza un controllo di modifica.

## <a name="remarks"></a>Commenti

La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) imposta e visualizza il testo della finestra. Per un controllo di modifica, il testo è il contenuto del controllo di modifica. Per una casella combinata, il testo è il contenuto della parte del controllo di modifica della casella combinata. Per un pulsante, il testo è il nome del pulsante. Per altre finestre, il testo è il titolo della finestra.

Questo messaggio non modifica la selezione corrente nella casella di riepilogo di una casella combinata. Un'applicazione deve usare il [**messaggio \_ CB SELECTSTRING**](../controls/cb-selectstring.md) per selezionare l'elemento in una casella di riepilogo che corrisponde al testo nel controllo di modifica.

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

[**WM \_ GETTEXT**](wm-gettext.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**CB \_ SELECTSTRING**](../controls/cb-selectstring.md)
</dt> </dl>

 

 
