---
description: Il tipo di dati SCE \_ ENUMERATION CONTEXT è un handle \_ opaco fornito dal set di strumenti di configurazione della sicurezza. Viene usato dalla funzione PFSCE \_ QUERY INFO per spostarsi nel database di \_ sicurezza.
ms.assetid: 05629c49-e36b-4045-93d0-d0f4bc09b08a
title: SCE_ENUMERATION_CONTEXT (Scesvc.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16b102c1eb2998f09dbe95c79c500e0bc66f4a790464071dbf9704a17a1348c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004999"
---
# <a name="sce_enumeration_context"></a>CONTESTO DI ENUMERAZIONE SCE \_ \_

Il **tipo di dati SCE ENUMERATION \_ \_ CONTEXT** è un handle opaco fornito dal set di strumenti di configurazione della sicurezza. Viene usato dalla funzione [**PFSCE \_ QUERY \_ INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) per spostarsi nel database di sicurezza.


```C++
typedef ULONG SCE_ENUMERATION_CONTEXT, *PSCE_ENUMERATION_CONTEXT;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Scesvc.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INFORMAZIONI QUERY PFSCE \_ \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> </dl>

 

