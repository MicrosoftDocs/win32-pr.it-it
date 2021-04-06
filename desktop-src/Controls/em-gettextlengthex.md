---
title: Messaggio di EM_GETTEXTLENGTHEX (RichEdit. h)
description: Calcola la lunghezza del testo in diversi modi. Viene in genere chiamato prima di creare un buffer per ricevere il testo dal controllo.
ms.assetid: 42c89b7b-e48d-4517-9993-ce58ff9e4e40
keywords:
- Controlli di Windows Message EM_GETTEXTLENGTHEX
topic_type:
- apiref
api_name:
- EM_GETTEXTLENGTHEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2d91674e07ef60c2ce95535983a31cf380f9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873709"
---
# <a name="em_gettextlengthex-message"></a>\_Messaggio GetTextLengthEx em

Calcola la lunghezza del testo in diversi modi. Viene in genere chiamato prima di creare un buffer per ricevere il testo dal controllo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Puntatore a una struttura [**GetTextLengthEx**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) che riceve le informazioni sulla lunghezza del testo.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il messaggio restituisce il numero di **TCHAR** nel controllo di modifica, a seconda dell'impostazione dei flag nella struttura [**GetTextLengthEx**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) . Se sono stati impostati flag incompatibili nel membro **Flags** , il messaggio restituisce E \_ INVALIDARG.

## <a name="remarks"></a>Commenti

Questo messaggio è un modo rapido e semplice per determinare il numero di caratteri nella versione Unicode del controllo Rich Edit. Tuttavia, per una tabella codici di destinazione non Unicode, è possibile che si converta in una combinazione di caratteri a byte singolo e a byte doppio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)
</dt> </dl>

 

 





