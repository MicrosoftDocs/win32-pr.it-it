---
title: Tipi di dati del servizio di accesso remoto (Ras.h)
description: I tipi di dati seguenti vengono usati dall'API del servizio di accesso remoto.
ms.assetid: aaa7f971-9c23-4738-a386-9b7db859f6be
keywords:
- RASIPV4ADDR
- RASIPV6ADDR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26df8b8336b9b96ec338a79ed846519fb8a0ca019e6dd5996b9ac17087faa371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028251"
---
# <a name="remote-access-service-data-types"></a>Tipi di dati del servizio di accesso remoto

I tipi di dati seguenti vengono usati dall'API del servizio di accesso remoto.


```C++
typedef in_addr RASIPV4ADDR;
typedef in6_addr RASIPV6ADDR;
```



<dl> <dt>

**RASIPV4ADDR**
</dt> <dd>

Oggetto [**in \_ addr**](/windows/desktop/api/winsock2/ns-winsock2-in_addr) che contiene un indirizzo IPv4.

> [!Note]  
> Supportato in Windows Vista o versioni successive di Windows.

 

</dd> <dt>

**RASIPV6ADDR**
</dt> <dd>

Componente [**aggiuntivo in6 \_ che**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) contiene un indirizzo IPv6.

> [!Note]  
> Supportato in Windows Vista o versioni successive di Windows.

 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Ras.h</dt> </dl> |



 

