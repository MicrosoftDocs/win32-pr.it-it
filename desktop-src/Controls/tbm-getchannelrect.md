---
title: TBM_GETCHANNELRECT messaggio (Commctrl.h)
description: Recupera le dimensioni e la posizione del rettangolo di delimitazione per il canale di un trackbar.
ms.assetid: 353edae3-1a26-4e85-8a32-ba8b5a976d24
keywords:
- TBM_GETCHANNELRECT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TBM_GETCHANNELRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af2c9932782a150635365c1cdcb74b624f6863b27180136bc9483e8d0de3ba1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078105"
---
# <a name="tbm_getchannelrect-message"></a>Messaggio \_ TBM GETCHANNELRECT

Recupera le dimensioni e la posizione del rettangolo di delimitazione per il canale di un trackbar. Il canale è l'area su cui si sposta il dispositivo di scorrimento. Contiene l'evidenziazione quando viene selezionato un intervallo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura RECT.**](/previous-versions//dd162897(v=vs.85)) Il messaggio riempie questa struttura con il rettangolo di delimitazione del canale, nelle coordinate client della finestra del trackbar.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

