---
title: LVM_GETITEM messaggio (Commctrl.h)
description: Recupera alcuni o tutti gli attributi di un elemento della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro ListView GetItem.
ms.assetid: 684ad96a-2c3b-4148-b66c-41f8322500bb
keywords:
- LVM_GETITEM di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVM_GETITEM
- LVM_GETITEMA
- LVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05338abce0396c5cc527c8a1c04176b3b59243a684c66a263cb190d59ac68b98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088901"
---
# <a name="lvm_getitem-message"></a>Messaggio \_ LVM GETITEM

Recupera alcuni o tutti gli attributi di un elemento della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ ListView GetItem.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) che specifica le informazioni da recuperare e riceve informazioni sull'elemento della visualizzazione elenco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Quando viene inviato il messaggio **\_ LVM GETITEM,** i membri **iItem** e **iSubItem** identificano l'elemento o l'elemento secondario su cui recuperare le informazioni e il membro **mask** specifica gli attributi da recuperare. Per un elenco dei valori possibili, vedere la descrizione della struttura [**LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema)

Se il flag LVIF TEXT è impostato nel membro mask della struttura \_ [**LVITEM,**](/windows/win32/api/commctrl/ns-commctrl-lvitema) il membro **pszText** deve puntare a un buffer valido e il membro **cchTextMax** deve essere impostato sul numero di caratteri in tale buffer.  Le applicazioni non devono presupporre che il testo verrà necessariamente inserito nel buffer specificato. Il controllo può invece modificare il **membro pszText** della struttura in modo che punti al nuovo testo, anziché posizionarlo nel buffer.

Se il **membro mask** specifica il valore LVIF STATE, il membro stateMask deve specificare i bit di \_ stato dell'elemento da  recuperare. Nell'output, **il** membro di stato contiene i valori dei bit di stato specificati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVM \_ GETITEMW** (Unicode) e **LVM \_ GETITEMA** (ANSI)<br/>                   |



 

 





