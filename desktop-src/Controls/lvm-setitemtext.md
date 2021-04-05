---
title: Messaggio LVM_SETITEMTEXT (COMmctrl. h)
description: Modifica il testo di un elemento o di un elemento secondario della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetItemText di ListView.
ms.assetid: 1a9c7e4d-78e0-44c7-bf4f-d0fc7a0049f3
keywords:
- Controlli di Windows Message LVM_SETITEMTEXT
topic_type:
- apiref
api_name:
- LVM_SETITEMTEXT
- LVM_SETITEMTEXTA
- LVM_SETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d326e48047325fc9aff2c6607da6d7d377965adf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873893"
---
# <a name="lvm_setitemtext-message"></a>\_Messaggio SETITEMTEXT LVM

Modifica il testo di un elemento o di un elemento secondario della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetItemText di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero dell'elemento della visualizzazione elenco.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . Il membro **iSubItem** è l'indice dell'elemento secondario oppure può essere zero per impostare l'etichetta dell'elemento. Il membro **pszText** è l'indirizzo di una stringa con terminazione null che contiene il nuovo testo. può anche essere **null**. Il membro **pszText** può anche essere LPSTR \_ TEXTCALLBACK per indicare un elemento di callback per il quale la finestra padre archivia il testo. In questo caso, il controllo elenco-visualizzazione Invia all'elemento padre un codice di notifica [**LVN \_ GETDISPINFO**](lvn-getdispinfo.md) quando è necessario il testo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se si invia questo messaggio in modo esplicito, viene restituito **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVM \_ SETITEMTEXTW** (Unicode) e **LVM \_ SETITEMTEXTA** (ANSI)<br/>           |



 

 





