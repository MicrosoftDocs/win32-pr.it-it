---
description: Questa classe è la classe del tipo di evento per le chiamate di sistema immettere gli eventi. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 1ab32977-3f59-4816-b311-67142475dff2
title: Classe SysCallEnter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallEnter
- SysCallEnter.SysCallAddress
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1497491de622e564b945e8a80fcb1d8755886f39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980079"
---
# <a name="syscallenter-class"></a>Classe SysCallEnter

Questa classe è la classe del tipo di evento per le chiamate di sistema immettere gli eventi.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{51}, EventTypeName{"SysClEnter"}]
class SysCallEnter : PerfInfo
{
  uint32 SysCallAddress;
};
```

## <a name="members"></a>Members

La classe **SysCallEnter** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **SysCallEnter** dispone di queste proprietà.

<dl> <dt>

**SysCallAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), puntatore
</dt> </dl>

Indirizzo della chiamata di funzione NT da immettere.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 




