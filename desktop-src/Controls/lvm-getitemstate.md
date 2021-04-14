---
title: Messaggio LVM_GETITEMSTATE (COMmctrl. h)
description: Recupera lo stato di un elemento della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetItemState di ListView.
ms.assetid: 862960ed-a64a-4d66-b384-9228932eae6f
keywords:
- Controlli di Windows Message LVM_GETITEMSTATE
topic_type:
- apiref
api_name:
- LVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817b355e78f22c01c289f681d256ee6b4d0aa882
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478520"
---
# <a name="lvm_getitemstate-message"></a>\_Messaggio GETITEMSTATE LVM

Recupera lo stato di un elemento della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetItemState di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemstate) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento della visualizzazione elenco.

</dd> <dt>

*lParam* 
</dt> <dd>

Informazioni sullo stato da recuperare. Questo parametro può essere una combinazione dei valori seguenti:



| Valore                                                                                                                                                                           | Significato                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**\_taglia lvis**</dt> </dl>                                  | L'elemento è contrassegnato per un'operazione di taglia e incolla.<br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**\_DROPHILITED lvis**</dt> </dl>          | L'elemento è evidenziato come destinazione di trascinamento della selezione.<br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS con stato \_ attivo**</dt> </dl>                      | L'elemento ha lo stato attivo, quindi è racchiuso da un rettangolo di attivazione standard. Sebbene sia possibile selezionare più di un elemento, solo un elemento può avere lo stato attivo.<br/> |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ selezionato**</dt> </dl>                   | L'elemento è selezionato. L'aspetto di un elemento selezionato dipende dal fatto che abbia lo stato attivo e anche sui colori di sistema usati per la selezione.<br/>             |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**\_OVERLAYMASK lvis**</dt> </dl>          | Usare questa maschera per recuperare l'indice dell'immagine sovrapposta dell'elemento.<br/>                                                                                                 |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**\_STATEIMAGEMASK lvis**</dt> </dl> | Usare questa maschera per recuperare l'indice dell'immagine di stato dell'elemento.<br/>                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce lo stato corrente per l'elemento specificato. Gli unici bit validi nel valore restituito sono quelli che corrispondono al set di bit nel parametro *lParam* .

## <a name="remarks"></a>Commenti

Le informazioni sullo stato di un elemento includono un set di flag di bit, nonché gli indici dell'elenco di immagini che indicano l'immagine di stato e l'immagine sovrapposta dell'elemento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETITEMSTATE LVM**](lvm-setitemstate.md)
</dt> </dl>

 

 





