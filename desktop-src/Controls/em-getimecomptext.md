---
title: EM_GETIMECOMPTEXT messaggio (Richedit.h)
description: Recupera il testo della composizione IME (Input Method Editor).
ms.assetid: 1516305c-5f87-4ae0-97db-8709c71abacc
keywords:
- EM_GETIMECOMPTEXT dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- EM_GETIMECOMPTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dd915f037275d428df37ca02a206b936a63bfd2f6ac8fbb605d1573b9535789
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049071"
---
# <a name="em_getimecomptext-message"></a>Messaggio EM \_ GETIMECOMPTEXT

Recupera il testo della composizione IME (Input Method Editor).

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Struttura [**IMECOMPTEXT.**](/windows/desktop/api/Richedit/ns-richedit-imecomptext)

</dd> <dt>

*lParam* 
</dt> <dd>

Buffer che riceve il testo della composizione. Le dimensioni di questo buffer sono contenute nel membro **cb** della *struttura wParam.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, il valore restituito è il numero di caratteri Unicode copiati nel buffer. In caso contrario, è zero.

## <a name="remarks"></a>Commenti

Questo messaggio accetta solo stringhe Unicode.

**Avviso di sicurezza:** Assicurarsi di avere un buffer sufficiente per le dimensioni dell'input. La mancata esecuzione di questa operazione potrebbe causare problemi per l'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP1 \[\]<br/>                                  |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext)
</dt> </dl>

 

 





