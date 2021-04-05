---
title: Messaggio TTM_UPDATETIPTEXT (COMmctrl. h)
description: Imposta il testo della descrizione comando per uno strumento.
ms.assetid: 2a7432dd-76f9-42b4-b639-178dce1d89ef
keywords:
- Controlli di Windows Message TTM_UPDATETIPTEXT
topic_type:
- apiref
api_name:
- TTM_UPDATETIPTEXT
- TTM_UPDATETIPTEXTA
- TTM_UPDATETIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6c94b14ec83c190ce019ecba1413d2fa05f0103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120274"
---
# <a name="ttm_updatetiptext-message"></a>\_Messaggio TTM UPDATETIPTEXT

Imposta il testo della descrizione comando per uno strumento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . I membri **hInst** e **lpszText** devono specificare l'handle dell'istanza e l'indirizzo del testo. I membri **HWND** e **UID** identificano lo strumento da aggiornare. Prima di inviare questo messaggio, è necessario compilare il membro **cbSize** della struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TTM \_ UPDATETIPTEXTW** (Unicode) e **TTM \_ UPDATETIPTEXTA** (ANSI)<br/>       |



 

 





