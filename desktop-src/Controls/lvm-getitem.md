---
title: Messaggio LVM_GETITEM (COMmctrl. h)
description: Recupera alcuni o tutti gli attributi di un elemento della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro ListView GetItem.
ms.assetid: 684ad96a-2c3b-4148-b66c-41f8322500bb
keywords:
- Controlli di Windows Message LVM_GETITEM
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
ms.openlocfilehash: c19632567db5e37059b1b028a8ec1fc9385268cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742994"
---
# <a name="lvm_getitem-message"></a>\_Messaggio GETITEM LVM

Recupera alcuni o tutti gli attributi di un elemento della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) che specifica le informazioni per recuperare e ricevere informazioni sull'elemento della visualizzazione elenco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Quando viene inviato il messaggio **LVM \_ GetItem** , i membri **iItem** e **iSubItem** identificano l'elemento o l'elemento secondario per il recupero delle informazioni su e il membro **mask** specifica gli attributi da recuperare. Per un elenco di valori possibili, vedere la descrizione della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .

Se il \_ flag di testo LVIF è impostato nel membro **mask** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) , il membro **pszText** deve puntare a un buffer valido e il membro **cchTextMax** deve essere impostato sul numero di caratteri nel buffer. Le applicazioni non devono presupporre che il testo venga necessariamente inserito nel buffer specificato. Il controllo può invece modificare il membro **pszText** della struttura in modo che punti al nuovo testo, anziché posizionarlo nel buffer.

Se il membro **mask** specifica il \_ valore dello stato LVIF, è necessario che il membro **stateMask** specifichi i bit di stato dell'elemento da recuperare. Nell'output il membro di **stato** contiene i valori dei bit di stato specificati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVM \_ GETITEMW** (Unicode) e **LVM \_ getitema** (ANSI)<br/>                   |



 

 





