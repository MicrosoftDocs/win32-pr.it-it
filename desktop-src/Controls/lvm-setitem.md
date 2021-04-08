---
title: Messaggio LVM_SETITEM (COMmctrl. h)
description: Imposta alcuni o tutti gli attributi di un elemento della visualizzazione elenco. È anche possibile inviare \_ l'elemento per impostare il testo di un elemento secondario. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetItem ListView.
ms.assetid: f1189b5d-bce7-4569-b4b9-bd750d7ef505
keywords:
- Controlli di Windows Message LVM_SETITEM
topic_type:
- apiref
api_name:
- LVM_SETITEM
- LVM_SETITEMA
- LVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623339c3d1ecc7a74cf20b5e52fb621666391bd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048127"
---
# <a name="lvm_setitem-message"></a>\_Messaggio SETITEM LVM

Imposta alcuni o tutti gli attributi di un elemento della visualizzazione elenco. È anche possibile inviare \_ l'elemento per impostare il testo di un elemento secondario. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetItem ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) che contiene gli attributi del nuovo elemento. I membri **iItem** e **iSubItem** identificano l'elemento o l'elemento secondario e il membro **mask** specifica gli attributi da impostare. Se il membro **mask** specifica il \_ valore di testo LVIF, il membro **pszText** è l'indirizzo di una stringa con terminazione null e il membro **cchTextMax** viene ignorato. Se il membro **mask** specifica il \_ valore dello stato LVIF, il membro **stateMask** specifica quali Stati dell'elemento modificare e il membro di **stato** contiene i valori per tali Stati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Per impostare gli attributi di un elemento della visualizzazione elenco, impostare il membro **iItem** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) sull'indice dell'elemento e impostare il membro **iSubItem** su zero. Per un elemento, è possibile impostare i membri **state**, **pszText**, **IImage** e **lParam** della struttura **LVITEM** .

Per impostare il testo di un elemento secondario, impostare i membri **iItem** e **iSubItem** per indicare l'elemento secondario specifico e usare il membro **pszText** per specificare il testo. In alternativa, è possibile usare la [**macro \_ SetItemText di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) per impostare il testo di un elemento secondario. Non è possibile impostare i membri **state** o **lParam** per gli elementi secondari perché gli elementi secondari non dispongono di questi attributi. Nella versione 4,70 e successive, è possibile impostare il membro **IImage** per gli elementi secondari. Se il controllo elenco-visualizzazione ha lo stile esteso [**LVS \_ ex \_ SUBITEMIMAGES**](extended-list-view-styles.md) , verrà visualizzata l'immagine dell'elemento secondario. Le versioni precedenti ignoreranno l'immagine dell'elemento secondario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVM \_ SETITEMW** (Unicode) e **LVM \_ setitema** (ANSI)<br/>                   |



 

 





