---
title: Messaggio MCM_SIZERECTTOMIN (COMmctrl. h)
description: Calcola il numero di calendari che si adattano al rettangolo specificato, quindi restituisce la dimensione minima che un rettangolo deve contenere per adattarsi a tale numero di calendari. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal SizeRectToMin.
ms.assetid: d52a7f68-e0c9-4646-a4aa-97129dffeb5d
keywords:
- Controlli di Windows Message MCM_SIZERECTTOMIN
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
ms.openlocfilehash: f525f4cca9280b92fab0b9b86aa1d950ed990ef4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121306"
---
# <a name="mcm_sizerecttomin-message"></a>\_Messaggio SIZERECTTOMIN MCM

Calcola il numero di calendari che si adattano al rettangolo specificato, quindi restituisce la dimensione minima che un rettangolo deve contenere per adattarsi a tale numero di calendari. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ SizeRectToMin**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

On entry, contiene un puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che descrive un'area maggiore o uguale alla dimensione necessaria per adattarsi al numero desiderato di calendari. Quando questa funzione viene restituita, contiene la struttura **Rect** minima che corrisponde a questo numero di calendari.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Non utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

