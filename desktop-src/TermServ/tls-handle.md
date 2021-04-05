---
title: TLS_HANDLE
description: Rappresenta un handle per un server licenze Desktop remoto.
ms.assetid: 6da51660-a9fd-4e49-97e3-ba0829b1bbbf
ms.tgt_platform: multiple
keywords:
- TLS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09764072b42e14aea2d1b8242dbc3cbb044442b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740714"
---
# <a name="tls_handle"></a>\_handle TLS

Rappresenta un handle per un server licenze Desktop remoto. Questo handle viene restituito dalla funzione [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .

> [!Note]  
> A questo tipo di dati non è associato alcun file di intestazione. Per usarlo, è necessario definirlo come illustrato in questo argomento.

 


```C++
typedef HANDLE TLS_HANDLE;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dt>

[**TLSDisconnectFromServer**](tlsdisconnectfromserver.md)
</dt> </dl>

 

 





