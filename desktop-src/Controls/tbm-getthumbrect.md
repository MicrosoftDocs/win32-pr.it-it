---
title: TBM_GETTHUMBRECT messaggio (Commctrl.h)
description: Recupera le dimensioni e la posizione del rettangolo di delimitazione per il dispositivo di scorrimento in un trackbar.
ms.assetid: f53fd7af-36f8-4490-aa95-f1fa20f34efb
keywords:
- TBM_GETTHUMBRECT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TBM_GETTHUMBRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4d2582ccfb5276f65cbf1187458774622e62f6dd87d8dcadd2e16a7447f769a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046361"
---
# <a name="tbm_getthumbrect-message"></a>Messaggio \_ GETTHUMBRECT TBM

Recupera le dimensioni e la posizione del rettangolo di delimitazione per il dispositivo di scorrimento in un trackbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura RECT.**](/previous-versions//dd162897(v=vs.85)) Il messaggio riempie questa struttura con il rettangolo di delimitazione del dispositivo di scorrimento del trackbar nelle coordinate client della finestra del trackbar.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

