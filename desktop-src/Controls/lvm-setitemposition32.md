---
title: Messaggio LVM_SETITEMPOSITION32 (COMmctrl. h)
description: Sposta un elemento in una posizione specificata in un controllo visualizzazione elenco (deve essere in una visualizzazione icona o piccola).
ms.assetid: 77db5fd0-bbc3-47ad-95ef-61ef4ac022bc
keywords:
- Controlli di Windows Message LVM_SETITEMPOSITION32
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 450963e4adf5ea2b0644f8d155145ba577efab83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048422"
---
# <a name="lvm_setitemposition32-message"></a>\_Messaggio SETITEMPOSITION32 LVM

Sposta un elemento in una posizione specificata in un controllo visualizzazione elenco (deve essere in una visualizzazione icona o piccola). Questo messaggio è diverso dal messaggio [**LVM \_ SETITEMPOSITION**](lvm-setitemposition.md) in quanto usa coordinate a 32 bit. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetItemPosition32 di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition32) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento della visualizzazione elenco per il quale impostare la posizione.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura di [**punti**](/previous-versions//dd162805(v=vs.85)) che contiene la nuova posizione dell'elemento, in coordinate di visualizzazione elenco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

