---
title: HTTP_RESPONSE (http. h)
description: La versione della struttura di \_ risposta HTTP dipende dalla versione della coda di richieste utilizzata come segue la coda di richieste dell'API del server http versione 1,0. si tratta di una \_ struttura di richiesta HTTP \_ V1. HTTP Server API versione 2,0 coda di richieste questa è una \_ struttura richiesta HTTP \_ v2.
ms.assetid: F94646C0-7293-4543-842B-F08D8C7E2247
keywords:
- HTTP_RESPONSE
- HTTP_RESPONSE
- PHTTP_RESPONSE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a8445021aa61b94ae83a55937b1db5ca4e3c577
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400494"
---
# <a name="http_response"></a>\_risposta http

La versione della struttura **di \_ risposta http** dipende dalla versione della coda di richieste utilizzata come indicato di seguito:

-   HTTP Server API versione 1,0 coda richieste: si tratta di una struttura [**\_ richiesta HTTP \_ V1**](/windows/desktop/api/Http/ns-http-http_request_v1) .
-   HTTP Server API versione 2,0 coda richieste: si tratta di una struttura [**\_ richiesta HTTP \_ v2**](/windows/desktop/api/Http/ns-http-http_request_v2) .

Non usare la [**\_ richiesta HTTP \_ V1**](/windows/desktop/api/Http/ns-http-http_request_v1) e [**la \_ richiesta HTTP \_ v2**](/windows/desktop/api/Http/ns-http-http_request_v2) direttamente nel codice. l'uso della **\_ risposta http** garantisce invece la corretta versione della struttura in base alla versione della coda di richieste.


```C++
typedef HTTP_REQUEST_V1 HTTP_RESPONSE;
typedef HTTP_REQUEST_V2 HTTP_RESPONSE;
typedef HTTP_RESPONSE* PHTTP_RESPONSE;
```



<dl> <dt>

**\_risposta http**
</dt> <dd>

Richiesta proveniva da una coda di richieste V1.

</dd> <dt>

**\_risposta http**
</dt> <dd>

Richiesta proveniva da una coda di richieste V2.

</dd> <dt>

**\_risposta PHTTP**
</dt> <dd>

Puntatore a una struttura di **\_ risposta http** .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                    |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Http. h</dt> </dl> |



 

 





