---
title: Messaggio di EM_SETBKGNDCOLOR (RichEdit. h)
description: Il \_ messaggio SETBKGNDCOLOR em imposta il colore di sfondo per un controllo Rich Edit.
ms.assetid: 0ad191cd-6370-493e-bfe2-5aa8d81ed999
keywords:
- Controlli di Windows Message EM_SETBKGNDCOLOR
topic_type:
- apiref
api_name:
- EM_SETBKGNDCOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091f04909e2660498f1380628439c067b5438b6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874361"
---
# <a name="em_setbkgndcolor-message"></a>\_Messaggio SETBKGNDCOLOR em

Il **messaggio \_ SETBKGNDCOLOR em** imposta il colore di sfondo per un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica se utilizzare il colore di sistema. Se questo parametro è un valore diverso da zero, lo sfondo viene impostato sul colore di sistema dello sfondo della finestra. In caso contrario, lo sfondo viene impostato sul colore specificato.

</dd> <dt>

*lParam* 
</dt> <dd>

Struttura [**COLORREF**](/windows/desktop/gdi/colorref) che specifica il colore se *wParam* è zero. Per generare un **COLORREF**, usare la macro [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce il colore di sfondo originale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Altre risorse**
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> <dt>

[**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> </dl>

 

