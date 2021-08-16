---
title: LVM_SUBITEMHITTEST messaggio (Commctrl.h)
description: Determina quale elemento o elemento secondario della visualizzazione elenco si trova in una determinata posizione. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro ListView SubItemHitTest.
ms.assetid: 1468febb-af0d-4c04-b0b1-cda5ec77aa2c
keywords:
- LVM_SUBITEMHITTEST dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- LVM_SUBITEMHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 341f9b3f84646abe975c6543aef802450496154862353b7bbdd1af2c07c087ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830642"
---
# <a name="lvm_subitemhittest-message"></a>Messaggio LVM \_ SUBITEMHITTEST

Determina quale elemento o elemento secondario della visualizzazione elenco si trova in una determinata posizione. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView SubItemHitTest.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere 0. **Windows Vista.** Deve essere -1 se il **membro iGroup** di *lParam* deve essere recuperato.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura LVHITTESTINFO.**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) La [**struttura POINT**](/previous-versions//dd162805(v=vs.85)) **all'interno di LVHITTESTINFO** deve essere impostata su coordinate client da testare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento o dell'elemento secondario testato, se presente, oppure -1 in caso contrario. Se un elemento o un elemento secondario si trova in corrispondenza delle coordinate specificate, i campi della struttura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) verranno riempiti con le informazioni di hit applicabili.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

