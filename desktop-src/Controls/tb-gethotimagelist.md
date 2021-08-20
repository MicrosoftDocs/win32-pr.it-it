---
title: TB_GETHOTIMAGELIST messaggio (Commctrl.h)
description: Recupera l'elenco di immagini utilizzato da un controllo barra degli strumenti per visualizzare i pulsanti di scelta rapida.
ms.assetid: 63054449-2768-459c-933c-781d31bdcc15
keywords:
- TB_GETHOTIMAGELIST di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TB_GETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f69d1c77377553ae19a008f80e692e3c87487bc9874593d5f3d1e692658c4ad7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168514"
---
# <a name="tb_gethotimagelist-message"></a>TB \_ GETHOTIMAGELIST message (TB GETHOTIMAGELIST message)

Recupera l'elenco di immagini utilizzato da un controllo barra degli strumenti per visualizzare i pulsanti di scelta rapida.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle all'elenco di immagini utilizzato dal controllo per visualizzare i pulsanti di scelta rapida oppure **NULL** se non è impostato alcun elenco di immagini a caldo.

## <a name="remarks"></a>Commenti

Un pulsante è a caldo quando il cursore è posizionato su di esso. I controlli barra degli strumenti devono avere lo stile [**TBSTYLE \_ FLAT**](toolbar-control-and-button-styles.md) o [**TBSTYLE \_ LIST**](toolbar-control-and-button-styles.md) per avere elementi di tipo hot.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





