---
title: Messaggio di EM_PASTESPECIAL (RichEdit. h)
description: Incolla un formato degli Appunti specifico in un controllo Rich Edit.
ms.assetid: b4b9c1a7-943d-4dc8-bcb9-054c984b82ba
keywords:
- Controlli di Windows Message EM_PASTESPECIAL
topic_type:
- apiref
api_name:
- EM_PASTESPECIAL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9375dd4a333f0e29d5e8f2721409244cf80f1233
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874045"
---
# <a name="em_pastespecial-message"></a>\_Messaggio PASTESPECIAL em

Incolla un formato degli Appunti specifico in un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica i [formati degli Appunti](/windows/desktop/dataxchg/clipboard-formats).

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial) o **null**. Se un oggetto viene incollato, la struttura **REPASTESPECIAL** viene compilata con l'aspetto di visualizzazione desiderato. Se *lParam* è **null** o il membro **dwAspect** è zero, l'aspetto di visualizzazione usato sarà il contenuto del descrittore dell'oggetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial)
</dt> </dl>

 

