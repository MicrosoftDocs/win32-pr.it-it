---
title: Messaggio TB_GETIDEALSIZE (COMmctrl. h)
description: Ottiene la dimensione ideale della barra degli strumenti.
ms.assetid: d3b5ea4d-fd80-4f07-be4f-89b53a8bdf4d
keywords:
- Controlli di Windows Message TB_GETIDEALSIZE
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
ms.openlocfilehash: a59b8701a4f4debcfb8e43f37068e7e7a4ef4f11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047990"
---
# <a name="tb_getidealsize-message"></a>TB \_ GETIDEALSIZE messaggio

Ottiene la dimensione ideale della barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Valore **booleano** che indica se recuperare l'altezza o la larghezza ideale della barra degli strumenti. Utilizzare **true** per recuperare l'altezza ideale, **false** per recuperare la larghezza ideale.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura di [**dimensioni**](/previous-versions//dd145106(v=vs.85)) che riceve l'altezza o la larghezza in corrispondenza della quale verranno visualizzati tutti i pulsanti. Se *wParam* è **true**, solo il membro **CY** (Height) è valido. Se *wParam* è **false**, solo il membro **CX** (width) è valido.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

