---
title: EM_SETSTORYTYPE messaggio (Richedit.h)
description: Imposta il tipo di storia.
ms.assetid: 8FA335E1-EE0A-4F31-B800-C79F617A6019
keywords:
- EM_SETSTORYTYPE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_SETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e09c62c50441857aac6f4018800de7a145081d64de49cdf7e9ca673a5370db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062881"
---
# <a name="em_setstorytype-message"></a>Messaggio EM \_ SETSTORYTYPE

Imposta il tipo di storia.


```C++
#define EM_SETSTORYTYPE       (WM_USER + 291)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice della storia.

</dd> <dt>

*lParam* 
</dt> <dd>

Nuovo tipo di storia. Per un elenco dei tipi di storie, vedere [**EM \_ GETSTORYTYPE**](em-getstorytype.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo di storia impostato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





