---
title: PBM_SETBKCOLOR messaggio (Commctrl.h)
description: Imposta il colore di sfondo nell'indicatore di stato.
ms.assetid: e28af958-babb-4c2e-9202-89b608c22f8e
keywords:
- PBM_SETBKCOLOR di controllo Windows messaggio
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
ms.openlocfilehash: 54bdee330aba5a4ff96fc5b26fa7f99553ff8331dd8822fcd350fbae5813c813
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986181"
---
# <a name="pbm_setbkcolor-message"></a>Messaggio \_ SETBKCOLOR PBM

Imposta il colore di sfondo nell'indicatore di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

**Valore COLORREF** che specifica il nuovo colore di sfondo. Specificare il valore CLR \_ DEFAULT per fare in modo che l'indicatore di stato usi il colore di sfondo predefinito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il colore di sfondo precedente o CLR \_ DEFAULT se il colore di sfondo è il colore predefinito.

## <a name="remarks"></a>Commenti

Quando gli stili di visualizzazione sono abilitati, questo messaggio non ha alcun effetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





