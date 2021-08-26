---
title: TCM_REMOVEIMAGE messaggio (Commctrl.h)
description: Rimuove un'immagine dall'elenco di immagini di un controllo Struttura a schede. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro RemoveImage di TabCtrl.
ms.assetid: f2761338-0afa-47d8-9d9c-1d5a4a7f7bcf
keywords:
- TCM_REMOVEIMAGE dei messaggi Windows
topic_type:
- apiref
api_name:
- TCM_REMOVEIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d2305386f948e1dc4522124708b31ca360203ba9723241c99262fcdb5d2b20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104841"
---
# <a name="tcm_removeimage-message"></a>Messaggio REMOVEIMAGE di TCM \_

Rimuove un'immagine dall'elenco di immagini di un controllo Struttura a schede. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ RemoveImage di TabCtrl.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_removeimage)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'immagine da rimuovere.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il controllo Struttura a schede aggiorna l'indice dell'immagine di ogni scheda, in modo che ogni scheda rimanga associata alla stessa immagine di prima. Se una scheda usa l'immagine da rimuovere, la scheda verrà impostata in modo da non avere alcuna immagine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





