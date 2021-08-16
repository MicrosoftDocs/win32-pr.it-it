---
title: LVM_GETEXTENDEDLISTVIEWSTYLE messaggio (Commctrl.h)
description: Ottiene gli stili estesi attualmente in uso per un determinato controllo di visualizzazione elenco. Puoi inviare questo messaggio in modo esplicito o usare la \_ macro ListView GetExtendedListViewStyle.
ms.assetid: 5cfccdb8-a81c-4fa9-a4fa-19cf49bd6ce0
keywords:
- LVM_GETEXTENDEDLISTVIEWSTYLE del messaggio Windows controlli
topic_type:
- apiref
api_name:
- LVM_GETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04b2f83f5a8bd55f01aa84e315512c5ccb1b28b17f196c0199fc417544a6737
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968301"
---
# <a name="lvm_getextendedlistviewstyle-message"></a>Messaggio LVM \_ GETEXTENDEDLISTVIEWSTYLE

Ottiene gli stili estesi attualmente in uso per un determinato controllo di visualizzazione elenco. Puoi inviare questo messaggio in modo esplicito o usare la macro [**\_ ListView GetExtendedListViewStyle.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore DWORD** che rappresenta gli stili attualmente in uso per un determinato controllo di visualizzazione elenco. Questo valore può essere una combinazione di [stili List-View estesi](extended-list-view-styles.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





