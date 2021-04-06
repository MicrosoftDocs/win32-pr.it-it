---
title: Messaggio DTM_SETMCCOLOR (COMmctrl. h)
description: Imposta il colore per una porzione specificata del calendario mensile all'interno di un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DateTime SetMonthCalColor.
ms.assetid: cee72c1d-58da-4ee5-850e-a615ec6ad079
keywords:
- Controlli di Windows Message DTM_SETMCCOLOR
topic_type:
- apiref
api_name:
- DTM_SETMCCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e496abb4dd28b040dd4a8035073ffa32a3f3847
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742562"
---
# <a name="dtm_setmccolor-message"></a>\_Messaggio SETMCCOLOR DTM

Imposta il colore per una porzione specificata del calendario mensile all'interno di un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ SetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) .

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

Valore **COLORREF** che rappresenta il colore che verrà impostato per l'area specificata del calendario mensile.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **COLORREF** che rappresenta l'impostazione del colore precedente per la parte specificata del controllo calendario mensile, se ha esito positivo. In caso contrario, il messaggio restituisce-1.

## <a name="remarks"></a>Commenti

Quando gli stili di visualizzazione sono abilitati, questo messaggio non ha alcun effetto tranne quando *wParam* è MCSC \_ sfondo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





