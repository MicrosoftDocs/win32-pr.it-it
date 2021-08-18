---
title: RAS_PPP_IPCP_RESULT struttura (Rassapi.h)
description: La struttura RAS PPP IPCP RESULT viene usata per segnalare il risultato di un'operazione di proiezione \_ \_ IP \_ (Internet Protocol) PPP per una porta.
ms.assetid: edbdc8f2-ba56-4d34-8908-f7eccc2ebf61
keywords:
- RAS_PPP_IPCP_RESULT struttura RAS
topic_type:
- apiref
api_name:
- RAS_PPP_IPCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa0425289b7ffd686f0d908f9789a2c24606978f37e05dfada5b937b8ce05b21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789615"
---
# <a name="ras_ppp_ipcp_result-structure"></a>Struttura \_ RAS PPP \_ IPCP \_ RESULT

\[La **struttura RAS \_ PPP \_ IPCP \_ RESULT** non è supportata a Windows Vista.\]

La **struttura RAS \_ PPP \_ IPCP \_ RESULT** viene usata per segnalare il risultato di un'operazione di proiezione IP (Internet Protocol) PPP per una porta.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _RAS_PPP_IPCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPADDRESSLEN + 1];
} RAS_PPP_IPCP_RESULT;
```



## <a name="members"></a>Members

<dl> <dt>

**dwError**
</dt> <dd>

Indica i risultati dell'operazione di proiezione IP. Il valore NO \_ ERROR indica l'esito positivo, nel qual caso il membro **wszAddress** è valido. Se l'operazione di proiezione non è riuscita, **dwError** è un codice di errore di Winerror.h o Raserror.h.

</dd> <dt>

**wszAddress**
</dt> <dd>

Stringa Unicode con terminazione Null che specifica l'indirizzo IP assegnato al client remoto. Questa stringa ha il formato *a***.** _b_* _._ *_c_*_._ * _d_.

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

 

 





