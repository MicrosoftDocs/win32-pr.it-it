---
title: Messaggio MCM_SETCOLOR (COMmctrl. h)
description: Imposta il colore per una determinata parte di un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal Secolor.
ms.assetid: 4ceb7b0e-82be-474a-a163-7e71356818c0
keywords:
- Controlli di Windows Message MCM_SETCOLOR
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
ms.openlocfilehash: 476aafd8356359cf6b4313f4b945253af6b493c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121310"
---
# <a name="mcm_setcolor-message"></a>\_Messaggio di SECOLORI MCM

Imposta il colore per una determinata parte di un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ Secolor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcolor) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore di tipo **int** che specifica il colore del calendario mensile da impostare. I valori validi sono i seguenti:



| Valore                                                                                                                                                                     | Significato                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <dt>**\_sfondo MCSC**</dt> </dl>       | Imposta il colore di sfondo visualizzato tra i mesi.<br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <dt>**\_MONTHBK MCSC**</dt> </dl>                | Imposta il colore di sfondo visualizzato nel mese.<br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <dt>**\_testo MCSC**</dt> </dl>                         | Imposta il colore utilizzato per visualizzare il testo all'interno di un mese.<br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <dt>**\_TITLEBK MCSC**</dt> </dl>                | Imposta il colore di sfondo visualizzato nel titolo del calendario.<br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <dt>**\_TITLETEXT MCSC**</dt> </dl>          | Consente di impostare il colore utilizzato per visualizzare il testo all'interno del titolo del calendario.<br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <dt>**\_TRAILINGTEXT MCSC**</dt> </dl> | Imposta il colore utilizzato per visualizzare il testo dell'intestazione e il giorno finale. Le intestazioni e i giorni finali sono i giorni dei mesi precedenti e successivi visualizzati nel calendario del mese corrente.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Valore [**COLORREF**](/windows/desktop/gdi/colorref) che rappresenta il colore che verrà impostato per l'area specificata del calendario mensile.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore [**COLORREF**](/windows/desktop/gdi/colorref) che rappresenta l'impostazione del colore precedente per la parte specificata del controllo calendario mensile, se ha esito positivo. In caso contrario, il risultato restituito è-1.

## <a name="remarks"></a>Commenti

Se gli stili di visualizzazione sono attivi, questo messaggio non ha alcun effetto tranne quando *wParam* è MCSC \_ sfondo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

