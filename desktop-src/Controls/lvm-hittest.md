---
title: Messaggio LVM_HITTEST (COMmctrl. h)
description: Determina quale elemento della visualizzazione elenco, se presente, si trova in una posizione specificata. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro di ListView HitTest.
ms.assetid: 81df4ed1-30bd-4b63-9cb9-5163cb7cf52c
keywords:
- Controlli di Windows Message LVM_HITTEST
topic_type:
- apiref
api_name:
- LVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb770c8f5a47f1dcbbf23a11443afa581aea2e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964735"
---
# <a name="lvm_hittest-message"></a>\_Messaggio HITTEST di LVM

Determina quale elemento della visualizzazione elenco, se presente, si trova in una posizione specificata. È possibile inviare questo messaggio in modo esplicito o tramite la macro di [**ListView \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere 0. **Windows Vista.** Deve essere-1 se è necessario recuperare i membri **iGROUP** e **ISubItem** della struttura *lParam* .</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) che contiene la posizione di hit test e riceve informazioni sui risultati dell'hit test.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento in corrispondenza della posizione specificata, se presente, oppure-1 in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





