---
title: Messaggio LVM_SETHOTCURSOR (COMmctrl. h)
description: Imposta il valore HCURSOR usato dal controllo di visualizzazione elenco quando il puntatore è posizionato su un elemento mentre è abilitata la funzionalità di rilevamento a caldo.
ms.assetid: e3ff8608-9389-4167-839b-ecc2be01bb64
keywords:
- Controlli di Windows Message LVM_SETHOTCURSOR
topic_type:
- apiref
api_name:
- LVM_SETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e743f74eda3b59f04f6f4793b47d76da3bab881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739946"
---
# <a name="lvm_sethotcursor-message"></a>\_Messaggio SETHOTCURSOR LVM

Imposta il valore HCURSOR usato dal controllo di visualizzazione elenco quando il puntatore è posizionato su un elemento mentre è abilitata la funzionalità di rilevamento a caldo. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetHotCursor di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) . Per verificare se è abilitata la funzionalità di rilevamento attivo, chiamare [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il cursore da impostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore HCURSOR che rappresenta il cursore attivo precedente.

## <a name="remarks"></a>Commenti

Un controllo di visualizzazione elenco Usa il rilevamento a caldo e la selezione del passaggio del mouse quando lo stile [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) è impostato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

