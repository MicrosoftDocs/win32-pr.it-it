---
title: Messaggio TTM_NEWTOOLRECT (COMmctrl. h)
description: Imposta un nuovo rettangolo di delimitazione per uno strumento.
ms.assetid: 81d1b745-310e-482e-8c6e-6e98e1e67b66
keywords:
- Controlli di Windows Message TTM_NEWTOOLRECT
topic_type:
- apiref
api_name:
- TTM_NEWTOOLRECT
- TTM_NEWTOOLRECTA
- TTM_NEWTOOLRECTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75417059b0108877d04c79af25ac98245461ad5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476780"
---
# <a name="ttm_newtoolrect-message"></a>\_Messaggio TTM NEWTOOLRECT

Imposta un nuovo rettangolo di delimitazione per uno strumento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . I membri **HWND** e **UID** identificano uno strumento e il membro **Rect** specifica il nuovo rettangolo di delimitazione. Prima di inviare questo messaggio, è necessario compilare il membro **cbSize** della struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TTM \_ NEWTOOLRECTW** (Unicode) e **TTM \_ NEWTOOLRECTA** (ANSI)<br/>           |



 

 





