---
title: TB_AUTOSIZE messaggio (Commctrl.h)
description: Determina il ridimensionamento di una barra degli strumenti.
ms.assetid: 11aff184-6f18-43a2-9bdc-462fc5ba1680
keywords:
- TB_AUTOSIZE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TB_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b363546c5a079d2d73a0a3573a582ac27d6348b4db879d6c4371d639021f5d2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018729"
---
# <a name="tb_autosize-message"></a>TB \_ AUTOSIZE message

Determina il ridimensionamento di una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Un'applicazione invia il messaggio **TB \_ AUTOSIZE** dopo aver causato la modifica delle dimensioni di una barra degli strumenti impostando le dimensioni del pulsante o della bitmap o aggiungendo stringhe per la prima volta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





