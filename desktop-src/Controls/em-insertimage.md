---
title: Messaggio di EM_INSERTIMAGE (RichEdit. h)
description: Sostituisce la selezione con un BLOB che visualizza un'immagine.
ms.assetid: 147B298B-C4A9-455B-9736-A0B09D72902B
keywords:
- Controlli di Windows Message EM_INSERTIMAGE
topic_type:
- apiref
api_name:
- EM_INSERTIMAGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9ff1e0fd355cf5dd8d43d211c44fda6417c638
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475557"
---
# <a name="em_insertimage-message"></a>\_Messaggio INSERTIMAGE em

Sostituisce la selezione con un BLOB che visualizza un'immagine.


```C++
#define EM_INSERTIMAGE       (WM_USER + 314)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**di \_ \_ parametri dell'immagine RichEdit**](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters) che contiene il BLOB dell'immagine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo o uno dei codici di errore seguenti.



| Codice restituito                                                                                    | Descrizione                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**E \_ Non riuscita**</dt> </dl>        | Impossibile inserire l'immagine. <br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | Il parametro *lParam* è null o punta a un'immagine non valida. |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | La memoria disponibile è insufficiente.<br/>                  |



 

## <a name="remarks"></a>Commenti

Se la selezione è un punto di inserimento, il BLOB dell'immagine viene inserito nel punto di inserimento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_INSERTTABLE em**](em-inserttable.md)
</dt> </dl>

 

 





