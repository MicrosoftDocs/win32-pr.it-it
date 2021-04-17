---
title: Messaggio PGM_RECALCSIZE (COMmctrl. h)
description: Impone al controllo pager di ricalcolare la dimensione della finestra contenuta. L'invio di questo messaggio comporterà l'invio di una \_ notifica PGN CALCSIZE. È possibile inviare questo messaggio in modo esplicito o utilizzare la \_ macro RecalcSize del cercapersone.
ms.assetid: 51b75ce8-2b41-4f1a-830e-b25e7d77dccb
keywords:
- Controlli di Windows Message PGM_RECALCSIZE
topic_type:
- apiref
api_name:
- PGM_RECALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b407221543a42b4dbff4490508a02b570622d69c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476312"
---
# <a name="pgm_recalcsize-message"></a>\_Messaggio RECALCSIZE PGM

Impone al controllo pager di ricalcolare la dimensione della finestra contenuta. L'invio di questo messaggio comporterà l'invio di una notifica [PGN \_ CALCSIZE](pgn-calcsize.md) . È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ RecalcSize del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





