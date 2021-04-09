---
title: Messaggio UDM_SETBASE (COMmctrl. h)
description: Imposta la base radice per un controllo di scorrimento. Il valore di base determina se la finestra Buddy Visualizza numeri in cifre decimali o esadecimali. I numeri esadecimali sono sempre senza segno e i numeri decimali sono firmati.
ms.assetid: c76cdec1-e73b-4b4b-89be-9a00ff2ea172
keywords:
- Controlli di Windows Message UDM_SETBASE
topic_type:
- apiref
api_name:
- UDM_SETBASE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6bcd7d6154b4ba732e5ffbbec889b326ec8176
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964544"
---
# <a name="udm_setbase-message"></a>UDM- \_ messaggio di base

Imposta la base radice per un controllo di scorrimento. Il valore di base determina se la finestra Buddy Visualizza numeri in cifre decimali o esadecimali. I numeri esadecimali sono sempre senza segno e i numeri decimali sono firmati.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Nuovo valore di base per il controllo. Questo parametro può essere 10 per Decimal o 16 per l'esadecimale.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è il valore di base precedente. Se viene specificata una base non valida, il valore restituito è zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





