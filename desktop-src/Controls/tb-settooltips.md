---
title: TB_SETTOOLTIPS messaggio (Commctrl.h)
description: Associa un controllo descrizione comando a una barra degli strumenti.
ms.assetid: a645f1f2-9333-4e25-985a-107cffb9b97f
keywords:
- TB_SETTOOLTIPS di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TB_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a75827df49eeaf8b6175cd14180ebb26ddbb642588ee77d625c701eee457baaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061231"
---
# <a name="tb_settooltips-message"></a>TB \_ SETTOOLTIPS message

Associa un controllo descrizione comando a una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il controllo della descrizione comando.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Tutti i pulsanti aggiunti a una barra degli strumenti prima di inviare il messaggio **\_ SETTOOLTIPS tb** non verranno registrati con il controllo descrizione comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





