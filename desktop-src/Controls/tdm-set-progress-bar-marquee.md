---
title: Messaggio TDM_SET_PROGRESS_BAR_MARQUEE (COMmctrl. h)
description: Avvia e arresta la visualizzazione Marquee dell'indicatore di stato in una finestra di dialogo attività e imposta la velocità del Marquee.
ms.assetid: df947171-a916-4db9-abe0-57a3bf11037f
keywords:
- Controlli di Windows Message TDM_SET_PROGRESS_BAR_MARQUEE
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_MARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f73d3d4308d2e3f963c015b6e36f385902bea6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048700"
---
# <a name="tdm_set_progress_bar_marquee-message"></a>Messaggio del Marquee indicatore di \_ stato set TDM \_ \_ \_

Avvia e arresta la visualizzazione Marquee dell'indicatore di stato in una finestra di dialogo attività e imposta la velocità del Marquee.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Valore **bool** che indica se attivare o disattivare la visualizzazione Marquee. Utilizzare **true** per attivare la visualizzazione Marquee oppure **false** per disattivarla.

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

**Uint** che specifica il tempo, in millisecondi, tra gli aggiornamenti dell'animazione Marquee. Se questo parametro è zero, l'animazione Marquee viene aggiornata ogni 30 millisecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

Per informazioni sulla modalità Marquee, vedere [controllo indicatore di stato](progress-bar-control.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





