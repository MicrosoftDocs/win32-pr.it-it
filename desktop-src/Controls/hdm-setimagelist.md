---
title: HDM_SETIMAGELIST messaggio (Commctrl.h)
description: Assegna un elenco di immagini a un controllo intestazione esistente. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Header SetImageList o Header \_ SetStateImageList.
ms.assetid: 1d7f07fa-f6f4-422a-949c-97d0388343e3
keywords:
- HDM_SETIMAGELIST dei messaggi Windows
topic_type:
- apiref
api_name:
- HDM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2034a6880721914961b3bd75907df2e7b4e53360ccb3b10162f238068d85031d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435811"
---
# <a name="hdm_setimagelist-message"></a>Messaggio \_ HDM SETIMAGELIST

Assegna un elenco di immagini a un controllo intestazione esistente. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Header SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) [**o Header \_ SetStateImageList.**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist)

## <a name="parameters"></a>Parametri

<dl> <dt>*wParam*</dt> <dd>Uno dei valori seguenti:

| Valore                                                                                                                                                      | Significato                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <dt>**HDSIL \_ NORMAL**</dt> </dl> | Indica che si tratta di un normale elenco di immagini.<br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <dt>**STATO \_ HDSIL**</dt> </dl>    | Indica che si tratta di un elenco di immagini di stato.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per un elenco di immagini.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle all'elenco di immagini associato in precedenza al controllo . Restituisce **NULL in caso** di errore o se in precedenza non è stato impostato alcun elenco di immagini.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





