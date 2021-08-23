---
description: Questa classe è la classe del tipo di evento per gli eventi di invio di messaggi ALPC. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 7f12259b-f737-4bef-9dea-2ffe3517e0da
title: ALPC_Send_Message classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Send_Message
- ALPC_Send_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8a3e53e514f80f89f1b1e97c1edde9b86add0db7a29de9443c5a1b48085a40fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070331"
---
# <a name="alpc_send_message-class"></a>Classe Send Message di \_ \_ ALPC

Questa classe è la classe del tipo di evento per gli eventi di invio di messaggi ALPC.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType(33), EventTypeName("ALPC-Send-Message")]
class ALPC_Send_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a>Members

La **classe ALPC \_ Send \_ Message** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe ALPC \_ Send \_ Message** ha queste proprietà.

<dl> <dt>

**MessageID**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore del messaggio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 




