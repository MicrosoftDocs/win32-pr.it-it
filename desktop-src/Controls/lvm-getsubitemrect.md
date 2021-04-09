---
title: Messaggio LVM_GETSUBITEMRECT (COMmctrl. h)
description: Recupera le informazioni sul rettangolo di delimitazione per un elemento secondario in un controllo visualizzazione elenco.
ms.assetid: 985876b2-6eb3-4c96-88ea-ddec67ef5b5a
keywords:
- Controlli di Windows Message LVM_GETSUBITEMRECT
topic_type:
- apiref
api_name:
- LVM_GETSUBITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd1184c52d60b86e008685b87c9f5555cf801b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120978"
---
# <a name="lvm_getsubitemrect-message"></a>\_Messaggio GETSUBITEMRECT LVM

Recupera le informazioni sul rettangolo di delimitazione per un elemento secondario in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetSubItemRect di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getsubitemrect) (scelta consigliata). Questo messaggio deve essere utilizzato solo con i controlli visualizzazione elenco che utilizzano lo stile del [**\_ report LVS**](list-view-window-styles.md) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento padre dell'elemento secondario.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceverà le informazioni sul rettangolo di delimitazione dell'elemento secondario. I membri devono essere inizializzati in base alle relazioni membro/valore seguenti:



| Valore                                                                                                                             | Significato                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <dt>**In alto**</dt> </dl>    | Indice in base uno dell'elemento secondario.<br/>                                                                                    |
| <span id="left"></span><span id="LEFT"></span><dl> <dt>**sinistra**</dt> </dl> | Valore del flag (vedere la sezione Osservazioni). Indica la parte dell'elemento secondario della visualizzazione elenco per la quale recuperare il rettangolo di delimitazione.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

Di seguito sono riportati i valori di flag che è possibile impostare.



| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------|
| **Valore flag** | **Significato**                                                                                                         |
| limiti di LVIR \_   | Restituisce il rettangolo di delimitazione dell'intero elemento, inclusi l'icona e l'etichetta.                                    |
| \_icona LVIR     | Restituisce il rettangolo di delimitazione dell'icona o dell'icona piccola.                                                           |
| \_etichetta LVIR    | Restituisce il rettangolo di delimitazione dell'intero elemento, inclusi l'icona e l'etichetta. Si tratta di un limite identico a LVIR \_ . |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

