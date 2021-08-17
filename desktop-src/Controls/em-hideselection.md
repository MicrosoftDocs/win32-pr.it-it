---
title: EM_HIDESELECTION messaggio (Richedit.h)
description: Il messaggio EM \_ HIDESELECTION nasconde o mostra la selezione in un controllo Rich Edit.
ms.assetid: 1245618f-c9e6-4876-9133-6009370cdb97
keywords:
- EM_HIDESELECTION dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- EM_HIDESELECTION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d9e33ba0fd8f9a97dcc7ef9ba0a76acfd76110a4d718fa282f3ba66d8f1ef6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437931"
---
# <a name="em_hideselection-message"></a>MESSAGGIO \_ EM HIDESELECTION

Il **messaggio EM \_ HIDESELECTION** nasconde o mostra la selezione in un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore che specifica se nascondere o visualizzare la selezione. Se questo parametro è zero, viene visualizzata la selezione. In caso contrario, la selezione è nascosta.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





