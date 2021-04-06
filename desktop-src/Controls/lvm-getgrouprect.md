---
title: Messaggio LVM_GETGROUPRECT (COMmctrl. h)
description: Ottiene il rettangolo per un gruppo specificato. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetGroupRect di ListView.
ms.assetid: 9441a6c5-11d8-4f52-80dd-1b60befd9b9d
keywords:
- Controlli di Windows Message LVM_GETGROUPRECT
topic_type:
- apiref
api_name:
- LVM_GETGROUPRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2cbdfb1ec6e670e7b5d333694f3a1ca56d287b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963805"
---
# <a name="lvm_getgrouprect-message"></a>\_Messaggio GETGROUPRECT LVM

Ottiene il rettangolo per un gruppo specificato. Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetGroupRect di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgrouprect) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Specifica il gruppo per **iGroupId** (vedere la struttura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) ).

</dd> <dt>

*lParam* \[ in uscita\]
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) per ricevere informazioni sul gruppo specificato da *wParam*. Il ricevitore del messaggio è responsabile dell'impostazione dei membri della struttura con le informazioni per il gruppo specificato da *wParam*.

Il processo chiamante è responsabile dell'allocazione della memoria per la struttura. Impostare il membro **superiore** di [**Rect**](/previous-versions//dd162897(v=vs.85)) su uno dei flag seguenti per specificare le coordinate del rettangolo da ottenere.



| Valore                                                                                                                                                                  | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVGGR_GROUP"></span><span id="lvggr_group"></span><dl> <dt>**\_gruppo LVGGR**</dt> </dl>                | Coordinate dell'intero gruppo espanso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="LVGGR_HEADER"></span><span id="lvggr_header"></span><dl> <dt>**\_intestazione LVGGR**</dt> </dl>             | Coordinate dell'intestazione Only (gruppo compresso).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="LVGGR_LABEL"></span><span id="lvggr_label"></span><dl> <dt>**\_etichetta LVGGR**</dt> </dl>                | Solo coordinate dell'etichetta.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="LVGGR_SUBSETLINK"></span><span id="lvggr_subsetlink"></span><dl> <dt>**\_SUBSETLINK LVGGR**</dt> </dl> | Coordinate del solo collegamento del subset (subset di markup). Un controllo visualizzazione elenco può limitare il numero di elementi visibili visualizzati in ogni gruppo. Viene visualizzato un collegamento all'utente per consentire all'utente di espandere il gruppo. Questo flag restituirà il rettangolo di delimitazione del collegamento del subset se il gruppo è un subset (stato del gruppo di LVGS \_ subset, vedere la struttura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup), **stato** membro). Questo flag viene fornito in modo che le applicazioni di accessibilità possano trovare il collegamento.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

