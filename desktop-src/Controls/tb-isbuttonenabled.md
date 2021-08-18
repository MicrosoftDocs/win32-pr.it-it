---
title: TB_ISBUTTONENABLED messaggio (Commctrl.h)
description: Determina se il pulsante specificato in una barra degli strumenti è abilitato.
ms.assetid: 055ed89a-2f3a-4174-b249-c6e68afbad31
keywords:
- TB_ISBUTTONENABLED dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- TB_ISBUTTONENABLED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07ceb230edb693e065a7ef0455c1374b410a2dcd86995dc1a0ec8c2b354ae028
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918461"
---
# <a name="tb_isbuttonenabled-message"></a>Messaggio \_ DI TB ISBUTTONENABLED

Determina se il pulsante specificato in una barra degli strumenti è abilitato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore di comando del pulsante.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se il pulsante è abilitato oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





