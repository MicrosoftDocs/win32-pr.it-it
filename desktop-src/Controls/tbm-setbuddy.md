---
title: TBM_SETBUDDY messaggio (Commctrl.h)
description: Assegna una finestra come finestra degli amici per un controllo trackbar. Le finestre di controllo trackbar vengono visualizzate automaticamente in una posizione relativa all'orientamento del controllo (orizzontale o verticale).
ms.assetid: ab35911f-bf81-47f3-98aa-0901aa877dea
keywords:
- TBM_SETBUDDY di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TBM_SETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4f2586c84740cb2d5e8b1f1aadfb910cd241270d3e18363accf1f166c3c35ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167187"
---
# <a name="tbm_setbuddy-message"></a>Messaggio \_ SETBUDDY TBM

Assegna una finestra come finestra degli amici per un controllo trackbar. Le finestre di controllo trackbar vengono visualizzate automaticamente in una posizione relativa all'orientamento del controllo (orizzontale o verticale).

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore che specifica la posizione in cui visualizzare la finestra del controllo utente. I valori validi sono i seguenti:



| Valore                                                                                                                                | Significato                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>**true**</dt> </dl>    | L'amico verrà visualizzato a sinistra del trackbar se il controllo trackbar usa lo stile [**TBS \_ HORZ.**](trackbar-control-styles.md) Se il trackbar usa lo [**stile TBS \_ VERT,**](trackbar-control-styles.md) l'amico viene visualizzato sopra il controllo trackbar.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>**False**</dt> </dl> | L'amico verrà visualizzato a destra del trackbar se il controllo trackbar usa lo stile [**TBS \_ HORZ.**](trackbar-control-styles.md) Se il trackbar usa lo [**stile TBS \_ VERT,**](trackbar-control-styles.md) l'amico viene visualizzato sotto il controllo trackbar.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la finestra che verrà impostata come amico del controllo trackbar.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle alla finestra assegnata in precedenza al controllo in tale posizione.

## <a name="remarks"></a>Commenti

> [!Note]  
> I controlli Trackbar supportano fino a due finestre di controllo. Può essere utile quando è necessario visualizzare testo o immagini a ogni estremità del controllo.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





