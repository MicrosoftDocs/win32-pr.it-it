---
title: Messaggio LVM_SETIMAGELIST (COMmctrl. h)
description: Assegna un elenco di immagini a un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro ListView.
ms.assetid: 5241065b-85e4-412e-9868-fd5b15ff7c17
keywords:
- Controlli di Windows Message LVM_SETIMAGELIST
topic_type:
- apiref
api_name:
- LVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 779d31fd781a72dbdfbc4738e091482ca4a08528
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963762"
---
# <a name="lvm_setimagelist-message"></a>Messaggio dell'immagine di LVM \_

Assegna un elenco di immagini a un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o utilizzando [**la \_ macro ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo di elenco di immagini. Questo parametro può essere uno dei valori seguenti:



| Valore                                                                                                                                                                     | Significato                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <dt>**LVSIL \_ normale**</dt> </dl>                | Elenco immagini con icone grandi.<br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <dt>**LVSIL \_ Small**</dt> </dl>                   | Elenco immagini con icone piccole.<br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <dt>**\_stato LVSIL**</dt> </dl>                   | Elenco immagini con immagini di stato.<br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <dt>**\_GROUPHEADER LVSIL**</dt> </dl> | Elenco di immagini per l'intestazione di gruppo.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'elenco di immagini da assegnare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per l'elenco di immagini precedentemente associato al controllo, se ha esito positivo, oppure **null** in caso contrario.

## <a name="remarks"></a>Commenti

L'elenco di immagini corrente verrà eliminato definitivamente quando il controllo visualizzazione elenco viene eliminato definitivamente, a meno che non sia impostato lo stile di [**\_ SHAREIMAGELISTS LVS**](list-view-window-styles.md) . Se si usa questo messaggio per sostituire un elenco di immagini con un altro, l'applicazione deve eliminare in modo esplicito tutti gli elenchi di immagini diversi da quello corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





