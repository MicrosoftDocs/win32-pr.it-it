---
title: Messaggio TB_GETHOTIMAGELIST (COMmctrl. h)
description: Recupera l'elenco di immagini utilizzato da un controllo Toolbar per visualizzare i pulsanti di scelta rapida.
ms.assetid: 63054449-2768-459c-933c-781d31bdcc15
keywords:
- Controlli di Windows Message TB_GETHOTIMAGELIST
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
ms.openlocfilehash: 9e19c1f3989b0d749a9c663d00b5fb7b54d67fc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120003"
---
# <a name="tb_gethotimagelist-message"></a>TB \_ GETHOTIMAGELIST messaggio

Recupera l'elenco di immagini utilizzato da un controllo Toolbar per visualizzare i pulsanti di scelta rapida.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle all'elenco di immagini che il controllo utilizza per visualizzare i pulsanti sensibili o **null** se non è impostato alcun elenco di immagini attive.

## <a name="remarks"></a>Commenti

Un pulsante è attivo quando il cursore è posizionato su di esso. Per gli elementi attivi, i controlli della barra degli strumenti devono avere lo stile di [**\_ elenco**](toolbar-control-and-button-styles.md) [**TBSTYLE \_ Flat**](toolbar-control-and-button-styles.md) o TBSTYLE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





