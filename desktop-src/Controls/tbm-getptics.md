---
title: TBM_GETPTICS messaggio (Commctrl.h)
description: Recupera l'indirizzo di una matrice che contiene le posizioni dei segni di graduazione per un trackbar.
ms.assetid: d15a4b4d-2ced-40a4-9351-ed7ecc5a5751
keywords:
- TBM_GETPTICS del messaggio Windows controlli
topic_type:
- apiref
api_name:
- TBM_GETPTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f67bc6f1e5f67f262559d1c63401f1c19f8680798beae92d8847d4908f7cbe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078075"
---
# <a name="tbm_getptics-message"></a>Messaggio \_ TBM GETPTICS

Recupera l'indirizzo di una matrice che contiene le posizioni dei segni di graduazione per un trackbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indirizzo di una matrice **di valori DWORD.** Gli elementi della matrice specificano le posizioni logiche dei segni di graduazione del trackbar, senza includere il primo e l'ultimo segno di graduazione creati dal trackbar. Le posizioni logiche possono essere qualsiasi valore intero nell'intervallo di posizioni del dispositivo di scorrimento minimo e massimo del trackbar.

## <a name="remarks"></a>Commenti

Il numero di elementi nella matrice è minore di due rispetto al conteggio dei tick restituito dal messaggio [**\_ TBM GETNUMTICS.**](tbm-getnumtics.md) Si noti che i valori nella matrice possono includere posizioni duplicate e non essere in ordine sequenziale. Il puntatore restituito è valido fino a quando non si modificano i segni di graduazione del trackbar.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





