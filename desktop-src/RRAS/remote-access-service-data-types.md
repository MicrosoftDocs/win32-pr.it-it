---
title: Tipi di dati del servizio di accesso remoto (RAS. h)
description: I tipi di dati seguenti vengono usati dall'API del servizio di accesso remoto.
ms.assetid: aaa7f971-9c23-4738-a386-9b7db859f6be
keywords:
- RASIPV4ADDR
- RASIPV6ADDR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8aa2fdae531c5aae0986d3289802565c6914fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964186"
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

[**\_ Addr IN6**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) che contiene un indirizzo IPv6.

> [!Note]  
> Supportato in Windows Vista o versioni successive di Windows.

 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>RAS. h</dt> </dl> |



 

