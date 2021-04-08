---
title: Messaggio LVM_GETEXTENDEDLISTVIEWSTYLE (COMmctrl. h)
description: Ottiene gli stili estesi attualmente in uso per un determinato controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetExtendedListViewStyle di ListView.
ms.assetid: 5cfccdb8-a81c-4fa9-a4fa-19cf49bd6ce0
keywords:
- Controlli di Windows Message LVM_GETEXTENDEDLISTVIEWSTYLE
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
ms.openlocfilehash: 273da9e7eac85475b90ad05dc5fdd7f70d524562
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047859"
---
# <a name="lvm_getextendedlistviewstyle-message"></a>\_Messaggio GETEXTENDEDLISTVIEWSTYLE LVM

Ottiene gli stili estesi attualmente in uso per un determinato controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetExtendedListViewStyle di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore DWORD** che rappresenta gli stili attualmente in uso per un determinato controllo di visualizzazione elenco. Questo valore può essere una combinazione di [stili di List-View estesa](extended-list-view-styles.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





