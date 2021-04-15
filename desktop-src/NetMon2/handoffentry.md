---
description: La struttura HANDOFFENTRY definisce una voce di protocollo specifica in una struttura HANDOFFTABLE.
ms.assetid: 85793326-3007-4dd9-9325-3447d6e09883
title: Struttura HANDOFFENTRY (Netmon. h)
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
ms.openlocfilehash: 7c04c7bc90fdd0f36beb6aed26a6b84c077eff5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525128"
---
# <a name="handoffentry-structure"></a>Struttura HANDOFFENTRY

La struttura **HANDOFFENTRY** definisce una voce di protocollo specifica in una struttura **HANDOFFTABLE** .

Questa struttura viene compilata da Network Monitor in base alle informazioni contenute in un file con estensione ini fornito dall'utente durante la chiamata della funzione [**CreateHandoffTable**](createhandofftable.md) . Questa struttura non deve mai essere modificata in modo esplicito da un'applicazione.

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

**Hoe \_ sig**
</dt> <dd>

Firma che identifica questa voce come una voce di tabella di continuità.

</dd> <dt>

**\_ProtIdentNumber Hoe**
</dt> <dd>

Numero di protocollo fornito dal file ini fornito dall'utente.

</dd> <dt>

**\_ProtocolHandle Hoe**
</dt> <dd>

Handle del protocollo creato utilizzando il nome del protocollo fornito dal file ini fornito dall'utente.

</dd> <dt>

**\_ProtocolData Hoe**
</dt> <dd>

Dati dell'istanza del protocollo forniti dal file ini fornito dall'utente.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene compilata da Network Monitor quando Network Monitor crea una tabella con continuità.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[HANDOFFTABLE](handofftable.md)
</dt> </dl>

 

 




