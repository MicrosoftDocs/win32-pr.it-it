---
description: Questa classe è la classe del tipo di evento per gli eventi di uscita delle chiamate di sistema. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: bb9a2770-f37b-4055-8811-59ba117adf82
title: Classe SysCallExit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallExit
- SysCallExit.SysCallNtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: aa297ced8f6c0d17c0c01da9ce11705d30fe7448c8bc2f2ae6358ddc85f653be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102061"
---
# <a name="syscallexit-class"></a>Classe SysCallExit

Questa classe è la classe del tipo di evento per gli eventi di uscita delle chiamate di sistema.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{52}, EventTypeName{"SysClExit"}]
class SysCallExit : PerfInfo
{
  uint32 SysCallNtStatus;
};
```

## <a name="members"></a>Members

La **classe SysCallExit** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe SysCallExit** ha queste proprietà.

<dl> <dt>

**SysCallNtStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1), Format("x")
</dt> </dl>

Codice di stato restituito dalla chiamata di sistema NT.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 




