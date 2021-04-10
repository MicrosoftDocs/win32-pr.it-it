---
description: Definisce i valori che determinano come recuperare le credenziali di un account del servizio gestito del gruppo (gMSA).
ms.assetid: 90891448-22F6-497A-A612-3DAB8622C325
title: Enumerazione CRED_FETCH (Secpkg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRED_FETCH
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: 6a7c30f29826b017bc7a3badd796955ec31a1ca7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968010"
---
# <a name="cred_fetch-enumeration"></a>\_Enumerazione recupero cred

Definisce i valori che determinano come recuperare le credenziali di un account del servizio gestito del gruppo (gMSA).

## <a name="syntax"></a>Sintassi


```C++
typedef enum _CRED_FETCH { 
  CredFetchDefault  = 0,
  CredFetchDPAPI    = 1,
  CredFetchForced   = 2
} CRED_FETCH;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span>**CredFetchDefault**
</dt> <dd>

Indica che il sistema operativo deve prima tentare di recuperare la password dalla cache locale. Se è il momento di recuperare la password, il sistema operativo deve contattare un controller di dominio per la password. Se l'operazione ha esito negativo, restituire le password memorizzate nella cache con il valore di stato success.

</dd> <dt>

<span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span>**CredFetchDPAPI**
</dt> <dd>

Restituisce le credenziali DPAPI locali al chiamante. Gli SSP ( [*Security Support Provider*](/windows/desktop/SecGloss/s-gly) ) in genere non richiedono l'utilizzo di questa enumerazione.

</dd> <dt>

<span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span>**CredFetchForced**
</dt> <dd>

Impone al sistema operativo di provare a leggere la password dal controller di dominio. Durante il tempo di rollover della password, è possibile che la password sia stata modificata nel controller di dominio e in altri host membro, ma l'host membro gMSA riconosce la password come ancora valida. Ciò può verificarsi a causa di problemi di sfasamento dell'orologio tra controller di dominio diversi. Quando si specifica questo valore, il sistema operativo determina se è possibile che si verifichi una modifica della password a causa dello sfasamento dell'orologio e, in caso affermativo, recupera la password. In caso contrario, vengono restituite le credenziali memorizzate nella cache. Se non sono presenti credenziali memorizzate nella cache, il sistema operativo tenta di ottenerne uno dal controller di dominio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Secpkg. h</dt> </dl> |



 

