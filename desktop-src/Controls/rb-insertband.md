---
title: Messaggio RB_INSERTBAND (COMmctrl. h)
description: Inserisce una nuova banda in un controllo Rebar.
ms.assetid: ac621f65-b8ab-41d6-928d-a48fbea572e7
keywords:
- Controlli di Windows Message RB_INSERTBAND
topic_type:
- apiref
api_name:
- RB_INSERTBAND
- RB_INSERTBANDA
- RB_INSERTBANDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39b45eb662fb4c2058b87837352339c84762188
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874685"
---
# <a name="rb_insertband-message"></a>\_Messaggio INSERTBAND RB

Inserisce una nuova banda in un controllo Rebar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della posizione in cui verrà inserita la banda. Se questo parametro viene impostato su-1, il controllo aggiungerà la nuova banda nell'ultima posizione.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) che definisce la banda da inserire. Prima di inviare questo messaggio, è necessario impostare il membro **cbSize** della struttura su **sizeof**(REBARBANDINFO).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **RB \_ INSERTBANDW** (Unicode) e **RB \_ INSERTBANDA** (ANSI)<br/>               |



 

 





