---
title: MCM_GETCOLOR messaggio (Commctrl.h)
description: Recupera il colore per una determinata parte di un controllo calendario mensile. È possibile inviare questo messaggio in modo esplicito o tramite la macro GetColor di \_ MonthCal.
ms.assetid: 6c30ad0d-7584-402a-9c27-3c12c49c87f3
keywords:
- MCM_GETCOLOR di Windows messaggi
topic_type:
- apiref
api_name:
- MCM_GETCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 254b140e801f4d4440c9b292999e5c8f91175a30750b08bfd30abd6afd84f73d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062091"
---
# <a name="mcm_getcolor-message"></a>Messaggio \_ MCM GETCOLOR

Recupera il colore per una determinata parte di un controllo calendario mensile. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ GetColor di MonthCal.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcolor)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore di tipo **int** che specifica il colore del calendario mensile da recuperare. I valori validi sono i seguenti:



| Valore                                                                                                                                                                     | Significato                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <dt>**MCSC \_ BACKGROUND**</dt> </dl>       | Recupera il colore di sfondo visualizzato tra i mesi.<br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <dt>**MCSC \_ MONTHBK**</dt> </dl>                | Recupera il colore di sfondo visualizzato all'interno del mese.<br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <dt>**TESTO \_ MCSC**</dt> </dl>                         | Recupera il colore usato per visualizzare il testo entro un mese.<br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <dt>**MCSC \_ TITLEBK**</dt> </dl>                | Recupera il colore di sfondo visualizzato nel titolo del calendario.<br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <dt>**MCSC \_ TITLETEXT**</dt> </dl>          | Recupera il colore usato per visualizzare il testo all'interno del titolo del calendario.<br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <dt>**MCSC \_ TRAILINGTEXT**</dt> </dl> | Recupera il colore usato per visualizzare il testo del giorno dell'intestazione e del giorno finale. L'intestazione e i giorni finali sono i giorni dei mesi precedenti e successivi visualizzati nel calendario mensile corrente.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore COLORREF** che rappresenta l'impostazione del colore per la parte specificata del controllo calendario mensile in caso di esito positivo. In caso contrario, questo messaggio restituisce -1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





