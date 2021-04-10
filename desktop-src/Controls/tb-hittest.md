---
title: Messaggio TB_HITTEST (COMmctrl. h)
description: Determina se un punto si trova in un controllo Toolbar.
ms.assetid: d08f3805-2042-470e-8f5a-8a6a681d1189
keywords:
- Controlli di Windows Message TB_HITTEST
topic_type:
- apiref
api_name:
- TB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6264bc0191f091d3819081ddd67e428b64c84570
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964039"
---
# <a name="tb_hittest-message"></a>\_Messaggio HITTEST TB

Determina se un punto si trova in un controllo Toolbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura di [**punti**](/previous-versions//dd162805(v=vs.85)) che contiene la coordinata x dell'hit test nel membro **x** e la coordinata y dell'hit test nel membro **y** . Le coordinate sono relative all'area client della barra degli strumenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero. Se il valore restituito è zero o un valore positivo, si tratta dell'indice in base zero dell'elemento non separatore in cui si trova il punto. Se il valore restituito è negativo, il punto non si trova all'interno di un pulsante. Il valore assoluto del valore restituito è l'indice di un elemento separatore o l'elemento non separatore più vicino.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

