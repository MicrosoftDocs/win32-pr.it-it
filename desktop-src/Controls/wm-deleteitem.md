---
title: WM_DELETEITEM messaggio (Winuser.h)
description: Inviato al proprietario di una casella di riepilogo o di una casella combinata quando la casella di riepilogo o la casella combinata viene eliminata definitivamente o quando gli elementi vengono rimossi dal messaggio \_ LB DELETESTRING, LB \_ RESETCONTENT, CB DELETESTRING o \_ CB \_ RESETCONTENT.
ms.assetid: c3adf8fb-45f2-44f1-8821-6ffa7d76dc78
keywords:
- WM_DELETEITEM di controllo Windows messaggio
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
ms.openlocfilehash: 1f461b63d751822d9a4c602993314bf0677cff754881269ab44458ab17f3a439
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018539"
---
# <a name="wm_deleteitem-message"></a>Messaggio \_ WM DELETEITEM

Inviato al proprietario di una casella di riepilogo o di una casella combinata quando la casella di riepilogo o la casella combinata viene eliminata definitivamente o quando gli elementi vengono rimossi dal messaggio [**LB \_ DELETESTRING**](lb-deletestring.md), [**LB \_ RESETCONTENT**](lb-resetcontent.md), [**CB \_ DELETESTRING**](cb-deletestring.md)o [**CB \_ RESETCONTENT.**](cb-resetcontent.md) Il sistema invia un **messaggio \_ DELETEITEM WM** per ogni elemento eliminato. Il sistema invia il messaggio **WM \_ DELETEITEM** per qualsiasi casella di riepilogo o elemento della casella combinata eliminato con dati diversi da zero.


```C++
WM_DELETEITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'identificatore del controllo che ha inviato il **messaggio \_ DELETEITEM WM.**

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) che contiene informazioni sull'elemento eliminato da una casella di riepilogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve **restituire TRUE** se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Microsoft Windows NT e versioni successive: Windows invia un messaggio **\_ DELETEITEM WM** solo per gli elementi eliminati da una casella di riepilogo disegnata dal proprietario (con lo stile [**LBS \_ OWNERDRAWFIXED**](list-box-styles.md) o [**LBS \_ OWNERDRAWVARIABLE)**](list-box-styles.md) o da una casella combinata disegnata dal proprietario (con lo stile [**CBS \_ OWNERDRAWFIXED**](combo-box-styles.md) o [**CBS \_ OWNERDRAWVARIABLE).**](combo-box-styles.md)

Windows 95: Windows invia il messaggio **\_ DELETEITEM WM** per qualsiasi elemento di casella di riepilogo o casella combinata eliminato con dati di elemento diversi da zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**CB \_ DELETESTRING**](cb-deletestring.md)
</dt> <dt>

[**CB \_ RESETCONTENT**](cb-resetcontent.md)
</dt> <dt>

[**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct)
</dt> <dt>

[**LB \_ DELETESTRING**](lb-deletestring.md)
</dt> <dt>

[**LB \_ RESETCONTENT**](lb-resetcontent.md)
</dt> </dl>

 

 





