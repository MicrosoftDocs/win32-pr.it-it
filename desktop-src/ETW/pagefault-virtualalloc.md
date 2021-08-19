---
description: Questa classe è la classe del tipo di evento per gli eventi di allocazione virtuale. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 037d33e0-da94-4834-bc02-814c1cae1d8d
title: PageFault_VirtualAlloc classe
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
ms.openlocfilehash: fa3dd8eb53e9c1a79cf38edde0d9c4dba93ea85b0994bfb316b97064f211f26e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927571"
---
# <a name="pagefault_virtualalloc-class"></a>Classe PageFault \_ VirtualAlloc

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

La **classe PageFault \_ VirtualAlloc** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe PageFault \_ VirtualAlloc** ha queste proprietà.

<dl> <dt>

**Baseaddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1), Pointer
</dt> </dl>

Indirizzo iniziale in corrispondenza del quale è stata allocata o liberata la memoria.

</dd> <dt>

**Flag**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(4), Format("x")
</dt> </dl>

Tipo di allocazione di memoria eseguita. Per i valori possibili, vedere il *parametro flAllocationType* della [**funzione VirtualAllocEx.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)

</dd> <dt>

**Processid**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(3)
</dt> </dl>

Il processo proprietario della memoria (può essere diverso dal thread che ha eseguito l'allocazione).

</dd> <dt>

**RegionSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(2), Extension("SizeT")
</dt> </dl>

Dimensione, in byte, della memoria allocata o liberata.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PageFault \_ V2**](pagefault-v2.md)
</dt> </dl>

 

 
