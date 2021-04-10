---
title: Messaggio di EM_GETIMECOMPTEXT (RichEdit. h)
description: Recupera il testo della composizione IME (Input Method Editor).
ms.assetid: 1516305c-5f87-4ae0-97db-8709c71abacc
keywords:
- Controlli di Windows Message EM_GETIMECOMPTEXT
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
ms.openlocfilehash: 834c55d6b5e40de7dcacfeb3e2d0c2e0878a0f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964577"
---
# <a name="em_getimecomptext-message"></a>\_Messaggio GETIMECOMPTEXT em

Recupera il testo della composizione IME (Input Method Editor).

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Struttura [**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext) .

</dd> <dt>

*lParam* 
</dt> <dd>

Buffer che riceve il testo di composizione. La dimensione di questo buffer è contenuta nel membro **CB** della struttura *wParam* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, il valore restituito è il numero di caratteri Unicode copiati nel buffer. In caso contrario, è zero.

## <a name="remarks"></a>Commenti

Questo messaggio accetta solo stringhe Unicode.

**Avviso di sicurezza:** Assicurarsi di disporre di un buffer sufficiente per le dimensioni dell'input. In caso contrario, potrebbero verificarsi problemi per l'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP1 \[\]<br/>                                  |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext)
</dt> </dl>

 

 





