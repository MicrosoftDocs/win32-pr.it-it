---
title: MCM_SIZERECTTOMIN messaggio (Commctrl.h)
description: Calcola il numero di calendari che si adatteranno al rettangolo specificato e quindi restituisce le dimensioni minime necessarie per adattare un rettangolo al numero di calendari specificato. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro MonthCal SizeRectToMin.
ms.assetid: d52a7f68-e0c9-4646-a4aa-97129dffeb5d
keywords:
- MCM_SIZERECTTOMIN controlli Windows messaggio
topic_type:
- apiref
api_name:
- MCM_SIZERECTTOMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 547b8e401f270cbca1ff666ba0f1eb263ab3f9245f8a51e6874a7627597b9bfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799231"
---
# <a name="mcm_sizerecttomin-message"></a>MCM \_ SIZERECTTOMIN message

Calcola il numero di calendari che si adatteranno al rettangolo specificato e quindi restituisce le dimensioni minime necessarie per adattare un rettangolo al numero di calendari specificato. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MonthCal \_ SizeRectToMin.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

All'ingresso, contiene un puntatore a una struttura [**RECT**](/previous-versions//dd162897(v=vs.85)) che descrive un'area maggiore o uguale alla dimensione necessaria per adattare il numero desiderato di calendari. Quando questa funzione viene restituita, contiene la **struttura RECT** minima che corrisponde a questo numero di calendari.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Non utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

