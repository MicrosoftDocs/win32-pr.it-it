---
title: Windows Tipi di dati del log eventi (WinEvt.h)
description: Windows Registro eventi definisce i tipi di dati seguenti
ms.assetid: 1aad25fe-7503-4ef8-a40a-63457bd9a007
keywords:
- EVT_HANDLE
- PEVT_HANDLE
- EVT_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c309dd52471bd501aa2668220d39882ab8de7e1c23a646084364659df4ae4fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619991"
---
# <a name="windows-event-log-data-types"></a>Windows Tipi di dati del log eventi

Windows Registro eventi definisce i tipi di dati seguenti:


```C++
typedef HANDLE EVT_HANDLE;
typedef HANDLE* PEVT_HANDLE;
typedef HANDLE EVT_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

**EVT \_ HANDLE**
</dt> <dd>

Handle per un oggetto Windows registro eventi.

</dd> <dt>

**PEVT \_ HANDLE**
</dt> <dd>

Puntatore all'handle di un oggetto Windows registro eventi.

</dd> <dt>

**HANDLE DI PROPRIETÀ DELLA MATRICE DI OGGETTI EVT \_ \_ \_ \_**
</dt> <dd>

Handle per una matrice di oggetti Windows log eventi.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>WinEvt.h</dt> </dl> |



 

 





