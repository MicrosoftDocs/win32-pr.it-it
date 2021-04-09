---
title: Messaggio EM_NOSETFOCUS (COMmctrl. h)
description: Impedisce a un controllo di modifica a riga singola di ricevere lo stato attivo della tastiera. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro Edit NoSetFocus.
ms.assetid: aeb5ed6b-7d4f-4c0d-a172-6cee7cab959c
keywords:
- Controlli di Windows Message EM_NOSETFOCUS
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
ms.openlocfilehash: b82830cda3402d2089d3421debaa7c4dbf13de5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120719"
---
# <a name="em_nosetfocus-message"></a>\_Messaggio NOSETFOCUS em

\[Progettato per uso interno; sconsigliato per l'utilizzo nelle applicazioni. Questo messaggio potrebbe non essere supportato nelle versioni future di Windows.\]

Impedisce a un controllo di modifica a riga singola di ricevere lo stato attivo della tastiera. È possibile inviare questo messaggio in modo esplicito o usando la macro [**Edit \_ NoSetFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus) .

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

Una volta inviato questo messaggio, l'effetto è permanente.

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

[**Modifica \_ NoSetFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus)
</dt> <dt>

[**\_TAKEFOCUS em**](em-takefocus.md)
</dt> </dl>

 

 





