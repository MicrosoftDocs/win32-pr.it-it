---
title: Messaggio TB_INSERTBUTTON (COMmctrl. h)
description: Inserisce un pulsante in una barra degli strumenti.
ms.assetid: 6be27817-5d86-4649-bd63-173845197763
keywords:
- Controlli di Windows Message TB_INSERTBUTTON
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
ms.openlocfilehash: 4e08eed328a99d4a8927a7e09084bf122f2e4e84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119447"
---
# <a name="tb_insertbutton-message"></a>TB \_ INSERTBUTTON messaggio

Inserisce un pulsante in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero di un pulsante. Il messaggio inserisce il pulsante nuovo a sinistra di questo pulsante.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) contenente informazioni sul pulsante da inserire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TB \_ INSERTBUTTONW** (Unicode) e **TB \_ INSERTBUTTONA** (ANSI)<br/>           |



 

 





