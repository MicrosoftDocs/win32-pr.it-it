---
title: Messaggio WM_MENUDRAG (winuser. h)
description: Inviato al proprietario di un menu di trascinamento della selezione quando l'utente trascina una voce di menu.
ms.assetid: 99e8f490-ef1e-4964-a3a1-47030a88f10c
keywords:
- Menu del messaggio WM_MENUDRAG e altre risorse
topic_type:
- apiref
api_name:
- WM_MENUDRAG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67e83c41576a716d292187df4cb08fa803271c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302728"
---
# <a name="wm_menudrag-message"></a>\_Messaggio MENUDRAG WM

Inviato al proprietario di un menu di trascinamento della selezione quando l'utente trascina una voce di menu.


```C++
#define WM_MENUDRAG                     0x0123
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Posizione dell'elemento in cui è iniziata l'operazione di trascinamento.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il menu contenente l'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

L'applicazione deve restituire uno dei valori seguenti.



| Codice/valore restituito                                                                                                                                   | Descrizione                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**MND \_ CONTINUA**</dt> <dt>0</dt> </dl> | Il menu deve rimanere attivo. Se il mouse viene rilasciato, deve essere ignorato.<br/> |
| <dl> <dt>**MND \_ ENDMENU**</dt> <dt>1</dt> </dl>  | Il menu deve terminare.<br/>                                                      |



 

## <a name="remarks"></a>Commenti

L'applicazione può chiamare la funzione [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) in risposta a questo messaggio.

Per creare un menu di trascinamento della selezione, chiamare [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo) con **MNS \_ DragDrop**.

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

[**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Menu](menus.md)
</dt> </dl>

 

