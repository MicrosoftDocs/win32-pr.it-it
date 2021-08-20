---
title: TB_INSERTBUTTON messaggio (Commctrl.h)
description: Inserisce un pulsante in una barra degli strumenti.
ms.assetid: 6be27817-5d86-4649-bd63-173845197763
keywords:
- TB_INSERTBUTTON dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TB_INSERTBUTTON
- TB_INSERTBUTTONA
- TB_INSERTBUTTONW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 909a4e039450e001757cd054cf27a15d24af392d6a55841c2857e2312252145c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829652"
---
# <a name="tb_insertbutton-message"></a>Messaggio \_ INSERTBUTTON TB

Inserisce un pulsante in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero di un pulsante. Il messaggio inserisce il nuovo pulsante a sinistra di questo pulsante.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) contenente informazioni sul pulsante da inserire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TB \_ INSERTBUTTONW** (Unicode) e **TB \_ INSERTBUTTONA** (ANSI)<br/>           |



 

 





