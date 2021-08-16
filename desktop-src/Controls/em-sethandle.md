---
title: EM_SETHANDLE messaggio (Winuser.h)
description: Imposta l'handle della memoria che verrà utilizzata da un controllo di modifica su più righe.
ms.assetid: 0eae9365-62af-4040-8a51-273997a00b81
keywords:
- EM_SETHANDLE controlli di Windows messaggio
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
ms.openlocfilehash: b3ece3eb9c385b5f4d468a7dd2f08ff3335a4314b4c90569cdba453c4815728f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412592"
---
# <a name="em_sethandle-message"></a>Messaggio \_ EM SETHANDLE

Imposta l'handle della memoria che verrà utilizzata da un controllo di modifica su più righe.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il buffer di memoria utilizzato dal controllo di modifica per archiviare il testo attualmente visualizzato anziché allocare la propria memoria. Se necessario, il controllo rialloca questa memoria.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Prima di impostare un nuovo handle di memoria, un'applicazione deve inviare un messaggio [**EM \_ GETHANDLE**](em-gethandle.md) per recuperare l'handle del buffer di memoria corrente e liberare tale memoria.

Un controllo di modifica rialloca automaticamente il buffer specificato ogni volta che richiede spazio aggiuntivo per il testo oppure rimuove testo sufficiente in modo che non sia più necessario spazio aggiuntivo.

L'invio di un messaggio **EM \_ SETHANDLE** cancella il buffer di annullamento ([**EM \_ CANUNDO**](em-canundo.md) restituisce zero) e il flag di modifica interno ([**EM \_ GETMODIFY**](em-getmodify.md) restituisce zero). La finestra del controllo di modifica viene ridisegnata.

**Rich Edit:** Il **messaggio EM \_ SETHANDLE** non è supportato. I controlli Rich Edit non archiviano il testo come una semplice matrice di caratteri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ CANUNDO**](em-canundo.md)
</dt> <dt>

[**EM \_ GETHANDLE**](em-gethandle.md)
</dt> <dt>

[**EM \_ GETMODIFY**](em-getmodify.md)
</dt> </dl>

 

 





