---
title: Struttura RAS_PPP_ATCP_RESULT (rassapi. h)
description: La struttura dei risultati di RAS \_ PPP \_ ATCP \_ viene utilizzata per segnalare il risultato di un'operazione di proiezione del protocollo AppleTalk per una porta.
ms.assetid: ac9df618-f79c-4066-a37e-f92e64e951dd
keywords:
- RAS struttura RAS_PPP_ATCP_RESULT
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
ms.openlocfilehash: 66f3f950af9d5bdde8feef085457a895212ad04b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964326"
---
# <a name="ras_ppp_atcp_result-structure"></a>\_Struttura di \_ \_ risultati ATCP di Ras PPP

\[La struttura dei **risultati di Ras \_ PPP \_ ATCP \_** non è supportata a partire da Windows Vista.\]

La struttura dei **risultati di Ras \_ PPP \_ ATCP \_** viene utilizzata per segnalare il risultato di un'operazione di proiezione del protocollo AppleTalk per una porta.

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

Specifica un valore che indica i risultati dell'operazione di proiezione AppleTalk. Il valore nessun \_ errore indica l'esito positivo, nel qual caso il membro **wszAddress** è valido. Se l'operazione di proiezione ha esito negativo, **dwError** è un codice di errore di Winerror. h o Raserror. h.

</dd> <dt>

**wszAddress**
</dt> <dd>

Specifica una stringa Unicode con terminazione null che specifica l'indirizzo IP assegnato al client remoto.

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

[**\_risultato della \_ proiezione \_ PPP RAS**](ras-ppp-projection-result-str.md)
</dt> </dl>

 

 





