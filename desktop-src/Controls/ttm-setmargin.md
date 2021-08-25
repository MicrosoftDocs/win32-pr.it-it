---
title: TTM_SETMARGIN messaggio (Commctrl.h)
description: Imposta i margini superiore, sinistro, inferiore e destro per una finestra della descrizione comando. Un margine è la distanza, in pixel, tra il bordo della finestra della descrizione comando e il testo contenuto nella finestra della descrizione comando.
ms.assetid: f1663861-c217-42dd-8249-7647b1651910
keywords:
- TTM_SETMARGIN dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- TTM_SETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04e5792b33f7f9f5a997759ba390c1b8a713308f95c4ba3f7b5cd0460747ff62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914061"
---
# <a name="ttm_setmargin-message"></a>TTM \_ SETMARGIN message

Imposta i margini superiore, sinistro, inferiore e destro per una finestra della descrizione comando. Un margine è la distanza, in pixel, tra il bordo della finestra della descrizione comando e il testo contenuto nella finestra della descrizione comando.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura RECT**](/previous-versions//dd162897(v=vs.85)) che contiene le informazioni sul margine da impostare. I membri della struttura **RECT** non definiscono un rettangolo di delimitazione. Ai fini di questo messaggio, i membri della struttura vengono interpretati come segue:



| Valore                                                                                                                                   | Significato                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <dt>**In alto**</dt> </dl>          | Distanza, in pixel, tra il bordo superiore e la parte superiore del testo della descrizione comando.<br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <dt>**Sinistra**</dt> </dl>       | Distanza, in pixel, tra il bordo sinistro e l'estremità sinistra del testo della descrizione comando.<br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <dt>**Fondoschiena**</dt> </dl> | Distanza, in pixel, tra il bordo inferiore e la parte inferiore del testo della descrizione comando.<br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <dt>**va bene**</dt> </dl>    | Distanza, in pixel, tra il bordo destro e l'estremità destra del testo della descrizione comando.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene utilizzato.

## <a name="remarks"></a>Commenti

Questo messaggio non ha alcun effetto quando l'applicazione viene eseguita Windows Vista e gli stili di visualizzazione sono abilitati per la descrizione comando. È possibile disabilitare gli stili di visualizzazione per la descrizione comando [**usando SetWindowTheme.**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TTM \_ GETMARGIN**](ttm-getmargin.md)
</dt> </dl>

 

