---
title: RAS_PPP_ATCP_RESULT struttura (Rassapi.h)
description: La struttura RAS PPP ATCP RESULT viene usata per segnalare il risultato di un'operazione di proiezione \_ \_ del protocollo \_ AppleTalk per una porta.
ms.assetid: ac9df618-f79c-4066-a37e-f92e64e951dd
keywords:
- RAS_PPP_ATCP_RESULT struttura RAS
topic_type:
- apiref
api_name:
- RAS_PPP_ATCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa3122026613ba5012f950a98a615dbb8c9ef34133a2a24249fca545eaa2060
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789635"
---
# <a name="ras_ppp_atcp_result-structure"></a>Struttura \_ RAS PPP \_ ATCP \_ RESULT

\[La **struttura \_ RAS PPP \_ ATCP \_ RESULT** non è supportata a Windows Vista.\]

La **struttura RAS \_ PPP \_ ATCP \_ RESULT** viene usata per segnalare il risultato di un'operazione di proiezione del protocollo AppleTalk per una porta.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _RAS_PPP_ATCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_ATADDRESSLEN + 1];
} RAS_PPP_ATCP_RESULT;
```



## <a name="members"></a>Members

<dl> <dt>

**dwError**
</dt> <dd>

Specifica un valore che indica i risultati dell'operazione di proiezione AppleTalk. Il valore NO \_ ERROR indica l'esito positivo, nel qual caso il membro **wszAddress** è valido. Se l'operazione di proiezione non riesce, **dwError** è un codice di errore di Winerror.h o Raserror.h.

</dd> <dt>

**wszAddress**
</dt> <dd>

Specifica una stringa Unicode con terminazione Null che specifica l'indirizzo IP assegnato al client remoto.

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

[**RISULTATO \_ DELLA PROIEZIONE PPP \_ \_ RAS**](ras-ppp-projection-result-str.md)
</dt> </dl>

 

 





