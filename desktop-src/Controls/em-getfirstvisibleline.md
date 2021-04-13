---
title: Messaggio EM_GETFIRSTVISIBLELINE (winuser. h)
description: Ottiene l'indice in base zero della riga visibile in alto in un controllo di modifica su più righe. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 022838d2-7948-4c5a-92ca-655822c4f672
keywords:
- Controlli di Windows Message EM_GETFIRSTVISIBLELINE
topic_type:
- apiref
api_name:
- EM_GETFIRSTVISIBLELINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb759be166b69b3cfa488e9e23d61d9e0ec42d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518303"
---
# <a name="em_getfirstvisibleline-message"></a>\_Messaggio GETFIRSTVISIBLELINE em

Ottiene l'indice in base zero della riga visibile in alto in un controllo di modifica su più righe. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'indice in base zero della riga visibile in alto in un controllo di modifica su più righe.

**Controlli di modifica:** Per i controlli di modifica a riga singola, il valore restituito è l'indice in base zero del primo carattere visibile.

**Controlli Rich Edit:** Per i controlli Rich Edit a riga singola, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Il numero di righe e la lunghezza delle righe in un controllo di modifica dipendono dalla larghezza del controllo e dall'impostazione corrente di WordWrap.

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



 

 





