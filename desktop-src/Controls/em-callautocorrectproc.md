---
title: EM_CALLAUTOCORRECTPROC messaggio (Richedit.h)
description: Chiama la funzione di callback di correzione automatica archiviata dal messaggio EM SETAUTOCORRECTPROC, a condizione che il testo che precede il punto di inserimento sia un candidato per la \_ correzione automatica.
ms.assetid: 93116467-B345-4FD9-9162-3E01CF3C6F20
keywords:
- EM_CALLAUTOCORRECTPROC dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- EM_CALLAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ad76ec66018b4e673913c433ce16a1294944f69c9d33a5dbaedb85ba21f985a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916081"
---
# <a name="em_callautocorrectproc-message"></a>Messaggio \_ EM CALLAUTOCORRECTPROC

Chiama la funzione di callback di correzione automatica archiviata dal messaggio [**EM \_ SETAUTOCORRECTPROC,**](em-setautocorrectproc.md) a condizione che il testo che precede il punto di inserimento sia un candidato per la correzione automatica.


```C++
#define EM_CALLAUTOCORRECTPROC       (WM_USER + 255)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Carattere di tipo **WCHAR.** Se questo carattere è una tabulazione (U+0009) e il carattere che precede il punto di inserimento non è una tabulazione, il carattere che precede il punto di inserimento viene considerato come parte della stringa candidata per la correzione automatica anziché come delimitatore di stringa. in caso contrario, *wParam* non ha alcun effetto.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è zero se il messaggio ha esito positivo o diverso da zero se si verifica un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[**EM \_ GETAUTOCORRECTPROC**](em-getautocorrectproc.md)
</dt> <dt>

[**EM \_ SETAUTOCORRECTPROC**](em-setautocorrectproc.md)
</dt> </dl>

 

 





