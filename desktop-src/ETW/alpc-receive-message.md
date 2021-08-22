---
description: Questa classe è la classe del tipo di evento per gli eventi di ricezione dei messaggi ALPC. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 6aa98240-e559-47b6-ae55-5a6379e08077
title: ALPC_Receive_Message classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Receive_Message
- ALPC_Receive_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 98a565ea445ddd803ce217abca3993c2561d464829635bbb1a546824f27c3b8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070361"
---
# <a name="alpc_receive_message-class"></a>Classe Messaggio \_ di ricezione \_ ALPC

Questa classe è la classe del tipo di evento per gli eventi di ricezione dei messaggi ALPC.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType(34), EventTypeName("ALPC-Receive-Message")]
class ALPC_Receive_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a>Members

La **classe ALPC \_ Receive \_ Message** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe ALPC \_ Receive \_ Message** ha queste proprietà.

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



 

 




