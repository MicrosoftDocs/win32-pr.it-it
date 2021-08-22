---
title: TB_ISBUTTONPRESSED messaggio (Commctrl.h)
description: Determina se il pulsante specificato in una barra degli strumenti è premuto.
ms.assetid: b8e2434c-24c2-47eb-b243-ffdaf31d5b8f
keywords:
- TB_ISBUTTONPRESSED dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- TB_ISBUTTONPRESSED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187b7dd6c39fb972d53391dcbd67d7b45bb895a2e521fa8db22c2a7a411c05e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119503641"
---
# <a name="tb_isbuttonpressed-message"></a>TB \_ ISBUTTONPRESSED message

Determina se il pulsante specificato in una barra degli strumenti è premuto.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore di comando del pulsante.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se il pulsante viene premuto oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





