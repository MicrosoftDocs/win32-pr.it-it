---
title: Messaggio SB_GETBORDERS (COMmctrl. h)
description: Recupera le larghezze correnti dei bordi orizzontali e verticali di una finestra di stato.
ms.assetid: 120c1e0d-6f42-424e-94e0-a080d216d39d
keywords:
- Controlli di Windows Message SB_GETBORDERS
topic_type:
- apiref
api_name:
- SB_GETBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854df2cd367a852a2e6a0e638b470187efabe58c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120706"
---
# <a name="sb_getborders-message"></a>\_Messaggio SB GETborders

Recupera le larghezze correnti dei bordi orizzontali e verticali di una finestra di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice di interi con tre elementi. Il primo elemento riceve la larghezza del bordo orizzontale, il secondo riceve la larghezza del bordo verticale e il terzo riceve la larghezza del bordo tra i rettangoli.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

I bordi determinano la spaziatura tra il bordo esterno della finestra e i rettangoli all'interno della finestra che contengono testo. I bordi determinano anche la spaziatura tra i rettangoli.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





