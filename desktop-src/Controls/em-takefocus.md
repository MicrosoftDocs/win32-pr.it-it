---
title: Messaggio EM_TAKEFOCUS (COMmctrl. h)
description: Impone a un controllo di modifica a riga singola di ricevere lo stato attivo. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro Edit TakeFocus.
ms.assetid: 27470857-4219-4426-bc69-e1271afc6ffb
keywords:
- Controlli di Windows Message EM_TAKEFOCUS
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
ms.openlocfilehash: 5e4abdf926cdd337760b5cf151c3f8ee08cb418b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476828"
---
# <a name="em_takefocus-message"></a>\_Messaggio TAKEFOCUS em

\[Progettato per uso interno; sconsigliato per l'utilizzo nelle applicazioni. Questo messaggio potrebbe non essere supportato nelle versioni future di Windows.\]

Impone a un controllo di modifica a riga singola di ricevere lo stato attivo. È possibile inviare questo messaggio in modo esplicito o usando la macro [**Edit \_ TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus) .

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

Il valore restituito non viene utilizzato.

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

L'uso di questo messaggio potrebbe compromettere la sicurezza del programma.

## <a name="remarks"></a>Commenti

Questo messaggio viene ignorato se il controllo di modifica non è un controllo di modifica a riga singola.

Se il controllo di modifica ha ricevuto in precedenza un messaggio [**\_ NOSETFOCUS em**](em-nosetfocus.md) , il controllo di modifica apparirà lo stato attivo senza che sia effettivamente presente. in caso contrario, il controllo di modifica riceve lo stato attivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**Modifica \_ TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus)
</dt> <dt>

[**\_NOSETFOCUS em**](em-nosetfocus.md)
</dt> </dl>

 

 





