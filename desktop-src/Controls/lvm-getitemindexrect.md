---
title: Messaggio LVM_GETITEMINDEXRECT (COMmctrl. h)
description: Recupera il rettangolo di delimitazione per tutto o parte di un elemento secondario nella visualizzazione corrente di un controllo visualizzazione elenco. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetItemIndexRect di ListView.
ms.assetid: 17704d24-c029-4d41-b198-04d1e78698e0
keywords:
- Controlli di Windows Message LVM_GETITEMINDEXRECT
topic_type:
- apiref
api_name:
- LVM_GETITEMINDEXRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31ccd114713326c4796ca69f56fc2c38daf145db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478521"
---
# <a name="lvm_getitemindexrect-message"></a>\_Messaggio GETITEMINDEXRECT LVM

Recupera il rettangolo di delimitazione per tutto o parte di un elemento secondario nella visualizzazione corrente di un controllo visualizzazione elenco. Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetItemIndexRect di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemindexrect) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Puntatore a una struttura [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) per l'elemento padre dell'elemento secondario. Il processo chiamante è responsabile dell'allocazione di questa struttura e dell'impostazione dei relativi membri. *wParam* non può essere **null**.

</dd> <dt>

*lParam* \[ in uscita\]
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) per ricevere le coordinate. Il processo chiamante è responsabile dell'allocazione di questa struttura. *lParam* non può essere **null**. Imposta il membro **superiore** sull'indice dell'elemento secondario. Impostare il membro **Left** su uno dei valori seguenti, che indica la parte dell'elemento secondario per cui deve essere recuperato il rettangolo di delimitazione.



| Valore                                                                                                                                                   | Significato                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <dt>**limiti di LVIR \_**</dt> </dl> | Restituisce il rettangolo di delimitazione dell'intero elemento secondario, incluse l'icona e l'etichetta.<br/> |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <dt>**\_icona LVIR**</dt> </dl>       | Restituisce il rettangolo di delimitazione dell'icona o dell'icona piccola dell'elemento secondario.<br/>            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <dt>**\_etichetta LVIR**</dt> </dl>    | Restituisce il rettangolo di delimitazione del testo dell'elemento secondario.<br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

