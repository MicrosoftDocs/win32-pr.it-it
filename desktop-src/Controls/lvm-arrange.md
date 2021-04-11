---
title: Messaggio LVM_ARRANGE (COMmctrl. h)
description: Dispone gli elementi nella visualizzazione icone. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro Arrange di ListView.
ms.assetid: f7dbcdd2-3cc9-4bae-827e-8bac3b49486c
keywords:
- Controlli di Windows Message LVM_ARRANGE
topic_type:
- apiref
api_name:
- LVM_ARRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a1b6a081cf963a649329951358ea4c972f200f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119015"
---
# <a name="lvm_arrange-message"></a>\_Messaggio di disposizione LVM

Dispone gli elementi nella visualizzazione icone. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ Arrange di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Uno dei valori seguenti che specifica l'allineamento:



| Valore                                                                                                                                                            | Significato                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span id="LVA_ALIGNLEFT"></span><span id="lva_alignleft"></span><dl> <dt>**\_ALIGNLEFT LVA**</dt> </dl>    | Non implementato. Applicare invece lo stile [**\_ ALIGNLEFT di LVS**](list-view-window-styles.md) .<br/> |
| <span id="LVA_ALIGNTOP"></span><span id="lva_aligntop"></span><dl> <dt>**\_ALIGNTOP LVA**</dt> </dl>       | Non implementato. Applicare invece lo stile [**\_ ALIGNTOP di LVS**](list-view-window-styles.md) .<br/>   |
| <span id="LVA_DEFAULT"></span><span id="lva_default"></span><dl> <dt>**\_impostazione predefinita LVA**</dt> </dl>          | Allinea gli elementi in base agli stili di allineamento correnti del controllo visualizzazione elenco (valore predefinito).<br/>           |
| <span id="LVA_SNAPTOGRID"></span><span id="lva_snaptogrid"></span><dl> <dt>**\_SNAPTOGRID LVA**</dt> </dl> | Blocca tutte le icone nella posizione della griglia più vicina.<br/>                                                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo; in caso contrario, **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





