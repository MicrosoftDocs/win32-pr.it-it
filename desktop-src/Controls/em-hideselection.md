---
title: Messaggio di EM_HIDESELECTION (RichEdit. h)
description: Il \_ messaggio HIDESELECTION em nasconde o Mostra la selezione in un controllo Rich Edit.
ms.assetid: 1245618f-c9e6-4876-9133-6009370cdb97
keywords:
- Controlli di Windows Message EM_HIDESELECTION
topic_type:
- apiref
api_name:
- EM_HIDESELECTION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a5690e52c2a25f5a359de205ac1584e1ef45ed4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963832"
---
# <a name="em_hideselection-message"></a>\_Messaggio HIDESELECTION em

Il **messaggio \_ HIDESELECTION em** nasconde o Mostra la selezione in un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore che specifica se nascondere o mostrare la selezione. Se questo parametro è zero, viene visualizzata la selezione. In caso contrario, la selezione sarà nascosta.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





