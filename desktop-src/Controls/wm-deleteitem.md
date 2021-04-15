---
title: Messaggio WM_DELETEITEM (winuser. h)
description: Inviato al proprietario di una casella di riepilogo o di una casella combinata quando la casella di riepilogo o la casella combinata viene distrutta o quando gli elementi vengono rimossi dal \_ messaggio lb DELETESTRING, lb \_ ResetContent, CB \_ DELETESTRING o CB \_ ResetContent.
ms.assetid: c3adf8fb-45f2-44f1-8821-6ffa7d76dc78
keywords:
- Controlli di Windows Message WM_DELETEITEM
topic_type:
- apiref
api_name:
- WM_DELETEITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf37f8a367d23353903bd3cda85b573f6884ff2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476474"
---
# <a name="wm_deleteitem-message"></a>\_Messaggio DeleteItem WM

Inviato al proprietario di una casella di riepilogo o di una casella combinata quando la casella di riepilogo o la casella combinata viene distrutta o quando gli elementi vengono rimossi dal messaggio [**lb \_ DELETESTRING**](lb-deletestring.md), [**lb \_ ResetContent**](lb-resetcontent.md), [**CB \_ DELETESTRING**](cb-deletestring.md)o [**CB \_ ResetContent**](cb-resetcontent.md) . Il sistema invia un messaggio **WM \_ DeleteItem** per ogni elemento eliminato. Il sistema invia il messaggio **WM \_ DeleteItem** per qualsiasi casella di riepilogo o casella combinata eliminata con dati di elementi diversi da zero.


```C++
WM_DELETEITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'identificatore del controllo che ha inviato il messaggio **WM \_ DeleteItem** .

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) che contiene informazioni sull'elemento eliminato da una casella di riepilogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire **true** se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Microsoft Windows NT e versioni successive: Windows invia un messaggio **WM \_ DeleteItem** solo per gli elementi eliminati da una casella di riepilogo creata dal proprietario (con lo [**stile \_ OwnerDrawVariable**](list-box-styles.md) [**lbs \_ OwnerDrawFixed**](list-box-styles.md) o lbs) o una casella combinata creata dal proprietario (con lo stile [**CBS \_ OwnerDrawFixed**](combo-box-styles.md) o [**CBS \_ OwnerDrawVariable**](combo-box-styles.md) ).

Windows 95: Windows invia il messaggio **WM \_ DeleteItem** per qualsiasi casella di riepilogo o casella combinata eliminata con dati di elementi diversi da zero.

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

[**CB \_ DELETESTRING**](cb-deletestring.md)
</dt> <dt>

[**CB \_ ResetContent**](cb-resetcontent.md)
</dt> <dt>

[**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct)
</dt> <dt>

[**\_DELETESTRING lb**](lb-deletestring.md)
</dt> <dt>

[**\_ResetContent lb**](lb-resetcontent.md)
</dt> </dl>

 

 





