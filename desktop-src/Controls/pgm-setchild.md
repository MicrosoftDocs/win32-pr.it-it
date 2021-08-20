---
title: PGM_SETCHILD messaggio (Commctrl.h)
description: Imposta la finestra contenuta per il controllo pager.
ms.assetid: 717e6720-aa42-4ecd-9520-4618a04dc28d
keywords:
- PGM_SETCHILD dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- PGM_SETCHILD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da3424eabfb87d587ac8cd33802dfc03b3c3868d881b131360bfee2e8bc26730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830172"
---
# <a name="pgm_setchild-message"></a>PGM \_ SETCHILD message

Imposta la finestra contenuta per il controllo pager. Questo messaggio non modificherà l'elemento padre della finestra contenuta. assegna solo un handle di finestra al controllo pager per lo scorrimento. Nella maggior parte dei casi, la finestra contenuta sarà una finestra figlio. In questo caso, la finestra contenuta deve essere un elemento figlio del controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Pager SetChild.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la finestra da contenuto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





