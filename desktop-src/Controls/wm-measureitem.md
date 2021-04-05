---
title: Messaggio WM_MEASUREITEM (winuser. h)
description: Inviato alla finestra proprietaria di una casella combinata, una casella di riepilogo, un controllo visualizzazione elenco o una voce di menu quando viene creato il controllo o il menu.
ms.assetid: 6947bcd1-fd40-4238-b8f2-d4e06b90c0dc
keywords:
- Controlli di Windows Message WM_MEASUREITEM
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
ms.openlocfilehash: 43e14cc0c39e1d319fb9190f8ad7d51ea25f821c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874105"
---
# <a name="wm_measureitem-message"></a>\_Messaggio MeasureItem WM

Inviato alla finestra proprietaria di una casella combinata, una casella di riepilogo, un controllo visualizzazione elenco o una voce di menu quando viene creato il controllo o il menu.

Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_MEASUREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene il valore del membro **CtlID** della struttura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) a cui punta il parametro *lParam* . Questo valore identifica il controllo che ha inviato il messaggio **WM \_ MeasureItem** . Se il valore è zero, il messaggio è stato inviato da un menu. Se il valore è diverso da zero, il messaggio è stato inviato da una casella combinata o da una casella di riepilogo. Se il valore è diverso da zero e il valore del membro **ItemId** di **MEASUREITEMSTRUCT** a cui punta *lParam* è (uint) 1, il messaggio è stato inviato da un campo di modifica combinata.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) che contiene le dimensioni del controllo creato dal proprietario o della voce di menu.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire **true**.

## <a name="remarks"></a>Commenti

Quando la finestra proprietaria riceve il messaggio **WM \_ MeasureItem** , il proprietario compila la struttura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) a cui punta il parametro *lParam* del messaggio e restituisce; in questo modo si informa il sistema delle dimensioni del controllo. Se viene creata una casella di riepilogo o una casella combinata con lo stile [**\_ OwnerDrawVariable**](list-box-styles.md) o [**CBS \_ OwnerDrawVariable**](combo-box-styles.md) , questo messaggio viene inviato al proprietario per ogni elemento nel controllo. in caso contrario, il messaggio viene inviato una sola volta.

Il sistema invia il messaggio **WM \_ MeasureItem** alla finestra proprietaria di caselle combinate e caselle di riepilogo create con lo stile OwnerDrawFixed prima di inviare il messaggio [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) . Di conseguenza, quando il proprietario riceve questo messaggio, il sistema non ha ancora determinato l'altezza e la larghezza del tipo di carattere utilizzato nel controllo; le chiamate di funzione e i calcoli che richiedono questi valori devono verificarsi nella funzione principale dell'applicazione o della libreria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**\_INITDIALOG WM**](/windows/desktop/dlgbox/wm-initdialog)
</dt> </dl>

 

