---
title: Tipi di dati del registro eventi di Windows (WinEvt. h)
description: Il registro eventi di Windows definisce i tipi di dati seguenti
ms.assetid: 1aad25fe-7503-4ef8-a40a-63457bd9a007
keywords:
- EVT_HANDLE
- PEVT_HANDLE
- EVT_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a93794d8cc3a254fe182c439698324dccdfc20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741386"
---
# <a name="windows-event-log-data-types"></a>Tipi di dati del registro eventi di Windows

Nel registro eventi di Windows sono definiti i tipi di dati seguenti:


```C++
typedef HANDLE EVT_HANDLE;
typedef HANDLE* PEVT_HANDLE;
typedef HANDLE EVT_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

**\_handle evt**
</dt> <dd>

Handle per un oggetto registro eventi di Windows.

</dd> <dt>

**\_handle PEVT**
</dt> <dd>

Puntatore all'handle di un oggetto registro eventi di Windows.

</dd> <dt>

**\_ \_ \_ Handle proprietà matrice di oggetti evt \_**
</dt> <dd>

Handle per una matrice di oggetti del registro eventi di Windows.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>WinEvt. h</dt> </dl> |



 

 





