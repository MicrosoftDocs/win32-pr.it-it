---
title: Messaggio PBM_SETBKCOLOR (COMmctrl. h)
description: Imposta il colore di sfondo nell'indicatore di stato.
ms.assetid: e28af958-babb-4c2e-9202-89b608c22f8e
keywords:
- Controlli di Windows Message PBM_SETBKCOLOR
topic_type:
- apiref
api_name:
- PBM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ddfaf84695221cf998275d76a9d2d67773150da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742538"
---
# <a name="pbm_setbkcolor-message"></a>\_Messaggio SETBKCOLOR PBM

Imposta il colore di sfondo nell'indicatore di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore **COLORREF** che specifica il nuovo colore di sfondo. Specificare il \_ valore predefinito CLR per fare in modo che l'indicatore di stato utilizzi il colore di sfondo predefinito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il colore di sfondo precedente oppure il \_ valore predefinito CLR se il colore di sfondo è il colore predefinito.

## <a name="remarks"></a>Commenti

Quando gli stili di visualizzazione sono abilitati, questo messaggio non ha alcun effetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





