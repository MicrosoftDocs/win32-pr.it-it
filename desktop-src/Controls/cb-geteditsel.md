---
title: Messaggio CB_GETEDITSEL (winuser. h)
description: Ottiene le posizioni dei caratteri iniziali e finali della selezione corrente nel controllo di modifica di una casella combinata.
ms.assetid: 72b64135-e35a-4f72-9fc7-e6bedf495f23
keywords:
- Controlli di Windows Message CB_GETEDITSEL
topic_type:
- apiref
api_name:
- CB_GETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 319ce4a3c7a5a61903d4fc3bf04eed223e749787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048361"
---
# <a name="cb_geteditsel-message"></a>\_Messaggio GETEDITSEL CB

Ottiene le posizioni dei caratteri iniziali e finali della selezione corrente nel controllo di modifica di una casella combinata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Puntatore a un valore **DWORD** che riceve la posizione iniziale della selezione. Questo parametro può essere **NULL**.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un valore **DWORD** che riceve la posizione finale della selezione. Questo parametro può essere **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un valore **DWORD** in base zero con la posizione iniziale della selezione in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e con la posizione finale del primo carattere dopo l'ultimo carattere selezionato in [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente vengono illustrati due modi per recuperare l'intervallo di selezione corrente.


```C++
DWORD start, end;

// Get the range from [out] parameters.
// hwnd is the handle of the combo box control.
SendMessage(hwnd, CB_GETEDITSEL, (WPARAM)&start, (LPARAM)&end;

// Get the range from the return value.
DWORD range = SendMessage(hwnd, CB_GETEDITSEL, NULL, NULL);
start = LOWORD(range);
end = HIWORD(range);
```



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

[**CB \_ SETEDITSEL**](cb-seteditsel.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> </dl>

 

