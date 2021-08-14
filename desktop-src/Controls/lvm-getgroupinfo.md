---
title: LVM_GETGROUPINFO messaggio (Commctrl.h)
description: Ottiene informazioni sui gruppi.
ms.assetid: 72d84e0b-121e-473b-a34d-874234c598b6
keywords:
- LVM_GETGROUPINFO controlli Windows messaggio
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5c48a21a1bba0c6dd1af3fd567ea853dc922591c553ea11a935fb705ad65bf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411395"
---
# <a name="lvm_getgroupinfo-message"></a>Messaggio \_ LVM GETGROUPINFO

Ottiene informazioni sui gruppi.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>ID che specifica il gruppo di cui vengono recuperate le informazioni.</dd> <dt>

*lParam* 
</dt> <dd>Puntatore a <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**una struttura LVGROUP**</a> che riceve le informazioni recuperate. Impostare il **membro cbSize** di questa struttura su sizeof(LVGROUP). </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'ID del gruppo in caso di esito positivo oppure -1 in caso contrario.

## <a name="remarks"></a>Commenti

Prima di tentare di recuperare l'intestazione per un gruppo, assicurarsi che il gruppo non abbia lo stile \_ LBGS NOHEADER.

> [!Note]  
> Per usare questo messaggio, è necessario fornire un manifesto che specifica Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





