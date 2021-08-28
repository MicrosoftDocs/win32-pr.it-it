---
title: TTM_WINDOWFROMPOINT messaggio (Commctrl.h)
description: Consente a una routine di sottoclasse di fare in modo che una descrizione comando visualizza testo per una finestra diversa da quella sotto il cursore del mouse.
ms.assetid: f3bf6917-1745-4e4f-a9c1-8fe86b2b3906
keywords:
- TTM_WINDOWFROMPOINT controlli di Windows messaggio
topic_type:
- apiref
api_name:
- TTM_WINDOWFROMPOINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 572ce204fd9f0056ef77d62c7909a7281c478c38f6abeb95089ce86b0bdb1b8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109541"
---
# <a name="ttm_windowfrompoint-message"></a>TTM \_ WINDOWFROMPOINT message

Consente a una routine di sottoclasse di fare in modo che una descrizione comando visualizza testo per una finestra diversa da quella sotto il cursore del mouse.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**POINT**](/previous-versions//dd162805(v=vs.85)) che definisce il punto da controllare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'handle per la finestra che contiene il punto oppure **NULL** se non esiste alcuna finestra nel punto specificato.

## <a name="remarks"></a>Commenti

Questo messaggio deve essere elaborato da un'applicazione che sottoclassa una descrizione comando. Non deve essere inviata da un'applicazione. Una descrizione comando invia questo messaggio a se stesso prima di visualizzare il testo per una finestra. Modificando le coordinate del punto specificato da *lParam*, la routine della sottoclasse può determinare la visualizzazione del testo della descrizione comando per una finestra diversa da quella sotto il cursore del mouse.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

