---
title: EM_NOSETFOCUS messaggio (Commctrl.h)
description: Impedisce a un controllo di modifica a riga singola di ricevere lo stato attivo della tastiera. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro Modifica NoSetFocus.
ms.assetid: aeb5ed6b-7d4f-4c0d-a172-6cee7cab959c
keywords:
- EM_NOSETFOCUS dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- EM_NOSETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02ac35a30ff3deac7e9d6d227a6e8c403e6096e272ea89067dd817add9b2426e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831194"
---
# <a name="em_nosetfocus-message"></a>Messaggio EM \_ NOSETFOCUS

\[Destinato all'uso interno; non consigliato per l'uso nelle applicazioni. Questo messaggio potrebbe non essere supportato nelle versioni future di Windows.\]

Impedisce a un controllo di modifica a riga singola di ricevere lo stato attivo della tastiera. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ Modifica NoSetFocus.**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene usato.

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

L'uso di questo messaggio potrebbe compromettere la sicurezza del programma.

## <a name="remarks"></a>Commenti

Questo messaggio viene ignorato se il controllo di modifica non è un controllo di modifica a riga singola.

Dopo l'invio di questo messaggio, l'effetto è permanente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**Modifica \_ NoSetFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus)
</dt> <dt>

[**EM \_ TAKEFOCUS**](em-takefocus.md)
</dt> </dl>

 

 





