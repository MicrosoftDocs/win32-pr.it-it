---
title: LVM_GETITEMSTATE messaggio (Commctrl.h)
description: Recupera lo stato di un elemento di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro ListView GetItemState.
ms.assetid: 862960ed-a64a-4d66-b384-9228932eae6f
keywords:
- LVM_GETITEMSTATE dei messaggi Windows controllo
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
ms.openlocfilehash: 4737be14f3e975f87a6cbea460ef53dd40ecbb7b6a2d06c39a247dbe8aa0a14e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958300"
---
# <a name="lvm_getitemstate-message"></a>Messaggio LVM \_ GETITEMSTATE

Recupera lo stato di un elemento di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView GetItemState.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemstate)

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
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS \_ CUT**</dt> </dl>                                  | L'elemento è contrassegnato per un'operazione taglia e incolla.<br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS \_ DROPHILITED**</dt> </dl>          | L'elemento è evidenziato come destinazione di trascinamento della selezione.<br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS \_ CON STATO ATTIVO**</dt> </dl>                      | L'elemento ha lo stato attivo, quindi è racchiuso da un rettangolo di attivazione standard. Anche se è possibile selezionare più di un elemento, solo un elemento può avere lo stato attivo.<br/> |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ SELEZIONATO**</dt> </dl>                   | L'elemento è selezionato. L'aspetto di un elemento selezionato dipende dal fatto che abbia lo stato attivo e anche dai colori di sistema usati per la selezione.<br/>             |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**MASCHERA DI SOVRAPPOSIZIONE LVIS \_**</dt> </dl>          | Usare questa maschera per recuperare l'indice dell'immagine sovrapposta dell'elemento.<br/>                                                                                                 |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS \_ STATEIMAGEMASK**</dt> </dl> | Usare questa maschera per recuperare l'indice dell'immagine di stato dell'elemento.<br/>                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce lo stato corrente per l'elemento specificato. Gli unici bit validi nel valore restituito sono quelli che corrispondono ai bit impostati nel *parametro lParam.*

## <a name="remarks"></a>Commenti

Le informazioni sullo stato di un elemento includono un set di flag di bit e indici dell'elenco immagini che indicano l'immagine di stato e l'immagine di sovrapposizione dell'elemento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LVM \_ SETITEMSTATE**](lvm-setitemstate.md)
</dt> </dl>

 

 





