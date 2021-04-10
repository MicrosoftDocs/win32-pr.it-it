---
title: Messaggio LVM_SETEXTENDEDLISTVIEWSTYLE (COMmctrl. h)
description: Imposta gli stili estesi nei controlli visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro ListView SetExtendedListViewStyle o ListView \_ SetExtendedListViewStyleEx.
ms.assetid: eb3f47ed-484a-49a8-94b0-e50ee081bd69
keywords:
- Controlli di Windows Message LVM_SETEXTENDEDLISTVIEWSTYLE
topic_type:
- apiref
api_name:
- LVM_SETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7d36869283d863bef7b31187a002125c9cd79bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963765"
---
# <a name="lvm_setextendedlistviewstyle-message"></a>\_Messaggio SETEXTENDEDLISTVIEWSTYLE LVM

Imposta gli stili estesi nei controlli visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la macro [**ListView \_ SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) o [**ListView \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore **DWORD** che specifica quali stili in *lParam* devono essere interessati. Questo parametro può essere una combinazione di [**stili di List-View estesa**](extended-list-view-styles.md). Solo gli stili estesi in *wParam* verranno modificati. Tutti gli altri stili verranno mantenuti così come sono. Se questo parametro è zero, saranno interessati tutti gli stili in *lParam* .

</dd> <dt>

*lParam* 
</dt> <dd>

Valore **DWORD** che specifica gli stili del controllo visualizzazione elenco esteso da impostare. Questo parametro può essere una combinazione di [**stili di List-View estesa**](extended-list-view-styles.md). Gli stili che non sono impostati, ma che vengono specificati in *wParam*, vengono rimossi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **DWORD** che contiene gli stili del controllo visualizzazione elenco esteso precedente.

## <a name="remarks"></a>Commenti

Il parametro *wParam* consente di modificare uno o più stili estesi senza dover prima recuperare gli stili esistenti. Se ad esempio si passa [**LVS \_ ex \_ FULLROWSELECT**](extended-list-view-styles.md) per *wParam* e 0 per *lParam*, lo stile **LVS \_ ex \_ FULLROWSELECT** verrà cancellato, ma tutti gli altri stili rimarranno invariati.

Per motivi di compatibilità con le versioni precedenti, la macro [**\_ SetExtendedListViewStyle di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) non è stata aggiornata per l'uso di *wParam*. Per usare il valore *wParam* , usare la [**macro \_ SetExtendedListViewStyleEx di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) .

Quando si usa questo messaggio per impostare lo stile della [**\_ \_ casella di controllo LVS ex**](extended-list-view-styles.md) , qualsiasi indice di immagine di stato impostato in precedenza verrà rimosso. Tutte le caselle di controllo verranno inizializzate sullo stato deselezionato. L'indice dell'immagine di stato è contenuto in bit da 12 a 15 del membro di **stato** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





