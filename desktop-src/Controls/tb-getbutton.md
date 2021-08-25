---
title: TB_GETBUTTON messaggio (Commctrl.h)
description: Recupera informazioni sul pulsante specificato in una barra degli strumenti.
ms.assetid: d90d053c-0daf-4a5a-b7ca-b9b4472c65a3
keywords:
- TB_GETBUTTON dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- TB_GETBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e36d8cd4e382570884b0cb30f7c95615e2342544cab0970e9864e9fde7882f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919031"
---
# <a name="tb_getbutton-message"></a>Messaggio \_ GETBUTTON TB

Recupera informazioni sul pulsante specificato in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero del pulsante per il quale recuperare le informazioni.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla [**struttura TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) che riceve le informazioni sul pulsante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





