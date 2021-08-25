---
title: DTM_SETMCCOLOR messaggio (Commctrl.h)
description: Imposta il colore per una determinata parte del calendario mensile all'interno di un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DateTime SetMonthCalColor.
ms.assetid: cee72c1d-58da-4ee5-850e-a615ec6ad079
keywords:
- DTM_SETMCCOLOR dei messaggi Windows controlli
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
ms.openlocfilehash: 5154c2e450f5ef3c12c85fe3307f37958fea807226ab436241038c9ad639d4dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877821"
---
# <a name="dtm_setmccolor-message"></a>Messaggio DTM \_ SETMCCOLOR

Imposta il colore per una determinata parte del calendario mensile all'interno di un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ DateTime SetMonthCalColor.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor)

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

Valore **COLORREF** che rappresenta il colore che verrà impostato per l'area specificata del calendario mensile.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore COLORREF** che rappresenta l'impostazione del colore precedente per la parte specificata del controllo calendario mensile in caso di esito positivo. In caso contrario, il messaggio restituisce -1.

## <a name="remarks"></a>Commenti

Quando gli stili di visualizzazione sono abilitati, questo messaggio non ha alcun effetto tranne quando *wParam* è MCSC \_ BACKGROUND.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





