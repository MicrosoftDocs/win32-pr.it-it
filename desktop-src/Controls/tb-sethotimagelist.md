---
title: TB_SETHOTIMAGELIST messaggio (Commctrl.h)
description: Imposta l'elenco di immagini che verrà utilizzato dal controllo barra degli strumenti per visualizzare i pulsanti di scelta rapida.
ms.assetid: 3c29cdde-bd57-4194-984f-220dbf963733
keywords:
- TB_SETHOTIMAGELIST dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- TB_SETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12d07c66add48fa8022f7b8505bee377be184af3ed8195251b3a92b46d0ff58c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318851"
---
# <a name="tb_sethotimagelist-message"></a>TB \_ SETHOTIMAGELIST message (TB SETHOTIMAGELIST message)

Imposta l'elenco di immagini che verrà utilizzato dal controllo barra degli strumenti per visualizzare i pulsanti di scelta rapida.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'elenco di immagini che verrà impostato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle all'elenco di immagini usato in precedenza per visualizzare i pulsanti di scelta rapida oppure **NULL** se in precedenza non è stato impostato alcun elenco di immagini.

## <a name="remarks"></a>Commenti

Un pulsante è a caldo quando il cursore è posizionato su di esso. I controlli barra degli strumenti devono avere lo stile [**TBSTYLE \_ FLAT**](toolbar-control-and-button-styles.md) o [**TBSTYLE \_ LIST**](toolbar-control-and-button-styles.md) per avere elementi di tipo hot.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





