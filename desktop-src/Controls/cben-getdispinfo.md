---
title: CBEN_GETDISPINFO di notifica (Commctrl.h)
description: Inviato per recuperare le informazioni di visualizzazione su un elemento di callback. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: a181be28-0001-4953-8e59-77aff2dc40be
keywords:
- CBEN_GETDISPINFO codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- CBEN_GETDISPINFO
- CBEN_GETDISPINFOA
- CBEN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 896d282426c11f40fe949c73f44eb963a399c5c210e839198527f9bc903e2fdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413694"
---
# <a name="cben_getdispinfo-notification-code"></a>Codice di \_ notifica GETDISPINFO CBEN

Inviato per recuperare le informazioni di visualizzazione su un elemento di callback. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
CBEN_GETDISPINFO

    pDispInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) che contiene informazioni sul codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

L'applicazione che elabora questo codice di notifica deve restituire zero.

## <a name="remarks"></a>Commenti

La [**struttura NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) contiene una [**struttura COMBOBOXEXITEM.**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) Il **membro mask** specifica le informazioni richieste dal controllo .

Compilare i membri appropriati della struttura per restituire le informazioni richieste al controllo . Se il gestore di messaggi imposta il membro **mask** della struttura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) su CBEIF DI SETITEM, il controllo archivia le informazioni e non \_ le \_ richiederà di nuovo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **CBEN \_ GETDISPINFOW** (Unicode) e **CBEN \_ GETDISPINFOA** (ANSI)<br/>         |



 

 





