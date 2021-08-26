---
description: Questa classe è la classe del tipo di evento per l'attesa alPC per nuovi eventi di messaggio. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 7f7fa4b8-ed12-49a0-a84e-37f66af4f5f1
title: ALPC_Wait_For_New_Message classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Wait_For_New_Message
- ALPC_Wait_For_New_Message.IsServerPort
- ALPC_Wait_For_New_Message.PortName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 67b3e52e59345eea95db7485e0764f31f88669241159ffc857d46cf230a5e8b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901551"
---
# <a name="alpc_wait_for_new_message-class"></a>AlPC \_ Wait for New Message \_ \_ \_ class

Questa classe è la classe del tipo di evento per l'attesa alPC per nuovi eventi di messaggio.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType(36), EventTypeName("ALPC-Wait-For-New-Message")]
class ALPC_Wait_For_New_Message : ALPC
{
  uint32 IsServerPort;
  string PortName;
};
```

## <a name="members"></a>Members

La **classe WAIT For New \_ \_ \_ \_ Message** di ALPC ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe WAIT For New \_ \_ \_ \_ Message** di ALPC ha queste proprietà.

<dl> <dt>

**IsServerPort**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la porta è una porta del server.

</dd> <dt>

**PortName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa contenente il nome della porta su cui è in attesa ALPC.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 




