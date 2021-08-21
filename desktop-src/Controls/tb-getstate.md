---
title: TB_GETSTATE messaggio (Commctrl.h)
description: Recupera informazioni sullo stato del pulsante specificato in una barra degli strumenti, ad esempio se è abilitato, premuto o selezionato.
ms.assetid: e8a9e1ff-506f-413b-8f8c-986c25bce736
keywords:
- TB_GETSTATE dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- TB_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1757cfd71427904dc7060cc0084c64b82f143e1a8db666e40fe9e08c64c7ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168237"
---
# <a name="tb_getstate-message"></a>MESSAGGIO \_ GETSTATE TB

Recupera informazioni sullo stato del pulsante specificato in una barra degli strumenti, ad esempio se è abilitato, premuto o selezionato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore di comando del pulsante per il quale recuperare le informazioni.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce le informazioni sullo stato del pulsante in caso di esito positivo oppure -1 in caso contrario. Le informazioni sullo stato del pulsante possono essere una combinazione dei valori elencati in [**Stati dei pulsanti della**](toolbar-button-states.md)barra degli strumenti .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





