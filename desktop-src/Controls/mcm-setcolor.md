---
title: MCM_SETCOLOR messaggio (Commctrl.h)
description: Imposta il colore per una determinata parte di un controllo calendario mensile. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro MonthCal SetColor.
ms.assetid: 4ceb7b0e-82be-474a-a163-7e71356818c0
keywords:
- MCM_SETCOLOR dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- MCM_SETCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0915f78ad2dc666d6476cebb51be4f8b8c6102cb1433da59af7b9a1342deedc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697151"
---
# <a name="mcm_setcolor-message"></a>Messaggio \_ MCM SETCOLOR

Imposta il colore per una determinata parte di un controllo calendario mensile. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ MonthCal SetColor.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcolor)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore di tipo **int** che specifica il colore del calendario mensile da impostare. I valori validi sono i seguenti:



| Valore                                                                                                                                                                     | Significato                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <dt>**MCSC \_ BACKGROUND**</dt> </dl>       | Impostare il colore di sfondo visualizzato tra i mesi.<br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <dt>**MCSC \_ MONTHBK**</dt> </dl>                | Impostare il colore di sfondo visualizzato all'interno del mese.<br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <dt>**TESTO \_ MCSC**</dt> </dl>                         | Impostare il colore usato per visualizzare il testo entro un mese.<br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <dt>**MCSC \_ TITLEBK**</dt> </dl>                | Impostare il colore di sfondo visualizzato nel titolo del calendario.<br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <dt>**MCSC \_ TITLETEXT**</dt> </dl>          | Impostare il colore usato per visualizzare il testo all'interno del titolo del calendario.<br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <dt>**MCSC \_ TRAILINGTEXT**</dt> </dl> | Impostare il colore usato per visualizzare il testo del giorno dell'intestazione e del giorno finale. I giorni di intestazione e di fine sono i giorni dei mesi precedenti e successivi visualizzati nel calendario del mese corrente.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**Valore COLORREF**](/windows/desktop/gdi/colorref) che rappresenta il colore che verrà impostato per l'area specificata del calendario mensile.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un [**valore COLORREF**](/windows/desktop/gdi/colorref) che rappresenta l'impostazione del colore precedente per la parte specificata del controllo calendario mensile in caso di esito positivo. In caso contrario, il valore restituito è -1.

## <a name="remarks"></a>Commenti

Se gli stili di visualizzazione sono attivi, questo messaggio non ha alcun effetto tranne quando *wParam* è MCSC \_ BACKGROUND.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

