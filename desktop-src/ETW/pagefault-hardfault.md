---
description: Questa classe è la classe del tipo di evento per gli eventi di errore di pagina hard. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 9837cc45-6485-46c3-a5d9-0d33e443cd32
title: PageFault_HardFault classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_HardFault
- PageFault_HardFault.InitialTime
- PageFault_HardFault.ReadOffset
- PageFault_HardFault.VirtualAddress
- PageFault_HardFault.FileObject
- PageFault_HardFault.TThreadId
- PageFault_HardFault.ByteCount
api_type:
- NA
api_location: ''
ms.openlocfilehash: fdabfab80eadc75fa05ffe148363a85cb5ddefad9abb626cfa4e1c3fa6fe2a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394614"
---
# <a name="pagefault_hardfault-class"></a>Classe PageFault \_ HardFault

Questa classe è la classe del tipo di evento per gli eventi di errore di pagina hard.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{32}, EventTypeName{"HardFault"}]
class PageFault_HardFault : PageFault_V2
{
  object InitialTime;
  uint64 ReadOffset;
  uint32 VirtualAddress;
  uint32 FileObject;
  uint32 TThreadId;
  uint32 ByteCount;
};
```

## <a name="members"></a>Members

La **classe PageFault \_ HardFault** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe PageFault \_ HardFault** ha queste proprietà.

<dl> <dt>

**ByteCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(6)
</dt> </dl>

Quantità di dati letti da ReadOffset per soddisfare l'errore.

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(4), Pointer
</dt> </dl>

Trova la corrispondenza del valore di questo puntatore al valore del puntatore **FileObject** in un [**evento FileIo \_ Name**](fileio-name.md) per determinare il nome del file.

</dd> <dt>

**InitialTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1), Extension("WmiTime")
</dt> </dl>

Timestamp di inizio in corrispondenza del quale si è verificato l'errore di pagina.

</dd> <dt>

**ReadOffset**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(2), Format("x")
</dt> </dl>

Offset di file da cui sono stati letti i dati per soddisfare l'errore.

</dd> <dt>

**TThreadId**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(5), Format("x")
</dt> </dl>

Identificatore del thread che ha rilevato l'errore di pagina.

</dd> <dt>

**VirtualAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(3), Pointer
</dt> </dl>

Indirizzo di errore.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PageFault \_ V2**](pagefault-v2.md)
</dt> </dl>

 

 




