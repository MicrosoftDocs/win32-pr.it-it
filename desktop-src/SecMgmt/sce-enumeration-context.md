---
description: Il \_ tipo di dati del contesto di enumerazione SCE \_ è un handle opaco fornito dal set di strumenti di configurazione della sicurezza. Viene usato dalla \_ funzione informazioni query PFSCE \_ per spostarsi nel database di sicurezza.
ms.assetid: 05629c49-e36b-4045-93d0-d0f4bc09b08a
title: SCE_ENUMERATION_CONTEXT (Scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e380f6f99d68ad63199c3b82f5aa1e5ace8ddf0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343116"
---
# <a name="sce_enumeration_context"></a>\_contesto di enumerazione SCE \_

Il tipo di dati del **\_ \_ contesto di enumerazione SCE** è un handle opaco fornito dal set di strumenti di configurazione della sicurezza. Viene usato dalla funzione [**\_ \_ informazioni query PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) per spostarsi nel database di sicurezza.


```C++
typedef ULONG SCE_ENUMERATION_CONTEXT, *PSCE_ENUMERATION_CONTEXT;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Scesvc. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_informazioni query \_ PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> </dl>

 

