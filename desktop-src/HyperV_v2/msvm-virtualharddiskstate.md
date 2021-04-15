---
description: Fornisce informazioni sullo stato per un'immagine del disco rigido virtuale esistente.
ms.assetid: b0177906-71dc-4be8-b351-97d7ef427acd
title: Classe Msvm_VirtualHardDiskState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskState
- Msvm_VirtualHardDiskState.FileSize
- Msvm_VirtualHardDiskState.InUse
- Msvm_VirtualHardDiskState.MinInternalSize
- Msvm_VirtualHardDiskState.PhysicalSectorSize
- Msvm_VirtualHardDiskState.Alignment
- Msvm_VirtualHardDiskState.FragmentationPercentage
- Msvm_VirtualHardDiskState.Timestamp
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 15d0a8b150e83c17946a6d1b66c7086383f08466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484356"
---
# <a name="msvm_virtualharddiskstate-class"></a>\_Classe MSVM VirtualHardDiskState

Fornisce informazioni sullo stato per un'immagine del disco rigido virtuale esistente.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskState
{
  uint64   FileSize;
  boolean  InUse;
  uint64   MinInternalSize;
  uint32   PhysicalSectorSize;
  uint32   Alignment;
  uint32   FragmentationPercentage;
  DATETIME Timestamp;
};
```

## <a name="members"></a>Members

La **classe \_ VirtualHardDiskState di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ VirtualHardDiskState di MSVM** dispone di queste proprietà.

<dl> <dt>

**Allineamento**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il tipo di allineamento del disco rigido virtuale. Si tratta di uno dei valori seguenti.



| Valore                                                                        | Significato                        |
|------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>0</dt> </dl> | allineamento a 512 byte.<br/> |
| <dl> <dt>1</dt> </dl> | allineamento a 4 KB.<br/>     |



 

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensioni del file del disco rigido virtuale, ovvero la quantità effettiva di spazio di archiviazione utilizzata dal file, in byte.

</dd> <dt>

**FragmentationPercentage**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Approssimazione della percentuale di blocchi di dischi virtuali frammentati nel file del disco rigido virtuale.

</dd> <dt>

**InUse**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

La proprietà viene riservata per un utilizzo futuro.

</dd> <dt>

**MinInternalSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensioni minime in byte in cui è possibile compattare il disco rigido virtuale. Questa dimensione viene arrotondata per eccesso al successivo multiplo più grande delle dimensioni del settore.

</dd> <dt>

**PhysicalSectorSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensioni del settore fisico utilizzate dal disco fisico sottostante, in byte.

</dd> <dt>

**Timestamp**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Timestamp del disco rigido virtuale

> [!Note]  
> Aggiunta in Windows 10 e Windows Server 2016.

 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetVirtualHardDiskState**](getvirtualharddiskstate-msvm-imagemanagementservice.md)
</dt> </dl>

 

 




