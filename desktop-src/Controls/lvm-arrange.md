---
title: LVM_ARRANGE messaggio (Commctrl.h)
description: Dispone gli elementi nella visualizzazione icona. Puoi inviare questo messaggio in modo esplicito o usando la macro Arrange \_ di ListView.
ms.assetid: f7dbcdd2-3cc9-4bae-827e-8bac3b49486c
keywords:
- LVM_ARRANGE di controllo Windows messaggio
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
ms.openlocfilehash: 98d7e3595c276815af8708a54d6e81c2a40192d8d07e6cbce514481723799d04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062651"
---
# <a name="lvm_arrange-message"></a>Messaggio ARRANGE di \_ LVM

Dispone gli elementi nella visualizzazione icona. Puoi inviare questo messaggio in modo esplicito o usando la macro [**Arrange \_ di ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Uno dei valori seguenti che specifica l'allineamento:



| Valore                                                                                                                                                            | Significato                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span id="LVA_ALIGNLEFT"></span><span id="lva_alignleft"></span><dl> <dt>**LVA \_ ALIGNLEFT**</dt> </dl>    | Non implementato. Applicare invece [**lo stile LVS \_ ALIGNLEFT.**](list-view-window-styles.md)<br/> |
| <span id="LVA_ALIGNTOP"></span><span id="lva_aligntop"></span><dl> <dt>**LVA \_ ALIGNTOP**</dt> </dl>       | Non implementato. Applicare invece [**lo stile LVS \_ ALIGNTOP.**](list-view-window-styles.md)<br/>   |
| <span id="LVA_DEFAULT"></span><span id="lva_default"></span><dl> <dt>**LVA \_ DEFAULT**</dt> </dl>          | Allinea gli elementi in base agli stili di allineamento correnti del controllo visualizzazione elenco (valore predefinito).<br/>           |
| <span id="LVA_SNAPTOGRID"></span><span id="lva_snaptogrid"></span><dl> <dt>**LVA \_ SNAPTOGRID**</dt> </dl> | Blocca tutte le icone alla posizione della griglia più vicina.<br/>                                                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo. in caso contrario, **FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





