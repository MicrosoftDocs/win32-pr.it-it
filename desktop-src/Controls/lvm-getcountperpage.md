---
title: LVM_GETCOUNTPERPAGE messaggio (Commctrl.h)
description: Calcola il numero di elementi che possono essere adattati verticalmente nell'area visibile di un controllo visualizzazione elenco in visualizzazione elenco o report. Vengono conteggiati solo gli elementi completamente visibili. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro ListView GetCountPerPage.
ms.assetid: 2ffd2bb1-cddf-4a4a-a4a8-087c9dc3fec0
keywords:
- LVM_GETCOUNTPERPAGE controlli Windows messaggio
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
ms.openlocfilehash: deb5e7acf0c3db4add2d986a1821b9a76ae30fc1aec0af369e48e35e2a424f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968341"
---
# <a name="lvm_getcountperpage-message"></a>Messaggio LVM \_ GETCOUNTPERPAGE

Calcola il numero di elementi che possono essere adattati verticalmente nell'area visibile di un controllo visualizzazione elenco in visualizzazione elenco o report. Vengono conteggiati solo gli elementi completamente visibili. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView GetCountPerPage.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcountperpage)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di elementi completamente visibili in caso di esito positivo. Se la visualizzazione corrente è una visualizzazione icona o icona piccola, il valore restituito è il numero totale di elementi nel controllo visualizzazione elenco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





