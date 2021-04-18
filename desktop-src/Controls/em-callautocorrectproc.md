---
title: Messaggio di EM_CALLAUTOCORRECTPROC (RichEdit. h)
description: Chiama la funzione di callback di correzione automatica archiviata dal \_ messaggio SETAUTOCORRECTPROC em, purché il testo che precede il punto di inserimento sia candidato per la correzione automatica.
ms.assetid: 93116467-B345-4FD9-9162-3E01CF3C6F20
keywords:
- Controlli di Windows Message EM_CALLAUTOCORRECTPROC
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
ms.openlocfilehash: 73109d2499fc01a1d811066dc6059593c7ed5e0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477626"
---
# <a name="em_callautocorrectproc-message"></a>\_Messaggio CALLAUTOCORRECTPROC em

Chiama la funzione di callback di correzione automatica archiviata dal [**messaggio \_ SETAUTOCORRECTPROC em**](em-setautocorrectproc.md) , purché il testo che precede il punto di inserimento sia candidato per la correzione automatica.


```C++
#define EM_CALLAUTOCORRECTPROC       (WM_USER + 255)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Carattere di tipo **WCHAR**. Se il carattere è una tabulazione (U + 0009) e il carattere che precede il punto di inserimento è t a Tab, il carattere che precede il punto di inserimento viene considerato come parte della stringa candidata di correzione automatica anziché come delimitatore di stringa. in caso contrario, *wParam* non ha alcun effetto.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è zero se il messaggio riesce oppure un valore diverso da zero se si verifica un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[**\_GETAUTOCORRECTPROC em**](em-getautocorrectproc.md)
</dt> <dt>

[**\_SETAUTOCORRECTPROC em**](em-setautocorrectproc.md)
</dt> </dl>

 

 





