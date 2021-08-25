---
title: EM_LINESCROLL messaggio (Winuser.h)
description: Scorre il testo in un controllo di modifica su più righe.
ms.assetid: 5398082d-f1ef-4a3a-9e5a-83cf286adbf1
keywords:
- EM_LINESCROLL controlli Windows messaggio
topic_type:
- apiref
api_name:
- EM_LINESCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6da4adbd789a8d9ae3344a1a49d39c7f5fbe22b7ec1ca51fcc6cead98ea7780
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048641"
---
# <a name="em_linescroll-message"></a>Messaggio \_ EM LINESCROLL

Scorre il testo in un controllo di modifica su più righe.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

**Controlli di modifica:** Numero di caratteri da scorrere orizzontalmente.

**Controlli Rich Edit:** Questo parametro non viene usato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Numero di righe da scorrere verticalmente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio viene inviato a un controllo di modifica su più righe, il valore restituito è **TRUE.**

Se il messaggio viene inviato a un controllo di modifica a riga singola, il valore restituito è **FALSE.**

## <a name="remarks"></a>Commenti

Il controllo non scorre verticalmente oltre l'ultima riga di testo nel controllo di modifica. Se la riga corrente più il numero di righe specificato dal *parametro lParam* supera il numero totale di righe nel controllo di modifica, il valore viene regolato in modo che l'ultima riga del controllo di modifica sia scorretta fino alla parte superiore della finestra del controllo di modifica.

**Controlli di modifica:** Il **messaggio EM \_ LINESCROLL** scorre il testo verticalmente o orizzontalmente in un controllo di modifica su più righe. Il **messaggio EM \_ LINESCROLL** può essere usato per scorrere orizzontalmente oltre l'ultimo carattere di qualsiasi riga.

**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive. Il **messaggio EM \_ LINESCROLL** scorre il testo verticalmente in un controllo di modifica su più righe. Per informazioni sulla compatibilità delle versioni rich edit con le diverse versioni del sistema, vedere [Informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



 

 





