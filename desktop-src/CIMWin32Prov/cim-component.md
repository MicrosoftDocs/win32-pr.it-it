---
description: L' \_ associazione componente CIM rappresenta le parti di una relazione tra mses.
ms.assetid: a074e2f7-b092-4d3c-be5e-2069b643431b
ms.tgt_platform: multiple
title: Classe CIM_Component (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Component
- CIM_Component.GroupComponent
- CIM_Component.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b516118bc0cd6f12285933b1c15e7f2801ad40d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877981"
---
# <a name="cim_component-class-cimwin32-wmi-providers"></a>Classe CIM_Component (provider WMI CIMWin32)

L' **associazione \_ componente CIM** rappresenta le parti di una relazione tra mses.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Abstract, Aggregation, UUID("{8502C573-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Component
{
  CIM_ManagedSystemElement REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a>Members

La classe del **\_ componente CIM** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe del **\_ componente CIM** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

[**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) che descrive l'elemento padre nell'associazione.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

[**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) che descrive l'elemento figlio nell'associazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI non implementa questa classe. Per ulteriori informazioni sulle classi derivate dal **\_ componente CIM**, vedere [classi Win32](win32-provider.md).

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

