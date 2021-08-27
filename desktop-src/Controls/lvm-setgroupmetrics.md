---
title: LVM_SETGROUPMETRICS messaggio (Commctrl.h)
description: Imposta le informazioni sulla visualizzazione dei gruppi.
ms.assetid: 268b478d-da1f-4efe-9ee9-af3f12e089ee
keywords:
- LVM_SETGROUPMETRICS controlli di Windows messaggio
topic_type:
- apiref
api_name:
- LVM_SETGROUPMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32f978c763fd1602d06f921a5da38a895fb1d3c76573341d9ca4f2987a0d3c7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077261"
---
# <a name="lvm_setgroupmetrics-message"></a>Messaggio \_ LVM SETGROUPMETRICS

Imposta le informazioni sulla visualizzazione dei gruppi.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere **NULL.**</dd> <dt>

*lParam* 
</dt> <dd>Puntatore a <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**una struttura LVGROUPMETRICS**</a> che contiene le metriche da impostare.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per usare questo messaggio, è necessario specificare un manifesto Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





