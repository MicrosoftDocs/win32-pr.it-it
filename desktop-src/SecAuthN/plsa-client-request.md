---
description: Tipo di dati opaco.
ms.assetid: 384dd6e0-726f-4100-a036-1cca6a332a64
title: PLSA_CLIENT_REQUEST (Ntsecpkg. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3685c3cd38843edfd4ae708a18761b6ee698c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231711"
---
# <a name="plsa_client_request"></a>\_richiesta client \_ PLSA

Il tipo di dati della **\_ \_ richiesta client PLSA** è un tipo di dati opaco.

L' [*autorità di sicurezza locale*](../secgloss/l-gly.md) (LSA) la usa internamente per mantenere le informazioni client correlate alle singole richieste.


```C++
#include <windows.h>

typedef PVOID *PLSA_CLIENT_REQUEST;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Ntsecpkg. h</dt> </dl> |



 

 
