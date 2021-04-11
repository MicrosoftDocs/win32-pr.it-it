---
title: Messaggio LVM_SETITEMSTATE (COMmctrl. h)
description: Modifica lo stato di un elemento in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetItemState di ListView.
ms.assetid: aecd14dd-cfd0-4c7c-bddc-f65022de68c9
keywords:
- Controlli di Windows Message LVM_SETITEMSTATE
topic_type:
- apiref
api_name:
- LVM_SETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2120d6d1d2cd3044368ebb343cdf0fe240d805c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119934"
---
# <a name="lvm_setitemstate-message"></a>\_Messaggio SETITEMSTATE LVM

Modifica lo stato di un elemento in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetItemState di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento della visualizzazione elenco. Se questo parametro è-1, la modifica dello stato viene applicata a tutti gli elementi.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . Il membro **stateMask** specifica quali bit di stato modificare e il membro di **stato** contiene i nuovi valori per tali bit. Gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se si invia questo messaggio in modo esplicito, viene restituito **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Il valore dello stato di un elemento include un set di flag di bit che indicano lo stato dell'elemento. Il valore dello stato può includere anche gli indici dell'elenco immagini che indicano l'immagine di stato e l'immagine sovrapposta dell'elemento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





