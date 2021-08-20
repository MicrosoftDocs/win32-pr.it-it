---
title: Tipi di dati DNS (Windns.h)
ms.assetid: 652012a5-e45d-4ea6-896a-17e8b1ed4a05
description: 'Altre informazioni su: Tipi di dati DNS'
keywords:
- IP4_ADDRESS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81756daaff73e7d5afc1b7c749cd976a9ede09d74ae70eb7db05d9e5d12f2f62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076865"
---
# <a name="dns-data-types"></a>Tipi di dati DNS

Per DNS sono definiti i tipi di dati seguenti:


```C++
typedef DWORD IP4_ADDRESS;
```



<dl> <dt>

**INDIRIZZO \_ IP4**
</dt> <dd>

Valore che rappresenta un protocollo IP versione 4 (IPv4). Ad esempio, l'indirizzo IPv4 decimale virgola, **127.0.0.1,** è rappresentato nell'ordine dei byte dell'host **0x7F000001**.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                          |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Windns.h</dt> </dl> |



 

 





