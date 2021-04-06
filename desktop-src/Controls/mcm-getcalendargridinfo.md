---
title: Messaggio MCM_GETCALENDARGRIDINFO (COMmctrl. h)
description: Ottiene informazioni su una griglia di calendari.
ms.assetid: 6b385362-f963-4041-bc9f-d2b7a890c9b4
keywords:
- Controlli di Windows Message MCM_GETCALENDARGRIDINFO
topic_type:
- apiref
api_name:
- MCM_GETCALENDARGRIDINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506f6193ab32d059bb85fa4583441bfbe027f224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743994"
---
# <a name="mcm_getcalendargridinfo-message"></a>\_Messaggio GETCALENDARGRIDINFO MCM

Ottiene informazioni su una griglia di calendari.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**MCGRIDINFO**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo) contenente informazioni sulla griglia del calendario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**True** se ha esito positivo, in caso contrario **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





