---
title: Messaggio TTM_WINDOWFROMPOINT (COMmctrl. h)
description: Consente a una routine di sottoclasse di fare in modo che una descrizione comando visualizzi un testo per una finestra diversa da quella sotto il cursore del mouse.
ms.assetid: f3bf6917-1745-4e4f-a9c1-8fe86b2b3906
keywords:
- Controlli di Windows Message TTM_WINDOWFROMPOINT
topic_type:
- apiref
api_name:
- TTM_WINDOWFROMPOINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68679f6b6c2477a8279c22f11d0d300e44c8370d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742258"
---
# <a name="ttm_windowfrompoint-message"></a>\_Messaggio TTM WINDOWFROMPOINT

Consente a una routine di sottoclasse di fare in modo che una descrizione comando visualizzi un testo per una finestra diversa da quella sotto il cursore del mouse.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura di [**punti**](/previous-versions//dd162805(v=vs.85)) che definisce il punto da controllare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'handle della finestra che contiene il punto oppure **null** se nessuna finestra è presente nel punto specificato.

## <a name="remarks"></a>Commenti

Questo messaggio deve essere elaborato da un'applicazione che sottoclassa una descrizione comando. Non è destinato a essere inviato da un'applicazione. Una descrizione comando Invia questo messaggio a se stesso prima di visualizzare il testo di una finestra. Modificando le coordinate del punto specificato da *lParam*, la procedura della sottoclasse può causare la visualizzazione del testo di una finestra diversa da quella sotto il cursore del mouse da parte della descrizione comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

