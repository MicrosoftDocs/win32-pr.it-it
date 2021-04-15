---
title: Messaggio di EM_GETELLIPSISSTATE (RichEdit. h)
description: Recupera lo stato dei puntini di sospensione corrente.
ms.assetid: D02AE225-F5BF-401A-9877-55C68946CDBE
keywords:
- Controlli di Windows Message EM_GETELLIPSISSTATE
topic_type:
- apiref
api_name:
- EM_GETELLIPSISSTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 905bc8ecc180189f46e896aa0d9aaa3ba88b3f0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476834"
---
# <a name="em_getellipsisstate-message"></a>\_Messaggio GETELLIPSISSTATE em

Recupera lo stato dei puntini di sospensione corrente.


```C++
#define EM_GETELLIPSISSTATE       (WM_USER + 322)
```



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

Il valore restituito è TRUE se i puntini di sospensione vengono visualizzati e FALSE in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETELLIPSISMODE em**](em-getellipsismode.md)
</dt> <dt>

[**\_SETELLIPSISMODE em**](em-setellipsismode.md)
</dt> </dl>

 

 





