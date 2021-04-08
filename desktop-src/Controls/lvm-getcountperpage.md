---
title: Messaggio LVM_GETCOUNTPERPAGE (COMmctrl. h)
description: Calcola il numero di elementi che possono essere posizionati verticalmente nell'area visibile di un controllo di visualizzazione elenco in visualizzazione elenco o report. Vengono conteggiati solo gli elementi completamente visibili. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetCountPerPage di ListView.
ms.assetid: 2ffd2bb1-cddf-4a4a-a4a8-087c9dc3fec0
keywords:
- Controlli di Windows Message LVM_GETCOUNTPERPAGE
topic_type:
- apiref
api_name:
- LVM_GETCOUNTPERPAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 734d460754f9ae8a11c3a42d8eacebf31d0b6fc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047862"
---
# <a name="lvm_getcountperpage-message"></a>\_Messaggio GETCOUNTPERPAGE LVM

Calcola il numero di elementi che possono essere posizionati verticalmente nell'area visibile di un controllo di visualizzazione elenco in visualizzazione elenco o report. Vengono conteggiati solo gli elementi completamente visibili. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetCountPerPage di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcountperpage) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di elementi completamente visibili in caso di esito positivo. Se la visualizzazione corrente è una visualizzazione icona o piccola, il valore restituito è il numero totale di elementi nel controllo elenco-visualizzazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





