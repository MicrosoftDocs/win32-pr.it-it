---
title: Struttura RAS_PPP_PROJECTION_RESULT (rassapi. h)
description: La struttura dei risultati della \_ proiezione PPP RAS \_ \_ viene usata per segnalare i risultati delle varie operazioni di proiezione PPP per una porta.
ms.assetid: 061b1b51-4b6f-4127-8ee5-8a1913a2aa99
keywords:
- RAS struttura RAS_PPP_PROJECTION_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_PROJECTION_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9aa3aef828249b5c72f9e7cdd1bd3b69c96832
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741794"
---
# <a name="ras_ppp_projection_result-structure"></a>\_Struttura di \_ Risultati della proiezione PPP RAS \_

\[La struttura dei **\_ \_ \_ Risultati della proiezione PPP RAS** non è supportata a partire da Windows Vista.\]

La struttura dei risultati della **\_ \_ proiezione \_ PPP RAS** viene usata per segnalare i risultati delle varie operazioni di proiezione PPP per una porta.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _RAS_PPP_PROJECTION_RESULT {
  RAS_PPP_NBFCP_RESULT nbf;
  RAS_PPP_IPCP_RESULT  ip;
  RAS_PPP_IPXCP_RESULT ipx;
  RAS_PPP_ATCP_RESULT  at;
} RAS_PPP_PROJECTION_RESULT;
```



## <a name="members"></a>Members

<dl> <dt>

**nbf**
</dt> <dd>

Una struttura di [**\_ \_ \_ risultati NBFCP di Ras PPP**](ras-ppp-nbfcp-result-str.md) che segnala il risultato di un'operazione di proiezione di NBF (PPP NetBEUI Framer).

</dd> <dt>

**IP**
</dt> <dd>

Una struttura di [**\_ \_ \_ risultati protocollo IPCP RAS PPP**](ras-ppp-ipcp-result-str.md) che segnala il risultato di un'operazione di proiezione IP (Internet Protocol) PPP.

</dd> <dt>

**IPX**
</dt> <dd>

Struttura [**di \_ \_ \_ risultato IPXCP di Ras PPP**](ras-ppp-ipxcp-result-str.md) che indica il risultato di un'operazione di proiezione IPX (Internet-Packet Exchange) PPP.

</dd> <dt>

**at**
</dt> <dd>

Struttura [**di \_ \_ \_ risultati ATCP PPP RAS**](ras-ppp-atcp-result-str.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura segnala i risultati della proiezione per i protocolli NetBEUI, TCP/IP e IPX. Ogni struttura PPP dispone di un membro **dwError** che indica se le altre informazioni nella struttura sono valide. Se **dwError** non è un \_ errore, le altre informazioni sono valide. Se **dwError** è uno dei codici di errore in Winerror. h o Raserror. h, le altre informazioni non sono valide.

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

[**\_ \_ risultato ATCP PPP \_ RAS**](ras-ppp-atcp-result-str.md)
</dt> <dt>

[**\_ \_ risultato protocollo IPCP PPP \_ RAS**](ras-ppp-ipcp-result-str.md)
</dt> <dt>

[**\_ \_ risultato IPXCP PPP \_ RAS**](ras-ppp-ipxcp-result-str.md)
</dt> <dt>

[**\_ \_ risultato NBFCP PPP \_ RAS**](ras-ppp-nbfcp-result-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





