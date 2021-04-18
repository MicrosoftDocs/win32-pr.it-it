---
title: Messaggio TCM_SETPADDING (COMmctrl. h)
description: Imposta la quantità di spazio (riempimento) intorno all'icona e all'etichetta di ogni scheda in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl sepadding.
ms.assetid: c7f84c0d-8bf4-429a-b403-a0019575e72e
keywords:
- Controlli di Windows Message TCM_SETPADDING
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
ms.openlocfilehash: 353cde946944bda7dc8d285f863d976e29353996
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300967"
---
# <a name="tcm_setpadding-message"></a>\_Messaggio di SEPADDING TCM

Imposta la quantità di spazio (riempimento) intorno all'icona e all'etichetta di ogni scheda in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ sepadding**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è un valore **int** che specifica la quantità di spaziatura interna orizzontale, in pixel. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) è un valore **int** che specifica la quantità di spaziatura interna verticale, in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

