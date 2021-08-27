---
title: HDM_CREATEDRAGIMAGE messaggio (Commctrl.h)
description: Crea una versione semitrasparente dell'immagine di un elemento da usare come immagine di trascinamento. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Header CreateDragImage.
ms.assetid: 1b9dc515-d327-4634-a424-cc15a32f0f7c
keywords:
- HDM_CREATEDRAGIMAGE dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- HDM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1507f3e72ce75394aaad834fe5c0d876fc579a671ad8f2df00865b2278ad6e32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047231"
---
# <a name="hdm_createdragimage-message"></a>Messaggio HDM \_ CREATEDRAGIMAGE

Crea una versione semitrasparente dell'immagine di un elemento da usare come immagine di trascinamento. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Header CreateDragImage.**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero dell'elemento all'interno del controllo intestazione. L'immagine assegnata a questo elemento è la base per l'immagine trasparente.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un handle a un elenco di immagini che contiene la nuova immagine come unico elemento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





