---
title: Messaggio LVM_GETTOPINDEX (COMmctrl. h)
description: Recupera l'indice dell'elemento visibile in primo piano in visualizzazione elenco o report. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetTopIndex di ListView.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_gettopindex.htm
keywords:
- Controlli di Windows Message LVM_GETTOPINDEX
topic_type:
- apiref
api_name:
- LVM_GETTOPINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb1cb080588d1825fcbd9e6c5e7b1b573fd7ad2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302290"
---
# <a name="lvm_gettopindex-message"></a>\_Messaggio GETTOPINDEX LVM

Recupera l'indice dell'elemento visibile in primo piano in visualizzazione elenco o report. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetTopIndex di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento in caso di esito positivo. Restituisce zero se il controllo di visualizzazione elenco è in visualizzazione icona o icona piccola o se il controllo elenco-visualizzazione è in visualizzazione dettagli con gruppi abilitati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





