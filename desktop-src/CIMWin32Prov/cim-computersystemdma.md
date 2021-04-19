---
description: La \_ classe CIM ComputerSystemDMA rappresenta un'associazione tra un sistema di computer e i canali di accesso diretto alla memoria (DMA) disponibili.
ms.assetid: 7d5bce4b-973f-4452-b403-a2196bd4017a
ms.tgt_platform: multiple
title: Classe CIM_ComputerSystemDMA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemDMA
- CIM_ComputerSystemDMA.PartComponent
- CIM_ComputerSystemDMA.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 23748a3b10c11878069a81cd82f7f69d0ab75792
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304977"
---
# <a name="cim_computersystemdma-class"></a>CIM \_ ComputerSystemDMA (classe)

La classe **CIM \_ ComputerSystemDMA** rappresenta un'associazione tra un sistema di computer e i canali di accesso diretto alla memoria (DMA) disponibili.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{9B81340B-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemDMA : CIM_ComputerSystemResource
{
  CIM_DMA            REF PartComponent;
  CIM_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a>Members

La classe **CIM \_ ComputerSystemDMA** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ ComputerSystemDMA** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ComputerSystem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Un [**\_ ComputerSystem CIM**](cim-computersystem.md) che descrive il computer associato al DMA.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ DMA**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Un [**\_ DMA CIM**](cim-dma.md) che descrive un canale DMA del sistema del computer.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **CIM \_ ComputerSystemDMA** è derivata da [**CIM \_ ComputerSystemResource**](cim-computersystemresource.md).

WMI non implementa questa classe.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_COMPUTERSYSTEMRESOURCE CIM**](cim-computersystemresource.md)
</dt> </dl>

 

