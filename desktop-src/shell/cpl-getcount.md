---
description: Inviato alla funzione CPlApplet di un'Pannello di controllo per recuperare il numero di finestre di dialogo supportate dall'applicazione.
title: CPL_GETCOUNT messaggio (Cpl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6b88b56c-aad7-4144-ab95-15d7eef21861
api_name:
- CPL_GETCOUNT
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 58f95a62d17ccafd308666a5632a1f7a42ebfda6ca0a54dfb6dfa9d9eda9b684
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715481"
---
# <a name="cpl_getcount-message"></a>Messaggio \_ GETCOUNT CPL

Inviato alla funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) di un'Pannello di controllo per recuperare il numero di finestre di dialogo supportate dall'applicazione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

La [**funzione CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) restituisce il numero di finestre di dialogo supportate dall Pannello di controllo applicazione.

## <a name="remarks"></a>Commenti

Questo messaggio viene inviato immediatamente dopo il [**messaggio \_ CPL INIT.**](cpl-init.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                      |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Cpl.h</dt> </dl> |



 

 
