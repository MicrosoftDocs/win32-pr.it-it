---
title: SBM_GETSCROLLBARINFO messaggio (Winuser.h)
description: Inviato da un'applicazione per recuperare informazioni sulla barra di scorrimento specificata.
ms.assetid: db6f704f-99ee-448c-ae7a-dd5a23399fb6
keywords:
- SBM_GETSCROLLBARINFO dei messaggi Windows
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
ms.openlocfilehash: 11f779f237d0ad04fe3e3d8f3348c51c195470280c9b0c20d12c1e245d04a089
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119503981"
---
# <a name="sbm_getscrollbarinfo-message"></a>Messaggio \_ SBM GETSCROLLBARINFO

Inviato da un'applicazione per recuperare informazioni sulla barra di scorrimento specificata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) che riceve le informazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo o zero in caso contrario.

Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

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

[**GetScrollBarInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo)
</dt> <dt>

[**INFORMAZIONI SULLA BARRA DI SCORRIMENTO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo)
</dt> </dl>

 

