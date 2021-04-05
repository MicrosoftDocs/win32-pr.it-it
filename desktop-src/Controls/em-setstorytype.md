---
title: Messaggio di EM_SETSTORYTYPE (RichEdit. h)
description: Imposta il tipo di storia.
ms.assetid: 8FA335E1-EE0A-4F31-B800-C79F617A6019
keywords:
- Controlli di Windows Message EM_SETSTORYTYPE
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
ms.openlocfilehash: be6d1df04f93fca0119b58f978a6a0cb36ddf464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873590"
---
# <a name="em_setstorytype-message"></a>\_Messaggio SETSTORYTYPE em

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

Nuovo tipo di storia. Per un elenco di tipi di storie, vedere [**em \_ GETSTORYTYPE**](em-getstorytype.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo di storia che è stato impostato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





