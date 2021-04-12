---
title: Messaggio LVM_SUBITEMHITTEST (COMmctrl. h)
description: Determina quale elemento della visualizzazione elenco o elemento secondario si trova in una posizione specificata. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SubItemHitTest di ListView.
ms.assetid: 1468febb-af0d-4c04-b0b1-cda5ec77aa2c
keywords:
- Controlli di Windows Message LVM_SUBITEMHITTEST
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
ms.openlocfilehash: c811a3ed85b9eb157920f700b34d5d9c99597e67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475365"
---
# <a name="lvm_subitemhittest-message"></a>\_Messaggio SUBITEMHITTEST LVM

Determina quale elemento della visualizzazione elenco o elemento secondario si trova in una posizione specificata. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SubItemHitTest di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere 0. **Windows Vista.** Deve essere-1 se è necessario recuperare il membro **iGROUP** di *lParam* .</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) . La struttura di [**punti**](/previous-versions//dd162805(v=vs.85)) all'interno di **LVHITTESTINFO** deve essere impostata sulle coordinate client da sottoporre a hit test.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento o del sottoelemento testato, se presente, oppure-1 in caso contrario. Se un elemento o un elemento secondario si trova in corrispondenza delle coordinate specificate, i campi della struttura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) verranno riempiti con le informazioni di hit applicabili.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

