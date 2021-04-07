---
title: Messaggio EM_LINEINDEX (winuser. h)
description: Ottiene l'indice dei caratteri del primo carattere di una riga specificata in un controllo di modifica su più righe.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- Controlli di Windows Message EM_LINEINDEX
topic_type:
- apiref
api_name:
- EM_LINEINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611d4ff892f95287c45166ae55ff2389f454512c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964053"
---
# <a name="em_lineindex-message-winuserh"></a>Messaggio EM_LINEINDEX (winuser. h)

Ottiene l'indice dei caratteri del primo carattere di una riga specificata in un controllo di modifica su più righe. Un indice dei caratteri è l'indice in base zero del carattere a partire dall'inizio del controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di riga in base zero. Il valore-1 specifica il numero di riga corrente, ovvero la riga che contiene il punto di inserimento.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'indice dei caratteri della riga specificata nel parametro *wParam* oppure è-1 se il numero di riga specificato è maggiore del numero di righe nel controllo di modifica.

## <a name="remarks"></a>Commenti

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_LINEFROMCHAR em**](em-linefromchar.md)
</dt> </dl>

 

 





