---
title: Messaggio TB_SETHOTIMAGELIST (COMmctrl. h)
description: Imposta l'elenco di immagini che il controllo toolbar utilizzerà per visualizzare i pulsanti di scelta rapida.
ms.assetid: 3c29cdde-bd57-4194-984f-220dbf963733
keywords:
- Controlli di Windows Message TB_SETHOTIMAGELIST
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
ms.openlocfilehash: f9a84c3420eaf64710ac1f8764db20d2cfc88b7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964628"
---
# <a name="tb_sethotimagelist-message"></a>TB \_ SETHOTIMAGELIST messaggio

Imposta l'elenco di immagini che il controllo toolbar utilizzerà per visualizzare i pulsanti di scelta rapida.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'elenco di immagini che verrà impostato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per l'elenco di immagini precedentemente utilizzato per visualizzare i pulsanti di scelta rapida oppure **null** se non è stato impostato in precedenza alcun elenco di immagini.

## <a name="remarks"></a>Commenti

Un pulsante è attivo quando il cursore è posizionato su di esso. Per gli elementi attivi, i controlli della barra degli strumenti devono avere lo stile di [**\_ elenco**](toolbar-control-and-button-styles.md) [**TBSTYLE \_ Flat**](toolbar-control-and-button-styles.md) o TBSTYLE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





