---
title: Struttura RAS_PPP_NBFCP_RESULT (rassapi. h)
description: La struttura dei risultati di RAS \_ PPP \_ NBFCP \_ viene utilizzata per segnalare il risultato di un'operazione di proiezione NBF (PPP NetBEUI Framer) per una porta.
ms.assetid: 670bf125-cad5-481f-89e4-858e636316bd
keywords:
- RAS struttura RAS_PPP_NBFCP_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_NBFCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddcb1cfe28a72e390cedbcc35fa299dddbfb8634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119983"
---
# <a name="ras_ppp_nbfcp_result-structure"></a>\_Struttura di \_ \_ risultati NBFCP di Ras PPP

\[La struttura dei **risultati di Ras \_ PPP \_ NBFCP \_** non è supportata a partire da Windows Vista.\]

La struttura dei **risultati di Ras \_ PPP \_ NBFCP \_** viene utilizzata per segnalare il risultato di un'operazione di proiezione NBF (PPP NetBEUI Framer) per una porta.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _RAS_PPP_NBFCP_RESULT {
  DWORD dwError;
  DWORD dwNetBiosError;
  CHAR  szName[NETBIOS_NAME_LEN + 1];
  WCHAR wszWksta[NETBIOS_NAME_LEN + 1];
} RAS_PPP_NBFCP_RESULT;
```



## <a name="members"></a>Members

<dl> <dt>

**dwError**
</dt> <dd>

Indica i risultati dell'operazione di proiezione NBF. Il valore nessun \_ errore indica l'esito positivo, nel qual caso il membro **wszWksta** contiene il nome del computer remoto. Se l'operazione di proiezione ha esito negativo, **dwError** è un codice di errore di Winerror. h o Raserror. h.

</dd> <dt>

**dwNetBiosError**
</dt> <dd>

Ignora il membro nel server. è rilevante solo per il client.

</dd> <dt>

**szName**
</dt> <dd>

Ignora il membro nel server. è rilevante solo per il client.

</dd> <dt>

**wszWksta**
</dt> <dd>

Stringa Unicode con terminazione null che specifica il nome NetBIOS della workstation client RAS.

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

 

 





