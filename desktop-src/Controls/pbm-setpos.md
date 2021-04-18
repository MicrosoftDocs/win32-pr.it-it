---
title: Messaggio PBM_SETPOS (COMmctrl. h)
description: Imposta la posizione corrente di un indicatore di stato e ridisegnato la barra in modo da riflettere la nuova posizione.
ms.assetid: 9ebeaa19-0f42-4af7-85d8-aae22498fd6f
keywords:
- Controlli di Windows Message PBM_SETPOS
topic_type:
- apiref
api_name:
- PBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a157f6a220f4932d39d13f08df79afa99d7348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302056"
---
# <a name="pbm_setpos-message"></a>\_Messaggio SETPOS PBM

Imposta la posizione corrente di un indicatore di stato e ridisegnato la barra in modo da riflettere la nuova posizione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Intero con segno che diventa la nuova posizione.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la posizione precedente.

## <a name="remarks"></a>Commenti

Se *wParam* non è compreso nell'intervallo del controllo, la posizione viene impostata sul limite più vicino.

Non inviare questo messaggio a un controllo con stile di [**\_ selezione PBS**](progress-bar-control-styles.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





