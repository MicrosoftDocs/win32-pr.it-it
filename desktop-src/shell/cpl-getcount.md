---
description: Inviato alla funzione CPlApplet di un'applicazione del pannello di controllo per recuperare il numero di finestre di dialogo supportate dall'applicazione.
title: Messaggio CPL_GETCOUNT (cpl. h)
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
ms.openlocfilehash: 3bf8980fa29841d3c5341daeeccf26cea05db80c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525392"
---
# <a name="cpl_getcount-message"></a>\_Messaggio cpl GETcount

Inviato alla funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) di un'applicazione del pannello di controllo per recuperare il numero di finestre di dialogo supportate dall'applicazione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) restituisce il numero di finestre di dialogo supportate dall'applicazione del pannello di controllo.

## <a name="remarks"></a>Commenti

Questo messaggio viene inviato immediatamente dopo il messaggio [**cpl \_ init**](cpl-init.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                      |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Cpl. h</dt> </dl> |



 

 
