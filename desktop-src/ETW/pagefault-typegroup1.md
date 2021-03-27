---
description: Questa classe è la classe del tipo di evento per gli eventi di errore di pagina. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 59cb1091-af21-4fe6-87b8-17a262cc4467
title: Classe PageFault_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_TypeGroup1
- PageFault_TypeGroup1.VirtualAddress
- PageFault_TypeGroup1.ProgramCounter
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4bf1f49c909833d75af844c8f2f943a01b6a5d6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232277"
---
# <a name="pagefault_typegroup1-class"></a>\_Classe pagefault TypeGroup1

Questa classe è la classe del tipo di evento per gli eventi di errore di pagina.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault", "AccessViolation"}]
class PageFault_TypeGroup1 : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a>Members

La **classe \_ TypeGroup1 di pagefault** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ TypeGroup1 di pagefault** dispone di queste proprietà.

<dl> <dt>

ProgramCounter
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2), puntatore
</dt> </dl>

Puntatore all'istruzione corrente in esecuzione.

</dd> <dt>

VirtualAddress
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), puntatore
</dt> </dl>

Indirizzo virtuale della pagina che ha causato l'errore di pagina.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un errore di pagina si verifica quando una pagina cercata nella cache in memoria non viene trovata e deve essere recuperata da un'altra posizione nella memoria (un errore software) o dal disco (errore hardware).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PageFault \_ v2**](pagefault-v2.md)
</dt> </dl>

 

 




