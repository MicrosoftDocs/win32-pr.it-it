---
title: Messaggio DTM_GETIDEALSIZE (COMmctrl. h)
description: Ottiene le dimensioni necessarie per visualizzare il controllo senza ritagliare. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro DateTime GetIdealSize.
ms.assetid: 15ec26a1-645b-4a96-af66-1031e1a46c6c
keywords:
- Controlli di Windows Message DTM_GETIDEALSIZE
topic_type:
- apiref
api_name:
- DTM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a979883f431fea4627f52fe19c3716341e3f2328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225202"
---
# <a name="dtm_getidealsize-message"></a>\_Messaggio GETIDEALSIZE DTM

Ottiene le dimensioni necessarie per visualizzare il controllo senza ritagliare. Inviare questo messaggio in modo esplicito o utilizzando la macro [**DateTime \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato. Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura di [**dimensioni**](/previous-versions//dd145106(v=vs.85)) per la ricezione delle dimensioni ideali. L'applicazione chiamante è responsabile dell'allocazione di questa struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

