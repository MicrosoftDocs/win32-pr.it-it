---
title: WM_MEASUREITEM messaggio (Winuser.h)
description: Inviato alla finestra proprietaria di una casella combinata, una casella di riepilogo, un controllo visualizzazione elenco o una voce di menu quando viene creato il controllo o il menu.
ms.assetid: 6947bcd1-fd40-4238-b8f2-d4e06b90c0dc
keywords:
- WM_MEASUREITEM di controllo Windows messaggio
topic_type:
- apiref
api_name:
- WM_MEASUREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eae57fc163f19edcef6dc924072cd3389146b66e614b61d6f121237e82e1344
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957510"
---
# <a name="wm_measureitem-message"></a>Messaggio \_ WM MEASUREITEM

Inviato alla finestra proprietaria di una casella combinata, una casella di riepilogo, un controllo visualizzazione elenco o una voce di menu quando viene creato il controllo o il menu.

Una finestra riceve questo messaggio tramite la relativa [*funzione WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
WM_MEASUREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene il valore del **membro CtlID** della struttura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) a cui punta il *parametro lParam.* Questo valore identifica il controllo che ha inviato il **messaggio WM \_ MEASUREITEM.** Se il valore è zero, il messaggio è stato inviato da un menu. Se il valore è diverso da zero, il messaggio è stato inviato da una casella combinata o da una casella di riepilogo. Se il valore è diverso da zero e il valore del membro **itemID** di **MEASUREITEMSTRUCT** a cui *punta lParam* è (UINT) 1, il messaggio è stato inviato da un campo di modifica combinato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) che contiene le dimensioni del controllo o della voce di menu disegnata dal proprietario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire **TRUE.**

## <a name="remarks"></a>Commenti

Quando la finestra del proprietario riceve il messaggio **WM \_ MEASUREITEM,** il proprietario compila la struttura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) a cui punta il *parametro lParam* del messaggio e restituisce ; in questo modo il sistema viene informato delle dimensioni del controllo. Se viene creata una casella di riepilogo o una casella combinata con lo stile [**LBS \_ OWNERDRAWVARIABLE**](list-box-styles.md) o [**CBS \_ OWNERDRAWVARIABLE,**](combo-box-styles.md) questo messaggio viene inviato al proprietario per ogni elemento nel controllo. In caso contrario, questo messaggio viene inviato una sola volta.

Il sistema invia il **messaggio WM \_ MEASUREITEM** alla finestra proprietaria delle caselle combinate e delle caselle di riepilogo create con lo stile OWNERDRAWFIXED prima di inviare il [**messaggio WM \_ INITDIALOG.**](/windows/desktop/dlgbox/wm-initdialog) Di conseguenza, quando il proprietario riceve questo messaggio, il sistema non ha ancora determinato l'altezza e la larghezza del tipo di carattere usato nel controllo. Le chiamate di funzione e i calcoli che richiedono questi valori devono verificarsi nella funzione principale dell'applicazione o della libreria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog)
</dt> </dl>

 

