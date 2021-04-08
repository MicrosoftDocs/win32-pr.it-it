---
title: Messaggio RB_HITTEST (COMmctrl. h)
description: Determina quale parte di una banda Rebar si trova in un determinato punto sullo schermo, se in quel punto esiste una banda del controllo Rebar.
ms.assetid: 8f27db21-50d8-438f-a44c-2e65dd93fa2a
keywords:
- Controlli di Windows Message RB_HITTEST
topic_type:
- apiref
api_name:
- RB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e17283bfce255672391ba9d8b6acd60fe41045b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047921"
---
# <a name="rb_hittest-message"></a>Messaggio di RB \_ HITTEST

Determina quale parte di una banda Rebar si trova in un determinato punto sullo schermo, se in quel punto esiste una banda del controllo Rebar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo) . Prima di inviare il messaggio, è necessario inizializzare il membro **PT** di questa struttura sul punto che verrà sottoposto a hit testing, nelle coordinate del client.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice in base zero della banda nel punto specificato oppure-1 se non è presente alcuna banda del controllo Rebar nel punto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





