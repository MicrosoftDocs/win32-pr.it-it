---
title: EM_SETBKGNDCOLOR messaggio (Richedit.h)
description: Il messaggio EM \_ SETBKGNDCOLOR imposta il colore di sfondo per un controllo Rich Edit.
ms.assetid: 0ad191cd-6370-493e-bfe2-5aa8d81ed999
keywords:
- EM_SETBKGNDCOLOR di Windows messaggi
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
ms.openlocfilehash: 1173c2da9f3c04e49211224bd269d79c0634e1cb3f8ea959f6b58e354fdf0dda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412655"
---
# <a name="em_setbkgndcolor-message"></a>Messaggio \_ EM SETBKGNDCOLOR

Il **messaggio EM \_ SETBKGNDCOLOR** imposta il colore di sfondo per un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica se utilizzare il colore di sistema. Se questo parametro è un valore diverso da zero, lo sfondo viene impostato sul colore di sistema dello sfondo della finestra. In caso contrario, lo sfondo viene impostato sul colore specificato.

</dd> <dt>

*lParam* 
</dt> <dd>

Struttura [**COLORREF**](/windows/desktop/gdi/colorref) che specifica il colore se *wParam* è zero. Per generare un **COLORREF,** usare la macro [**RGB.**](/windows/desktop/api/wingdi/nf-wingdi-rgb)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce il colore di sfondo originale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Altre risorse**
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> <dt>

[**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> </dl>

 

