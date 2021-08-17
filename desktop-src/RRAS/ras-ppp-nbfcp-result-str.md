---
title: RAS_PPP_NBFCP_RESULT struttura (Rassapi.h)
description: La struttura RAS PPP NBFCP RESULT viene usata per segnalare il risultato di un'operazione di proiezione \_ \_ \_ NBF (NetBEUI Framer) PPP per una porta.
ms.assetid: 670bf125-cad5-481f-89e4-858e636316bd
keywords:
- RAS_PPP_NBFCP_RESULT struttura RAS
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
ms.openlocfilehash: e415e6aea75dcf78d19d776e4df0a6edf704db473eacf0c8ddbb366ffbf65947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789595"
---
# <a name="ras_ppp_nbfcp_result-structure"></a>Struttura \_ RAS PPP \_ NBFCP \_ RESULT

\[La **struttura \_ RAS PPP \_ NBFCP \_ RESULT** non è supportata a Windows Vista.\]

La **struttura RAS \_ PPP \_ NBFCP \_ RESULT** viene usata per segnalare il risultato di un'operazione di proiezione NBF (NetBEUI Framer) PPP per una porta.

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

Indica i risultati dell'operazione di proiezione NBF. Il valore NO ERROR indica l'esito positivo. In questo caso, il membro \_ **wszWksta** contiene il nome del computer remoto. Se l'operazione di proiezione non è riuscita, **dwError** è un codice di errore di Winerror.h o Raserror.h.

</dd> <dt>

**dwNetBiosError**
</dt> <dd>

Ignorare questo membro nel server. è rilevante solo nel client.

</dd> <dt>

**Szname**
</dt> <dd>

Ignorare questo membro nel server. è rilevante solo nel client.

</dd> <dt>

**wszWksta**
</dt> <dd>

Stringa Unicode con terminazione Null che specifica il nome NetBIOS della workstation client RAS.

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

 

 





