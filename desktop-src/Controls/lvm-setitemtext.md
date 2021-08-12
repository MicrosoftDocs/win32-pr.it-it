---
title: LVM_SETITEMTEXT messaggio (Commctrl.h)
description: Modifica il testo di un elemento di visualizzazione elenco o di un elemento secondario. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro ListView SetItemText.
ms.assetid: 1a9c7e4d-78e0-44c7-bf4f-d0fc7a0049f3
keywords:
- LVM_SETITEMTEXT di controllo Windows messaggio
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
ms.openlocfilehash: 14eb5ddcff18a84f93febb22ef6661d8871df9b5578cc79f071b6e51b557c87b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670874"
---
# <a name="lvm_setitemtext-message"></a>Messaggio \_ LVM SETITEMTEXT

Modifica il testo di un elemento di visualizzazione elenco o di un elemento secondario. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView SetItemText.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero dell'elemento della visualizzazione elenco.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema) Il **membro iSubItem** è l'indice dell'elemento secondario oppure può essere zero per impostare l'etichetta dell'elemento. Il **membro pszText** è l'indirizzo di una stringa con terminazione Null contenente il nuovo testo. può anche essere **NULL.** Il **membro pszText** può anche essere LPSTR TEXTCALLBACK per indicare un elemento di callback per il quale la \_ finestra padre archivia il testo. In questo caso, il controllo visualizzazione elenco invia all'elemento padre un codice di notifica [**\_ LVN GETDISPINFO**](lvn-getdispinfo.md) quando è necessario il testo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se si invia questo messaggio in modo esplicito, restituisce **TRUE in caso** di esito positivo o FALSE in caso **contrario.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVM \_ SETITEMTEXTW** (Unicode) e **LVM \_ SETITEMTEXTA** (ANSI)<br/>           |



 

 





