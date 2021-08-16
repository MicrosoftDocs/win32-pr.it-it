---
title: TB_CUSTOMIZE messaggio (Commctrl.h)
description: Visualizza la finestra di dialogo Personalizza barra degli strumenti.
ms.assetid: 45249467-d585-4ffd-8bbe-e39739059c40
keywords:
- TB_CUSTOMIZE dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TB_CUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765c4fe1cba535903ff1e60804ee6d4ec5743f5d3726212f9aca16742a40913b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957930"
---
# <a name="tb_customize-message"></a>MESSAGGIO \_ TB CUSTOMIZE

Visualizza la finestra **di dialogo Personalizza barra** degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

> [!Note]  
> La barra degli strumenti deve gestire le [notifiche TBN \_ QUERYINSERT](tbn-queryinsert.md) e [TBN \_ QUERYDELETE](tbn-querydelete.md) per **visualizzare** la finestra di dialogo Personalizza barra degli strumenti. Se la barra degli strumenti non gestisce tali notifiche, **TB \_ CUSTOMIZE** non ha alcun effetto.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





