---
title: Struttura RAS_PPP_IPCP_RESULT (rassapi. h)
description: La struttura dei risultati di RAS \_ PPP \_ protocollo IPCP \_ viene utilizzata per segnalare il risultato di un'operazione di proiezione IP (Internet Protocol) PPP per una porta.
ms.assetid: edbdc8f2-ba56-4d34-8908-f7eccc2ebf61
keywords:
- RAS struttura RAS_PPP_IPCP_RESULT
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
ms.openlocfilehash: eedcd7c7390e01849371eee2cbb24ffa2593900d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517878"
---
# <a name="ras_ppp_ipcp_result-structure"></a>\_Struttura di \_ \_ risultati protocollo IPCP di Ras PPP

\[La struttura dei **risultati di Ras \_ PPP \_ protocollo IPCP \_** non è supportata a partire da Windows Vista.\]

La struttura dei **risultati di Ras \_ PPP \_ protocollo IPCP \_** viene utilizzata per segnalare il risultato di un'operazione di proiezione IP (Internet Protocol) PPP per una porta.

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

Indica i risultati dell'operazione di proiezione IP. Il valore nessun \_ errore indica l'esito positivo, nel qual caso il membro **wszAddress** è valido. Se l'operazione di proiezione ha esito negativo, **dwError** è un codice di errore di Winerror. h o Raserror. h.

</dd> <dt>

**wszAddress**
</dt> <dd>

Stringa Unicode con terminazione null che specifica l'indirizzo IP assegnato al client remoto. Il formato di questa stringa è ****.** _b_* _._ *_c_*_._ * _d_.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del servizio di accesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Strutture di amministrazione del server RAS](ras-server-administration-structures.md)
</dt> <dt>

[**\_Porta RAS \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**\_risultato della \_ proiezione \_ PPP RAS**](ras-ppp-projection-result-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





