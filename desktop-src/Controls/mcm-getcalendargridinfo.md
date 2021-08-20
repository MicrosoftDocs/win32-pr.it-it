---
title: MCM_GETCALENDARGRIDINFO messaggio (Commctrl.h)
description: Ottiene informazioni su una griglia del calendario.
ms.assetid: 6b385362-f963-4041-bc9f-d2b7a890c9b4
keywords:
- MCM_GETCALENDARGRIDINFO di controllo Windows messaggio
topic_type:
- apiref
api_name:
- MCM_GETCALENDARGRIDINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26365b940b17617b1f00b93697fc78fa759dd2599d3398ccb8d92725159a70cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170168"
---
# <a name="mcm_getcalendargridinfo-message"></a>Messaggio \_ MCM GETCALENDARGRIDINFO

Ottiene informazioni su una griglia del calendario.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura MCGRIDINFO**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo) che contiene informazioni sulla griglia del calendario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**TRUE in** caso di esito positivo; in **caso contrario, FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





