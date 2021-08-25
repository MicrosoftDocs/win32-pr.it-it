---
title: TCM_SETPADDING messaggio (Commctrl.h)
description: Imposta la quantità di spazio (spaziatura interna) intorno all'icona e all'etichetta di ogni scheda in un controllo Struttura a schede. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro TabCtrl SetPadding.
ms.assetid: c7f84c0d-8bf4-429a-b403-a0019575e72e
keywords:
- TCM_SETPADDING dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- TCM_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969ae3c7c240c38a6643682321c14e5744f2d2c2eec188004d1c3b2e6f2b3835
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876241"
---
# <a name="tcm_setpadding-message"></a>TCM \_ SETPADDING message

Imposta la quantità di spazio (spaziatura interna) intorno all'icona e all'etichetta di ogni scheda in un controllo Struttura a schede. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ TabCtrl SetPadding.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding)

## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

LOWORD [**è**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) un valore **INT** che specifica la quantità di spaziatura interna orizzontale, in pixel. [**HIWORD è**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) un **valore INT** che specifica la quantità di spaziatura interna verticale, in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

