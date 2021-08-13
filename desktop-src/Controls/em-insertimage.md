---
title: EM_INSERTIMAGE messaggio (Richedit.h)
description: Sostituisce la selezione con un BLOB che visualizza un'immagine.
ms.assetid: 147B298B-C4A9-455B-9736-A0B09D72902B
keywords:
- EM_INSERTIMAGE del messaggio Windows controlli
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
ms.openlocfilehash: 7418a8fe4b7c627d211bce7bf2591ed684d82e42089fbe9bedeb2f76a6b9d3e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437891"
---
# <a name="em_insertimage-message"></a>Messaggio \_ EM INSERTIMAGE

Sostituisce la selezione con un BLOB che visualizza un'immagine.


```C++
#define EM_INSERTIMAGE       (WM_USER + 314)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura RICHEDIT \_ IMAGE \_ PARAMETERS**](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters) che contiene il BLOB dell'immagine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo o uno dei codici di errore seguenti.



| Codice restituito                                                                                    | Descrizione                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Impossibile inserire l'immagine. <br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | Il *parametro lParam* è NULL o punta a un'immagine non valida. |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                  |



 

## <a name="remarks"></a>Commenti

Se la selezione è un punto di inserimento, il BLOB dell'immagine viene inserito in corrispondenza del punto di inserimento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ INSERTTABLE**](em-inserttable.md)
</dt> </dl>

 

 





