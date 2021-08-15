---
description: La struttura HANDOFFENTRY definisce una voce di protocollo specifica in una struttura HANDOFFTABLE.
ms.assetid: 85793326-3007-4dd9-9325-3447d6e09883
title: Struttura HANDOFFENTRY (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 692b9e925442920a67434f74c9e8a8ebd225fc417cbbf419b6eb568aa9eee2df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117981414"
---
# <a name="handoffentry-structure"></a>Struttura HANDOFFENTRY

La **struttura HANDOFFENTRY** definisce una voce di protocollo specifica in **una struttura HANDOFFTABLE.**

Questa struttura viene compilata da Network Monitor in base alle informazioni in un file .ini fornito dall'utente quando si chiama la [**funzione CreateHandoffTable.**](createhandofftable.md) Questa struttura non deve mai essere modificata in modo esplicito da un'applicazione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _SESSIONSTATS {
  DWORD      hoe_sig;
  DWORD      hoe_ProtIdentNumber;
  HPPROTOCOL hoe_ProtocolHandle;
  DWORD      hoe_ProtocolData;
} HANDOFFENTRY, *LPHANDOFFENTRY;
```



## <a name="members"></a>Members

<dl> <dt>

**hoe \_ sig**
</dt> <dd>

Firma che identifica questa voce come voce della tabella handoff.

</dd> <dt>

**hoe \_ ProtIdentNumber**
</dt> <dd>

Numero di protocollo fornito dall'utente .ini file.

</dd> <dt>

**Hoe \_ ProtocolHandle**
</dt> <dd>

Handle del protocollo creato usando il nome del protocollo fornito dall'utente .ini file.

</dd> <dt>

**hoe \_ ProtocolData**
</dt> <dd>

Dati dell'istanza del protocollo forniti dall'utente .ini file.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene compilata da Network Monitor quando Network Monitor crea una tabella handoff.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[HANDOFFTABLE](handofftable.md)
</dt> </dl>

 

 




