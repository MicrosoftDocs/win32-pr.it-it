---
title: Messaggio RB_SETBANDINFO (COMmctrl. h)
description: Imposta le caratteristiche di una banda esistente in un controllo Rebar.
ms.assetid: 00021c35-612d-4278-b10c-6e9f1f45a543
keywords:
- Controlli di Windows Message RB_SETBANDINFO
topic_type:
- apiref
api_name:
- RB_SETBANDINFO
- RB_SETBANDINFOA
- RB_SETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92e81377a40f8b6054f5d8cfae16837621b77b61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477866"
---
# <a name="rb_setbandinfo-message"></a>\_Messaggio SETBANDINFO RB

Imposta le caratteristiche di una banda esistente in un controllo Rebar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della banda per ricevere le nuove impostazioni.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) che definisce la banda da modificare e le nuove impostazioni. Prima di inviare questo messaggio, è necessario impostare il membro **cbSize** della struttura sulla struttura **sizeof**(REBARBANDINFO). Inoltre, è necessario impostare il **membro** REBARBANDINFO della struttura  sulla dimensione del buffer **lpText** quando \_ viene specificato il testo RBBIM.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **RB \_ SETBANDINFOW** (Unicode) e **RB \_ SETBANDINFOA** (ANSI)<br/>             |



 

 





