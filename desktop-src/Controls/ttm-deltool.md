---
title: Messaggio TTM_DELTOOL (COMmctrl. h)
description: Rimuove uno strumento da un controllo ToolTip.
ms.assetid: 433b6f1c-3e9f-4e3a-9834-d447a3f9e6a5
keywords:
- Controlli di Windows Message TTM_DELTOOL
topic_type:
- apiref
api_name:
- TTM_DELTOOL
- TTM_DELTOOLA
- TTM_DELTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d943259c5496757c0f15ca4127d0a5e6a4237fbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301657"
---
# <a name="ttm_deltool-message"></a>\_Messaggio TTM DELTOOL

Rimuove uno strumento da un controllo ToolTip.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . I membri **HWND** e **UID** identificano lo strumento da rimuovere e il membro **cbSize** deve specificare le dimensioni della struttura. Tutti gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TTM \_ DELTOOLW** (Unicode) e **TTM \_ DELTOOLA** (ANSI)<br/>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_ADDTOOL TTM**](ttm-addtool.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni sui controlli ToolTip](tooltip-controls.md)
</dt> </dl>

 

 





