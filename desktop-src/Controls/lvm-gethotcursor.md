---
title: Messaggio LVM_GETHOTCURSOR (COMmctrl. h)
description: Recupera il valore HCURSOR utilizzato quando il puntatore è posizionato su un elemento mentre è abilitata la funzionalità di rilevamento a caldo. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetHotCursor di ListView.
ms.assetid: 064d04b2-d74e-4a80-aec6-97a3c53fc4fb
keywords:
- Controlli di Windows Message LVM_GETHOTCURSOR
topic_type:
- apiref
api_name:
- LVM_GETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddd8fa4c038bf2fb1c10816319504dd9de32c0e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743007"
---
# <a name="lvm_gethotcursor-message"></a>\_Messaggio GETHOTCURSOR LVM

Recupera il valore HCURSOR utilizzato quando il puntatore è posizionato su un elemento mentre è abilitata la funzionalità di rilevamento a caldo. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetHotCursor di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotcursor) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore HCURSOR che rappresenta l'handle del cursore utilizzato dal controllo elenco-visualizzazione quando è abilitata la funzionalità di rilevamento a caldo.

## <a name="remarks"></a>Commenti

Un controllo di visualizzazione elenco Usa il rilevamento a caldo e la selezione del passaggio del mouse quando lo stile [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) è impostato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





