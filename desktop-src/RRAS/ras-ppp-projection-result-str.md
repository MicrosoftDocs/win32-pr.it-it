---
title: RAS_PPP_PROJECTION_RESULT struttura (Rassapi.h)
description: La struttura RAS PPP PROJECTION RESULT viene usata per segnalare i risultati delle varie operazioni di \_ \_ \_ proiezione PPP per una porta.
ms.assetid: 061b1b51-4b6f-4127-8ee5-8a1913a2aa99
keywords:
- RAS_PPP_PROJECTION_RESULT struttura RAS
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
ms.openlocfilehash: 6ce1bb82b34490f8a1f3734225cbde1e761c575a2019a30db7790bfc7fa3c169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789585"
---
# <a name="ras_ppp_projection_result-structure"></a>Struttura RAS \_ PPP \_ PROJECTION \_ RESULT

\[La **struttura RAS \_ PPP PROJECTION \_ \_ RESULT** non è supportata a Windows Vista.\]

La **struttura RAS \_ PPP PROJECTION \_ \_ RESULT** viene usata per segnalare i risultati delle varie operazioni di proiezione PPP per una porta.

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

Struttura [**RAS \_ PPP \_ NBFCP \_ RESULT**](ras-ppp-nbfcp-result-str.md) che segnala il risultato di un'operazione di proiezione NBF (NetBEUI Framer) PPP.

</dd> <dt>

**Ip**
</dt> <dd>

Struttura [**RAS \_ PPP \_ IPCP \_ RESULT**](ras-ppp-ipcp-result-str.md) che segnala il risultato di un'operazione di proiezione IP (PPP Internet Protocol).

</dd> <dt>

**Ipx**
</dt> <dd>

Struttura [**RAS \_ PPP \_ IPXCP \_ RESULT**](ras-ppp-ipxcp-result-str.md) che segnala il risultato di un'operazione di proiezione IPX (Internetwork Packet Exchange) PPP.

</dd> <dt>

**at**
</dt> <dd>

Struttura [**RAS \_ PPP \_ ATCP \_ RESULT.**](ras-ppp-atcp-result-str.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura segnala i risultati della proiezione per i protocolli NetBEUI, TCP/IP e IPX. Ogni struttura PPP ha **un membro dwError** che indica se le altre informazioni nella struttura sono valide. Se **dwError** è NO \_ ERROR, le altre informazioni sono valide. Se **dwError** è uno dei codici di errore in Winerror.h o Raserror.h, le altre informazioni non sono valide.

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

[**RAS \_ PPP \_ ATCP \_ RESULT**](ras-ppp-atcp-result-str.md)
</dt> <dt>

[**RISULTATO \_ \_ IPCP RAS PPP \_**](ras-ppp-ipcp-result-str.md)
</dt> <dt>

[**RISULTATO \_ DI RAS PPP \_ \_ IPXCP**](ras-ppp-ipxcp-result-str.md)
</dt> <dt>

[**RAS \_ PPP \_ NBFCP \_ RESULT**](ras-ppp-nbfcp-result-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





