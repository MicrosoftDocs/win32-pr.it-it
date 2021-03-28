---
description: Questa classe è la classe del tipo di evento per gli eventi di allocazione virtuale. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 037d33e0-da94-4834-bc02-814c1cae1d8d
title: Classe PageFault_VirtualAlloc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_VirtualAlloc
- PageFault_VirtualAlloc.BaseAddress
- PageFault_VirtualAlloc.RegionSize
- PageFault_VirtualAlloc.ProcessId
- PageFault_VirtualAlloc.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: f9e754bc3dc09f492682d5a522a6489cfde27ceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344001"
---
# <a name="pagefault_virtualalloc-class"></a>\_Classe pagefault VirtualAlloc

Questa classe è la classe del tipo di evento per gli eventi di allocazione virtuale.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{98, 99}, EventTypeName{"VirtualAlloc", "VirtualFree"}]
class PageFault_VirtualAlloc : PageFault_V2
{
  uint32 BaseAddress;
  object RegionSize;
  uint32 ProcessId;
  uint32 Flags;
};
```

## <a name="members"></a>Members

La **classe \_ VirtualAlloc di pagefault** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ VirtualAlloc di pagefault** dispone di queste proprietà.

<dl> <dt>

**BaseAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), puntatore
</dt> </dl>

Indirizzo iniziale a cui è stata allocata o liberata la memoria.

</dd> <dt>

**Flag**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (4), Format ("x")
</dt> </dl>

Tipo di allocazione di memoria eseguita. Per i valori possibili, vedere il parametro *flAllocationType* della funzione [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) .

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (3)
</dt> </dl>

Il processo che possiede la memoria (può essere diverso dal thread che ha eseguito l'allocazione).

</dd> <dt>

**RegionSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **Object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2), Extension ("SizeT")
</dt> </dl>

Dimensione, in byte, della memoria allocata o liberata.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PageFault \_ v2**](pagefault-v2.md)
</dt> </dl>

 

 
