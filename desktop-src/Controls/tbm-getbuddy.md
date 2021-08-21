---
title: TBM_GETBUDDY messaggio (Commctrl.h)
description: Recupera l'handle per una finestra del controllo trackbar in una determinata posizione. La posizione specificata è relativa all'orientamento del controllo (orizzontale o verticale).
ms.assetid: 69e4e467-150d-4505-b1c2-2ed9dd83f1a6
keywords:
- TBM_GETBUDDY di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TBM_GETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e03053981ed16b97d68d5b2f0c77db64062d64fd2df7b5a347e4757736d4844
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829615"
---
# <a name="tbm_getbuddy-message"></a>Messaggio \_ GETBUDDY TBM

Recupera l'handle per una finestra del controllo trackbar in una determinata posizione. La posizione specificata è relativa all'orientamento del controllo (orizzontale o verticale).

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore che indica l'handle della finestra di controllo che verrà recuperato, in base alla posizione relativa. I valori validi sono i seguenti:



| Valore                                                                                                                                    | Significato                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE****</dt> </dl>    | Recupera l'handle per il controllo a sinistra del trackbar. Se il controllo trackbar usa lo [**stile TBS \_ VERT,**](trackbar-control-styles.md) il messaggio recupererà l'amico sopra il trackbar.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE****</dt> </dl> | Recupera l'handle per il controllo a destra del trackbar. Se il controllo trackbar usa lo [**stile TBS \_ VERT,**](trackbar-control-styles.md) il messaggio recupererà l'amico sotto il trackbar.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle alla finestra degli amici nella posizione specificata da *wParam* o **NULL** se in tale posizione non è presente alcuna finestra di tipo amico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





