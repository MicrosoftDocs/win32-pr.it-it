---
title: EM_PASTESPECIAL messaggio (Richedit.h)
description: Incolla un formato degli Appunti specifico in un controllo Rich Edit.
ms.assetid: b4b9c1a7-943d-4dc8-bcb9-054c984b82ba
keywords:
- EM_PASTESPECIAL dei messaggi Windows controlli
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
ms.openlocfilehash: 2dc1af4dd0566cdf8e256b34f87fcc52ea855bc521c87cbe390e02b8b1cf7b06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412802"
---
# <a name="em_pastespecial-message"></a>MESSAGGIO \_ EM PASTESPECIAL

Incolla un formato degli Appunti specifico in un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica i formati [degli Appunti.](/windows/desktop/dataxchg/clipboard-formats)

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial) o **NULL.** Se un oggetto viene incollato, la **struttura REPASTESPECIAL** viene compilata con l'aspetto di visualizzazione desiderato. Se *lParam* è **NULL** o **il membro dwAspect** è zero, l'aspetto di visualizzazione usato sarà il contenuto del descrittore di oggetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial)
</dt> </dl>

 

