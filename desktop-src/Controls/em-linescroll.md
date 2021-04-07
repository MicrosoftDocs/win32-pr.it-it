---
title: Messaggio EM_LINESCROLL (winuser. h)
description: Scorre il testo in un controllo di modifica su più righe.
ms.assetid: 5398082d-f1ef-4a3a-9e5a-83cf286adbf1
keywords:
- Controlli di Windows Message EM_LINESCROLL
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
ms.openlocfilehash: 646e225ef269ccddca2cdc29caf635d94c1671e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048559"
---
# <a name="em_linescroll-message"></a>\_Messaggio LINESCROLL em

Scorre il testo in un controllo di modifica su più righe.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

**Controlli di modifica:** Numero di caratteri da scorrere orizzontalmente.

**Controlli Rich Edit:** Questo parametro non viene utilizzato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Numero di righe da scorrere verticalmente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio viene inviato a un controllo di modifica su più righe, il valore restituito è **true**.

Se il messaggio viene inviato a un controllo di modifica a riga singola, il valore restituito è **false**.

## <a name="remarks"></a>Commenti

Il controllo non scorre verticalmente oltre l'ultima riga di testo nel controllo di modifica. Se la riga corrente più il numero di righe specificato dal parametro *lParam* supera il numero totale di righe nel controllo di modifica, il valore viene regolato in modo che l'ultima riga del controllo di modifica venga spostata all'inizio della finestra di modifica del controllo.

**Controlli di modifica:** Il **messaggio \_ LINESCROLL em** scorre il testo verticalmente o orizzontalmente in un controllo di modifica su più righe. Il **messaggio \_ LINESCROLL em** può essere usato per scorrere orizzontalmente oltre l'ultimo carattere di una riga.

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Il **messaggio \_ LINESCROLL em** scorre verticalmente il testo in un controllo di modifica su più righe. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



 

 





