---
title: Costanti del registro eventi di Windows (WinEvt. h)
description: Il registro eventi di Windows definisce le costanti seguenti
ms.assetid: d3a4a136-ca33-4dad-95ad-af1be6687843
topic_type:
- apiref
api_name:
- EVT_VARIANT_TYPE_MASK
- EVT_VARIANT_TYPE_ARRAY
- EVT_READ_ACCESS
- EVT_WRITE_ACCESS
- EVT_CLEAR_ACCESS
- EVT_ALL_ACCESS
api_location:
- WinEvt.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d592cea0eb1738f5ee04ce53faa9a5fa06c0d52a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400601"
---
# <a name="windows-event-log-constants"></a>Costanti registro eventi di Windows

Nel registro eventi di Windows sono definite le costanti seguenti:

<dl> <dt>

<span id="EVT_VARIANT_TYPE_MASK"></span><span id="evt_variant_type_mask"></span>**\_ \_ maschera tipo variante \_ evt**
</dt> <dd> <dl> <dt>

0x7F
</dt> <dt>



Maschera di bit utilizzata per mascherare il bit di matrice del tipo Variant, in modo che sia possibile determinare il tipo di dati del valore Variant contenuto nella struttura [**\_ Variant evt**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) .


</dt> </dl> </dd> <dt>

<span id="EVT_VARIANT_TYPE_ARRAY"></span><span id="evt_variant_type_array"></span>**\_matrice di \_ tipi \_ Variant evt**
</dt> <dd> <dl> <dt>

128
</dt> <dt>



Questo bit è impostato per il membro del **tipo** della struttura [**\_ Variant evt**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) se la variante contiene un puntatore a una matrice di valori, anziché il valore stesso.


</dt> </dl> </dd> <dt>

<span id="EVT_READ_ACCESS"></span><span id="evt_read_access"></span>**\_accesso in lettura evt \_**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Autorizzazione di controllo di accesso in lettura che consente di leggere le informazioni da un log eventi.


</dt> </dl> </dd> <dt>

<span id="EVT_WRITE_ACCESS"></span><span id="evt_write_access"></span>**\_accesso in scrittura a evt \_**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>



Autorizzazione di controllo di accesso in scrittura che consente la scrittura di informazioni in un log eventi.


</dt> </dl> </dd> <dt>

<span id="EVT_CLEAR_ACCESS"></span><span id="evt_clear_access"></span>**\_accesso evt Clear \_**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>



Deselezionare l'autorizzazione di controllo di accesso che consente la cancellazione di tutte le informazioni da un log eventi.


</dt> </dl> </dd> <dt>

<span id="EVT_ALL_ACCESS"></span><span id="evt_all_access"></span>**EVT \_ tutti gli \_ accessi**
</dt> <dd> <dl> <dt>

0x7
</dt> <dt>



All (lettura, scrittura, cancellazione ed eliminazione) autorizzazione di controllo di accesso.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>WinEvt. h</dt> </dl> |



 

 





