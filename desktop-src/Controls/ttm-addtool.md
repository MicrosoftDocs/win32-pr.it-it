---
title: Messaggio TTM_ADDTOOL (COMmctrl. h)
description: Registra uno strumento con un controllo ToolTip.
ms.assetid: c974866b-20e7-45bc-914e-9dcf9af161e0
keywords:
- Controlli di Windows Message TTM_ADDTOOL
topic_type:
- apiref
api_name:
- TTM_ADDTOOL
- TTM_ADDTOOLA
- TTM_ADDTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29dad3e297f8c3430f18286afa9a998eaf578a26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301658"
---
# <a name="ttm_addtool-message"></a>\_Messaggio TTM ADDTOOL

Registra uno strumento con un controllo ToolTip.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) contenente le informazioni necessarie al controllo ToolTip per visualizzare il testo per lo strumento. Prima di inviare questo messaggio, è necessario compilare il membro **cbSize** della struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TTM \_ ADDTOOLW** (Unicode) e **TTM \_ ADDTOOLA** (ANSI)<br/>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_DELTOOL TTM**](ttm-deltool.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni sui controlli ToolTip](tooltip-controls.md)
</dt> </dl>

 

 





