---
title: TCM_GETCURFOCUS messaggio (Commctrl.h)
description: Restituisce l'indice dell'elemento con lo stato attivo in un controllo Struttura a schede. È possibile inviare questo messaggio in modo esplicito o tramite la macro TabCtrl \_ GetCurFocus.
ms.assetid: ae6ee159-c769-41d6-b0bb-2a9ade4c0e71
keywords:
- TCM_GETCURFOCUS dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TCM_GETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 694fb64b033d279292a687c39959925a68999c0b232c847bdf6ec6b476c725e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104941"
---
# <a name="tcm_getcurfocus-message"></a>Messaggio GETCURFOCUS di TCM \_

Restituisce l'indice dell'elemento con lo stato attivo in un controllo Struttura a schede. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**TabCtrl \_ GetCurFocus.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcurfocus)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento della scheda con lo stato attivo.

## <a name="remarks"></a>Commenti

L'elemento con lo stato attivo può essere diverso dall'elemento selezionato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





