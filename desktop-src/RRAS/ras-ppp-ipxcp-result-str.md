---
title: RAS_PPP_IPXCP_RESULT struttura (Rassapi.h)
description: La struttura RAS PPP IPXCP RESULT viene usata per segnalare il risultato di un'operazione di proiezione \_ \_ \_ IPX (Internetwork Packet Exchange) PPP per una porta.
ms.assetid: e1236e1b-f0ef-46cf-a12f-35529215752c
keywords:
- RAS_PPP_IPXCP_RESULT struttura RAS
topic_type:
- apiref
api_name:
- RAS_PPP_IPXCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc79b7700fc47176928688b517377f5e02903da04841b50949937448065086d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789605"
---
# <a name="ras_ppp_ipxcp_result-structure"></a>Struttura \_ RAS PPP \_ IPXCP \_ RESULT

\[La **struttura RAS \_ PPP \_ IPXCP \_ RESULT** non è supportata a Windows Vista.\]

La **struttura RAS \_ PPP \_ IPXCP \_ RESULT** viene usata per segnalare il risultato di un'operazione di proiezione IPX (Internetwork Packet Exchange) PPP per una porta.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _RAS_PPP_IPXCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPXADDRESSLEN + 1];
} RAS_PPP_IPXCP_RESULT;
```



## <a name="members"></a>Members

<dl> <dt>

**dwError**
</dt> <dd>

Indica i risultati dell'operazione di proiezione IPX. Il valore NO \_ ERROR indica l'esito positivo, nel qual caso il membro **wszAddress** è valido. Se l'operazione di proiezione non è riuscita, **dwError** è un codice di errore di Winerror.h o Raserror.h.

</dd> <dt>

**wszAddress**
</dt> <dd>

Stringa Unicode con terminazione Null che specifica l'indirizzo IPX assegnato al client remoto. Questa stringa contiene ***net*.** _form_ del nodo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Rassapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del servizio di accesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Strutture di amministrazione del server RAS](ras-server-administration-structures.md)
</dt> <dt>

[**PORTA \_ RAS \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**RISULTATO \_ DELLA \_ PROIEZIONE RAS PPP \_**](ras-ppp-projection-result-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





