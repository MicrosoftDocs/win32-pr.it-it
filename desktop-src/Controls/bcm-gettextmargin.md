---
title: BCM_GETTEXTMARGIN messaggio (Commctrl.h)
description: Ottiene i margini utilizzati per disegnare testo in un controllo pulsante. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Button GetTextMargin.
ms.assetid: 6c141752-e636-41c4-9d05-df8b320ff59f
keywords:
- BCM_GETTEXTMARGIN di controllo Windows messaggio
topic_type:
- apiref
api_name:
- BCM_GETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea871d0054558e1522011d4fdb00fdd3c82a0dd1562fe3420d3295bbab89a01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120064411"
---
# <a name="bcm_gettextmargin-message"></a>Messaggio BCM \_ GETTEXTMARGIN

Ottiene i margini utilizzati per disegnare testo in un controllo pulsante. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Button GetTextMargin.**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) che contiene i margini da utilizzare per disegnare il testo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, restituisce **TRUE.** In caso contrario, **restituisce FALSE.**

## <a name="remarks"></a>Commenti

> [!Note]  
> Per usare questo messaggio, è necessario specificare un manifesto Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

