---
title: Messaggio EM_GETLIMITTEXT (winuser. h)
description: Ottiene il limite di testo corrente per un controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 778967f0-c090-46a2-9f27-194b17bbb1be
keywords:
- Controlli di Windows Message EM_GETLIMITTEXT
topic_type:
- apiref
api_name:
- EM_GETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53da76f43716fd7934011a96d449ffa37c254cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873389"
---
# <a name="em_getlimittext-message"></a>\_Messaggio GETLIMITTEXT em

Ottiene il limite di testo corrente per un controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

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

Il valore restituito è il limite di testo.

## <a name="remarks"></a>Commenti

**Modificare i controlli, rich edit 2,0 e versioni successive:** Il limite di testo è la quantità massima di testo, in **TCHAR** s, che il controllo può contenere. Per testo ANSI, indica il numero di byte; per il testo Unicode, indica il numero di caratteri. Due documenti con lo stesso limite di caratteri produrranno lo stesso limite di testo, anche se uno è ANSI e l'altro è Unicode.

**Modifica dettagliata 1,0:** Il limite di testo è la quantità massima di testo, in byte, che il controllo Rich Edit può contenere.

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETLIMITTEXT em**](em-setlimittext.md)
</dt> </dl>

 

 





