---
title: TTM_NEWTOOLRECT messaggio (Commctrl.h)
description: Imposta un nuovo rettangolo di delimitazione per uno strumento.
ms.assetid: 81d1b745-310e-482e-8c6e-6e98e1e67b66
keywords:
- TTM_NEWTOOLRECT dei messaggi Windows controlli
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
ms.openlocfilehash: 13889b0e9c0d80392b88130c33e5e9723ceb776a60a6b941d205d514d96ca22f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750981"
---
# <a name="ttm_newtoolrect-message"></a>TTM \_ NEWTOOLRECT message

Imposta un nuovo rettangolo di delimitazione per uno strumento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura TOOLINFO.**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) I **membri hwnd** **e uId** identificano uno strumento e il membro **rect** specifica il nuovo rettangolo di delimitazione. Il **membro cbSize** di questa struttura deve essere compilato prima di inviare questo messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TTM \_ NEWTOOLRECTW** (Unicode) e **TTM \_ NEWTOOLRECTA** (ANSI)<br/>           |



 

 





