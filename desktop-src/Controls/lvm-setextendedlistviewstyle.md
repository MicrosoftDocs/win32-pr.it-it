---
title: LVM_SETEXTENDEDLISTVIEWSTYLE messaggio (Commctrl.h)
description: Imposta gli stili estesi nei controlli visualizzazione elenco. Puoi inviare questo messaggio in modo esplicito o usare la \_ macro ListView SetExtendedListViewStyle o \_ ListView SetExtendedListViewStyleEx.
ms.assetid: eb3f47ed-484a-49a8-94b0-e50ee081bd69
keywords:
- LVM_SETEXTENDEDLISTVIEWSTYLE dei controlli Windows messaggio
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
ms.openlocfilehash: 336732b927c7ee6170e777f2f7c1cd57eac6baa2c7706870e681f602e2309c37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077281"
---
# <a name="lvm_setextendedlistviewstyle-message"></a>Messaggio LVM \_ SETEXTENDEDLISTVIEWSTYLE

Imposta gli stili estesi nei controlli visualizzazione elenco. Puoi inviare questo messaggio in modo esplicito o usare la macro [**\_ ListView SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) o [**\_ ListView SetExtendedListViewStyleEx.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

**Valore DWORD** che specifica quali stili in *lParam* devono essere interessati. Questo parametro può essere una combinazione di [**stili List-View estesi**](extended-list-view-styles.md). Verranno modificati solo gli stili estesi in *wParam.* Tutti gli altri stili verranno mantenuti così come sono. Se questo parametro è zero, tutti gli stili in *lParam* saranno interessati.

</dd> <dt>

*lParam* 
</dt> <dd>

**Valore DWORD** che specifica gli stili estesi del controllo visualizzazione elenco da impostare. Questo parametro può essere una combinazione di [**stili List-View estesi**](extended-list-view-styles.md). Gli stili non impostati, ma specificati in *wParam*, vengono rimossi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore DWORD** che contiene gli stili dei controlli visualizzazione elenco estesi precedenti.

## <a name="remarks"></a>Commenti

Il *parametro wParam* consente di modificare uno o più stili estesi senza dover prima recuperare gli stili esistenti. Ad esempio, se si passa [**LVS \_ EX \_ FULLROWSELECT**](extended-list-view-styles.md) per *wParam* e 0 per *lParam*, lo stile **LVS \_ EX \_ FULLROWSELECT** verrà cancellato, ma tutti gli altri stili rimarranno invariati.

Per motivi di compatibilità con le versioni precedenti, la macro [**\_ ListView SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) non è stata aggiornata per l'uso *di wParam.* Per usare il *valore wParam,* usa la macro [**\_ ListView SetExtendedListViewStyleEx.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex)

Quando si usa questo messaggio per impostare lo stile [**LVS \_ EX \_ CHECKBOXES,**](extended-list-view-styles.md) qualsiasi indice dell'immagine di stato impostato in precedenza verrà eliminato. Tutte le caselle di controllo verranno inizializzate allo stato deselezionato. L'indice dell'immagine di stato è contenuto nei bit da 12 a 15 del membro **di** stato della [**struttura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





