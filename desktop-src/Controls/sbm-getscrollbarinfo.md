---
title: Messaggio SBM_GETSCROLLBARINFO (winuser. h)
description: Inviato da un'applicazione per recuperare informazioni sulla barra di scorrimento specificata.
ms.assetid: db6f704f-99ee-448c-ae7a-dd5a23399fb6
keywords:
- Controlli di Windows Message SBM_GETSCROLLBARINFO
topic_type:
- apiref
api_name:
- SBM_GETSCROLLBARINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8bdd78eb665bd069d854538bb2bdfae1a946765
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741375"
---
# <a name="sbm_getscrollbarinfo-message"></a>\_Messaggio GETSCROLLBARINFO SBM

Inviato da un'applicazione per recuperare informazioni sulla barra di scorrimento specificata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) che riceve le informazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo o zero.

Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

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

[**GetScrollBarInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo)
</dt> <dt>

[**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo)
</dt> </dl>

 

