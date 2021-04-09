---
title: Messaggio LVM_CREATEDRAGIMAGE (COMmctrl. h)
description: Crea un elenco di immagini di trascinamento per l'elemento specificato. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro CreateDragImage di ListView.
ms.assetid: face4c8f-01ff-4f5a-a468-e306a50dae35
keywords:
- Controlli di Windows Message LVM_CREATEDRAGIMAGE
topic_type:
- apiref
api_name:
- LVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace975b178fee85e2794b518a78b40b375c65ae7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119011"
---
# <a name="lvm_createdragimage-message"></a>\_Messaggio CREATEDRAGIMAGE LVM

Crea un elenco di immagini di trascinamento per l'elemento specificato. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ CreateDragImage di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_createdragimage) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura di [**punti**](/previous-versions//dd162805(v=vs.85)) che riceve la posizione iniziale dell'angolo superiore sinistro dell'immagine, in coordinate della visualizzazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per l'elenco di immagini di trascinamento, in caso di esito positivo, oppure **null** .

## <a name="remarks"></a>Commenti

L'applicazione è responsabile dell'eliminazione dell'elenco di immagini quando non è più necessario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

