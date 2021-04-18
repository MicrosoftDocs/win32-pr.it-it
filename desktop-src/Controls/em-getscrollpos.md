---
title: Messaggio di EM_GETSCROLLPOS (RichEdit. h)
description: Ottiene la posizione di scorrimento corrente del controllo di modifica.
ms.assetid: 26e122da-f1b4-4694-978c-ff678dad5d9f
keywords:
- Controlli di Windows Message EM_GETSCROLLPOS
topic_type:
- apiref
api_name:
- EM_GETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70458abca94e483f8e202f13ecaed3df04a68366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476486"
---
# <a name="em_getscrollpos-message"></a>\_Messaggio GETSCROLLPOS em

Ottiene la posizione di scorrimento corrente del controllo di modifica.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura di [**punti**](/previous-versions//dd162805(v=vs.85)) . Dopo la chiamata di **em \_ GETSCROLLPOS**, questo parametro contiene un punto nello spazio del testo virtuale del documento, espresso in pixel. Questo punto sarà il punto attualmente disponibile nell'angolo superiore sinistro della finestra di controllo di modifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce sempre 1.

## <a name="remarks"></a>Commenti

I valori restituiti nella struttura [**Point**](/previous-versions//dd162805(v=vs.85)) sono valori a 16 bit, anche nei campi wide a 32 bit.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Componente ridistribuibile<br/>          | Modifica avanzata 3,0<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETSCROLLPOS em**](em-setscrollpos.md)
</dt> </dl>

 

