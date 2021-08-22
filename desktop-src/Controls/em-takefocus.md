---
title: EM_TAKEFOCUS messaggio (Commctrl.h)
description: Forza un controllo di modifica a riga singola a ricevere lo stato attivo della tastiera. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro Modifica TakeFocus.
ms.assetid: 27470857-4219-4426-bc69-e1271afc6ffb
keywords:
- EM_TAKEFOCUS di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_TAKEFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8283f2f9ea033439ef9ad7ec0ce40b08bb6396db8f5ebc7a9b1d513f29c209a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437141"
---
# <a name="em_takefocus-message"></a>Messaggio \_ EM TAKEFOCUS

\[Destinato all'uso interno; non consigliato per l'uso nelle applicazioni. Questo messaggio potrebbe non essere supportato nelle versioni future di Windows.\]

Forza un controllo di modifica a riga singola a ricevere lo stato attivo della tastiera. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ Modifica TakeFocus.**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus)

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

Se il controllo di modifica ha ricevuto in precedenza un messaggio [**EM \_ NOSETFOCUS,**](em-nosetfocus.md) il controllo di modifica avrà lo stato attivo senza averlo effettivamente; in caso contrario, il controllo di modifica riceverà lo stato attivo.

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

[**Modificare \_ TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus)
</dt> <dt>

[**EM \_ NOSETFOCUS**](em-nosetfocus.md)
</dt> </dl>

 

 





