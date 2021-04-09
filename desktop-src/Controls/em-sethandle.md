---
title: Messaggio EM_SETHANDLE (winuser. h)
description: Imposta l'handle della memoria che verrà utilizzata da un controllo di modifica su più righe.
ms.assetid: 0eae9365-62af-4040-8a51-273997a00b81
keywords:
- Controlli di Windows Message EM_SETHANDLE
topic_type:
- apiref
api_name:
- EM_SETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8f918d056db1000c6018f55d89095a73a15109
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121034"
---
# <a name="em_sethandle-message"></a>\_Messaggio filehandle em

Imposta l'handle della memoria che verrà utilizzata da un controllo di modifica su più righe.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il buffer di memoria utilizzato dal controllo di modifica per archiviare il testo attualmente visualizzato anziché allocare la propria memoria. Se necessario, il controllo rialloca la memoria.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Prima che un'applicazione imposti un nuovo handle di memoria, deve inviare un messaggio [**\_ GetHandle em**](em-gethandle.md) per recuperare l'handle del buffer di memoria corrente e liberare tale memoria.

Un controllo di modifica rialloca automaticamente il buffer specificato ogni volta che è necessario spazio aggiuntivo per il testo o rimuove un testo sufficiente, in modo che non sia più necessario spazio aggiuntivo.

L'invio di un messaggio di controllo **\_ em** Cancella il buffer di annullamento ([**em \_ CANUNDO**](em-canundo.md) restituisce zero) e il flag di modifica interno ([**em \_ GetModify**](em-getmodify.md) restituisce zero). La finestra modifica controllo viene ridisegnato.

**Modifica avanzata:** Il messaggio della **\_ gestione** dei messaggi em non è supportato. I controlli Rich Edit non archiviano il testo come una semplice matrice di caratteri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_CANUNDO em**](em-canundo.md)
</dt> <dt>

[**GetHandle EM \_**](em-gethandle.md)
</dt> <dt>

[**GetModify EM \_**](em-getmodify.md)
</dt> </dl>

 

 





