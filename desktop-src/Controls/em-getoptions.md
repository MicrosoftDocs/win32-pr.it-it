---
title: EM_GETOPTIONS messaggio (Richedit.h)
description: Recupera le opzioni del controllo Rich Edit.
ms.assetid: 183f0fed-8666-4ed5-ac48-362c818378d2
keywords:
- EM_GETOPTIONS dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- EM_GETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cba85b5fe3ffd47763d25b9ca13bf10f6202a6876e25d300f66d9af3852edd5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019519"
---
# <a name="em_getoptions-message"></a>Messaggio EM \_ GETOPTIONS

Recupera le opzioni del controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce una combinazione dei valori del flag di opzione corrente descritti nel messaggio [**EM \_ SETOPTIONS.**](em-setoptions.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ SETOPTIONS**](em-setoptions.md)
</dt> </dl>

 

 





