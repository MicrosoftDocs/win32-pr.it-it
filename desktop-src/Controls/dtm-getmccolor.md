---
title: Messaggio DTM_GETMCCOLOR (COMmctrl. h)
description: Ottiene il colore per una porzione specificata del calendario mensile all'interno di un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DateTime GetMonthCalColor.
ms.assetid: 892e8c23-f0d0-4fd6-98ed-39592c4d316f
keywords:
- Controlli di Windows Message DTM_GETMCCOLOR
topic_type:
- apiref
api_name:
- DTM_GETMCCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690c461c5bccbd050fb3d698d1a41c6d1e513944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479464"
---
# <a name="dtm_getmccolor-message"></a>\_Messaggio GETMCCOLOR DTM

Ottiene il colore per una porzione specificata del calendario mensile all'interno di un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ GetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore di tipo **int** che specifica il colore del calendario mensile da recuperare. I valori validi sono i seguenti:



| Valore                                                                                                                                                                     | Significato                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <dt>**\_sfondo MCSC**</dt> </dl>       | Recupera il colore di sfondo visualizzato tra i mesi.<br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <dt>**\_MONTHBK MCSC**</dt> </dl>                | Recupera il colore di sfondo visualizzato nel mese.<br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <dt>**\_testo MCSC**</dt> </dl>                         | Recupera il colore utilizzato per visualizzare il testo nel corso di un mese.<br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <dt>**\_TITLEBK MCSC**</dt> </dl>                | Recupera il colore di sfondo visualizzato nel titolo del calendario.<br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <dt>**\_TITLETEXT MCSC**</dt> </dl>          | Recupera il colore utilizzato per visualizzare il testo all'interno del titolo del calendario.<br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <dt>**\_TRAILINGTEXT MCSC**</dt> </dl> | Recupera il colore utilizzato per visualizzare il testo dell'intestazione e del giorno finale. Le intestazioni e i giorni finali sono i giorni dei mesi precedenti e successivi visualizzati nel calendario del mese corrente.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **COLORREF** che rappresenta l'impostazione del colore per la parte specificata del controllo calendario mensile, se ha esito positivo. Il messaggio restituisce-1 in caso di esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





