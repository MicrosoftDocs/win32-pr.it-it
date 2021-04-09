---
description: Il \_ tipo di dati dell'handle SCE è un handle opaco fornito dal set di strumenti di configurazione della sicurezza. Viene usato dalle \_ \_ funzioni info query PFSCE e PFSCE \_ set \_ Info Support per passare le informazioni tra l'allegato e il database di sicurezza.
ms.assetid: 8db91e6f-b31e-40c6-a158-b4b3b00ba0c0
title: SCE_HANDLE (Scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fef21dbe03d97dfa14537d5df132ba3cb222643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128774"
---
# <a name="sce_handle"></a>\_handle SCE

Il tipo di dati dell' **\_ handle SCE** è un handle opaco fornito dal set di strumenti di configurazione della sicurezza. Viene usato dalle funzioni [**\_ \_ info query PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) e [**PFSCE \_ set \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) support per passare le informazioni tra l'allegato e il database di sicurezza.


```C++
typedef PVOID SCE_HANDLE;
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
</dt> <dt>

[**\_informazioni sul set di PFSCE \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)
</dt> </dl>

 

