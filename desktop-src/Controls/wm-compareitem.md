---
title: Messaggio WM_COMPAREITEM (winuser. h)
description: Inviato per determinare la posizione relativa di un nuovo elemento nell'elenco ordinato di una casella combinata creata dal proprietario o di una casella di riepilogo.
ms.assetid: 22882730-9fd6-4b45-a563-d7b00ed26564
keywords:
- Controlli di Windows Message WM_COMPAREITEM
topic_type:
- apiref
api_name:
- WM_COMPAREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f269b90f00e69cce2fb84e6b4efa76e554ad96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475113"
---
# <a name="wm_compareitem-message"></a>\_Messaggio COMPAREITEM WM

Inviato per determinare la posizione relativa di un nuovo elemento nell'elenco ordinato di una casella combinata creata dal proprietario o di una casella di riepilogo. Ogni volta che l'applicazione aggiunge un nuovo elemento, il sistema invia questo messaggio al proprietario di una casella combinata o di una casella di riepilogo creata con lo stile di [**\_ ordinamento**](list-box-styles.md) [**CBS \_ Sort**](combo-box-styles.md) o lbs.


```C++
WM_COMPAREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'identificatore del controllo che ha inviato il messaggio **WM \_ COMPAREITEM** .

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) contenente gli identificatori e i dati forniti dall'applicazione per due elementi nella casella combinata o casella di riepilogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito indica la posizione relativa dei due elementi. Potrebbe trattarsi di uno dei valori indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                                                  |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>**Valore**</dt> </dl> | Significato<br/>                                           |
| <dl> <dt>**-1**</dt> </dl>    | L'elemento 1 precede l'elemento 2 nell'ordinamento.<br/>       |
| <dl> <dt>**0**</dt> </dl>     | Gli elementi 1 e 2 sono equivalenti nell'ordinamento.<br/> |
| <dl> <dt>**1**</dt> </dl>     | L'elemento 1 segue l'elemento 2 nell'ordinamento.<br/>        |



 

## <a name="remarks"></a>Commenti

Quando il proprietario di una casella combinata creata dal proprietario o di una casella di riepilogo riceve questo messaggio, il proprietario restituisce un valore che indica quale elemento specificato dalla struttura [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) verrà visualizzato prima dell'altro. In genere, il sistema invia questo messaggio più volte fino a quando non determina la posizione esatta del nuovo elemento.

Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a un **bool** e restituire direttamente il valore. Il \_ valore DWL MSGRESULT impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.

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

[**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> </dl>

 

