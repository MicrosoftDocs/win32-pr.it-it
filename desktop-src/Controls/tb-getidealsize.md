---
title: TB_GETIDEALSIZE messaggio (Commctrl.h)
description: Ottiene le dimensioni ideali della barra degli strumenti.
ms.assetid: d3b5ea4d-fd80-4f07-be4f-89b53a8bdf4d
keywords:
- TB_GETIDEALSIZE dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TB_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1844f3ae4200c1120f784c03e5f80d2df4457319cf81e12c88ce0ed84525117d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119816311"
---
# <a name="tb_getidealsize-message"></a>TB \_ GETIDEALSIZE message

Ottiene le dimensioni ideali della barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Valore **BOOL che** indica se recuperare l'altezza o la larghezza ideale della barra degli strumenti. Usare **TRUE** per recuperare l'altezza ideale, **FALSE** per recuperare la larghezza ideale.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura SIZE**](/previous-versions//dd145106(v=vs.85)) che riceve l'altezza o la larghezza in corrispondenza della quale verranno visualizzati tutti i pulsanti. Se *wParam* è **TRUE,** è valido solo il membro **cy** (height). Se *wParam* è **FALSE,** è valido solo il membro **cx** (width).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

